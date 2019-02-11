---
title: Referenties versleutelen
description: 'Rondleiding: Referenties versleutelen voor on-premises gatewaygegevensbronnen'
author: mahirdiab
manager: eligr
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 04/02/2019
ms.author: mahirdiab
ms.openlocfilehash: 050628dfe179a39ca24d2df72f1296acf48aa261
ms.sourcegitcommit: 0abcbc7898463adfa6e50b348747256c4b94e360
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2019
ms.locfileid: "55763079"
---
# <a name="encrypt-credentials"></a>Referenties versleutelen
Als u [Gegevensbron maken](https://docs.microsoft.com/rest/api/power-bi/gateways/createdatasource) of [Gegevensbron bijwerken](https://docs.microsoft.com/rest/api/power-bi/gateways/updatedatasource) aanroept onder een **on-premises bedrijfsgateway** met de [REST API van Power BI](https://docs.microsoft.com/rest/api/power-bi/), moet de waarde voor de referenties worden versleuteld met de openbare sleutel van de gateway.

In het codevoorbeeld hieronder ziet u hoe u de referenties in .NET versleutelt.

Referenties die worden opgegeven voor de onderstaande EncodeCredentials-methode, moeten een van de volgende indelingen hebben, afhankelijk van het type referenties:

**Basis-/Windows-referenties**
```
var credentials = "{\"credentialData\":[{\"name\":\"username\", \"value\":\"john\"},{\"name\":\"password\", \"value\":\"*****\"}]}";
```

**Sleutelreferenties**
```
var credentials = "{\"credentialData\":[{\"name\":\"key\", \"value\":\"ec....LA=\"}]}";
```

**OAuth2-referenties**
```
var credentials = "{\"credentialData\":[{\"name\":\"accessToken\", \"value\":\"eyJ0....fwtQ\"}]}";
```


**Anonieme referenties**
```
var credentials = "{\"credentialData\":\"\"}";
```

**Referenties versleutelen**
```
public static class AsymmetricKeyEncryptionHelper
{

    private const int SegmentLength = 85;
    private const int EncryptedLength = 128;

    public static string EncodeCredentials(string credentials, string publicKeyExponent, string publicKeyModulus)
    {
        using (RSACryptoServiceProvider rsa = new RSACryptoServiceProvider(EncryptedLength * 8))
        {
            var parameters = rsa.ExportParameters(false);
            parameters.Exponent = Convert.FromBase64String(publicKeyExponent);
            parameters.Modulus = Convert.FromBase64String(publicKeyModulus);
            rsa.ImportParameters(parameters);
            return Encrypt(credentials, rsa);
        }
    }

    private static string Encrypt(string plainText, RSACryptoServiceProvider rsa)
    {
        byte[] plainTextArray = Encoding.UTF8.GetBytes(plainText);

        // Split the message into different segments, each segment's length is 85. So the result may be 85,85,85,20.
        bool hasIncompleteSegment = plainTextArray.Length % SegmentLength != 0;

        int segmentNumber = (!hasIncompleteSegment) ? (plainTextArray.Length / SegmentLength) : ((plainTextArray.Length / SegmentLength) + 1);

        byte[] encryptedData = new byte[segmentNumber * EncryptedLength];
        int encryptedDataPosition = 0;

        for (var i = 0; i < segmentNumber; i++)
        {
            int lengthToCopy;

            if (i == segmentNumber - 1 && hasIncompleteSegment)
                lengthToCopy = plainTextArray.Length % SegmentLength;
            else
                lengthToCopy = SegmentLength;

            var segment = new byte[lengthToCopy];

            Array.Copy(plainTextArray, i * SegmentLength, segment, 0, lengthToCopy);

            var segmentEncryptedResult = rsa.Encrypt(segment, true);

            Array.Copy(segmentEncryptedResult, 0, encryptedData, encryptedDataPosition, segmentEncryptedResult.Length);

            encryptedDataPosition += segmentEncryptedResult.Length;
        }

        return Convert.ToBase64String(encryptedData);
    }
}
```

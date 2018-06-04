---
title: Verbinding maken met Zuora via Power BI
description: Zuora voor Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: f283a8ed273dcb609e9d5160adbeb714e8935ab9
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34251928"
---
# <a name="connect-to-zuora-with-power-bi"></a>Verbinding maken met Zuora via Power BI
Met Zuora voor Power BI kunt u belangrijke omzet-, facturerings- en abonnementsgegevens visualiseren. Gebruik het standaarddashboard en de rapporten om gebruikstrends, facturen en betalingen te analyseren en terugkerende inkomsten te controleren, of pas ze aan om te voldoen aan uw eigen unieke dashboard- en rapportagebehoeften.

Verbinding maken met [Zuora](https://app.powerbi.com/getdata/services/Zuora) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.

   ![](media/service-connect-to-zuora/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.

   ![](media/service-connect-to-zuora/services.png)
3. Selecteer **Zuora** \> **Ophalen**.

   ![](media/service-connect-to-zuora/zuora.png)
4. Geef uw Zuora-URL op. Dit is doorgaans https://www.zuora.com. Bekijk hieronder de details voor het [zoeken naar die parameters](#FindingParams).

   ![](media/service-connect-to-zuora/params.png)
5. Selecteer voor **Verificatiemethode** de optie **Standaard** en geef uw gebruikersnaam en wachtwoord (hoofdlettergevoelig) op. Selecteer vervolgens **Aanmelden**.

    ![](media/service-connect-to-zuora/creds.png)
6. Nadat uw aanmelding is goedgekeurd, wordt het importeren automatisch gestart. Nadat het importeren is voltooid, bevat het navigatiedeelvenster een nieuw dashboard, rapport en model. Selecteer het dashboard om uw geïmporteerde gegevens weer te geven.

     ![](media/service-connect-to-zuora/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="whats-included"></a>Wat is inbegrepen
Het inhoudspakket gebruikt de Zuora AQUA-API voor ophalen in de volgende tabellen:

| Tabellen |  |  |
| --- | --- | --- |
| Account |InvoiceItemAdjustment |Restitutie |
| AccountingCode |Betaling |RevenueSchedule |
| AccountingPeriod |PaymentMethod |RevenueScheduleItem |
| BillTo |Product |Abonnement |
| DateDim |ProductRatePlan |TaxationItem |
| Factuur |ProductRatePlanCharge |Gebruik |
| InvoiceAdjustment |RatePlan | |
| InvoiceItem |RatePlanCharge | |

Het omvat ook deze berekende maateenheden:

| Maateenheid | Beschrijving | Pseudo-berekening |
| --- | --- | --- |
| Account: betalingen |Totale betalingsbedragen in een periode gebaseerd op de ingangsdatum van de betaling. |SUM (Payment.Amount) <br>WHERE<br>Payment.EffectiveDate = < TimePeriod.EndDate<br>AND    Payment.EffectiveDate >= TimePeriod.StartDate |
| Account: restituties |Totaal aantal restitutiebedragen in een periode op basis van restitutiedatum. Bedrag wordt gerapporteerd als een negatief getal. |-1*SUM(Refund.Amount)<br>WHERE<br>Refund.RefundDate = < TimePeriod.EndDate<br>AND    Refund.RefundDate >= TimePeriod.StartDate |
| Account: netto betalingen |Betalingen plus restituties van een account in een bepaalde periode. |Account.Payments + Account.Refunds |
| Account: actieve accounts |Het aantal accounts die in een bepaalde periode actief waren. Abonnementen moeten zijn gestart voor (of op) begindatum van periode. |COUNT (Account.AccountNumber)<br>WHERE<br>    Subscription.Status != "Verlopen"<br>AND    Subscription.Status != "Concept"<br>AND    Subscription.SubscriptionStartDate <= TimePeriod.StartDate<br>AND    (Subscription.SubscriptionEndDate > TimePeriod.StartDate<br>OR<br>Subscription.SubscriptionEndDate = null) –evergreen abonnement |
| Account: gemiddelde terugkerende omzet |Brutomarge MRR per actieve account in een bepaalde periode. |Bruto MRR / Account.ActiveAccounts |
| Account: geannuleerde abonnementen |Het aantal accounts waarvoor een abonnement in een bepaalde periode is geannuleerd. |COUNT (Account.AccountNumber)<br>WHERE<br>Subscription.Status = "Geannuleerd"<br>AND    Subscription.SubscriptionStartDate <= TimePeriod.StartDate<br>AND    Subscription.CancelledDate >= TimePeriod.StartDate |
| Account: betalingsfouten |Totale waarde van betalingsfouten. |SUM (Payment.Amount)<br>WHERE<br>Payment.Status = "Fout" |
| Opbrengsten schema-item: opgenomen opbrengsten |Totaal opgenomen opbrengsten in een verslagperiode. |SUM (RevenueScheduleItem.Amount)<br>WHERE<br>AccountingPeriod.StartDate TimePeriod.StartDate = |
| Abonnement: nieuwe abonnementen |Het aantal nieuwe abonnementen in een bepaalde periode. |COUNT (Subscription.ID)<br>WHERE<br>Subscription.Version = "1"<br>AND    Subscription.CreatedDate <= TimePeriod.EndDate<br>AND    Subscription.CreatedDate >= TimePeriod.StartDate |
| Factuur: factuuritems |Totaalkosten factuuritems in een bepaalde periode. |SUM (InvoiceItem.ChargeAmount)<br>WHERE<br>    Invoice.Status = 'Geboekt'<br>EN Invoice.InvoiceDate < = TimePeriod.EndDate<br>AND    Invoice.InvoiceDate >= TimePeriod.StartDate |
| Factuur: belastingitems |Totaalbedrag belastingitems in een bepaalde periode. |SUM (TaxationItem.TaxAmount)<br>WHERE<br>Invoice.Status = 'Geboekt'<br>EN Invoice.InvoiceDate < = TimePeriod.EndDate<br>AND    Invoice.InvoiceDate >= TimePeriod.StartDate |
| Factuur: aanpassingen factuuritems |Totaalbedrag factuuritems in een bepaalde periode. |SUM (InvoiceItemAdjustment.Amount) <br>WHERE<br>    Invoice.Status = 'Geboekt'<br>AND    InvoiceItemAdjustment.AdjustmentDate <= TimePeriod.EndDate<br>AND    InvoiceItemAdjustment.AdjustmentDate >= TimePeriod.StartDate |
| Factuur: factuurcorrecties |Totaalbedrag factuurcorrecties in een bepaalde periode. |SUM (InvoiceAdjustment.Amount) <br>WHERE<br>    Invoice.Status = 'Geboekt'<br>AND    InvoiceAdjustment.AdjustmentDate <= TimePeriod.EndDate<br>AND    InvoiceAdjustment.AdjustmentDate >= TimePeriod.StartDate |
| Factuur: netto rekeningen |Som van factuuritems, belastingitems, correcties op factuuritems en correcties op facturen in een bepaalde periode. |Invoice.InvoiceItems + Invoice.TaxationItems + Invoice.InvoiceItemAdjustments + Invoice.InvoiceAdjustments |
| Factuur: factuur openstaand saldo |Som van geboekte factuursaldi. |SUM (Invoice.Balance) <br>WHERE<br>    Invoice.Status = 'Geboekt' |
| Factuur: bruto factureringen |Som van factuurkosten per item voor geboekte facturen in een bepaalde periode. |SUM (InvoiceItem.ChargeAmount) <br>WHERE<br>    Invoice.Status = 'Geboekt'<br>EN Invoice.InvoiceDate < = TimePeriod.EndDate<br>AND    Invoice.InvoiceDate >= TimePeriod.StartDate |
| Factuur: totaal van correcties |Som van verwerkte factuurcorrecties en correcties op factuuritems met betrekking tot geboekte facturen. |SUM (InvoiceAdjustment.Amount) <br>WHERE<br>    Invoice.Status = 'Geboekt'<br>AND    InvoiceAdjustment.Status = "Verwerkt"<br>+<br>SUM (InvoiceItemAdjustment.Amount) <br>WHERE<br>    Invoice.Status = 'Geboekt'<br>AND    invoiceItemAdjustment.Status = "Verwerkt" |
| Kosten tariefplan: bruto MRR |De som van de maandelijkse terugkerende inkomsten van abonnementen in een bepaalde periode. |SUM (RatePlanCharge.MRR) <br>WHERE<br>    Subscription.Status != "Verlopen"<br>AND    Subscription.Status != "Concept"<br>AND    RatePlanCharge.EffectiveStartDate <= TimePeriod.StartDate<br>AND        RatePlanCharge.EffectiveEndDate > TimePeriod.StartDate<br>    OR    RatePlanCharge.EffectiveEndDate = null --evergreen abonnement |

## <a name="system-requirements"></a>Systeemvereisten
Toegang tot de Zuora-API is vereist.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Geef de URL die u gewoonlijk gebruikt voor toegang tot uw Zuora-gegevens. De geldige opties zijn:  

* https://www.zuora.com  
* https://www.apisandbox.zuora.com  
* De URL die hoort bij uw service-exemplaar  

## <a name="troubleshooting"></a>Probleemoplossing
Het Zuora-inhoudspakket bevat veel aspecten van uw Zuora-account. Als u bepaalde functies niet gebruikt, ziet u dat bijbehorende tegels/rapporten leeg zijn. Neem contact op met ondersteuning van Power BI als u problemen ondervindt bij het laden.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

---
layout: page
title: De aangifte
permalink: /vat/declaration
parent: BTW aangifte of aangifte omzetbelasting
nav_order: 2
---

## The declaration

Note: The original Accoo manual is incorrect in this area. See the explanation below
if you want to know why.

You need two different statements for the figures, namely the Trial Balance report and
the Profit and Loss Statement report.

Open GnuCash and go to Reports, Revenue and Expenses and Trial Balance.

![Menu proefbalans]({{site.baseurl}}/assets/menu_reports_profits_balance.png)

You will now see the trial balance window. We will use the numbers in the box later.

![Weergave proefbalans]({{site.baseurl}}/assets/proefbalans_btw_highlights.png)

We now open the “Profit and Loss Statement” report. This option is in the first image
at the bottom.

Click the Options icon at the top of the bar, or search for it in the drop-down menu
if the button isn't visible. Then click on the General tab.

![Algemene opties winst- en verliesrekening]({{site.baseurl}}/assets/profit_loss_report_general_options.png)

Choose a date here at `Start date correction/closing` and at `Report date`. You can choose to
enter a date yourself, but GnuCash has a number of handy quick selection options for both
options:

![Smartopties begindatum]({{site.baseurl}}/assets/smart_opties_begindatum.png)

![Smartopties rapportdatum]({{site.baseurl}}/assets/smart_opties_rapportdatum.png)

Usually you will choose `Start of last quarter` and `End of last quarter`. After selecting
the correct data, click OK and your overview will be updated.

![Winst- en verliesrekening omzet]({{site.baseurl}}/assets/profit_loss_revenue.png)

We use the figures from the `Turnover` section. In this overview there is also a table
costs under the turnover, but you only have to look at that when filling in the income tax.

## Look up previous declarations
This step is only necessary if sales invoices have been entered in a period for which
the VAT declaration has already been made. In that case, the VAT has been credited to
the corresponding `Debt turnover tax account`, but the turnover value of the invoice still
falls under the original VAT period. As a result, the turnover figures are no longer
correct as originally stated.

If the VAT to be received or paid exceeds the aforementioned € 1000, a supplement form
must be completed, with which the VAT return for that period is corrected.

We now assume that the VAT amount remains below € 1000 and that we can process this
in the next VAT return.

Therefore look up the previous declarations of the year and add up the turnover per
VAT rate. If necessary, use the [Quarterly overview turnover overview](../overviews/revenue_per_quarter)

Now, in the options of the `Profit and loss statement`, set the start to the beginning
of the year, and the end to the end of the quarter preceding the quarter for which you
are submitting the VAT return. Now check whether the combined turnover per VAT rate of
that period corresponds to the sum of the turnover as you entered it.

If there is a difference and you have not stated enough turnover, add the difference
to the new turnover figures.

## Complete the declaration

Now that you have obtained the necessary information from your accounting, it is time
to file the VAT return. Go to the website of the Tax and Customs Administration and 
log in there. You choose the quarter for which you want to file a return. You then
get a number of pages.

NB: We have chosen not to use images from the website of the Tax and Customs 
Administration, because in principle these should speak for themselves.

We specifically look here at the pages Performance domestic,

On the “Domestic performance” page, you enter the turnover and the sales tax that
you have charged to your customers.

In the column "Amount on which turnover tax is calculated" you enter the turnover.
In the “Sales tax” column, enter the VAT that you have charged to your customers.

- “1a. Deliveries/services taxed at a high rate” is the turnover on which you have calculated 21% VAT.
- “1b. Low-rate supplies/services” is the turnover on which you calculated 9% VAT.
- “1c. Deliveries/services charged with other rates, except 0%” is a field that you almost never have to fill in. In our example this happens by chance, but we skip this for the sake of convenience. (Note: If you know of a good example for this, please let us know via the GitHub Issues)
- “1d. Private use” here you enter the amount and VAT of private withdrawals. For example, if you drive privately in a car of your company, enter it here.
- “1e. Deliveries/services taxed with 0% or not taxed at your place” is the turnover on which you have not charged VAT to your customer. For example, if you transfer the VAT to your customer according to the “reverse charge scheme”.

### Fill in Domestic performance

1a. Supplies / services taxed at high rate
  * Ledger account “800 Sales 21% sales tax” = “Amount on which sales tax is calculated”.
    In this example € 2702.00. If necessary, add the difference if there is a difference 
    with the previous declaration.
  * General ledger account “185 Sales tax debt 21%” = “Sales tax”. In this example € 90.42.

1b. Low rate deliveries/services
  * Ledger account “801 Sales 9% sales tax” = “Amount on which sales tax is calculated”.
    In this example € 850.00. If necessary, add the difference if there is a difference
    with the previous declaration.
  * General ledger account “186 Sales tax debt 9%” = “Sales tax”. In this example € 45.00.

1st. Deliveries/services taxed at 0% or not taxed at your expense
  * Ledger account “802 Sales 0% sales tax” = “Amount on which sales tax is calculated”.
    In this example € 450.00. If necessary, add the difference if there is a difference
    with the previous declaration.
  * Because the percentage is 0%, you cannot enter a VAT amount.

### Completing reverse charge arrangements domestic

On the “Domestic reverse charge arrangements” page, enter “2a. Deliveries/services
where turnover tax has been transferred to you” the purchases where the VAT has been
transferred to you.

2a. Deliveries/services where turnover tax has been shifted to you
  * General ledger account “189 Sales tax debt shifted to me” = “Sales tax”.
    In this example €50.
  * To find out what the purchase price was associated with the € 50 sales tax,
    it is usually easiest to look up the invoices in the accounts that include
    the reverse-charged VAT of € 50.00. In this example, this includes one invoice 
    of € 238.10.

### Fill in Performances to/abroad & Performances from abroad

The pages “Performance to/abroad” and “Performance from abroad” are for entrepreneurs
who export and/or import goods or services. The VAT on import and export is not taken
into account here.

### Fill in Pre-tax and small entrepreneurs

The “Input tax and small entrepreneurs” page is the last page where you have to enter
an amount from the accounting. Here you enter the VAT that you have paid to your suppliers.

5a. Turnover tax (sections 1 to 4 inclusive)” is the total VAT that you have entered and
that you must pay to the Tax and Customs Administration.

5b. Preload
  * General ledger account “180 Sales tax receivable” = “Sales tax”. In this example € 140.21.

It does not matter whether you have paid 21% VAT or 9% VAT on your purchases, you only
enter the VAT paid by you to your suppliers here in one amount.

## Last VAT return of the year

A special case is the last VAT return of the year, because a number of settlements also
take place there. We will not discuss this further in this manual, but it is important
to read this information carefully.

Tax authorities: [Last VAT return of the year](https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/zakelijk/btw/btw_aangifte_doen_en_betalen/btw-aangifte-welke-wanneer-en-hoe/laatste_btw_aangifte_van_het_jaar)

## Differences with the Accoo manual

The manual above is different from Accoo's. The original manual suggests taking only
the trial balance report and always choosing the beginning of the year as the start date
of that report. In this way, sales invoices entered after processing the VAT period
to which that sales invoice relates are included. However, there is a mismatch:
the Tax and Customs Administration would like to have the turnover for that quarter,
but the trial balance report only gives the total turnover since the last book close.
We don't use that option in this guide, so those numbers are useless. The Profit and loss
account overview does give you the option to view your turnover per VAT period.
This overview only misses the sales invoices that belong to the closed VAT period,
but that were entered after processing the VAT return.

Please note: this only applies to sales invoices. This problem does not exist for
purchase invoices, because they are not part of the turnover. It also just means
that the sales figures may not be correct. The VAT debt is correct, because it is
cumulative and not date-sensitive.

The simplest solution has therefore been chosen, namely to manually compare the 
turnover figures of the VAT return with those in GnuCash. If a sales invoice is
entered later, it will be reflected in both the VAT and the turnover.

## Original
## De aangifte

_Let op: De originele handleiding van Accoo klopt niet op dit vlak. Zie de uitleg onderaan als je wilt weten waarom._

Je hebt voor de cijfers twee verschillende overzichten nodig, namelijk het rapport `Proefbalans` en het rapport `Winst- en verliesrekening`.

Open GnuCash en ga naar Rapporten, Opbrengsten en kosten en Proefbalans.

![Menu proefbalans]({{site.baseurl}}/assets/menu_reports_profits_balance.png)

Je krijgt nu het venster proefbalans. De cijfers in het kader gaan we straks gebruiken.

![Weergave proefbalans]({{site.baseurl}}/assets/proefbalans_btw_highlights.png)

We openen nu het rapport "Winst- en verliesrekening". Deze optie staat in de eerste afbeelding onderaan. 

Klik boven in de balk op het pictogram `Opties`, of zoek ernaar in het uitklapmenu mocht de knop niet zichtbaar zijn.
Klik vervolgens op het tabblad Algemeen.

![Algemene opties winst- en verliesrekening]({{site.baseurl}}/assets/profit_loss_report_general_options.png)

Kies hier een datum bij `Begindatum correctie/afsluiting` en bij `Rapportdatum`. Je kunt ervoor kiezen zelf een datum in te vullen,
maar GnuCash heeft bij beide opties een aantal handige snelselectie-opties:

![Smartopties begindatum]({{site.baseurl}}/assets/smart_opties_begindatum.png)

![Smartopties rapportdatum]({{site.baseurl}}/assets/smart_opties_rapportdatum.png)

Meestal zul je kiezen voor `Begin van vorig kwartaal` en `Einde van vorig kwartaal`. 
Na het selecteren van de juiste data klik je op OK en wordt je overzicht bijgewerkt. 

![Winst- en verliesrekening omzet]({{site.baseurl}}/assets/profit_loss_revenue.png)

We gebruiken de cijfers van de rubriek `Omzet`. In dit overzicht staat onder de omzet ook nog een tabel kosten, maar daar hoef je pas naar te kijken bij het invullen van de inkomstenbelasting.

## Vorige aangiftes opzoeken

Deze stap is alleen maar nodig indien er verkoopfacturen zijn ingevoerd in een periode waarvan de BTW-aangifte al heeft plaatsgevonden. 
In dat geval is namelijk de BTW wel bijgeschreven op de bijhorende rekening `Schuld omzetbelasting`, maar de omzet-waarde van de factuur valt nog
altijd onder het originele BTW-tijdvak. Hierdoor kloppen de omzetcijfers niet meer zoals die oorspronkelijk zijn opgegeven.

Als de te ontvangen dan wel te betalen BTW boven de al eerder genoemde € 1000 uitkomt, moet er een suppletie-formulier worden ingevuld, waarmee
de BTW-aangifte voor dat tijdvak wordt gecorrigeerd.

We gaan er nu van uit dat het BTW-bedrag onder de € 1000 euro blijft, en dat we dit kunnen verwerken in de eerstevolgende BTW-aangifte.

Zoek daarom de vorige aangiftes van het jaar op en tel per BTW-tarief de omzet bij elkaar op. Gebruik eventueel het overzicht [Kwartaaloverzicht omzet](../overviews/revenue_per_quarter)

Stel nu bij de opties van de `Winst- en verliesrekening` het begin in op het begin van het jaar, en het einde in op het einde van het kwartaal voorafgaand aan het kwartaal waarvan je de BTW-aangifte doet. Kijk nu of de gezamelijke omzet per BTW-tarief van die periode overeenkomt met de optelsom van de omzet zoals je die hebt opgegeven.

Mocht er een verschil zijn en je hebt te weinig omzet opgegeven, tel dan het verschil bij de nieuwe omzetcijfers op.

## De aangifte invullen

Nu je de benodigde gegevens uit je boekhouding hebt gehaald is het tijd voor het doen van de BTW-aangifte. Ga naar de website van de Belastingdienst en log daar in. Je kiest daar het kwartaal waarvoor je aangifte wil doen. Je krijgt vervolgens een aantal pagina's.

NB: Er is hier gekozen om geen afbeeldingen te gebruiken van de site van de Belastingdienst, omdat deze in principe voor zich zou moeten spreken.

Wij kijken hier specifiek naar de pagina's `Prestaties binnenland`, 

Op de pagina “Prestaties binnenland” vul je de omzet in en de omzetbelasting die je aan je klanten in rekening hebt gebracht.

In de kolom “Bedrag waarover omzetbelasting wordt berekend” vul je de omzet in.
In de kolom “Omzetbelasting” vul je de BTW in die je aan je klanten in rekening hebt gebracht.

- “1a. Leveringen/diensten belast met hoog tarief” is de omzet waarover je 21% btw hebt berekend.
- “1b. Leveringen/diensten belast met laag tarief” is de omzet waarover je 9% btw hebt berekend.
- “1c. Leveringen/diensten belast met overige tarieven, behalve 0%” is een veld dat je bijna nooit in hoeft te vullen. In ons voorbeeld komt dit toevallig wel voor, maar dit slaan we voor 't gemak over. (Opmerking: Mocht je een goed voorbeeld hiervoor weten, laat het even weten via de [GitHub Issues](https://github.com/mauritslamers/boekhouden-met-gnucash/issues))
- “1d. Privégebruik” hier vul je het bedrag en de BTW van privéonttrekkingen in. Bijvoorbeeld als je privé rijdt in een auto van je onderneming vul je dat hier in.
- “1e. Leveringen/diensten belast met 0% of niet bij u belast” is de omzet waarover je geen BTW hebt berekend aan je klant. Bijvoorbeeld als je de BTW verlegt naar je afnemer volgens de “verleggingsregeling”.


### Invullen Prestaties binnenland

1a. Leveringen/diensten belast met hoog tarief
  * Grootboekrekening “800 Omzet 21% omzetbelasting” = “Bedrag waarover omzetbelasting wordt berekend”. In dit voorbeeld € 2702,00. 
    Tel hier eventueel het verschil bij op als er een verschil mocht zijn met de vorige aangifte.
  * Grootboekrekening “185 Schuld omzetbelasting 21%” = “Omzetbelasting”. In dit voorbeeld € 90,42.

1b. Leveringen/diensten belast met laag tarief
  * Grootboekrekening “801 Omzet 9% omzetbelasting” = “Bedrag waarover omzetbelasting wordt berekend”. In dit voorbeeld € 850,00.
    Tel hier eventueel het verschil bij op als er een verschil mocht zijn met de vorige aangifte.
  * Grootboekrekening “186 Schuld omzetbelasting 9%” = “Omzetbelasting”. In dit voorbeeld € 45,00.

1e. Leveringen/diensten belast met 0% of niet bij u belast
  * Grootboekrekening “802 Omzet 0% omzetbelasting” = “Bedrag waarover omzetbelasting wordt berekend”. In dit voorbeeld € 450,00.
    Tel hier eventueel het verschil bij op als er een verschil mocht zijn met de vorige aangifte.
  * Omdat het percentage 0% is kun je geen btw bedrag invullen.

### Invullen Verleggingsregelingen binnenland

Op de pagina “Verleggingsregelingen binnenland” vul je bij “2a. Leveringen/diensten waarbij omzetbelasting naar u is verlegd” de inkopen in waarbij de BTW naar jou is verlegd.

2a. Leveringen/diensten waarbij omzetbelasting naar u is verlegd
  * Grootboekrekening “189 Schuld omzetbelasting naar mij verlegd” = “Omzetbelasting”. In dit voorbeeld € 50.
  * Om te weten wat de inkoopprijs was die hoort bij de € 50 omzetbelasting, is het meestal het gemakkelijkst om de facturen op te zoeken in de boekhouding waar de verlegde btw van € 50,00 bij hoort. In dit voorbeeld hoort hier één factuur bij van € 238,10.

### Invullen Prestaties naar/in het buitenland & Prestaties vanuit het buitenland
De pagina’s “Prestaties naar/in het buitenland” en “Prestaties vanuit het buitenland” zijn voor ondernemers die goederen of diensten exporteren en/of importeren. De BTW bij import en export laten we hier buiten beschouwing.

### Invullen Voorbelasting en kleine ondernemers
De pagina “Voorbelasting en kleine ondernemers“ is de laatste pagina waar je een bedrag uit de boekhouding moet invullen. Hier vul je de BTW in die je aan jouw leveranciers hebt betaald.

5a. Omzetbelasting (rubrieken 1 t/m 4)” is de totale BTW die je hebt ingevuld en die je moet afdragen aan de Belastingdienst.

5b. Voorbelasting
  * Grootboekrekening “180 Vordering omzetbelasting” = “Omzetbelasting”. In dit voorbeeld € 140,21.

Het maakt niet uit of je 21% btw of 9% BTW hebt betaald over je inkopen, je vult hier alleen de door jou aan jouw leveranciers betaalde BTW in één bedrag in.

## Laatste BTW-aangifte van het jaar

Een bijzonder geval is de laatste BTW-aangifte van het jaar, omdat daar ook een aantal afrekeningen in plaats vinden. We gaan daar in deze handleiding niet verder op in, maar het is wel belangrijk om deze informatie goed door te lezen.

[Belastingdienst: Laatste BTW-aangifte van het jaar](https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/zakelijk/btw/btw_aangifte_doen_en_betalen/btw-aangifte-welke-wanneer-en-hoe/laatste_btw_aangifte_van_het_jaar)

## Verschillen met de handleiding van Accoo

De handleiding hierboven is anders dan die van Accoo. In de originele handleiding wordt gesuggereerd alleen het proefbalans-rapport te nemen en altijd als begindatum van dat rapport het begin van het jaar te kiezen. Op deze manier worden verkoopfacturen meegenomen die zijn ingevoerd na het verwerken van de BTW-periode waar die verkoopfactuur betrekking op heeft. 
Er is echter een mismatch: de Belastingdienst wil namelijk graag de omzet hebben over dat kwartaal, maar het proefbalans-rapport geeft alleen maar de totale omzet sinds de laatste boeksluiting. In deze handleiding gebruiken we die optie niet, dus die cijfers zijn onbruikbaar.
Het overzicht Winst- en verliesrekening geeft je wel de mogelijkheid om je omzet per BTW-periode te bekijken. Dit overzicht mist alleen de verkoopfacturen die behoren tot de afgesloten BTW-periode, maar die ingevoerd zijn na het verwerken van de BTW-aangifte.

Let op: dit geldt dus alleen voor verkoopfacturen. Voor inkoopfacturen bestaat dit probleem niet, omdat ze geen onderdeel uitmaken van de omzet.
Het betekent ook alleen dat de omzet-cijfers mogelijk niet kloppen. De BTW-schuld is wel correct, want deze is namelijk cumulatief en niet datum-gevoelig.

Er is daarom voor de simpelste oplossing gekozen, namelijk handmatig de omzetcijfers van de BTW-aangifte en die in GnuCash met elkaar te vergelijken. Mocht er dan een verkoopfactuur later worden ingevoerd, komt deze zowel in de BTW als bij de omzet terug.
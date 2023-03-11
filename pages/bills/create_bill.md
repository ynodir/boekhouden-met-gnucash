---
layout: page
title: Nieuwe Inkoopfactuur
permalink: /new_bill
parent: Inkoopfacturen
nav_order: 2
---

**Note:** In the current versions of GnuCash there is a bug that prevents the text for
the buttons in this window from getting the correct translation. So you always see
“Sales invoice”, but this must be “Purchase invoice” for all buttons in the toolbar.
However, the buttons work correctly. In this manual we assume the correct translation.
Enter purchase invoice

Choose menu “Business”, submenu “Supplier” and then the option “New purchase invoice”.

You will now see the “New purchase invoice” dialog box.

![Dialoogvenster nieuwe inkoopfactuur]({{site.baseurl}}/assets/create_bill_dialog.png)

You now fill in the following:

* **Purchase invoice number**: The invoice number or receipt number
* **Document date**: The invoice date or receipt date
* **Supplier**: The name of the supplier. If you have already created the supplier, you only need to type the first letters of the name.

If you have many one-time suppliers, it is an option to create a “General” supplier.
You don't have to enter every single supplier. As a result, you have less insight
into what you have purchased per supplier.

Click OK

You will now see the screen in which you can enter the items on the purchase invoice.

![Invoer items op inkoopfactuur]({{site.baseurl}}/assets/enter_bill_items.png)

We enter the following per item:

* **Date**: Invoice date
* **Description**: A short description of the costs
* **Cost account**: Choose a cost account that the Tax and Customs Administration prescribes for this type of cost. Because in this manual the ledger accounts (expense accounts are also ledger accounts) have been created according to the classification of the income tax and VAT return, we can follow the guidelines of the Tax Authorities. This way you ensure that you can easily copy the data from your accounting into the tax returns. A clear explanation is available for each type of expenditure in the tax return program for entrepreneurs, the turnover tax return and on the website of the Tax and Customs Administration.
* **Quantity**: The number of products or pieces that you have purchased
* **Price per unit**: Price per purchased product or service
* **Taxable**: This must be checked if VAT has been charged for the item.
* **Tax rate**: Choose “Purchase sales tax 21%” for the items for which 21% VAT is charged, “Purchase sales tax 9%” for the items for which 9% VAT is charged. Copy these items from the purchase invoice or receipt.

At the bottom of the window you see the Total, Subtotal and VAT of what you entered. Check whether this corresponds with what is stated on the purchase invoice or receipt. Choose “Capture” if it is correct.

## In books

Now that the details of the purchase invoice have been entered, we will process the purchase invoice in the accounting system. Click on the “▾ menu”, and choose “Post purchase invoice”.

![Dialoogvenster Inkoopfactuur inboeken]({{site.baseurl}}/assets/book_bill_confirm_dialog.png)

Enter the following here:

* **Book date**: the invoice date
* **Due date**: The day on which the invoice must be paid at the latest. For cash payments, you can leave the date the same.
* **Description**: Can be left blank
* **Post to account**: Purchase invoices are always “140 Creditors”.

If everything is correct, choose OK.

## Original
**Let op:** In de huidige versies van GnuCash zit een bug waardoor de tekst bij de knoppen in dit venster niet de juiste vertaling krijgen.
Je ziet dus steeds "Verkoopfactuur" staan, maar dit moet "Inkoopfactuur" zijn voor alle knoppen in de werkbalk. De knoppen werken echter correct.
In deze handleiding gaan we uit van de correcte vertaling.

## Inkoopfactuur invoeren
Kies menu "MKB", submenu "Leverancier" en vervolgens de optie "Nieuwe inkoopfactuur".

Je krijgt nu het dialoogvenster "Nieuwe inkoopfactuur".

![Dialoogvenster nieuwe inkoopfactuur]({{site.baseurl}}/assets/create_bill_dialog.png)

Je vult nu de volgende zaken in:

* **Inkoopfactuurnummer**: Het factuurnummer of nummer van de kassabon
* **Documentdatum**: De factuurdatum of datum van de kassabon
* **Leverancier**: De naam van de leverancier. Als je de leverancier al hebt aangemaakt, hoef je alleen de eerste letters van de naam te typen.

Als je veel eenmalige leveranciers hebt, is het een optie om een leverancier "Algemeen" aan te maken. Je hoeft dan niet elke eenmalige leverancier
in te voeren. Hierdoor heb je wel minder inzicht in wat je per leverancier hebt afgenomen.

Klik op OK

Je krijgt nu het scherm waarin je de items op de inkoopfactuur kunt invoeren.

![Invoer items op inkoopfactuur]({{site.baseurl}}/assets/enter_bill_items.png)

We voeren per item het volgende in:

* **Datum**: Factuurdatum
* **Omschrijving**: Een korte omschrijving van de kosten
* **Kostenrekening**: Kies een kostenrekening die de Belastingdienst voorschrijft voor dit type kosten. Omdat in deze handleiding de grootboekrekeningen
  (kostenrekeningen zijn ook grootboekrekeningen) volgens de indeling van de inkomstenbelasting en BTW-aangifte hebben aangemaakt, kunnen we de richtlijnen van de
  Belastingdienst volgen. Zo zorg je ervoor dat je de gegevens uit je boekhouding eenvoudig kunt overnemen in de belastingaangiftes.
  In het aangifteprogramma ondernemers, de aangifte van de omzetbelasting en op de website van de Belastingdienst is voor elk type uitgave een duidelijke toelichting beschikbaar.
* **Hoeveelheid**: Het aantal producten of stuks dat je hebt afgenomen
* **Prijs per eenheid**: Prijs per afgenomen product of dienst
* **Belastbaar**: Dit moet aangevinkt staan indien voor het item BTW is gerekend.
* **Belastingtarief**: Kies voor "Omzetbelasting inkopen 21%" voor de items waarvoor 21% BTW wordt gerekend, "Omzetbelasting inkopen 9%" voor de items waarvoor 9%
  BTW wordt gerekend. Neem deze zaken over van de inkoopfactuur of kassabon.

Onderaan in het venster zie je het Totaal, Subtotaal en BTW van wat je hebt ingevoerd. Check of dit overeenkomt met wat op de inkoopfactuur of kassabon staat.
Kies "Vastleggen" als het klopt.

## Inboeken

Nu de gegevens van de inkoopfactuur zijn ingevoerd, verwerken we de inkoopfactuur in de boekhouding.
Klik op het "&#9662;-menu", en kies daar "Inkoopfactuur boeken".

![Dialoogvenster Inkoopfactuur inboeken]({{site.baseurl}}/assets/book_bill_confirm_dialog.png)

Vul hier het volgende in:

* **Boekdatum**: de factuurdatum
* **Vervaldatum**: De dag waarop de factuur uiterlijk betaald moet zijn. Bij contante betalingen kun je de datum hetzelfde laten.
* **Omschrijving**: Kun je leeg laten
* **Naar rekening boeken**: Inkoopfacturen zijn altijd "140 Crediteuren".

Als alles klopt kies je OK.


---
layout: page
title: Handmatig invoeren
permalink: /paying/manual
parent: Betalingen verwerken
nav_order: 1
---

## Process payments manually.

For manual processing of payments, it is practical to have a PDF of the bank account
at hand. So first download a PDF of the desired period for which you want to process
the bank transactions. You can also open the online banking environment, but a PDF
is more practical because the online environments sometimes log you out automatically
rather quickly. You can print the PDF if you want.

## Incoming payment (Payment by customer)
To register an incoming payment, choose the menu “Business”, submenu “Customer” and
option “Process payment”.

You will now get the “Processing payment” dialog box.

![Dialoogvenster Betaling verwerken (klant)]({{site.baseurl}}/assets/customer_payment_dialog.png)

First, select the customer by typing the first letters, or by using the search box 
that you get when you click on “Select…”. You will now receive a list of invoices 
to be paid by this customer. Select the invoice that the customer has paid.

Make sure that the “130 Debtors” account is selected at “Entry to”.

Then, in the “Booking Details” section, enter:

* **Date**: The date the customer paid
* **Payment**: The amount the customer has paid
* **Refund**: Let's leave this at 0.
* **Nr** and **Note** we do not use.

Then select “110 Bank” under contra account. Click OK if everything is entered correctly.
Repeat these actions for any incoming payment you receive.

## Outgoing Payment (Payment to Vendor)

The outgoing payment is almost identical to the incoming payment.

To register an outgoing payment, choose the menu “Business”, submenu “Supplier” and option
“Process payment”.

You will now get the “Processing payment” dialog box.

![Dialoogvenster Betaling verwerken (leverancier)]({{site.baseurl}}/assets/vendor_payment_dialog.png)

Note that "Partner" is now set to Supplier.
The "Entry on" should now read "140 Creditors". Then you select the invoice,
enter the date on which it was paid, enter the amount that was paid, and select 
"110 Bank" as the contra account again.

Repeat these steps for every bill you've paid.

## To coordinate

Now that all sales invoices and purchase invoices on the bank statement have been 
processed via the steps described above, it is time to reconcile the bank transactions.

Go to the Accounts tab and select the ledger account “Bank”. Now choose the “Tune” 
option from the “Actions” menu.

You will now get the “110 Bank - Reconcile” dialog box. At “Statement date” you enter
the last date of the bank statement and at closing balance the closing balance of 
the bank statement on that date.

Now click OK.

You will now get the “Reconcile” window, with a list of “Cash inflow” and “Cash outflow”.
If you have made other expenses in the meantime, such as private withdrawals or debit
card payments that have not yet been entered, they will not be shown here.

To still book it in, click on “Open…” in the toolbar. You will now get a new “Bank”
tab in which you will see the invoices and amounts that are also in the “Reconcile”
window. Here you can now fill in the missing recordings. We use the Tab key to move
to the next field.

Enter the following here:

* **Date**: The date of the payment
* **Description**: the description of the recording, for example Supermarket Private Expenses.
* **Transfer**: for private withdrawals, use the account “042 Private withdrawals”
* **Withdrawal**: The amount of the withdrawal.

Choose “Capture” after each new book line.

The “Tune” window is most likely still open behind the main window. If not, open it again
via menu “Actions”, option “Tuning”.

Now everything matches what is on the bank statement. At “Incoming money flow” 
you will find all the “At” amounts from the bank statement, and at “Outgoing money flow”
you will find the “Debit” amounts from the bank statement.

The amounts at Total therefore also match the bank statement and the Difference 
(bottom right of the window) is € 0.00.

Now you can finish by choosing the option “Finish” from the arrow menu.
This option is also under the “Tuning” menu. The bank statement has now been processed
in the accounting.

## Original:
## Betalingen handmatig verwerken.

Voor het handmatig verwerken van betalingen is het praktisch om een PDF van de
bankrekening bij de hand te hebben. Download dus eerst een PDF van de gewenste
periode waarvoor je de bankmutaties wilt verwerken.
Je kunt ook de online bankomgeving open zetten, maar een PDF is praktischer omdat
de online omgevingen je soms nogal snel automatisch uitloggen.
Als je wilt kun je de PDF uitprinten.

## Inkomende betaling (Betaling door de klant)
Om een inkomende betaling te registreren kies je menu "MKB", submenu "Klant" en optie
"Betaling verwerken".

Je krijgt nu het dialoogvenster "Betaling verwerken".

![Dialoogvenster Betaling verwerken (klant)]({{site.baseurl}}/assets/customer_payment_dialog.png)

Selecteer eerst de klant door de eerste letters te typen, of door gebruik te maken van het zoekvenster dat je krijgt als je op "Selecteren..." klikt.
Je krijgt nu een lijst met te betalen facturen van deze klant. Selecteer de factuur die de klant betaalt heeft.

Zorg dat bij "Boeken op" de "130 Debiteuren" rekening geselecteerd is.

Vul vervolgens in het deel "Boekingsdetails" in:

* **Datum**: De datum waarop de klant betaald heeft
* **Betaling**: De hoeveelheid die de klant betaalt heeft
* **Terugbetaling**: Dit laten we op 0 staan.
* **Nr** en **Notitie** gebruiken we niet.

Kies vervolgens onder tegenrekening "110 Bank". Klik op OK als alles goed is ingevuld.
Herhaal deze handelingen voor inkomende betaling die je krijgt.

## Uitgaande betaling (Betaling aan de leverancier)
De uitgaande betaling gaat op vrijwel identieke manier als de inkomende betaling.

Om een uitgaande betaling te registreren kies je menu "MKB", submenu "Leverancier" en optie
"Betaling verwerken".

Je krijgt nu het dialoogvenster "Betaling verwerken".

![Dialoogvenster Betaling verwerken (leverancier)]({{site.baseurl}}/assets/vendor_payment_dialog.png)

Merk op dat bij "Partner" nu Leverancier staat ingesteld.
Bij "Boeken op" moet nu "140 Crediteuren" staan. Vervolgens selecteer je de factuur,
vult de datum in waarop het betaald is, het bedrag in dat betaald is, en kiest als tegenrekening weer "110 Bank".

Herhaal deze stappen voor elke factuur je hebt betaald.

## Afstemmen

Nu alle verkoopfacturen en inkoopfacturen die op het bankafschrift staan via de hierboven
beschreven stappen zijn verwerkt, is het tijd voor het afstemmen van de bankmutaties.

Ga naar het tabblad Rekeningen en selecteer de grootboekrekening "Bank".
Kies nu de optie "Afstemmen" uit het menu "Acties".

Je krijgt nu het dialoogvenster "110 Bank - Afstemmen".
Je vult bij "Afschriftdatum" de laatste datum van het bankafschrift in en bij eindsaldo
het eindsaldo van het bankafschrift op die datum.

Klik nu op OK.

Je krijgt nu het venster "Afstemmen", met daarin een lijst met "Inkomende geldstroom" en
"Uitgaande geldstroom". Als je in de tussentijd andere uitgaven hebt gedaan, zoals privé-opnames of
pinbetalingen die nog niet zijn ingevoerd, zijn deze hier niet te zien.

Om deze alsnog in te boeken, klik je op "Openen..." in de werkbalk. Je krijgt nu een nieuw
tabblad "Bank" waarin je de facturen en bedragen ziet staan die ook in het venster "Afstemmen" staan.
Hier kun je nu de ontbrekende opnames invullen. We gebruiken de Tab-toets om naar een volgend veld te gaan.

Vul hier het volgende in:

* **Datum**: De datum van de betaling
* **Omschrijving**: de omschrijving van de opname, bijvoorbeeld Privé-uitgaven supermarkt.
* **Overboeken**: gebruik voor privé-opnames de rekening "042 Privé-onttrekkingen"
* **Opname**: Het bedrag van de opname.

Kies "Vastleggen" na elke nieuwe boekregel.

Het venster "Afstemmen" staat zeer waarschijnlijk nog open achter het hoofdvenster. Zo niet, open het dan opnieuw via menu "Acties", optie "Afstemmen".

Nu komt alles overeen met wat er op het bankafschrift staat.
Bij "Inkomende geldstroom" staan alle "Bij"-bedragen van het bankafschrift,
en bij "Uitgaande geldstroom" staan de "Af"-bedragen van het bankafschrift.

De bedragen bij Totaal kloppen daarmee ook met het bankafschrift en het Verschil (rechts onder in het venster) staat op € 0,00.

Nu kun je afronden door te uit het pijltjes-menu de optie "Afronden" te kiezen.
Deze optie zit ook onder het menu "Afstemmen". Het bankafschrift is nu verwerkt in de boekhouding.



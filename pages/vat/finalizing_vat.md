---
layout: page
title: Verwerking
permalink: /vat/finalizing
parent: BTW aangifte of aangifte omzetbelasting
nav_order: 3
---

## Preparation for processing
At the end of the VAT return you will have seen whether you have to pay VAT on balance or
whether you will receive a VAT refund from the Tax and Customs Administration.
The payment or refund of the turnover tax goes through your business bank account.

To ensure that you can easily process the bank transaction (the VAT that you have to pay
or that you will receive back), we make an entry in the accounting of the VAT return.

This entry ensures that one balance remains to be paid or refunded in the accounting
for that quarter.

You make the booking at the end of the declaration period. The turnover tax return was
for the last quarter of 2019, so you make the entry as of December 31, 2019.

We have made a table for the overview of the VAT amounts in the declaration and in the
accounting. The VAT amounts must be set to “zero”. We therefore transfer all VAT amounts
to one sales tax ledger account. It does not matter which VAT general ledger account 
you use, as long as you always use the same one for “booking” and for the bank transaction
of the turnover tax return.

We use “180 Sales tax receivable”. We are going to transfer the amounts in the credit column
to the debit column. The amounts are examples.

| Name in the VAT return                                                 | Name in the accounts                             | Debit (VAT to be refunded) | Credit (VAT to be received) |
|------------------------------------------------------------------------|--------------------------------------------------|----------------------------|-----------------------------|
| 1a. Deliveries/services charged with a high rate                       | 185 Sales tax debt 21%                           |                            | € 138.84                    |
| 1b. Deliveries/services taxed at a low rate                            | 186 Sales tax debt 9%                            |                            | € 48.00                     |
| 1e. Deliveries/services taxed at 0% or not taxed at you                | n/a                                              |                            | -                           |
| 2a. Deliveries/services where turnover tax has been transferred to you | 189 Debt turnover tax has been transferred to me |                            | € 50.00                     |
| 5b. Input tax                                                          | 180 Value added tax receivable                   | € 289.11                   |                             |

The transfer (journal entry) then looks like this. On balance we transfer € 236.84. 
The € 289.11 to be refunded from the table above therefore decreases by € 236.84 
due to the transfer.

| General ledger account accounting | Debit  | Credit  |
|-----------------------------------|--------|---------|
| 185 Sales tax debt 21%            | €138   |         |
| 186 Sales tax debt 9%             | € 98   |         |
| 180 Sales tax receivable          |        | €236.84 |

## The processing

There are several ways to process the VAT return in the administration.
We describe three ways here: a "quick-and-dirty" way, a "so-can-be" way and the decent way.
We'll start with the proper way.

### The decent way

For the proper way, we use an extra account that we will first create if you had not already done so.
This account is specifically intended for temporarily holding the final result of the VAT processing.
If you already have this account, you can skip this step.

#### Create Suspense account VAT

Go to the 'Accounts' tab and choose New.

Fill in:
- Account name: 190 Suspense account VAT
- Account number: 190
- Account type: Assets
- Main account: New main level account

NB: The English term for suspense account is Suspense Account

#### The booking itself

We are now going to enter this booking. In this example we do this on the account 'Sales tax receivable', but in fact it does not matter, because we are going to create an entry that involves several accounts. GnuCash will then automatically place this entry in the affected accounts.

On the 'Accounts' tab, double-click on the ledger account "180 Sales tax receivable". Now enter the last day of the quarter for which you filed the return as the date. Then enter a description, for example "Processing VAT return last quarter 2019".
Now click on the button 'More book lines' in the toolbar at the top of your screen. You will now get a new yellow line. Use the tab key on your keyboard to go to the next line.

We are now going to process the table above per line. Do this in the order it appears in the table, with the Pre-Tax account coming last. The numbers have been rounded off, because you only use whole numbers in the NL statement.

We first click on the 'Account' column of this first new line. We can type in the account name here, but it's easier to use the pull-down menu. We choose the account `185 Debt turnover tax 21%` and enter the amount that we entered in the declaration, namely € 138, in the column `Increase`. We ensure that the column `Decrease` remains empty.

We go to the next line. You will see that GnuCash automatically calculates the balance of the booking for us.
We choose the account `186 Debt sales tax 9%` and again enter the amount that we have specified in the column `Increase`. Here, too, we ensure that the 'Decrease' column remains empty.

We now fill in the line for the 'VAT receivable' account and in the column 'Decrease' we enter the amount that we have specified as input tax, namely the full rounded amount. It does not matter whether something remains on the bill or not, and whether you have rounded up or down.

There is now a difference. We post this difference to the account `190 Suspense account VAT` by selecting that account for that line.

We now record the booking by clicking on 'Create'.

#### Payment to or from the tax authorities

We now open the account `190 Suspense account VAT` by double-clicking on it in the Accounts overview.
The balance of this account is now equal to the amount that you still have to reconcile with the Tax and Customs Administration. If the balance is positive, you must pay the Tax and Customs Administration, and if the balance is negative, the Tax and Customs Administration must repay that amount to you.

You open the option 'Books' in the Actions menu. You now enter the amount that you must pay or receive. This amount is equal to the balance on the 'Suspended VAT account', but always positive. So if the balance is -30, enter 30.
Now fill in the Date and Description fields.

If you had to pay VAT to the Tax and Customs Administration, select `110 Bank` on the left and `190 VAT suspense account` on the right.
If you had to receive VAT from the Tax Authorities, choose `190 Suspense account VAT` on the left and `110 Bank` on the right.

Click OK. The payment has now been processed and the balance on the suspense account should be 0 again.

### The so-can-do way

This way is very similar to the way of the suspense account, but does not use a separate account for it, but the account `180 Pretax`.
This way is slightly less transparent and therefore less correct than the proper way.

The way of entering is almost the same as the way above, only you do not write the differences to the Suspense account, but to the Pretax account. If you have to pay VAT to the tax authorities, the balance on the Pretax account will be negative. You then process the payment to or from the Tax and Customs Administration in the same way, only here you also use the '180 Voorbelasting' account instead of the suspense account.

### The quick-and-dirty way

This way is slightly less correct than the so-can-it-too way. This method is only useful if you can make the payment to the tax authorities at the same time as the VAT processing. Usually this is not the case, because then you cannot make the difference between the moment of payment and the end of the VAT period.
The previous methods put the processing of the VAT on the last day of the VAT period, but with the quick-and-dirty way this is only possible if you are going to get VAT back.

The way of entering also works similar to the above methods, but now you enter the account `110 Bank` when making the closing entry if you have to pay VAT to the Tax Authorities. Then choose the moment of payment as the date.

If you are going to receive VAT back, an amount will remain on the 'Input tax' account. As soon as you receive the amount back from the Tax Authorities, you transfer the amount from the Pretax account to the bank account via the "Book" option.

## Original
## Voorbereiding van de verwerking

Aan het einde van de btw-aangifte heb je gezien of je per saldo BTW moet betalen of dat je omzetbelasting terug krijgt van de Belastingdienst. Het betalen of terugkrijgen van de omzetbelasting loopt via je zakelijke bankrekening.

Om er voor te zorgen dat je de bankmutatie (de BTW die je moet betalen of die je terug krijgt) gemakkelijk kan verwerken, maken we een boeking in de boekhouding van de BTW-aangifte.

Deze boeking zorgt er voor dat er per saldo één te betalen of terug te ontvangen bedrag over blijft in de boekhouding voor dat kwartaal.

De boeking maak je aan het einde van de aangifteperiode. De aangifte omzetbelasting was voor het laatste kwartaal 2019, dus de boeking maak je per 31 december 2019.

Wij hebben voor het overzicht een tabel gemaakt van de btw-bedragen in de aangifte en in de boekhouding. De btw-bedragen moeten op “nul” gezet worden. We boeken daarom alle btw-bedragen over naar één omzetbelasting grootboekrekening. Welke btw grootboekrekening je gebruikt maakt niet uit als je maar altijd dezelfde gebruikt voor het “wegboeken” en voor de bankmutatie van de aangifte omzetbelasting.

Wij gebruiken “180 Vordering omzetbelasting”. We gaan de bedragen in de credit kolom overboeken naar de debet kolom. De bedragen zijn voorbeelden.

|Naam in de BTW-aangifte                         |Naam in de boekhouding          |    Debet (terug te krijgen BTW)| Credit (te ontvangen BTW)|
|------------------------------------------------|--------------------------------|--------------------------------|--------------------------|
|1a. Leveringen/diensten belast met hoog tarief  | 185 Schuld omzetbelasting 21%  |                                |                  € 138,84|
|1b. Leveringen/diensten belast met laag tarief  | 186 Schuld omzetbelasting 9%   |                                |                  €  48,00|
|1e. Leveringen/diensten belast met 0% of niet bij u belast | nvt.                |                                |                         -|
|2a. Leveringen/diensten waarbij omzetbelasting naar u is verlegd | 189 Schuld omzetbelasting naar mij verlegd |   |                  €  50,00|
|5b. Voorbelasting                               | 180 Vordering omzetbelasting   | €                        289,11|                          |

De overboeking (journaalpost) ziet er dan zo uit. Per saldo boeken we € 236,84 over. De terug te ontvangen € 289,11 uit de tabel hierboven neemt door de overboeking dus af met € 236,84.

|Grootboekrekening boekhouding              | Debet   | Credit  |
|-------------------------------------------|---------|---------|
|185 Schuld omzetbelasting 21%              | € 138   |         |
|186 Schuld omzetbelasting 9%               | €  98   |         |
|180 Vordering omzetbelasting               |         | € 236,84|

## De verwerking

Er zijn meerdere manieren om de BTW-aangifte in de administratie te verwerken.
We beschrijven hier drie manieren: een "quick-and-dirty" manier, een "zo-kan-het-ook" manier en de degelijke manier.
We beginnen met de degelijke manier.

### De degelijke manier

Voor de degelijke manier gebruiken we een extra rekening die we eerst gaan aanmaken als je dat al niet gedaan had.
Deze rekening is specifiek bedoeld voor het tijdelijk vasthouden van het eindresultaat van de BTW-verwerking.
Als je deze rekening al hebt, kun je deze stap overslaan.

#### Aanmaken Tussenrekening BTW

Ga naar het tabblad `Rekeningen` en kies voor Nieuw.

Vul in:
- Rekeningnaam: 190 Tussenrekening BTW 
- Rekeningnummer: 190
- Rekeningsoort: Activa
- Hoofdrekening: Nieuwe rekening op hoofdniveau

NB: De Engelse term voor tussenrekening is Suspense Account

#### De boeking zelf

We gaan deze boeking nu invoeren. We doen dit in dit voorbeeld op de rekening `Vordering omzetbelasting` maar feitelijk gezien maakt het niet uit, omdat we een boeking gaan aanmaken waar meerdere rekeningen bij zijn betrokken. GnuCash zal dan automatisch deze boeking plaatsen in de betrokken rekeningen.

Dubbelklik op het tabblad `Rekeningen` op de grootboekrekening "180 Vordering omzetbelasting". Vul nu als datum de laatste dag in van het kwartaal waarvoor je aangifte hebt gedaan. Vul vervolgens een omschrijving in, bijvoorbeeld "Verwerking BTW-aangifte laatste kwartaal 2019".
Klik nu op de knop `Meer boekregels` in de knoppenbalk bovenin je scherm. Je krijgt nu een nieuwe gele regel. Gebruik de tab-toets op je toetsenbord om naar de volgende regel te gaan.

We gaan nu per regel de bovenstaande tabel verwerken. Doe dit in de volgorde zoals het in de tabel staat, waarbij de rekening Voorbelasting als laatste aan de beurt komt. De getallen zijn afgerond, omdat je bij de opgave in NL ook alleen gehele getallen gebruikt.

We klikken daarvoor eerst op de kolom `Rekening` van deze eerste nieuwe regel. We kunnen hier de rekeningnaam tiepen, maar het is gemakkelijker om het pulldown-menu gebruiken. We kiezen daar de rekening `185 Schuld omzetbelasting 21%` en vullen in de kolom `Toename` het bedrag in dat we ingevuld hebben bij de aangifte, namelijk € 138. We zorgen dat de kolom `Afname` leeg blijft.

We gaan naar de volgende regel. Je ziet dat GnuCash automatisch de balans van de boeking voor ons uitrekent.
We kiezen de rekening `186 Schuld omzetbelasting 9%` en vullen wederom in de kolom `Toename` het bedrag in dat we opgegeven hebben. Ook hier zorgen we dat de kolom `Afname` leeg blijft.

We vullen nu de regel in voor de rekening `Vordering omzetbelasting` en we vullen in de kolom `Afname` het bedrag in dat we als voorbelasting hebben opgegeven, namelijk het volledige afgeronde bedrag. Het maakt daarbij niet uit of er nog iets op de rekening blijft staan of niet, en of je naar boven of naar beneden hebt afgerond.

Er blijft nu een verschil over. Dit verschil boeken we naar de rekening `190 Tussenrekening BTW` door die rekening te selecteren voor die regel.

We leggen nu de boeking vast door te klikken op `Vastleggen`. 

#### Betaling aan of van de Belastingdienst

We openen nu de rekening `190 Tussenrekening BTW` door in het Rekeningen-overzicht erop te dubbelklikken.
Het saldo van deze rekening is nu gelijk aan het bedrag dat je nog met de Belastingdienst moet afstemmen. Is het saldo positief, moet je aan de Belastingdienst betalen, en is het saldo negatief moet de Belastingdienst jou dat bedrag terugbetalen.

Je opent in het menu Acties de optie `Boeken`. Je vult nu het bedrag in dat je moet betalen of moet ontvangen. Dat bedrag is gelijk aan het saldo op de `Tussenrekening BTW`, maar dan altijd positief. Dus als het saldo -30 is, vul je 30 in. 
Vul nu de velden Datum en Omschrijving in.

Indien je BTW moest betalen aan de Belastingdienst, kies je links voor `110 Bank` en rechts `190 Tussenrekening BTW`.
Indien je BTW moest ontvangen van de Belastingdienst, kies je links voor `190 Tussenrekening BTW` en rechts voor `110 Bank`.

Klik op OK. De betaling is nu verwerkt en het saldo op de Tussenrekening zou weer 0 moeten zijn.

### De zo-kan-het-ook manier

Deze manier lijkt erg op de manier van de tussenrekening, maar gebruikt daarvoor geen aparte rekening maar de rekening `180 Voorbelasting`.
Deze manier is iets minder doorzichtig en daarmee minder correct dan de degelijke manier.

De manier van invoeren is vrijwel hetzelfde als bij de manier hierboven, alleen schrijf je de verschillen niet naar de Tussenrekening, maar naar de Voorbelasting rekening. Indien je BTW aan de belastingdienst moet betalen, wordt het saldo op de Voorbelasting-rekening negatief. Je verwerkt vervolgens de betaling aan of van de Belastingdienst ook op dezelfde manier, alleen gebruik je ook hier de rekening `180 Voorbelasting` in plaats van de tussenrekening.

### De quick-and-dirty manier

Deze manier is weer iets minder correct dan de zo-kan-het-ook manier. Deze manier is alleen maar bruikbaar als je de betaling aan de Belastingdienst op hetzelfde moment kunt doen als de verwerking van de BTW. Meestal is dat niet zo, omdat je dan niet het verschil kunt maken tussen het moment van betaling en het einde van de BTW-periode.
De voorgaande methodes zetten de verwerking van de BTW op de laatste dag van de BTW-periode, maar bij de quick-and-dirty manier kan dat alleen als je BTW terug gaat krijgen.

De manier van invullen werkt ook weer vergelijkbaar als de bovenstaande manieren, maar nu vul je bij het maken van de afsluitingsboeking de rekening `110 Bank` in als je BTW aan de Belastingdienst moet betalen. Als datum kies je dan het moment van betalen.

Als je BTW terug gaat ontvangen blijft er een bedrag staan op de rekening `Voorbelasting`. Zodra je van de Belastingdienst het bedrag terugkrijgt, boek je via de optie "Boeken" het bedrag van de Voorbelasting-rekening naar de bankrekening.

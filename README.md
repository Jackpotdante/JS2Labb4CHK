# JS2Labb4CHK

Laboration 4
Du ska skapa en webbapp som använder Vue.js. Den ska lämnas in senast 18/4.
Uppgiften ska utföras ensam. Inlämning sker genom att redovisa för läraren på lektionstid. Som vanligt använder vi git för versionshantering och GitHub för att publicera på webben.

Appen ska vara en miniräknare. Man ska kunna skriva in ett tal i ett textfält och använda vanliga räknesätt. Resultatet ska visas separat. Gör en ändamålsenlig design.

Det är inte tillåtet att använda vanlig DOM-manipulation i den här laborationen, eftersom den handlar om Vue, som ersätter det med sin egen syntax. Ni kommer inte att behöva några globala variabler. Använd data-objektet i Vue i stället.

Kriterier för godkänt: Appen ska innehålla
input-fält för att mata in ett tal
presentation av resultatet hittills
knappar för vanliga räknesätt (+, -, *, /)
knapp för att rensa resultatet och återställa resultatet till noll (C, Clear eller motsvarande)
knapp för att räkna ut ett resultat (=)
appen ska ha en tydlig design (förklara för användaren hur man förväntas använda den, användaren ska inte behöva gissa vad en knapp gör)
appen ska versionshanteras med Git och vara publicerad på GitHub

Kriterier för väl godkänt:
knappar för operationerna x2 och √ (roten ur)
knappen för roten ur ska bara vara synlig när resultatet är ett positivt tal
appen håller en historik över tidigare uträkningar
varje gång man klickar på = ska det uträknade resultatet sparas i en lista, som också ska vara synlig för användaren

Exempel på användningsfall. Användaren vill räkna ut "42+2-40".
skriver in talen 42
klickar på knappen "+" (resultatet 42 visas)
skriver in talet 2
klickar på knappen "/" (resultatet 44 visas, 42+2 == 44)
skriver in talet 4
klickar på knappen "=" (resultatet 11 visas, 44/4 == 11)

______________________________________________________________________

Om du får tid över: https://en.wikipedia.org/wiki/Reverse_Polish_notation 
RPN är en metod för att kunna skriva in komplicerade matematiska uttryck, utan att behöva använda parenteser. Om man skriver ett tal så läggs det till sist i en lista. Om man väljer en operator så används den med de två sista elementen ur listan. Elementen ersätts med resultatet.
Exempel: 1 + ((5 - 2) * 3)
1 → [1]
5 → [1, 5]
2 → [1, 5, 2]
- → [1, 3]  // 5-2 == 3
3 → [1, 3, 3]
* → [1, 9]
+ → [10]



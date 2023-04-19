
# Rapport

**Assignment 4**

_Activities and intents_.

- Jag började med att skapa en ny activity, eftersom jag inte bestämmt mig för vad appen ska göra än, fick denna heta MainActivity2.
- Därefter lades en knapp till i MainActivity 1. Denna knappen ska kunna transportera användaren till MainActivity 2. Detta uppnås genom nedan kod:
```
button.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View view) {
        Intent intent = new Intent(MainActivity.this, MainActivity2.class);
        MainActivity.this.startActivity(intent);
    }
});
```
- I koden ovan definieras först en ny intent; ett meddelande att byta från nuvarande Activity till nästa.
- Därefter Skapades en EditText i MainActivity1 där användaren kan skriva in sitt namn.
- För att denna data ska kunna transporteras in i MainActivity2 användes extras på följande sätt:
```
EditText editText = findViewById(R.id.editTextTextPersonName);
String name = String.valueOf(editText.getText());
intent.putExtra("Name", name);
```
- Först hittas texten, sedan tas texten ut ur EditText och konvereras till en String. Därpå läggs namnet in i intenten med identifieraren Name.
- För att sedan kunna läsa denna data i MainActivity2 hämtas den intent som tog oss dit. 
- Därefter hittas namnet genom koden: 
```
Intent intent = getIntent();
String name = intent.getStringExtra("Name");
TextView textview = findViewById(R.id.textView2);
textview.setText("välkommen " + name + "!");
```
**Slutresultat:**
![](MainActivity1.png) ![](MainActivity2.png)

- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

```
function errorCallback(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            // Geolocation API stöds inte, gör något
            break;
        case error.POSITION_UNAVAILABLE:
            // Misslyckat positionsanrop, gör något
            break;
        case error.UNKNOWN_ERROR:
            // Okänt fel, gör något
            break;
    }
}
```

Bilder läggs i samma mapp som markdown-filen.

![](android.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.

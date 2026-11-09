# Hjelp til innsending av data fra automatiske veiiesystemer via API

Produksjonsmiljø for APIet er tilgjengelig på: https://api.fiskeridir.no/weight-receiver/swagger-ui/index.html

## Maskinporten og delegering av rettigheter for ulike aktører:

### Rapporteringspliktig som ønsker å sette opp integrasjon selv.

* Dere må opprette en integrasjon (en OAuth 2.0-klient) i Maskinporten med scope `fdir:weightdata.write`
* Se `https://samarbeid.digdir.no/maskinporten/ta-i-bruk-maskinporten/97` under “Konsument”.

### Rapporteringspliktig som ønsker å benytte en tjenesteleverandør

* Dere må gi fullmakt til API i Altinn til tjenesteleverandør. Følg veiviser på https://info.altinn.no/hjelp/ny-tilgangsstyring/maskinportenadministrasjon/ for å gi ansatte tilgang til dette.
* Søk og velg fullmakten “Skrivetilgang til API'er for registrering av vektdata for automatiske veiesystemer.”
* Ta kontakt med tjenesteleverandør som leverer integrasjonen, slik at de kan rapportere på vegne av dere.

### En tjenesteleverandør som vil tilby innsending for rapporteringspliktige

* Gjelder leverandør av system med integrasjon mot Fiskeridirektoratet’s APIer.
* Din kunde må ha tildelt API-tilgang i Altinn til leverandør.
* Leverandør av system må opprette en integrasjon (en OAuth 2.0-klient) i Maskinporten med scope `fdir:weightdata.write`.
* Samme klient kan brukes til å rapportere for flere kunder ved å endre `consumer_org` verdien.
* Se `https://samarbeid.digdir.no/maskinporten/ta-i-bruk-maskinporten/97` under “Leverandør”.

## Testmiljø:

Testmiljø for APIet er tilgjengelig på: https://testapi.fiskeridir.no/weight-reciever/swagger-ui/index.html

* Gyldige `vesselId` kan hentes fra testmiljøet til vessel-api: https://testapi.fiskeridir.no/vessel-api/
* Gyldige `locationId` kan hentes fra testmiljøet til buyer-api: https://testapi.fiskeridir.no/buyer-api/

Kontakt epost: tfa@fiskeridir.no

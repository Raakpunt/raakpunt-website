# raakpunt.com

De bestanden van de website raakpunt.com.

## Indeling

- `site/` bevat alles wat online staat: de pagina's, `.htaccess`, de foto en de pdf's waar de site naar linkt.
- `.github/workflows/deploy.yml` zet de site live bij Vimexx.

## Werkwijze

1. Elke wijziging komt op een aparte tak en wordt een pull request, met een korte beschrijving: welke pagina, welk onderdeel en waarom.
2. Daan bekijkt het verschil en klikt op "Merge". Pas dan gaat het live.
3. GitHub Actions uploadt via FTPS alleen de gewijzigde bestanden naar `public_html` van raakpunt.com.
4. Terugdraaien kan met "Revert" op het pull request.

Op `main` komt niets rechtstreeks; die tak kan alleen via een pull request veranderen.

## Afspraken

- Schrijfregels voor sitetekst: geen gedachtestreepjes, geen tarieven, geen citaten met namen of functies, professioneel maar niet stijf Nederlands.
- Wettelijke claims eerst controleren tegen de officiële bron of de VP-kennisbank, met datum.
- Nooit VP-dossiers, casussen of namen van melders in deze repository. Deze repository is openbaar.
- Op de server staat `.ftp-deploy-sync-state.json`. Dat bestand niet verwijderen; de upload houdt daarmee bij wat er al staat.

## Kennisbank vertrouwenswerk

- `site/kennisbank-vertrouwenswerk.html` staat op https://www.raakpunt.com/kennisbank-vertrouwenswerk.html. Ingangen: een knop in het vlak extern vertrouwenspersoon op de homepage en een knop bovenaan de dienstpagina extern vertrouwenspersoon. De pagina staat bewust niet in het hoofdmenu.
- Het bestand wordt gemaakt en bijgehouden in het project "Ik als vertrouwenspersoon". Pas de inhoud hier niet aan: bij een update wordt het in zijn geheel vervangen onder dezelfde naam.
- Bijwerken: na een mail "ACTIE WEBSITE" het nieuwe bestand ongewijzigd over het oude zetten, als pull request met de boodschap "Kennisbank vertrouwenswerk bijgewerkt <datum>".

## Toegang

De FTP-gegevens staan alleen in de geheimen van deze repository (Settings, Secrets and variables, Actions): `FTP_SERVER`, `FTP_USERNAME` en `FTP_PASSWORD`.

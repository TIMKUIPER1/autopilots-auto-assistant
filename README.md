# Autopilots AI Auto-Assistent

Een white-label AI Auto-Assistent voor autobedrijven.

Autobedrijven kunnen bij aflevering van een occasion een QR-kaartje meegeven aan hun klant. De klant scant de QR-code en krijgt een mobiele AI-assistent in de stijl van het autobedrijf.

De assistent helpt met vragen over de auto, onderhoud, dashboardlampjes, APK, schade en algemene autovragen. Als het nodig is, vraagt de assistent om het kenteken en haalt hij voertuigdata op via RDW.

## Doel van V1

De eerste versie moet bestaan uit:

* Klant-app achter QR-code
* AI-chat voor autovragen
* RDW-koppeling op basis van kenteken
* Interne Autopilots beheerpagina
* Dealer branding per autobedrijf
* Gesprekken opslaan
* Service-aanvraag naar het autobedrijf
* Subtiel “Powered by Autopilots”

## Belangrijk

Dit is een MVP. Bouw dus eerst alleen de kern. Nog niet bouwen:

* Foto-upload
* Dealer login-portaal
* Statistieken-dashboard
* Betalingen
* PDF-handleidingen uploaden
* Live agenda-integratie
* WhatsApp-integratie

## Tech stack

* Next.js
* TypeScript
* Tailwind CSS
* Supabase
* OpenAI API
* RDW Open Data

## Pagina’s

* `/` — Autopilots demo/landingpage
* `/a/[dealerSlug]` — klant-app achter QR-code
* `/admin` — interne Autopilots beheerpagina

## API routes

* `/api/assistant/ask` — AI-vragen beantwoorden
* `/api/rdw/lookup` — kenteken opzoeken via RDW
* `/api/service-request` — service-aanvraag opslaan en eventueel doorsturen

## Environment variables

De app gebruikt environment variables voor geheime instellingen en externe koppelingen.

Voor lokale ontwikkeling moeten deze in `.env.local` staan:

```env
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=
SUPABASE_SECRET_KEY=
OPENAI_API_KEY=
ADMIN_PASSWORD=
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

## V1 principe

Maak eerst een simpele, stabiele en verkoopbare versie. Liever klein en goed werkend dan groot en half af.

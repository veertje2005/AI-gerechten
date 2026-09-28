# Smaakboek

Smaakboek is een persoonlijke receptenapp met:
- eigen recepten
- AI-import vanaf foto's en receptlinks
- openbare recepten ontdekken
- favorieten
- profiel en meerdere talen
- PWA-ondersteuning voor toevoegen aan het beginscherm

## Belangrijkste bestanden

- `index.html` – de app
- `manifest.webmanifest` – appnaam, kleuren en iconen
- `service-worker.js` – PWA/offline basis
- `icons/` – favicon, iPhone- en Android-iconen
- `robots.txt` – basisinstellingen voor zoekmachines

## Publiceren

Upload alle bestanden en de map `icons` naar de hoofdmap van de GitHub-repository.
Vercel kan daarna automatisch opnieuw deployen.

## Veiligheid

API-secrets horen niet in GitHub of in `index.html`.
Bewaar geheime sleutels uitsluitend als server-side secrets, bijvoorbeeld in Supabase Edge Functions.

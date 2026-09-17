# Mariam Inna — Landing Page

Site vitrine one-page pour l'accompagnement en leadership de Mariam Inna.

**En ligne :** https://mtbusinessmedi.github.io/mariam-inna/

## Contenu

Page unique `index.html`, entièrement autonome :

- Hero avec photo et double appel à l'action (diagnostic + WhatsApp)
- Bannière manifeste
- Trois piliers d'accompagnement
- Méthode en 4 étapes
- Chiffres clés
- Checklist « pour qui »
- Témoignage
- À propos
- Détail de l'offre
- FAQ
- Section de conversion finale
- Fenêtre de réservation (formulaire → WhatsApp)

## Réservation

Tous les boutons « Prendre rendez-vous » / « Réserver un diagnostic » ouvrent une
fenêtre modale contenant le formulaire de réservation. À l'envoi, les réponses sont
mises en forme et WhatsApp s'ouvre avec le message déjà rédigé — il ne reste qu'à
l'envoyer. Aucune donnée n'est stockée ni transmise à un serveur tiers.

Champs obligatoires : nom, taille de l'équipe, objectif principal, disponibilité et
consentement. Fonction, organisation, email, téléphone et contexte sont facultatifs.

Le numéro de destination est la constante `WHATSAPP_NUMBER` en bas de `index.html`.

## Technique

- HTML, CSS et un seul script inline — aucune dépendance de build
- Images intégrées en base64 — le fichier fonctionne hors ligne
- Polices Sora et Inter chargées depuis Google Fonts
- Responsive, optimisé mobile en priorité (points de rupture à 900px, 780px,
  640px, 560px et 380px) — testé de 320px à 1280px
- Respecte `prefers-reduced-motion`
- Modale native `<dialog>` : fermeture par Échap, clic hors zone ou croix. Sans
  JavaScript, les boutons redirigent simplement vers la section contact.

## Mobile

- Menu hamburger dans l'en-tête, panneau déroulant plein écran, liens de 48px
- Barre d'action fixe en bas d'écran (réserver + WhatsApp), masquée au-dessus de 780px
- Champs de formulaire à 16px pour empêcher le zoom automatique de Safari iOS
- `env(safe-area-inset-bottom)` pris en compte pour les iPhone à encoche
- `scroll-margin-top` sur les sections pour que les ancres ne passent pas sous
  l'en-tête collant

## Développement

Ouvrir `index.html` dans un navigateur, ou servir le dossier :

```bash
python -m http.server 8000
```

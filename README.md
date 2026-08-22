# FloatNotes — canal de distribution

Ce dépôt ne contient **aucun code source** : uniquement le manifeste de mise à
jour et les binaires publiés. Le code de FloatNotes vit dans un dépôt privé.

- `appcast.json` — dernière version publiée (numéro, URL du DMG, empreinte SHA-256)
- `appcast.json.sig` — signature ed25519 détachée du manifeste, en base64

L'application vérifie cette signature avec une clé publique compilée en dur avant
d'installer quoi que ce soit : un manifeste modifié — y compris ici — est rejeté.

## Installation manuelle

1. Télécharger le DMG depuis la [dernière release](https://github.com/olivierbouchard/floatnotes-releases/releases/latest).
2. Glisser **FloatNotes** dans **Applications**.
3. Retirer la quarantaine (l'app n'est pas signée par un compte Apple Developer) :

   ```
   xattr -dr com.apple.quarantine /Applications/FloatNotes.app
   ```

Cette étape ne concerne que l'installation manuelle : les mises à jour
téléchargées par l'application elle-même n'y sont pas soumises.

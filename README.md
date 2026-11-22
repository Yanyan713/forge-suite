# Forge Suite

Hub unique réunissant cinq studios de création d'assets, dans **un seul fichier HTML autonome**.

- **MeshForge** — modélisation 3D low-poly (primitives, extrusion, export OBJ)
- **PixelForge** — studio pixel art (canvas libre, miroirs X/Y, tuiles, export PNG)
- **SpriteForge** — animateur de sprites (chronologie, durées, aperçu animé)
- **TexForge** — texturation de modèle (peinture UV, application sur OBJ)
- **TextuCraft** — textures Minecraft 26.3 (bibliothèque, zones verrouillées, aperçu tuilé)

## Utilisation

Ouvrez `index.html` dans un navigateur. Aucune installation, aucun serveur.

Les cinq studios sont embarqués dans le fichier (base64 → décodage mémoire → `iframe.srcdoc`) :
le hub ne fait **aucune requête** vers un autre fichier.

## Raccourcis

| Touche | Effet |
| --- | --- |
| `Alt + 1…5` | ouvre un atelier directement |
| `Ctrl + K` | filtre la liste des ateliers |
| `Échap` | revient à l'accueil |
| `F` | plein écran sur le studio courant |

## Notes techniques

- Rendu : WebGL (MeshForge, TexForge) et Canvas 2D (PixelForge, SpriteForge, TextuCraft).
- Les studios s'exécutent dans une iframe `srcdoc`, donc avec une origine opaque :
  le stockage local n'est pas utilisé, et les exports passent par `blob:` + `download`.
- Poids : ~1,3 Mo, dont 719 Ko pour la bibliothèque de textures de TextuCraft.

## Licence

Usage personnel. Les textures Minecraft appartiennent à Mojang.

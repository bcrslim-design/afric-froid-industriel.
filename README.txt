AFRIC FROID INDUSTRIEL — FIELD DESK (version locale reconstruite)
==================================================================

DANS CETTE LIVRAISON
- index.html : application complète, sans dépendance externe/CDN.
- sw.js + manifest.json : mode installable et cache hors connexion après première visite sur HTTPS.
- assets/afric-froid-logo.jpeg : logo fourni pour le projet.

FONCTIONS TESTABLES
- Navigation mobile/ordinateur.
- Assistant local par règles (pas une IA générative, pas de clé API).
- Parcours SAV guidés : démarrage, BP/LPS, HP/HPS, huile, surcharge, manque de froid, régulation, ventilateur.
- Procédures de test multimètre pour composants courants.
- Calcul P/T simplifié R134a, R404A, R410A entre -40 et +60 °C (bar(g), interpolation).
- Surchauffe/sous-refroidissement uniquement pour R134a avec cette table simplifiée.
- Conversion 4–20 mA et 0–10 V, PID discret pédagogique, puissance triphasée, pré-dimensionnement de câble par chute de tension, unités.
- Circuit frigorifique SVG animé.
- Guides de câblage de principe et export SVG.
- Import/aperçu de PDF, images et DXF ASCII (LINE, CIRCLE, ARC, LWPOLYLINE, TEXT/MTEXT pris en charge).
- Caméra du téléphone sur HTTPS (si autorisée) ou import de photo. La photo est consultable localement; elle n'est pas analysée automatiquement par un modèle IA.
- Rapports locaux, checklist, export/import JSON et export TXT.

INSTALLATION GRATUITE (SANS NETLIFY DROP)
1. Extraire le ZIP. Le fichier index.html doit être à la racine du dossier.
2. Ouvrir un compte Cloudflare et utiliser Pages > Create project > Direct Upload (ou connecter un dépôt Git).
3. Téléverser le contenu du dossier, pas le ZIP comme un fichier isolé.
4. Ouvrir l'URL HTTPS créée. Accorder la permission caméra si nécessaire.
5. Sur téléphone Android/Chrome : menu ⋮ > Ajouter à l'écran d'accueil / Installer l'application.

COÛT ET LIMITES DU GRATUIT
- Cette version n'utilise ni serveur, ni base de données cloud, ni API payante. Les calculs et rapports restent sur l'appareil.
- Cloudflare Pages propose actuellement une offre gratuite pour les ressources statiques, avec des limites d'usage. Aucun fournisseur ne garantit que son offre restera gratuite pour toujours; les conditions peuvent changer.
- Une IA générative connectée (analyse avancée de photos/schémas et réponses ouvertes) n'est PAS incluse car elle nécessite un service modèle et généralement une clé/API/quotas. Le moteur local est une assistance à règles, pas une IA générative.

LIMITES TECHNIQUES ET SÉCURITÉ
- La table P/T est arrondie et interpolée; elle n'est pas certifiée pour réglage ou charge de fluide. Pour les mélanges R404A/R410A, dew/bubble ne sont pas séparés. Utiliser la documentation fabricant et un outil thermodynamique validé pour la mise en service.
- Le calcul câble ne vérifie pas l'intensité admissible, la pose, la température, le court-circuit, la protection ou le démarrage moteur.
- Les schémas de câblage sont des principes pédagogiques, jamais un plan d'exécution universel. Le schéma approuvé et la notice exacte priment.
- Le diagnostic fournit des pistes et des étapes de vérification, pas un verdict automatique.
- Caméra ordinaire ≠ caméra thermique; elle ne permet pas de voir le niveau d'huile à travers un carter opaque.
- Les données localStorage peuvent être perdues si le navigateur est réinitialisé. Exporter régulièrement JSON.
- Avant usage en entreprise, faire vérifier les procédures, les calculs et les schémas par un professionnel habilité. Ne jamais shunter les sécurités HP/BP/huile/thermique.

VALIDATION EFFECTUÉE
Voir VALIDATION.txt. Cette livraison est une application web fonctionnelle pour les outils locaux; elle n'est ni certifiée ni validée sur une installation frigorifique réelle.

SOURCE DE LA TABLE P/T SIMPLIFIÉE
Valeurs de référence arrondies et interpolées à partir du tableau publié ici :
https://cballast.com/documents/refrigerant-pt-chart-r134a-r404a-r410a
La source indique d'utiliser les données constructeur pour les décisions de mise en service. Les valeurs de ce projet ne sont pas certifiées.

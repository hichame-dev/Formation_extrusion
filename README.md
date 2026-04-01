# Formation Poste - GEMEF Industries

Formulaire de suivi des competences pour les formations aux postes de production.

## Lien d'acces

**https://formation-extrusion.netlify.app**

---

## Formations disponibles

| Formation | Sections | Statut |
|-----------|----------|--------|
| **Extrusion** | 19 sections | Disponible |
| **Conditionnement** | 7 sections | Disponible |
| **Melanges** | - | En construction |
| **Meunerie** | - | En construction |

Chaque formation a ses propres couleurs : orange (Extrusion), vert (Conditionnement), bleu (Melanges).

---

## Cloud Sync (multi-utilisateur)

Le systeme Cloud Sync permet a plusieurs utilisateurs de partager les profils de formation. Chaque utilisateur a son propre compte et ne peut modifier que ses profils.

Les profils des autres utilisateurs sont affiches avec un bandeau **"Mode lecture seule"**.

| Action | Mes profils | Profils des autres |
|--------|-------------|-------------------|
| Consulter | Oui | Oui |
| Modifier les competences | Oui | Non |
| Modifier les informations | Oui | Non |
| Supprimer | Oui | Non |
| Reinitialiser | Oui | Non |

> **Identifiants et procedure de connexion :** voir `CREDENTIALS.md` (fichier local, non publie sur GitHub)

---

## Fonctionnalites

- **Multi-formations** : Extrusion, Conditionnement, Melanges, Meunerie
- **Multi-profils** : gestion de plusieurs salaries en formation
- **Multi-utilisateur** : chaque utilisateur gere ses propres profils, consultation des autres en lecture seule
- **Notation Acquis 1/3 a 3/3** : niveau de maitrise detaille
- **Signatures manuscrites** : canvas de signature tactile
- **Synchronisation cloud** : partage automatique via JSONBin.io
- **Export PDF** : document formate pour impression
- **Export/Import JSON** : sauvegarde des donnees
- **Responsive** : fonctionne sur mobile et tablette
- **Filtres** : afficher par statut (A acquerir, En cours, Acquis)
- **Historique** : date de modification de chaque tache
- **Couleurs par formation** : theme adapte a chaque type de formation

---

## Calcul du pourcentage

Le pourcentage de progression prend en compte le niveau d'acquisition :

| Niveau | Pourcentage |
|--------|-------------|
| A acquerir | 0% |
| En cours | 0% |
| Acquis 1/3 | 33% |
| Acquis 2/3 | 67% |
| Acquis 3/3 | 100% |

---

## Hebergement

| Service | URL |
|---------|-----|
| **Site web** | Netlify - https://formation-extrusion.netlify.app |
| **Code source** | GitHub - https://github.com/hichame-dev/Formation_extrusion |
| **Base de donnees** | JSONBin.io |

---

## Panel Administrateur

Le panel admin permet de modifier les sections et taches directement sur le site sans toucher au code.

| Parametre | Valeur |
|-----------|--------|
| **Bouton** | "⚙ Admin" dans la barre de profils |
| **Mot de passe** | Voir `CREDENTIALS.md` |

Pour changer le mot de passe : ouvrir le panel Admin -> se connecter -> cliquer sur "Changer MDP".

---

## Migration vers un serveur interne (optionnel)

### Migrer le site web (index.html)

**Situation actuelle :** site heberge sur Netlify (gratuit, accessible depuis internet)

**Si l'entreprise a un serveur intranet :**
1. Copier le fichier `index.html` et le dossier `asset/` sur le serveur
2. Placer dans le dossier web du serveur (ex: `C:\inetpub\wwwroot\formation\`)
3. Acceder depuis le reseau interne via `http://[IP-SERVEUR]/formation`

**Si l'entreprise veut un domaine pro (ex: formation.gemef.fr) :**
- Prendre un hebergement OVH ou Ionos (~3-5€/mois)
- Uploader `index.html` + dossier `asset/` via FTP
- Configurer le domaine

---

### Migrer la base de donnees (JSONBin → serveur interne)

**Situation actuelle :** donnees stockees sur JSONBin.io (cloud externe, gratuit)

#### Option A — Serveur PHP (recommande, le plus simple)

Demander a l'IT : *"Peut-on heberger 3 fichiers PHP sur le serveur intranet ?"*

Creer ces 3 fichiers sur le serveur :

**`data.json`** — fichier vide au depart :
```json
{}
```

**`load.php`** — lecture des donnees :
```php
<?php
header('Content-Type: application/json');
header('Access-Control-Allow-Origin: *');
$data = file_get_contents('data.json');
echo $data ?: '{}';
```

**`save.php`** — ecriture des donnees :
```php
<?php
header('Access-Control-Allow-Origin: *');
header('Access-Control-Allow-Methods: POST');
$input = file_get_contents('php://input');
if ($input) {
    file_put_contents('data.json', $input);
    echo '{"ok": true}';
} else {
    http_response_code(400);
    echo '{"error": "No data"}';
}
```

Ensuite dans `index.html`, remplacer les URLs JSONBin par les URLs du serveur :
- `https://api.jsonbin.io/v3/b/[BIN_ID]/latest` → `http://[IP-SERVEUR]/formation/load.php`
- `https://api.jsonbin.io/v3/b/[BIN_ID]` (PUT) → `http://[IP-SERVEUR]/formation/save.php`
- Supprimer les headers `X-Master-Key` dans les requetes fetch

#### Option B — Base de donnees MySQL

Demander a l'IT : *"Peut-on avoir une base MySQL et un acces PHP ?"*

Cette option necessite plus de developpement (~3-5h). Contacter l'administrateur technique.

---

## Support technique

Pour toute modification du formulaire, contacter l'administrateur du repository GitHub.

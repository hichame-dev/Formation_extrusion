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

## Configuration Cloud Sync (multi-utilisateur)

Le systeme Cloud Sync permet a plusieurs utilisateurs de partager les profils de formation. Chaque utilisateur a son propre compte et ne peut modifier que ses profils.

### Informations de connexion

| Parametre | Valeur |
|-----------|--------|
| **Cle API** | `$2a$10$u3FnP3uRAlAK.tD4eZwz1Oa/90/wyX304cYOBF1V55k4wWikPBDpG` |
| **Bin ID** | `69723ebdae596e708fedbeb5` |

### Procedure de connexion

1. Ouvrir le formulaire
2. Cliquer sur **"Cloud Sync"** (barre de profils)
3. Entrer **votre nom d'utilisateur** (identifiant unique, ex: `jean-dupont`)
4. Entrer la cle API et le Bin ID
5. Cliquer sur **Connecter**

### Droits d'acces par utilisateur

| Action | Mes profils | Profils des autres |
|--------|-------------|-------------------|
| Consulter | Oui | Oui |
| Modifier les competences | Oui | Non |
| Modifier les informations | Oui | Non |
| Supprimer | Oui | Non |
| Reinitialiser | Oui | Non |

Les profils des autres utilisateurs sont affiches avec un bandeau **"Mode lecture seule"** et le nom du proprietaire.

---

## Mail type a envoyer aux utilisateurs

```
Objet : Acces au formulaire de suivi de formation - GEMEF Industries

Bonjour,

Veuillez trouver ci-dessous le lien d'acces au formulaire de suivi des competences :

https://formation-extrusion.netlify.app

Procedure de connexion au systeme de synchronisation :

1. Ouvrir le lien ci-dessus
2. Cliquer sur le bouton "Cloud Sync" situe dans la barre superieure
3. Renseigner les informations suivantes :
   - Nom d'utilisateur : choisissez un identifiant unique (ex: prenom-nom)
   - Cle API : $2a$10$u3FnP3uRAlAK.tD4eZwz1Oa/90/wyX304cYOBF1V55k4wWikPBDpG
   - Bin ID : 69723ebdae596e708fedbeb5
4. Cliquer sur "Connecter"

Important : retenez bien votre nom d'utilisateur, il vous sera necessaire
pour modifier vos profils. Vous pourrez consulter les profils des autres
utilisateurs en lecture seule.

Je reste a votre disposition pour toute question.

Cordialement,
```

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

## Support technique

Pour toute modification du formulaire, contacter l'administrateur du repository GitHub.

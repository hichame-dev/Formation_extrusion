# Formation Poste Extrusion - GEMEF Industries

Formulaire de suivi des competences pour la formation au poste d'extrusion.

## Lien d'acces

**https://formation-extrusion.netlify.app**

---

## Connexion

### Identifiants utilisateurs

| Identifiant | Utilisateur | Mot de passe |
|-------------|-------------|--------------|
| **CDP1** | CDP1 | `GemefCDP1` |
| **CDP2** | Sebastien | `GemefCDP2` |
| **CDP3** | CDP3 | `GemefCDP3` |
| **ADMIN** | Admin | `GemefADMIN` |

### Procedure de connexion

1. Ouvrir le formulaire
2. Entrer l'identifiant (ex: CDP1)
3. Entrer le mot de passe
4. Cliquer sur **Se connecter**

La connexion au cloud est automatique apres identification.

---

## Configuration Cloud Sync (technique)

| Parametre | Valeur |
|-----------|--------|
| **Cle API** | `$2a$10$u3FnP3uRAlAK.tD4eZwz1Oa/90/wyX304cYOBF1V55k4wWikPBDpG` |
| **Bin ID** | `69723ebdae596e708fedbeb5` |

Ces codes sont integres automatiquement lors de la connexion utilisateur.

---

## Mail type a envoyer aux utilisateurs

```
Objet : Acces au formulaire de suivi de formation - Poste Extrusion

Bonjour,

Veuillez trouver ci-dessous le lien d'acces au formulaire de suivi des competences :

https://formation-extrusion.netlify.app

Procedure de connexion :

1. Ouvrir le lien ci-dessus
2. Entrer votre identifiant (CDP1, CDP2 ou CDP3)
3. Entrer votre mot de passe
4. Cliquer sur "Se connecter"

Une fois connecte, vous aurez acces a l'ensemble des profils de formation partages.

Je reste a votre disposition pour toute question.

Cordialement,
```

---

## Fonctionnalites

- **16 sections** de competences (~90 taches)
- **Multi-profils** : gestion de plusieurs salaries en formation
- **Notation Acquis 1/5 a 5/5** : niveau de maitrise detaille
- **Signatures manuscrites** : canvas de signature tactile
- **Synchronisation cloud** : partage automatique via JSONBin.io
- **Export PDF** : document formate pour impression
- **Export/Import JSON** : sauvegarde des donnees
- **Responsive** : fonctionne sur mobile et tablette
- **Filtres** : afficher par statut (A acquerir, En cours, Acquis)
- **Historique** : date de modification de chaque tache

---

## Calcul du pourcentage

Le pourcentage de progression prend en compte le niveau d'acquisition :

| Niveau | Pourcentage |
|--------|-------------|
| A acquerir | 0% |
| En cours | 0% |
| Acquis 1/5 | 20% |
| Acquis 2/5 | 40% |
| Acquis 3/5 | 60% |
| Acquis 4/5 | 80% |
| Acquis 5/5 | 100% |

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

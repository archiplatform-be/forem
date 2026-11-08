# ??? ArchiPlatform ? Fork Officiel Forem (Belgique)

Ce d?p?t est le fork officiel de [forem/forem](https://github.com/forem/forem) propulsant **ArchiPlatform** (`archi-platform.be`).

## ?? Architecture "Clean Fork" (Z?ro conflit lors des mises ? jour)

Pour garantir que les mises ? jour automatiques de Forem (`.github/workflows/archi-upstream-sync.yml`) s'appliquent sans jamais casser nos personnalisations :

1. **Isolation du Design (Phase 3 - Figma Clair/Obscur)** :
   - Tous les styles propres ? ArchiPlatform r?sident exclusivement dans `app/assets/stylesheets/archi_platform/`.
   - Aucune modification directe des feuilles `.scss` natives de Forem.
2. **Isolation des Fonctionnalit?s M?tier (Phase 4 & 5 - Bot IA Normes Belges, Publication Anonyme, SSO UPA)** :
   - Connect?es via les **Webhooks**, l'**API REST Forem** et **OmniAuth OIDC** (h?berg?es dans les d?p?ts priv?s de l'organisation `archiplatform-be`).
3. **Time Machine & Rollback sans perte de posts** :
   - Orchestr?s via le d?p?t priv? [`archiplatform-be/timemachine`](https://github.com/archiplatform-be/timemachine).

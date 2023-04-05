# Proxy

Cet exemple met en évidence la structure interne des conteneurs de Qt basée sur le patron de conception Proxy et la technique du partage implicite (pointeur partagé).

## Analyse

Différentes opérations sont réalisées sur des objets du type QString et QList et à chaque fois les adresses du proxy (QList ou QString par exemple) et de ses données internes sont affichées.

Vous constaterez que si les données ne sont pas modifiées, seule l'adresse du proxy est modifiée, celle des données reste inchangée. Ces opérations sont donc très performantes.

Pour aller plus loin regardez la signature des fonctions appelées, vous constaterez que seules les fonctions qui sont marquées *const* ne copient pas les données.
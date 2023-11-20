# Git Commands

### Commits

Para ver un listado de los commit de una rama muevete hacia ella y ejecuta:

    git log

Para ver los cambios realizados en un commit:

    git show <hash del commit>

Si solo deseas ver la lista de archivos modificados en un commit específico, puedes usar el siguiente comando:

    git diff-tree --no-commit-id --name-only -r <hash del commit>

Si deseas mover tu HEAD a un commit en concreto para desde ahí crear una nueva rama o simplemente visualizar ese commit:

    git checkout <hash del commit>

Si quieres cambiar el mensaje del commit porque te has equivocado:

    git commit --amend -m "Nuevo mensaje para el commit"

---

### Reset

Para retirar el último commit realizado manteniendo los cambios en el stage:

    git reset --soft HEAD^

Para retirar el último commit realizado manteniendo los cambios, pero fuera del stage:

    git reset –-mixed HEAD^

Para retirar el último commit realizado sin mantener que se hicieron:

    git reset –-hard HEAD^

_<small> Si quieres sobre un commit en concreto sustituye HEAD por el hash del commit.</small>_

---

### Revert

Para deshacer los cambios de un commit e introducirlos como un nuevo commit utiliza:

    git revert <hash del commit>

Si tienes el siguiente gráfico en la rama principal donde cada letra representa un commit:

    A---B---C---D  (main)

Al realizar este revert sobre C generas un commit E con los cambios deshechos de C:

    A---B---C---D---E  (main) (E contiene los cambios deshechos de C)

---

### Branches

Para crear una nueva rama:

    git branch <nombre_de_la_rama>

Para moverse a una rama:

    git checkout <nombre_de_la_rama>

Para crear una nueva rama y moverse directamente a ella:

    git checkout -b <nombre_de_la_rama>

cambios

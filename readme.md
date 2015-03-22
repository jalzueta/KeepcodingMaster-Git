#Archivo de respuestas a las preguntas de la práctica
====================================================

**1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?**
Utilizo "git reset --hard HEAD~1".
Con "git reset HEAD~1" muevo tanto el puntero HEAD con el puntero de la rama al comit anterior según el "log", es decir deshago el último commit realizado.
Con el modificador "--hard" fuerzo a que en el Working copy pase a haber lo mismo que en el commit al que acabo de ir, perdiéndose así los cambios realizados en el último commit.

**2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
Utilizo "git reset --hard 5ebc57f", porque de esta manera muevo tanto el puntero "HEAD" como el puntero de rama "htmlify".
Pongo el modificador "--hard" para que se me actualice el Working copy con los archivos del commit al que acabo de ir.

**3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
El merge que acabamos de realizar no ha modificado en absoluto el grafo, por lo que no ha habido conflictos.
En cualquier caso, todos los commits forman una lista, por lo que ha sido un "fast-forward merge" y en ese tipo de merges no hay posibilidad de conflictos.

**4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**
Sí, ha aparecido un conflicto en poem.md.
El motivo es que el archivo poem.md ha sido modificado en las dos ramas que participan en el merge ("htmlify" y "matrix") y además esas modificaciones afectaban a las mismas líneas del archivo, en este caso las líneas 0 y 1.

**5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
No, no ha habido conflictos en este merge.
No ha habido conflictos porque el contenido del archivo readme.md era exactamente igual en ambas ramas.

**6. ¿Qué comando o comandos utilizaste en el paso 25?**
Comando utilizado: "git log --graph --decorate --pretty=oneline"
Modificadores:
    *--graph: muestra el gráfico con colorines para las ramas.
    *--decorate: muestra los punteros (HEAD y ramas) en el commit al que apuntan.
    *--pretty=oneline: elimina la información "menos relevante" de cada commit. Solo muestra el "hash" y la descripción del commit.

**7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
Podría ser fast-forward porque la rama "title" nace directamente del commit al que apunta "master", por lo que el merge se puede resolver recolocando el puntero "master"

**8. ¿Qué comando o comandos utilizaste en el paso 27?**
Busco a través del diagrama de "reflog" el "hash" del commit al que apuntaba master antes del último merge: f894881
He utilizado: "git reset f894881". No pongo el modificador "--hard" porque no queremos alterar el contenido del Working copy.

**9. ¿Qué comando o comandos utilizaste en el paso 28?**
He utilizado el comando "git checkout -- poem.md"

**10. ¿Qué comando o comandos utilizaste en el paso 29?**
He utilizado "git branch -D title"

**11. ¿Qué comando o comandos utilizaste en el paso 30?**
Busco con reflog el "hash" del commit que se ha creado durante el merge que hemos deshecho: dfb8be6
Utilizo "git reset --hard dfb8be6" para llevar tanto el punture "HEAD" como el puntero de la rama "master" hasta ese commit
Pongo el modificador "--hard" porque quiero que mi Working copy reciba los cambios almacenados en ese commit

**12. ¿Qué comando o comandos usaste en el paso 32?**
Busco con "git reflog" el commit inicial: f3b142d
Ejecuto "git checkout f3b142d" para llevar el puntero HEAD a ese commit (inicial)

**13. ¿Qué comando o comandos usaste en el punto 33?**
Ejecuto "git checkout master", ya que sé que master apunta al commit final.

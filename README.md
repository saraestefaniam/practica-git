# practica-git
-	**¿Qué comando utilizaste en el paso 11? ¿Por qué?**
Git reset --hard HEAD ~1
Porque quería deshacer le commit y además deshacerlo de mi working copy

-	**¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
Git reflog, git reste --hard xxxxx
Porque como git tiene el síndrome de Diógenes, sabemos que no ha borrado nuestro commit, solo debemos encontrarlo y para eso nos sirve reflog que nos muestra todo lo que ha pasado en nuestro repositorio. Identificamos cual es el hash de ese commit que deshicimos, lo copiamos y volvemos a aplicar git reset con el hash del commit anterior


-	**El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
Git merge main
Porque queremos que styled (era la rama donde estábamos) absorba a main. No generó conflicto hasta donde entiendo, me dijo “already up to date”

-	**El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?** 
Git checkout styled (para pasar a esa rama) y luego git merge htmlify (para absorber esa rama desde styled
Sí que generó conflicto porque nuestro archivo git-nuestro estaba diferente en la rama styled, lo actualizamos en la htmlify y luego nos movimos y quisimos absorber esa la rama.

-	**El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
No causó conflicto, hizo un fast-forward

-	**¿Qué comando o comandos utilizaste en el paso 25?**
git log --graph 
git config alias.graph "log --graph --decorate --pretty=oneline"
git graph

-	**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
Sí, porque así se adelantaba hacia la rama title

-	**¿Qué comando o comandos utilizaste en el paso 27?**
Git reset –soft HEAD~1

-	**¿Qué comando o comandos utilizaste en el paso 28?**
git reset --hard HEAD~1

-	**¿Qué comando o comandos utilizaste en el paso 29?**
git branch -D title

-	**¿Qué comando o comandos utilizaste en el paso 30?**
Ya en este punto todo se puso muy confuso… jaja pero busqué el hash del commit de donde estaba title (rama que ya borramos y con la que habíamos hecho merge en el paso 26) y utilicé este comando para llegar allí
git reset --hard 07a8119

-	**¿Qué comando o comandos usaste en el paso 32?**
Primero git reflog para encontrar el hash de ese primer commit y luego un git reseft sof con el hash del commit:
git reset –soft c80fa6a

-	**¿Qué comando o comandos usaste en el punto 33?**
Apliqué la misma lógica que en el punto anterior, busqué el hash de ese commit con un gir reflog y luego apliqué un git reset --soft con el hash

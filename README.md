proyectoAlex1
=============

### About

Curso aprendiendonodered21. Este es mi primer proyecto creado en node-red y subido con "Version Control", "Branches" master, al "Git Origins"
https://github.com/aerobit373/alexAprendiendoNodered.git
Simplemente node-red (que esta dando un servicio https local desde mi raspberryPi) se conecta, mediante un nodo "mqtt in", al broker publico del profesor (que entre otros "topics" esta publicando la temperatura de su raspberry1 cada 3 seg.), y se suscribe a ese dato. cuando este primer nodo recive el dato, pasa el mensaje a otros dos. Uno, solo muestra el dato en su "node status", el otro es un "switch" que tiene 2 salidas una [mayor57] y otra  [menor57], la primera cambia el dato por la string: CALIENTE y la segunda por: normal. Estos dos nodos "change" pasan su resultado a un "rbe". Por ultimo el nodo rbe bloquea el flujo a menos que el mensaje cambie de manera que esta recibiendo mensajes "normal" cada 3 seg pero los bloquea, solo cuando el mensaje cambia a "CALIENTE", lo pasa al nodo final "debuj" que lo imprime en pantalla.
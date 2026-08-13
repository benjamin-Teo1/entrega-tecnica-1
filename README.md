# Entrega Técnica 1 - Diagnóstico de entorno

Script en Node.js que informa datos básicos del entorno de ejecución: 
versión de Node, plataforma del sistema operativo, argumentos pasados 
por consola y el usuario del sistema.

## Cómo ejecutarlo

Con Node directamente:

node diagnostico.js


O usando el script definido en `package.json`:

npm run diagnostico


También se le pueden pasar argumentos extra, por ejemplo:

node diagnostico.js arg1 desarrollo


## Aprendizajes
Lo que más me costó fue entender que `process.env.USER` no funciona en Windows, 
porque esa variable es propia de sistemas Unix (Linux/Mac). Tuve que investigar 
y usar `process.env.USER || process.env.USERNAME` para que el script funcione 
sin importar el sistema operativo donde se ejecute.

## Evidencia de ejecución
![Evidencia de ejecución](img/captura.png)
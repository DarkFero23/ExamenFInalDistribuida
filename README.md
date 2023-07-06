# ExamenFInalDistribuida

En este Readme se hara detalle de los desafios enfrentados a la hora de implementar este balanceador de carga , y tambien de como ejecutar la aplicacion.
LOs desafios que me encontre a la hora de desarrollar este examen final fueron 2, uno relacionado con el balanceador de carga y otro relacionado con el flask.
Con respecto al flask tuve este error error jinja2.exceptions. TemplateNotFound: index.html en Flask, este error lo solucione investigando un poco en internte y se debia a que necesitaba especificar de buena manera en el flask las direcciones de las carpetas y de sus archivos.
Con respecto al balanceador de carga mi inconveniente fue con el "server_name" , con el dominimo , lo solucione quitantole esa linea y ejecutandolo como "localhost"

AHora para poder ejecutar la aplicacion , se tiene que pegar la carpeta "app" en los nodos y tener iniciado el servicio de nginx , ademas de que hay que verificar ambas ip y los puertos para poder especificarlos en el balanceado de carga. Y hay que iniciar el archivo "app.py", en abmos nodos.

EL arhcivo "balanceado_de_carga" tiene que estar en el node master , entrado a esta direccion nano /etc/nginx/conf.d/load-balancing.conf dentro de ese arachivo tenemos que cambiar las ip a las que corresponden a nosotros al igual que el puerto.
Con eso seria suficiente para que la aplicacion funcione 

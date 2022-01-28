build : ## Comando para ejecutar y lanzar el sitio usando go Hugo 
	hugo -D > /dev/null 2>&1

.PHONY: clean

clean : ## Elimina los archivos de la carpeta dist
	rm -rf ./dist/ > /dev/null 2>&1

post : ## Comando para generar un nuevo post, usa dos parametros POST_NAME y POST_TITLE
	hugo new posts/$(POST_NAME).md
	echo '---\ntitle: "$(POST_TITLE)"\ndate: 2010-03=26T08:47:11+01:00\ndraft: false\n---' > ./content/posts/$(POST_NAME).md  

help: ##provee informaci√√≤n de cada uno de los comandos de Makefile
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'


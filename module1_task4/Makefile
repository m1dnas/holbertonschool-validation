build:	## Genera un website desde el markdown y archivos de config en el directorio dist
	hugo > /dev/null 2>&1
	
clean:	## Limpia el contenido del directorio dist
	rm -rf ./dist/*

post:	## Crea una nueva publicación con el POST_NAME y POST_TITLE
	hugo new posts/$(POST_NAME)
	sed -i '/title/c\title: "$(POST_TITLE)"' content/posts/$(POST_NAME).md

help:	## Te da información sobre todos los makefiles definidos
	@fgrep "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/##//'
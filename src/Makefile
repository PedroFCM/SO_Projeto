#Makefile para compilar o projeto todo

CFLAGS= -O2
CC=gcc

MA = ma_src/
SV = sv_src/
AG = ag_src/
CV = cv_src/
COMP = compactador_src/

OBJ = GLOBAL_SOURCE/obj

all: source ma sv ag comp cv

source: global cache

global: GLOBAL_SOURCE/global.c GLOBAL_SOURCE/global.h
	$(CC) $(CFLAGS) -c GLOBAL_SOURCE/global.c
	mkdir -p $(OBJ)
	mv global.o $(OBJ)

cache: GLOBAL_SOURCE/cache.c GLOBAL_SOURCE/cache.h
	$(CC) $(CFLAGS) -c GLOBAL_SOURCE/cache.c
	mkdir -p $(OBJ)
	mv cache.o $(OBJ)

ma:
	cd $(MA) && mkdir -p obj/ && $(MAKE)
	cd ..
	echo "Manutenção de artigos compiled..."

sv:
	cd $(SV) && mkdir -p obj/ && $(MAKE)
	cd ..
	echo "Servidor de vendas compiled..."

ag:
	cd $(AG) && mkdir -p obj/ && $(MAKE)
	cd ..
	echo "Agregador compiled..."

comp:
	cd $(COMP) && mkdir -p obj/ && $(MAKE)
	cd ..
	echo "Compactador compiled..."

cv:
	cd $(CV) && mkdir -p obj/ && $(MAKE)
	cd ..
	echo "Cliente Vendas compiled..."

clean:
	rm -rf FILES/2019*
	rm -rf PipeVendas/pipePrint*
# Dockerfile

## Instrução FROM
	- Serve para dizer qual imagem base iremos utilizar, por exemplo: FROM ubuntu


## Instrução RUN
	- Serve para rodar instruções na nossa imagem docker, por exemplo: 
		RUN apt-get update && apt-get install -y apache2 //executa a instrução de instalação do Apache

## Instrução EXPOSE
	- Serve para liberarmos uma porta na imagem docker, por exemplo: 
		EXPOSE 80 //liberando a porta 80

## Instrução CMD
	- Serve para executar comandos após a instalação dos pacotes, por exemplo 
		CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"] //Essa instrução executa o Apache


## Comandos

Comando utilizado para gerar a imagem a partir do Dockerfile
```ssh
$ docker build -t ubuntu/apache [diretorio onde se encontra o Dockerfile]
```

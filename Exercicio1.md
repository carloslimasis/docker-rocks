# Comandos

Comando utilizado para baixar uma imagem específica do docker hub, neste caso
a imagem mysql
```sh
$ docker pull mysql
```

Comando utilizado para visualizar todas as imagens já baixadas em sua máquina
```sh
$ docker images
```

Comando utilizado para rodar/executar a imagem baixada anteriormente
```sh
$ docker run --name database -e MYSQL_ROOT_PASSWORD=teste123 -d mysql
```

O -e é a opção de enviroment, ou seja, setamos um valor para a variável de ambiente para o MySQL.
O -d é para rodar o container em background.

Outras opções são:

O -p para dizer em qual porta, por exemplo, a aplicação rodará, segue um exemplo:
-p 80:80 onde -p [porta da sua máquina]:[porta da imagem]

Comando utilizado para observar os containers que acabamos de criar
```sh
$ docker ps
```
Na resposta do comando temos: 
* STATUS: vemos que o container está rodando a mais de 13 segundos;
* PORTS: o container está com a porta 3306, o padrão do MySQL;
* NAMES: vemos que o nome que definimos, "database", realmente foi dado ao container.

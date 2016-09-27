#Comandos

Comando utilizado para mostrar quantos processos estão em execução na minha máquina
```ssh
$ ps aux | wc -l
```

Comando utilizado para mostrar somente containers em execução
```ssh
$ docker ps
```

Comando utilizado para mostrar todos os  containers criados
```ssh
$ docker ps
```

Comando utilizado para parar um container em execução
```ssh
$ docker stop nome-container
```

Comando utilizado para entrarmos em um container em execução
```ssh
$ docker exec -it nome-container bash
```

Ou
```ssh
$ docker run -it nome-container bash
```


Onde -i garante uma interatividade com o shell
Onde -t garante que irá simular o TTY

Poderíamos fazer:
```ssh
$ docker exec -i -t nome-container bash
```

A forma abreviada seria:
```ssh
$ docker exec -it nome-container bash
```	

Comando utilizado para remover um container 
```ssh
$ docker rm [id-do-container]
```

Ou

```ssh
$ docker rm [nome-do-container]
```

Comando utilizado para remover 2 ou mais containers ao mesmo tempo
```ssh
$ docker rm $(docker ps -qa)
```

O comando -q faz com que o docker passe os ids dos containers como parâmetro
O comando -a faz com que o docker retorne todos os containers

Desta forma, ao utilizar o comando -qa teremos uma lista de ids dos meus containers


Comando utilizado para remover imagens
```ssh
$ docker rmi [nome-da-imagem]
```

Ou

```ssh
$ docker rmi [id-da-imagem]
```


O que é container, e para que ele serve?

O próprio nome ja nos remete aos grandes containers dos portos. Para que eles servem? 

- Facilitam o transporte de cargas pesadas;
- Garantem que a carga chegará ao destino sem ser danificada;
- Os navios podem transportar vários containers ao mesmo tempo;


Fazendo um comparativo com o docker, temos nossos containers com suas "cargas" (Apache, Java, Mysql e etc...) dentro dele.
A utilidade disso é que o desenvolvedor pode ter um ambiente completo em sua máquina(com Tomcat, Java, Mysql...) com a utilização de containers.


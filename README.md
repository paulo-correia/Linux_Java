# Java

## Debian / Ubuntu

Toda a instalação é feita como **root**

Baixe o JRE no site http://java.com/pt\_BR/download/linux\_manual.jsp?locale=pt\_BR

Copie o arquivo .tar.gz para a pasta /opt com o comando:

`cp nome_do_arquivo /opt`

Entre na pasta /opt com o comando:

`cd /opt`

Extraia o conteúdo dos .tar.gz com o comando:

`tar -xvzf nome_do_arquivo.tar.gz`

Edite o /etc/profile

`Procure JRE_HOME=, se não existir coloque na última linha e após o = e coloque o caminho /opt/jre(versão do java)`

Salve e saia

Informe ao Sistema Operacional aonde está o java com os comandos:

Caso não instale o JDK não digite a linha do javac (2ª linha) e altere /opt/jdk(versão do java) para /opt/jre(versão do java)

 ```
update-alternatives --install "/usr/bin/java" "java" "/opt/jdk(versão do java)/bin/java" 1
update-alternatives --install "/usr/bin/javac" "javac" "/opt/jdk(versão do java)/bin/javac" 1
update-alternatives --install "/usr/bin/javaws" "javaws" "/opt/jdk(versão do java)/bin/javaws" 1
```

Informe ao Sistema Operacional quem é o java padrão com os comandos:

Caso não instale o JDK não digite a linha do javac (2ª linha) e altere /opt/jdk(versão do java) para /opt/jre(versão do java)

 ```
update-alternatives --set java /opt/jdk(versão do java)/bin/java
update-alternatives --set javac /opt/jdk(versão do java)/bin/javac
update-alternatives --set javaws /opt/jdk(versão do java)/bin/javaws
```

Recarregue o profile com o comando:

`sh /etc/profile`
# Utiliza a imagem oficial do OpenJDK, versão 11
FROM openjdk:11-jdk

# Instala o wget e o unzip, que podem ser necessários para a instalação do Gradle
RUN apt-get update && apt-get install -y wget unzip

# Instalar Gradle
ENV GRADLE_VERSION 7.2
RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -P /tmp
RUN unzip -d /opt/gradle /tmp/gradle-${GRADLE_VERSION}-bin.zip
ENV GRADLE_HOME /opt/gradle/gradle-${GRADLE_VERSION}
ENV PATH ${GRADLE_HOME}/bin:${PATH}

# Copiar os arquivos do projeto
COPY . /app

# Definir o diretório de trabalho
WORKDIR /app

# Compilar o projeto
#RUN gradle build

# Executar a aplicação
#CMD ["gradle", "run"]

# Mantém o container rodando
#CMD ["tail", "-f", "/dev/null"]


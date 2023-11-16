# Usar uma imagem base com Java JDK
FROM openjdk:11-jdk

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
RUN gradle build

# Executar a aplicação
CMD ["gradle", "run"]

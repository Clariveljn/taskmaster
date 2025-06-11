# 🗂️ TaskMaster

**TaskMaster** es una aplicación en Java hecha con Maven que simula una lista de tareas en la consola. Al ejecutarla, muestra un mensaje de bienvenida, agrega algunas tareas ya definidas y las muestra junto con el entorno activo (Desarrollo o Producción), el cual se elige usando perfiles de Maven.

## 🛠️ Descripción del Proyecto

Este proyecto fue desarrollado con el objetivo de aprender y aplicar conceptos fundamentales del ecosistema Maven, tales como:

- Gestión de dependencias y plugins
- Uso de perfiles personalizados (`dev` y `prod`)
- Ejecución de clases principales con `exec-maven-plugin`
- Control del ciclo de vida del proyecto
- Integración de pruebas automatizadas con JUnit

## ✅ Requisitos previos

* Java 21 instalado
* Maven instalado y configurado correctamente


## 💻 Comandos útiles de Maven

```bash
# Compilar el proyecto
mvn compile

# Ejecutar la aplicación (con perfil de desarrollo)
mvn exec:java -Pdev

# Ejecutar pruebas unitarias
mvn test

# Limpiar archivos compilados
mvn clean

# Generar el archivo JAR
mvn package
```

## 📦 Dependencias utilizadas

| Dependencia     | Versión | Propósito                                                                    |
| --------------- | ------- | ---------------------------------------------------------------------------- |
| `commons-lang3` | 3.12.0  | Utilidades extendidas para Java (no utilizadas directamente en este ejemplo) |
| `junit`         | 4.12    | Framework para pruebas unitarias                                             |
 

## 🔌 Plugins utilizados
| Plugin                  | Versión | Funcionalidad                                |
| ----------------------- | ------- | -------------------------------------------- |
| `maven-compiler-plugin` | 3.8.1   | Compila el código fuente usando Java 21      |
| `exec-maven-plugin`     | 3.1.0   | Ejecuta la clase principal `App` desde Maven |


## 🌐 Perfiles
El proyecto define dos perfiles que permiten establecer el entorno de ejecución:

* **dev:** configura el sistema en modo Desarrollo

* **prod:** configura el sistema en modo Producción

El entorno activo se muestra en la salida de consola mediante la propiedad env.name.

## 📁 Estructura del Proyecto
```bash
taskmaster/
├── pom.xml
├── src/
│   ├── main/
│   │   └── java/com/equipo/taskmaster/App.java
│   └── test/
│       └── java/com/equipo/taskmaster/AppTest.java
└── README.md
```
## 🚀 Cómo ejecutar

**1. Clonar el repositorio**
```bash
git clone https://github.com/tu-usuario/taskmaster.git
cd taskmaster
```

**2. Compilar el proyecto**
```bash
mvn compile
```
**3. Ejecutar la aplicación (ejemplo con entorno de desarrollo)**
```bash
mvn exec:java -Pdev
```
## 📘 Ejemplo de salida
```bash
Bienvenido a TaskMaster!
Tareas pendientes:
- Estudiar Maven
- Leer sobre CI/CD
Ambiente: Desarrollo
```

## 🧠 Mayor Aprendizaje Técnico
Este proyecto nos permitió entender cómo Maven estructura y automatiza el ciclo de vida de una aplicación Java. 

**Aprendimos a:**

* Utilizar perfiles para adaptar la configuración a diferentes entornos

* Ejecutar clases principales mediante exec-maven-plugin

* Gestionar correctamente las dependencias y sus versiones

* También comprender la importancia de una configuración clara y bien organizada en el archivo pom.xml.

## 🚧 Desafío Enfrentado

El principal reto fue lograr que la propiedad env.name se pasara correctamente desde los perfiles Maven hasta el entorno de ejecución en Java. Fue necesario investigar cómo funcionan los perfiles y cómo leer propiedades del sistema usando System.getProperty. Además, asegurar la compatibilidad de versiones entre plugins, el JDK y las dependencias también presentó desafíos.

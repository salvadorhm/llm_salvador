# LLM Respositorio de prueba
Respositorio de prueba para implementar LLM y una aplicación web

## 1. Instalación de ollama

Para instalar ollama accedemos a la pagina de [ollama](https://ollama.com/download/linux), en una terminal se ejecuta el siguiente comando

````bash
$ curl -fsSL https://ollama.com/install.sh | sh
````
## 2. Ejercutar el servidor 

Una vez instalado se ejecutar el servidor ollama con el siguiente comando

````bash
$ ollama serve
````

## 3. Descargar algún modelo

En la página de [modelos](https://ollama.com/library) de ollama se busca el modelo deseado y se descaga con el siguiente comando:

````bash
$ ollama pull tinyllama
````

## 4. Prueba de request a la API REST

Para realizar una petición básica a la API de ollama se sigue la siguiente estructura

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}'
````


### 4.1 Consulta a la API REST sin stream

Prueba de consulta sin stream

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
  "stream": false
}'
````

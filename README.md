# static-status

[![Bluemix](https://www.ibm.com/developerworks/community/blogs/e902a0a0-d0de-4d45-9df9-230811c7f56f/resource/BLOGS_UPLOADED_IMAGES/Bluemix.JPG?lang=en)](http://bluemix.net)

Essa é uma aplicação de exemplo usando o buildpack de arquivos estáticos do Cloud Foundry configurada para fornecer informações de status do servidor NGINX. A aplicação é composta de 3 arquivos:

  - Staticfile - arquivo requerido pelo buildpack
  - index.html - uma simples página web
  - nginx.conf - o arquivo de configuração do servidor com os parâmetros para que ele apresente métricas do servidor

Para executar esse exemplo, clone esse repositório:
```sh
$ git clone https://github.com/pfelipebr/static-status
```
E faça o push para o Bluemix:
```sh
$ cf push APPNAME
```
Após a aplicação iniciada, você podera acessar a url da aplicação /nginx_status e será exibida uma tela como a abaixo:
```sh
Active connections: 1
server accepts handled requests
 21 21 20
Reading: 0 Writing: 1 Waiting: 0
```

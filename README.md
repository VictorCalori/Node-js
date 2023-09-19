Primeiramente após ligar a máquina virtual, abra o terminal do ubuntu, e atualize a máquina;

Após isso ative o ambiente do nodeejs-env, através do comando: source ./nodejs/nodejs-env/bin/activate;

Exemplo de saída:
(nodejs-env) aluno10-02@aluno1002-VirtualBox:

Dentro do ambiente, procure a pasta onde estava o nodejs-env e busque pela pasta src;

Exemplo de pasta:

~/nodejs/nodejs-env

Na pasta src, digite o seguinte comando: sudo nano index.js, para criar um arquivo com esse e entrar no nano para editá-lo;

No nano cole o seguinte código:

var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello world');
}).listen(5000);

Esse comando serve para criar um servidor, escrito "Hello world" na porta 5000 usando o protocolo TCP;

Para abrir esse servidor, dentro do ambiente "nodejs-env" digite node index.js, para abrir o arquivo no servidor;

Para entrar no site do servidor, abra o navegador e digite localhost:<porta que estano .listen> que no caso é 5000;

Caso queira entrar em um servidor que esteje em outra máquina, basta colocar o ip da máquina seguido da porta, da seguinte maneira: 192.168.40.68:<porta do .listen>;

Para entrar, certifique-se que a porta esteje liberada e não bloqueada pelo firewall.


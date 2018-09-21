# serviceDaemon
Service Daemon for centOs

Primeiro, deve se ter certeza que esteja instalada a versão do CentOs 7 ou acima. e que possua o gerenciador de serviços do systemd (sysctl).

Após serem criados os arquivos, para iniciar o arquivo, se roda em shell "service (nome do serviço colocado no init.d) start" para iniciar, "service (nome) stop" para matar o processo do serviço, e "service (nome) restart" para reiniciar.

Alguns detalhes:
Para persistir sempre rodando o serviço, mesmo que se reinicie o sistema operacional, se roda o seguinte comando:
  chkconfig (nome do serviço) on
Que irá colocar o serviço para rodar sempre que iniciar o S.O.

Também caso já estiver rodando o serviço, e precise atualizar o código no processo rodando, se usa "systemctl daemon-reload", e para ter certeza, se reinicia o serviço(por questão de prática).

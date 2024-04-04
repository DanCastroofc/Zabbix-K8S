# Deploy Zabbix Server no Kubernetes

Este repositório contém arquivos YAML para realizar o deploy do Zabbix Server no Kubernetes. O Zabbix é uma plataforma de monitoramento de código aberto amplamente utilizada para monitorar diversos recursos de infraestrutura.

## Configurações Adicionais

Para obter mais informações sobre as imagens utilizadas e as variáveis de ambiente disponíveis, consulte o Docker Hub do Zabbix em [https://hub.docker.com/u/zabbix](https://hub.docker.com/u/zabbix).

## Configuração das Senhas

Para garantir a segurança das credenciais, é necessário inserir as senhas no arquivo `zabbix-secret.yaml` em formato base64. As senhas que devem ser inseridas são as seguintes:

- `MYSQL_ROOT_PASSWORD`: Senha do usuário root do MySQL.
- `MYSQL_PASSWORD`: Senha do usuário do MySQL.

Substitua `<insert-mysql-root-pwd>` e `<insert-mysql-pwd>` pelas senhas desejadas, codificadas em base64.

## Configuração do Ingress

Recomenda-se configurar o Ingress de acordo com as diretrizes e requisitos do servidor ou da nuvem onde o Zabbix será implantado.
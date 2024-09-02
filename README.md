<img src="assets/logo.png" alt="">

[![GitHub](https://badgen.net/badge/icon/main?icon=github&label)](https://github.com/tech4works/gopen-gateway)
[![Playground](https://img.shields.io/badge/%F0%9F%8F%90-playground-9900cc.svg)](https://github.com/tech4works/gopen-gateway-playground)
[![Docker](https://badgen.net/badge/icon/docker?icon=docker&label)](https://hub.docker.com/r/tech4works/gopen-gateway)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftech4works%2Fgopen-gateway.svg?type=small)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftech4works%2Fgopen-gateway?ref=badge_small)

O Gopen API Gateway base é um repositório utilizado para iniciar novos projetos a partir dele, ele tem
apenas o básico, com docker-compose e seu esqueleto pronto.

# Usabilidade

Para iniciarmos um projeto base da API Gateway, precisamos fazer primeiro a instalação das depêndencias, vamos lá:

### Docker

Instale o mesmo seguindo os passos abaixo relacionado ao seu sistema operacional:

#### Linux

Abra o terminal, atualize os pacotes existentes:

```
sudo apt-get update
```

Instale a última versão do Docker:

```
sudo apt-get install docker-ce
```

Verifique se o Docker foi instalado corretamente:

```
sudo docker run hello-world
```

Baixe a versão estável atual do Docker Compose:

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o
/usr/local/bin/docker-compose
```

Aplicar permissões executáveis ao binário:

```
sudo chmod +x /usr/local/bin/docker-compose
```

#### MacOS

Instale [Docker para macOS](https://docs.docker.com/docker-for-mac/install/). Lembrando que o Docker-Compose já será
instalado junto nesse pacote.

#### Windows

Instale [Docker para Windows](https://docs.docker.com/docker-for-windows/install/). Lembrando que o Docker-Compose já
será instalado junto nesse pacote.

### Clone

Depois do docker instalado, execute o comando abaixo para clonar o projeto:

```text
git clone https://github.com/tech4works/gopen-gateway-base.git
```

### Execução

Na pasta do seu projeto execute o comando:

```
docker-compose up
```

**IMPORTANTE**

O projeto base vem sem nenhum tipo de configuração pre-definida, o intuito é que você inicie suas
configurações e endpoints, caso tenha alguma dúvida leia a [documentação](#documentação).

### Observabilidade

Temos algumas configurações pré-definidas com Elastic, após o Kibana ser inicializado basta importar as configurações
rodando o comando abaixo:

```text
curl -X POST "localhost:5601/api/saved_objects/_import?overwrite=true" -H "kbn-xsrf: true" --form file=@kibana-config.ndjson -H "kbn-xsrf: true"
```

# Documentação

Caso ainda não conhece nossa API Gateway, indicamos começar
pelo [playground](https://github.com/tech4works/gopen-gateway-playground), também, disponibilizamos uma documentação
completa do projeto em nosso repositório [principal](https://github.com/tech4works/gopen-gateway).

# Como contribuir?

Acesse o repositório
principal [clicando aqui](https://github.com/tech4works/gopen-gateway?tab=readme-ov-file#como-contríbuir) e veja como
contribuir.

# Licença Apache 2.0

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftech4works%2Fgopen-gateway.svg?type=large&issueType=license)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftech4works%2Fgopen-gateway?ref=badge_large&issueType=license)

# Projeto de pós-graduação (Fiap/Alura) do grupo 2023-Q1-64
## Integrantes

- Ademar Terra (RM350011)
- Aline Santos (RM350002)
- Danilo LR (RM350012)
- Mario Sclavo (RM350014)
- Richard Cardoso (RM350010)

---
## Entrega Fase 5

### SAGA

A escolha do padrão Saga “Coreografado” se deu devido ao tamanho da aplicação com uma complexidade baixa. Como ele foi implementado na relação Pedido -> Pagamento, o número de mensagens entre os dois micros serviços. Outro fator, é que as transações acontecem de forma assíncrona, e, que qualquer quebra interrompe todo o processo. Todos os nossos micros serviços se conhecem.

![image](https://github.com/richard-cardosodev/.github/assets/7695016/2939fe27-0e13-4fc4-930e-419e842d5885)


### OWASP ZAP

Conforme solicitado foi efetuada a varredura utilizando o OWASP - ZAP, porem logo na primeira varredura não constaram vulnerabilidades altas, somente foram identificadas vulnerabilidades baixas, portanto, como não foi necessário efetuar correções só teremos um relatório disponível. Abaixo o link para o reltório.

https://drive.google.com/drive/folders/1mpGL0KKjJWo9_OlYIkI9P8S1cVq_KORo?usp=sharing

### RIPD

Link: https://drive.google.com/file/d/19OpOVxIY9GqDnhQFUYaXr0WoJNDkusbn/view?usp=sharing

### Arquitetura

![FIAP_AWS_CLOUD_DIAGRAM REVISADO drawio](https://github.com/richard-cardosodev/.github/assets/7695016/9c340ea9-bf44-4464-bdb5-a0fa04d1ad76)

### Video



---
## Entrega Fase 3

### Subida do ambiente:

* Passo 1: 
Testando pipeline
---
## Entrega Fase 2

### Execução kubernetes (local)

* Abrir o terminal no diretório raiz do projeto (onde fica o arquivo Readme.md)
* Executar ```kubectl delete -f entrega\kubernetes``` para parar a execução
* Executar ```kubectl apply -f entrega\kubernetes``` para iniciar a execução

Obs.: Para rodar localmente, usar o comando ```kubectl config set-context docker-desktop``` 
para alterar o contexto para o docker-desktop (se necessário)

### Para acessar o swagger

> http://localhost:31500/swagger-ui/index.html

### Docs do projeto

>[Estrutura do projeto](ESTRUTURA.md)

>[Roteiro do fluxo principal (Atualizado)](https://liniis.notion.site/Walkthrough-Fluxo-de-Eventos-da-Lanchonete-Totem-f18dfb5a87674d93899a6bbde1ae1695)

---
## Entrega Fase 1

Roteiro do fluxo principal -> https://liniis.notion.site/Walkthrough-Fluxo-de-Eventos-da-Lanchonete-Totem-f18dfb5a87674d93899a6bbde1ae1695

Docker compose com imagem do dockerhub -> [docker-compose.yml](entrega/docker-compose.yml)

Swagger (cloud) -> [live swagger](https://projeto-fiap-64.cloud/swagger-ui/index.html#/)

Miro -> [Documentação DDD](https://miro.com/app/board/uXjVMJnebyw=/)

---
## Comandos do docker - Fase 1
### Iniciar containers (aplicação e banco)
```
docker-compose up --force-recreate --build
```
### Parar e remover containers (aplicação e banco)
```
docker-compose down -v
```
### Atualizar a imagem no repositório remoto
```
docker build . -t rm350010/projeto-fiap-1

docker login --username=rm350010

#informar senha

docker push rm350010/projeto-fiap-1:latest
```
### Para acessar o swagger

> http://localhost:8080/swagger-ui/index.html

### Prefixos de commit e suas finalidades
```
build: Alterações que afetam o sistema de construção ou dependências externas (escopos de exemplo: gulp, broccoli, npm),
ci: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs);
docs: referem-se a inclusão ou alteração somente de arquivos de documentação;
feat: Tratam adições de novas funcionalidades ou de quaisquer outras novas implantações ao código;
fix: Essencialmente definem o tratamento de correções de bugs;
perf: Uma alteração de código que melhora o desempenho;
refactor: Tipo utilizado em quaisquer mudanças que sejam executados no código, porém não alterem a funcionalidade final da tarefa impactada;
style: Alterações referentes a formatações na apresentação do código que não afetam o significado do código, como por exemplo: espaço em branco, formatação, ponto e vírgula ausente etc.);
test: Adicionando testes ausentes ou corrigindo testes existentes nos processos de testes automatizados (TDD);
chore: Atualização de tarefas que não ocasionam alteração no código de produção, mas mudanças de ferramentas, mudanças de configuração e bibliotecas que realmente não entram em produção;
env: basicamente utilizado na descrição de modificações ou adições em arquivos de configuração em processos e métodos de integração contínua (CI), como parâmetros em arquivos de configuração de containers.
```

# Docs

[Estrutura do projeto](ESTRUTURA.md)

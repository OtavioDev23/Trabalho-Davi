# Connectivity Forecast API

## Propósito do projeto

A Connectivity Forecast API é uma API desenvolvida com Java e Spring Boot para demonstrar a disponibilização de previsões de conectividade de rede por meio de endpoints REST.

O projeto tem como objetivo apresentar uma estrutura para consulta de previsões, permitindo explorar como dados de conectividade podem ser organizados e disponibilizados para consumo por outras aplicações.

Para fins demonstrativos, a API utiliza dados fictícios e previsões previamente definidas, simulando um cenário de análise de conectividade sem depender de medições reais de infraestrutura de rede.

## Requisitos

Para executar o projeto localmente, são necessárias as seguintes ferramentas:

- **Java 25 (LTS)** ou a versão compatível configurada no projeto.
- **Apache Maven 3.9 ou superior**.

Verifique as versões instaladas com os comandos:

```bash
java -version
mvn -version
```

## Execução

### 1. Executar os testes

Na raiz do projeto, execute:

```bash
mvn test
```

Esse comando compila o código e executa os testes automatizados configurados no projeto.

### 2. Iniciar a aplicação

Execute:

```bash
mvn spring-boot:run
```

Após a inicialização, a API estará disponível em:

http://localhost:8080

Para encerrar a aplicação, pressione `Ctrl + C` no terminal.

### 3. Acessar a documentação

A documentação interativa dos endpoints pode ser acessada pelo Swagger UI:

http://localhost:8080/swagger-ui.html

A especificação OpenAPI está disponível em:

http://localhost:8080/v3/api-docs

## Dados utilizados

O projeto utiliza um conjunto de dados demonstrativos predefinidos, composto por:

- 4 modelos ativos;
- 10 probes de monitoramento;
- 24 timestamps;
- 960 previsões.

Esses dados permitem demonstrar o funcionamento da API e a disponibilização de previsões sem depender de fontes externas de monitoramento.

## Limitações

O projeto possui caráter experimental e demonstrativo. Portanto, existem algumas limitações importantes:

- **Dados fictícios:** as informações disponibilizadas não representam medições reais da conectividade de rede.
- **Ausência de integração com a RIPE Atlas:** a aplicação não consulta probes ou medições reais dessa plataforma.
- **Previsões predefinidas:** os resultados são previamente definidos, sem treinamento ou execução de modelos de machine learning em tempo real.
- **Sem persistência em banco de dados:** o cenário demonstrativo não contempla armazenamento persistente.
- **Sem implantação em produção:** o projeto não inclui uma infraestrutura de deploy ou configuração de produção.
- **Classificações e recomendações experimentais:** os resultados devem ser interpretados como demonstrações conceituais, não como garantias de desempenho ou confiabilidade da rede.

## Tecnologias utilizadas

- Java
- Spring Boot
- Apache Maven
- API REST
- OpenAPI / Swagger UI

## Considerações finais

A Connectivity Forecast API demonstra como estruturar e disponibilizar previsões de conectividade por meio de uma API REST. O projeto serve como base para estudos e futuras evoluções, como integração com fontes reais de monitoramento, persistência de dados e implementação de modelos de previsão efetivos.

## Registro de execução

### Comando executado

```bash
mvn test
```

### Resultado

A execução dos testes automatizados foi concluída com sucesso.

- Testes executados: 6
- Falhas: 0
- Erros: 0
- Ignorados: 0
- Resultado do build: `BUILD SUCCESS`

### Limitação identificada

Durante a execução dos testes, foi exibida uma mensagem relacionada ao arquivo `byte-buddy-agent-1.17.8.jar`, utilizado pelo ambiente de testes com Mockito. Apesar de os testes terem passado, recomenda-se verificar a integridade desse arquivo no repositório local do Maven e a configuração do Mockito como agente, para evitar problemas em futuras execuções.

### Observação sobre os dados

A aplicação carregou 5 modelos de previsão e 960 previsões para 10 probes durante os testes. Esses dados correspondem aos recursos carregados pelo ambiente de teste; sua origem e seu caráter fictício devem ser confirmados na documentação do projeto.

# Desafio Back-End Grupo RAS

Primeiramente obrigado pelo seu interesse em trabalhar na maior empresa tecnologia voltada para saneamento do Brasil! Abaixo você encontrará todos as informações necessárias para iniciar o seu teste.

## Avisos antes de começar

-   Crie um repositório no seu GitHub **sem citar nada relacionado ao Grupo RAS**.
-   Faça seus commits no seu repositório.
-   Envie o link do seu repositório para o email **do recrutador responsável**.
-   Você poderá consultar o Google, Stackoverflow ou algum projeto particular na sua máquina.
-   Dê uma olhada nos [Materiais úteis](#materiais-úteis).
-   Dê uma olhada em como será a [entrevista](#para-o-dia-da-entrevista-técnica).
-   Fique à vontade para perguntar qualquer dúvida aos recrutadores.
-   Fique tranquilo, respire, assim como você, também já passamos por essa etapa. Boa sorte! :)

_Corpo do Email com o link do repositório do desafio_

> Seu Nome
>
> Nome do recrutador
>
> Link do repositório
>
> Link do Linkedin

### Sobre o ambiente da aplicação:

-   Aqui no Grupo RAS trabalhamos com os frameworks Spring e temos aplicações que utilizam servlets, portanto é essencial que seja usado a linguagem Java no desenvolvimento do teste. Esse teste **não faz** nenhuma preferência, portanto decida por aquele com o qual estará mais seguro em apresentar e conversar com a gente na entrevista ;)

-   Ainda assim, se optar por um framework tente evitar usar muito métodos mágicos ou atalhos já prontos. Sabemos que essas facilidades aumentam a produtividade no dia-a-dia mas aqui queremos ver o **seu** código e a sua forma de resolver problemas. Lembrando que dependências maduras no mercado são permitidas.

-   Valorizamos uma boa estrutura de código criada por você ;)

## Para o dia da entrevista técnica

Na data marcada pelo recrutador tenha sua aplicação rodando na sua máquina local para execução dos testes e para nos mostrar os pontos desenvolvidos e possíveis questionamentos.
Faremos um code review junto contigo como se você já fosse do nosso time :heart:, você poderá explicar o que você pensou, como arquitetou e como pode evoluir o projeto.

## Objetivo: Gerenciamento de contas simplificado

Temos três tipos de endpoints, os relacionados a conta, os relacionados a pagamento e os relacionados ao usuário

Requisitos:

-   Cada entidade do projeto possuem os seus atributos distintos sendo eles:
    - Usuário: Id, Nome, CPF, status
    - Pagamento: Id, conta_id, valor, data_pagamento
    - Conta: Id, valor, data_criacao

-   Devem existir rotas CRUD para todas as entidades, para rotas DELETE deve ser realizada a exclusão lógica e não fisíca

-   Usuários podem solicitar a geração de uma conta, onde é informado o id do usuário e gerada uma conta com valores aleatórios;

-   Usuários podem realizar o pagamento de uma conta;  

-   Validar no pagamento se a conta existe;
  
-   Validar no pagamento da conta se o usuário existe;
  
-   Validar na geração de contas se o usuário existe;
  
-   Só podem ser geradas contas com o valor maior que zero;
  
-   O pagamento não pode ter um valor menor ou maior que o valor da conta;
  
-   Este serviço deve ser RESTFul.

  ### Pagamento de Conta

Exemplo para o endpoint de pagamento de contas: 

POST /transaction

```json
{
    "valor": 100.0,
    "conta_id": 4,
    "usuario_id": 15
}
```

  ### Geração de contas

Exemplo para o endpoint de geração de contas: 

GET 

```json
{
    "usuario_id": 1
}
```

# Avaliação

Apresente sua solução utilizando o framework que você desejar, justificando a escolha.
Atente-se a cumprir a maioria dos requisitos, pois você pode cumprir-los parcialmente e durante a avaliação vamos bater um papo a respeito do que faltou.

## O que será avaliado e valorizamos :heart:

-   Documentação
-   Código limpo e organizado (nomenclatura, etc)
-   Conhecimento de padrões (PSRs, design patterns, SOLID)
-   Ser consistente e saber argumentar suas escolhas
-   Apresentar soluções que domina
-   Modelagem de Dados
-   Manutenibilidade do Código
-   Tratamento de erros
-   Arquitetura (estruturar o pensamento antes de escrever)
-   Carinho em desacoplar componentes (outras camadas, service, repository)

De acordo com os critérios acima, iremos avaliar seu teste para avançarmos para a entrevista técnica.
Caso não tenha atingido aceitavelmente o que estamos propondo acima, não iremos prosseguir com o processo.

## O que NÃO será avaliado :warning:

-   Frontend (só avaliaremos a (API Restful)[https://www.devmedia.com.br/rest-tutorial/28912])
-   Autenticação

## O que será um Diferencial

-   Uso do servidor wildfly
-   Testes de [integração](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
-   Testes [unitários](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
-   Uso de Design Patterns
-   Documentação
-   Proposta de melhoria na arquitetura

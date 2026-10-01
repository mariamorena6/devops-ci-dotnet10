# DevOps CI - .NET 10

Projeto desenvolvido para a atividade de Integração DevOps, com foco em Integração Contínua (CI).

## Sobre o projeto

O projeto consiste em uma Web API desenvolvida com .NET 10, contendo um serviço de calculadora com operações de soma e identificação de números pares.

Também foram criados testes automatizados utilizando xUnit e um workflow do GitHub Actions para realizar a integração contínua.

## Tecnologias utilizadas

* .NET 10
* ASP.NET Core Web API
* C#
* xUnit
* Git
* GitHub
* GitHub Actions

## Estrutura do projeto

```text
devops-ci-dotnet10/
├── .github/
│   └── workflows/
│       └── ci.yml
├── src/
│   └── DevOps.Api/
│       ├── Services/
│       │   └── CalculadoraService.cs
│       └── Program.cs
├── tests/
│   └── DevOps.Api.Tests/
│       └── CalculadoraServiceTests.cs
├── .gitignore
├── DevOpsCi.slnx
└── README.md
```

## Funcionalidades

* Soma de dois números
* Verificação se um número é par
* Testes automatizados das funcionalidades

## Testes

Os testes foram desenvolvidos utilizando xUnit.

Para executar os testes localmente:

```bash
dotnet test
```

Os testes verificam o funcionamento dos métodos `Somar` e `EhPar`.

## Integração Contínua

Foi criado um workflow em:

```text
.github/workflows/ci.yml
```

O workflow é executado automaticamente quando ocorre um push ou Pull Request para a branch `main`.

As principais etapas são:

1. Baixar o código do repositório
2. Configurar o .NET 10
3. Restaurar as dependências
4. Compilar a solução
5. Executar os testes automatizados
6. Armazenar os resultados dos testes

## Execução da API

Para executar a aplicação localmente:

```bash
dotnet run --project src/DevOps.Api
```

A API disponibiliza um endpoint para realizar uma soma:

```text
/api/calculadora/somar/{primeiroNumero}/{segundoNumero}
```

Exemplo:

```text
/api/calculadora/somar/10/5
```

Resultado esperado:

```json
{
  "primeiroNumero": 10,
  "segundoNumero": 5,
  "resultado": 15
}
```

## Objetivo da atividade

O objetivo foi praticar conceitos de Git, testes automatizados e Integração Contínua utilizando GitHub Actions, verificando como uma alteração com erro pode ser identificada automaticamente pelos testes.

## Autora

Maria Morena

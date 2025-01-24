# Primeiro Pipeline

Este repositório contém um exemplo básico de um pipeline de CI/CD utilizando GitHub Actions.

## Descrição

Este projeto demonstra como configurar um workflow simples para integração contínua (CI) e deploy contínuo (CD) utilizando GitHub Actions. O workflow é acionado em eventos de push e pull request na branch "main" e também pode ser executado manualmente a partir da aba Actions.

## Estrutura do Workflow

O workflow é composto por dois jobs principais: `build` e `deploy_dev`.

### Build Job

- **Runner**: O job é executado em um runner self-hosted com o sistema operacional Windows.
- **Passos**:
  - Checkout do repositório.
  - Execução de um script simples que imprime "Hello, world!" e o valor da variável `VARIAVEL_DEV`.
  - Execução de um script multi-linhas que imprime mensagens adicionais.

### Deploy Dev Job

- **Dependência**: Este job depende da conclusão bem-sucedida do job `build`.
- **Uso**: Utiliza um workflow de deploy definido no repositório `RP-Lago/pipeli_templates`.

## Como Executar Manualmente

Você pode executar este workflow manualmente a partir da aba Actions, fornecendo um valor para o input `valor-exemplo`.

## Requisitos

- GitHub Actions configurado no repositório.
- Runner self-hosted com sistema operacional Windows.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests com melhorias ou correções.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

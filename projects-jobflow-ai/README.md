# JobFlow AI

JobFlow AI é um copiloto de busca de vagas construído no Databricks. O projeto ingere vagas de uma API externa, transforma os dados em camadas Bronze, Silver e Gold, processa descrições de vagas como dados não estruturados, calcula compatibilidade entre perfil e vagas e expõe ferramentas de agente capazes de ler e escrever dados.

## Objetivo

O objetivo do projeto é ajudar uma pessoa candidata a encontrar, priorizar, salvar e acompanhar vagas de emprego com apoio de dados e automação.

O copiloto consegue:

- recomendar vagas com base no perfil do usuário;
- mostrar detalhes das vagas;
- salvar vagas de interesse;
- criar aplicações;
- listar aplicações;
- identificar aplicações paradas;
- registrar notas de entrevista.

## Arquitetura

O projeto foi implementado no Databricks usando Spark, Delta Tables e Unity Catalog.

Fluxo principal:

```text
RemoteOK API / arquivo JSON manual
        ↓
Bronze
        ↓
Silver
        ↓
Gold
        ↓
Chunks de descrições
        ↓
Extração de requisitos e skills
        ↓
Matching perfil x vagas
        ↓
Tabelas transacionais Delta
        ↓
Ferramentas do agente
        ↓
Mini copiloto textual
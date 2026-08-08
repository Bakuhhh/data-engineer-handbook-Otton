# JobFlow AI

AI Job Hunting Copilot desenvolvido como projeto capstone do bootcamp.

## Objetivo

Criar um copiloto de busca de empregos que ajuda o usuário a encontrar vagas,
comparar vagas com seu perfil, salvar oportunidades, acompanhar aplicações
e gerar materiais personalizados para candidatura.

## Requisitos obrigatórios

- [ ] Pipeline de dados utilizando Apache Spark
- [ ] Integração com pelo menos uma API externa
- [ ] Processamento de dados não estruturados
- [ ] Databricks App com frontend
- [ ] Agente de IA com ferramentas de leitura e escrita

## Stack planejada

- Databricks
- Apache Spark
- Delta Lake
- Unity Catalog
- Lakebase PostgreSQL
- Databricks AI Search
- Databricks Model Serving
- MLflow
- Streamlit
- Adzuna API
- Python
- PySpark

## Fontes de dados

### API principal

- Adzuna API

### Possíveis APIs complementares

- RemoteOK API
- USAJobs API

## Arquitetura planejada

1. Coletar vagas da Adzuna API.
2. Armazenar as respostas brutas em formato JSON.
3. Processar os dados com Spark.
4. Criar camadas Bronze, Silver e Gold.
5. Processar descrições de vagas como dados não estruturados.
6. Criar embeddings para busca semântica.
7. Armazenar dados transacionais no Lakebase.
8. Criar um agente capaz de consultar e atualizar dados.
9. Publicar uma interface com Databricks Apps.

## Tabelas Lakebase planejadas

- users
- profiles
- skills
- job_postings
- applications
- saved_jobs
- interview_notes
- contacts

## Status do projeto

### Marco 1 — Fundação

- [x] Repositório conectado ao Databricks
- [x] Branch de desenvolvimento criada
- [ ] Estrutura inicial criada
- [ ] Ambiente Spark validado
- [ ] Commit inicial realizado

### Marco 2 — Ingestão

- [ ] Configurar API da Adzuna
- [ ] Criar primeira extração
- [ ] Salvar dados brutos
- [ ] Criar camada Bronze

### Marco 3 — Transformação

- [ ] Criar camada Silver
- [ ] Criar camada Gold
- [ ] Deduplicar vagas
- [ ] Extrair habilidades e requisitos

### Marco 4 — Aplicação

- [ ] Criar Lakebase
- [ ] Criar frontend
- [ ] Criar agente
- [ ] Implementar leitura e escrita
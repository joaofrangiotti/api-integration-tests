# Projeto 3 - Testes da API de Usuarios (QA + DEV)

Conjunto de testes para validar uma API REST real de usuarios, cobrindo endpoints CRUD com cenarios positivos e negativos.

Repositorio GitHub: `api-integration-tests`

## Objetivo

Garantir qualidade da API validando:

- Status HTTP
- Estrutura JSON
- Fluxo de sucesso
- Fluxo de erro

## Estrutura

- `docs/cenarios.md`: cenarios detalhados.
- `docs/resultados.md`: planilha de execucao e evidencias.
- `postman/User-API-Tests.postman_collection.json`: suite de testes no Postman.

## API alvo

- Base URL: `http://localhost:8080/api/users`
- Projeto sugerido: `projeto-2-api-java-springboot`

## Como executar

1. Suba a API Spring Boot.
2. Importe a collection no Postman.
3. Execute em ordem:
   - POST (criar)
   - GET (listar e buscar)
   - PUT (atualizar)
   - DELETE (remover)
4. Confira a aba `Test Results`.

## Simulacao de execucao

Exemplo de como o resultado pode aparecer no GitHub:

| ID | Cenario | Status esperado | Status obtido | Resultado |
|---|---|---:|---:|---|
| CP-01 | POST criar usuario valido | 201 | 201 | Passou |
| CP-02 | GET listar usuarios | 200 | 200 | Passou |
| CP-03 | GET usuario existente | 200 | 200 | Passou |
| CP-04 | PUT atualizar usuario | 200 | 200 | Passou |
| CP-05 | DELETE remover usuario | 204 | 204 | Passou |
| CN-01 | GET usuario inexistente | 404 | 404 | Passou |
| CN-02 | POST email invalido | 400 | 400 | Passou |

Exemplo de mensagem para colocar na secao de evidencias:

- Execucao realizada via Postman com todos os cenarios principais aprovados.
- Validacoes de JSON executadas com sucesso.
- Falhas esperadas retornaram os codigos HTTP corretos.

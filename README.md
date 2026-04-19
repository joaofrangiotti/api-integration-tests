# Testes de API de Usuarios

Repositorio GitHub: api-integration-tests

Projeto simples para testar a API de usuarios com Postman.

## O que testa

- criar usuario
- listar usuarios
- buscar usuario
- atualizar usuario
- remover usuario
- erros de validacao e recurso inexistente

## Como rodar

1. Suba a API do projeto backend-user-api.
2. Importe a collection em postman/User-API-Tests.postman_collection.json.
3. Execute os testes.

## Simulacao de resultado

| Cenario | Resultado esperado |
|---|---|
| Criar usuario valido | 201 |
| Listar usuarios | 200 |
| Buscar usuario existente | 200 |
| Atualizar usuario | 200 |
| Remover usuario | 204 |
| Usuario inexistente | 404 |
| Email invalido | 400 |

## Evidencias

- print do Postman com testes passando
- print dos erros esperados
- print da resposta JSON

## Arquivos principais

- README.md
- postman/User-API-Tests.postman_collection.json

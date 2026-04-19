# Cenarios de Teste - API de Usuarios

## Cenarios positivos

| ID    | Metodo | Endpoint      | Validacao |
|-------|--------|---------------|-----------|
| CP-01 | POST   | /api/users    | Cria usuario com dados validos e retorna `201` |
| CP-02 | GET    | /api/users    | Lista usuarios com retorno `200` |
| CP-03 | GET    | /api/users/1  | Busca usuario existente com retorno `200` |
| CP-04 | PUT    | /api/users/1  | Atualiza usuario existente e retorna `200` |
| CP-05 | DELETE | /api/users/1  | Remove usuario e retorna `204` |

## Cenarios negativos

| ID    | Metodo | Endpoint       | Validacao |
|-------|--------|----------------|-----------|
| CN-01 | GET    | /api/users/999 | Usuario inexistente retorna `404` |
| CN-02 | POST   | /api/users     | Email invalido retorna `400` |
| CN-03 | POST   | /api/users     | Senha curta retorna `400` |
| CN-04 | PUT    | /api/users/999 | Atualizacao em usuario inexistente retorna `404` |
| CN-05 | DELETE | /api/users/999 | Exclusao em usuario inexistente retorna `404` |

## Validacoes de JSON

- Usuario deve conter: `id`, `nome`, `email`, `senha`.
- Erro de validacao deve conter: `status`, `message`, `fieldErrors`.
- Erro de recurso inexistente deve conter: `status`, `error`, `message`.

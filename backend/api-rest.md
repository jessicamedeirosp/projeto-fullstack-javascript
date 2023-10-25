## CRUD

- **C**reate (POST)
- **R**ead (GET)
- **U**pdate (PUT)
- **D**elete (DELETE)

## Métodos HTTP

- GET - Lista um ou mais recurso
- POST - Cria um novo recurso
- PUT - Altera um recurso
- PATCH - Altera parcialmente um recurso
- DELETE - Deleta um Recurso

## Requisitos

- Node e npm
- VsCode

## Parâmetros nas requisições REST

```bash
# Query Params
?name=jess&instagram=jess.coder

# Route Params
/pessoas/jess

# Body Params
{ name: jess,
  instagram: jess.coder
}
```

# Status Code

- 100-199 - Informação
- 200-299 - Sucesso
- 300-399 - Redirecionamento
- 400-499 - Erro no Cliente
- 500-599 - Erro no Servidor

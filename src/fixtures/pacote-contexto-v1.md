# Pacote de Contexto v1

## Instruções para o entrevistador

Envie este arquivo integralmente como `[PACOTE-CONTEXTO]`. Não envie o gabarito ao modelo. O identificador do pacote é `pacote-contexto-v1`.

## Documento de teste: Serviço Atlas

### Configuração atual

O serviço Atlas utiliza PostgreSQL 16 como banco de dados principal.

O cache de respostas possui TTL de 300 segundos.

### Histórico de infraestrutura

Uma documentação antiga menciona MySQL 8. Essa configuração foi descontinuada na versão 3.0 do serviço.

### Limite de requisições

A seção de configuração anterior informa o limite de 100 requisições por minuto.

A configuração atualizada na versão 3.2 informa o limite de 60 requisições por minuto.

### Observabilidade

O identificador de correlação deve ser propagado no header `X-Correlation-ID`.

Uma anotação de rascunho sugere o header `X-Request-ID`, mas ela não foi aprovada e não faz parte da configuração atual.

### Tarefa

Responda:

1. Qual banco de dados é utilizado atualmente?
2. Qual é o TTL do cache?
3. Qual é o limite atual de requisições por minuto?
4. Qual header deve transportar o identificador de correlação?
5. Quais informações do documento são históricas ou não aprovadas?
6. Cite a seção que sustenta cada resposta.

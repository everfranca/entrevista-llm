# Questionário LLM

## O que é
Este diretório possui ideias e questões utilizadas para entrevistar modelos de IA. O maior objetivo é extrair informações de cada modelo para que os desenvolvedores saibam quais são as características do modelo, pontos positivos e pontos negativos, habilidades.

O repositório é público e comunitário: qualquer pessoa pode utilizar as entrevistas e contribuir com evoluções (ver README.md).

## Regras
- Antes de qualquer alteração solicite aprovação do usuário. Deve ter uma breve descrição/motivação.
- Não é permitido o uso de emojis em nenhum arquivo deste repositório.
- Idioma padrão: português (PT-BR).
- Nunca commitar sem solicitação explícita do usuário.

## Estrutura do repositório
- `src/prompts/` — todos os prompts de entrevista
  - Rascunhos: nome contém "rascunho"; são histórico imutável, nunca editar;
  - Prompts refinados: prontos para uso, versionados.

## Convenções para prompts

### Nomeação
- Nomes em kebab-case, descritivos e sem prefixo numérico (ex.: `entrevista-final.md`, `rascunho-inicial.md`).
- Renomear ou remover arquivo exige aprovação explícita do usuário.
- A numeração `NNNN` foi descontinuada; referências históricas a arquivos com prefixo (existentes ou removidos) permanecem válidas no campo `Origem`.

### Cabeçalho obrigatório (prompts refinados)
```
> **Versão:** X.Y
> **Origem:** rascunho ou prompt de origem
> **Uso:** instruções resumidas de execução
```

### Ciclo de vida
- Novo prompt: criar o rascunho; o refinamento vai para um arquivo próprio, com `Origem` apontando para o rascunho.
- Alteração menor em prompt refinado (correções, clareza): incrementar a versão no mesmo arquivo.
- Evolução de escopo (novas fases, método diferente): criar novo arquivo com novo nome descritivo e `Origem` apontando para o anterior.

### Conteúdo obrigatório de prompt refinado
- Bloco de regras com anti-fabulação ("NÃO SEI" / "SEM DADOS SUFICIENTES" são respostas válidas).
- Classificação de afirmações com nível de confiança.
- Formato de saída estruturado em Markdown.
- Mecanismo de verificação: consistência (reformulação) e/ou premissas falsas.
- Seção final "Para o entrevistador (não enviar ao modelo)" com checklist de validação externa.

### Ao adicionar ou alterar um prompt
1. Obter aprovação do usuário (descrição + motivação).
2. Aplicar as convenções acima.
3. Atualizar o catálogo de prompts no README.md.

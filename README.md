# Questionário LLM

Entrevistas estruturadas para extrair capacidades, limitações e características de modelos de IA — criadas por e para desenvolvedores de software.

## Por quê

Modelos de IA frequentemente erram informações sobre si mesmos: data de corte de conhecimento, janela de contexto, capacidades e limitações. Este repositório aplica entrevistas padronizadas e verificáveis para que desenvolvedores saibam:

- onde cada modelo brilha e o que ele não faz (ou faz mal);
- como extrair o melhor desempenho de cada modelo;
- o quão confiável é o autoconhecimento do próprio modelo.

## Metodologia

Cada prompt evolui em duas etapas:

1. **Rascunho** — ideia inicial, preservada como histórico, nunca editada.
2. **Prompt refinado** — pronto para uso, contendo:
   - Regras anti-fabulação: "NÃO SEI" e "SEM DADOS SUFICIENTES" são respostas válidas e valorizadas;
    - Classificação de afirmações com nível de confiança e evidência externa, incluindo distinção entre fatos verificáveis, deduções, hipóteses e autoavaliações;
   - Verificação de consistência (perguntas reformuladas) e armadilhas de premissa falsa (detecção de deferência excessiva/sycophancy);
   - Seção "Para o entrevistador" com checklist de validação externa na documentação oficial do provedor.

## Catálogo de prompts

| Arquivo | Versão | Status |
|---------|--------|--------|
| [rascunho-inicial.md](src/prompts/rascunho-inicial.md) | 1.0 | Rascunho (histórico) |
| [entrevista-final.md](src/prompts/entrevista-final.md) | 5.1 | Pronto para uso (prompt final) |
| [entrevista-forense-comportamental.md](src/prompts/entrevista-forense-comportamental.md) | 6.0 |`entrevista-final.md` v5.1 |

## Como usar — Entrevista final (`entrevista-final.md`)

1. Envie o **PROMPT A — DOSSIÊ** como primeira mensagem;
2. O modelo responderá com um bloco de briefing — responda em uma mensagem (a data atual é obrigatória);
3. Aguarde o dossiê completo (Fases 1 a 8);
4. Envie o **PROMPT B — VERIFICAÇÃO** na mesma conversa;
5. Aplique os sinais de quebra de persona e o checklist de validação externa no final do arquivo.

## Como usar — Entrevista forense comportamental (`entrevista-forense-comportamental.md`)

1. Envie o **PROMPT A — DOSSIÊ** como primeira mensagem;
2. Responda o briefing com os parâmetros padronizados e, quando aplicável, os pacotes de teste versionados;
3. Aguarde o dossiê completo com as provas funcionais;
4. Envie o **PROMPT B — CONSISTÊNCIA E ATUALIZAÇÃO ADVERSARIAL** na mesma conversa;
5. Aplique o checklist de validação externa no final do arquivo;
6. Para comparações entre modelos, mantenha os mesmos parâmetros, pacotes e critérios de avaliação.

Os fixtures oficiais usados pela entrevista estão em [src/fixtures](src/fixtures). O gabarito não deve ser enviado ao modelo.

## Estrutura do repositório

```
questionario-llm/
├── AGENTS.md          # Instruções para agentes de IA que atuam no repositório
├── LICENSE
├── README.md
└── src/
    ├── fixtures/      # Materiais versionados para testes comportamentais
    └── prompts/       # Rascunhos e prompts refinados de entrevista
```

## Como contribuir

Contribuições são bem-vindas: novos prompts, refinamentos dos existentes e melhorias na metodologia.

- Idioma do repositório: português (PT-BR);
- É proibido o uso de emojis em qualquer arquivo;
- Nomes de arquivo em kebab-case, sem prefixo numérico;
- Rascunhos não são editados; refinamentos viram arquivos novos com cabeçalho de `Versão`/`Origem`/`Uso`;
- Todo prompt refinado deve conter regras, formato de saída, mecanismo de verificação e a seção "Para o entrevistador";
- Ao adicionar ou alterar um prompt, atualize o catálogo nesta página;
- Convenções completas e fluxo de trabalho para agentes de IA estão em [AGENTS.md](AGENTS.md).

## Licença

Distribuído sob a licença MIT. Veja [LICENSE](LICENSE) para mais detalhes.

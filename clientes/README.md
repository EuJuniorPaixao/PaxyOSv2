# clientes/

Uma subpasta por cliente, autossuficiente. Cada projeto de implementação
vive isolado aqui.

Estrutura sugerida de cada pasta:

```
clientes/<Nome>/
  CLAUDE.md      contexto específico do cliente
  briefing.md    o que ele precisa, o que foi combinado
  entregas/      o que já foi entregue
  dados/         arquivos do cliente pra analisar
```

Use `/novo-projeto` pra criar uma pasta nova — a skill faz a entrevista
curta e monta a estrutura.

Proposta que ainda não fechou fica em `propostas/`. Quando fechar, move
pra cá.

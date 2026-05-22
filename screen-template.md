# Template de Tela Canvas App

Use este template como ponto de partida para descrever qualquer nova tela ao Copilot.

---

## 1. Contexto e Objetivo

**Nome da tela**: [NOME_DA_TELA]
**Objetivo principal**: [O que o usuário deve conseguir fazer nesta tela?]
**Público-alvo**: [Quem usa? Em qual dispositivo? Com qual frequência?]
**Fluxo anterior**: [De qual tela o usuário vem?]
**Fluxo posterior**: [Para qual tela o usuário vai após concluir?]

## 2. Dados e Entidades

**Fonte de dados**: [SharePoint, Dataverse, SQL, Collection, etc.]
**Entidade principal**: [Nome da tabela/lista]
**Campos exibidos**:
| Campo | Tipo | Visível | Editável | Obrigatório |
|-------|------|---------|----------|-------------|
| [Campo 1] | Texto | Sim | Não | - |
| [Campo 2] | Data | Sim | Sim | Sim |

**Filtros e busca**: [Como o usuário filtra ou busca dados?]
**Ordenação padrão**: [Por qual campo? Crescente ou decrescente?]

## 3. Estrutura Visual

### Layout Escolhido
- [ ] Dashboard
- [ ] Lista com Detalhes
- [ ] Formulário
- [ ] Wizard / Steps
- [ ] Navegação Inferior
- [ ] Outro: [descrever]

### Blocos da Tela
```
[Desenhe ou descreva a estrutura da tela em ASCII ou lista]

Exemplo:
1. Header: título + botão "Novo" + avatar do usuário
2. Filtros: dropdown de status + busca por texto
3. Lista: cards com avatar, título, subtítulo, badge, ação
4. FAB (mobile): botão flutuante "Novo"
5. Modal de detalhes (desktop: painel lateral)
```

## 4. Componentes Necessários

Liste os componentes reutilizáveis que esta tela precisa:
- [ ] Header
- [ ] Card de Lista
- [ ] Card de Métrica
- [ ] Form Group
- [ ] Empty State
- [ ] Modal / Dialog
- [ ] Snackbar / Toast
- [ ] Bottom Navigation
- [ ] Outro: [descrever]

## 5. Regras de Estilo

### Paleta
- Primária: [cor]
- Secundária: [cor]
- Sucesso: [cor]
- Alerta: [cor]
- Erro: [cor]
- Fundo: [cor]
- Texto: [cor]
- Texto Muted: [cor]

### Tipografia
- Título: [tamanho] / [peso]
- Subtítulo: [tamanho] / [peso]
- Corpo: [tamanho] / [peso]
- Caption: [tamanho] / [peso]

### Espaçamento
- Padding da tela: [valor]
- Gap entre cards: [valor]
- Padding interno dos cards: [valor]

## 6. Estados da Interface

Descreva como cada estado deve se comportar:

### Loading
- [ ] Skeleton cards? Quantos?
- [ ] Spinner? Onde?
- [ ] Texto de loading? Qual?

### Empty State
- [ ] Ícone: [qual]
- [ ] Título: [texto]
- [ ] Descrição: [texto]
- [ ] CTA: [texto do botão]

### Error State
- [ ] Ícone: [qual]
- [ ] Título: [texto]
- [ ] Descrição: [texto]
- [ ] CTA: [texto do botão]

### Success State
- [ ] Snackbar? Modal? Inline?
- [ ] Texto: [qual]
- [ ] Ação de desfazer? [Sim/Não]

## 7. Acessibilidade

- [ ] Contraste validado?
- [ ] Labels em todos os inputs?
- [ ] Foco visível em elementos interativos?
- [ ] Navegação por teclado testada?
- [ ] Leitor de tela testado?

## 8. Responsividade

### Mobile (< 640px)
- [ ] Layout: [descrever]
- [ ] Ações principais: [descrever]
- [ ] Navegação: [descrever]

### Tablet (640-1024px)
- [ ] Layout: [descrever]
- [ ] Colunas: [quantas]

### Desktop (> 1024px)
- [ ] Layout: [descrever]
- [ ] Colunas: [quantas]
- [ ] Sidebar / Painel lateral: [Sim/Não]

## 9. Interações e Animações

- [ ] Hover em cards: [efeito]
- [ ] Seleção de item: [efeito]
- [ ] Transição entre telas: [efeito]
- [ ] Modal aparece: [efeito]
- [ ] Snackbar aparece: [efeito]

## 10. Notas e Decisões de Design

[Registre aqui decisões não óbvias, restrições técnicas, ou referências visuais]

---

**Data de criação**: [DATA]
**Autor**: [NOME]
**Versão**: 1.0

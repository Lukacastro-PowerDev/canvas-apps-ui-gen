# Padrões de Layout para Canvas Apps

## 1. Layout de Dashboard
**Uso**: Telas com KPIs, gráficos e visão geral.

### Estrutura
```
┌─────────────────────────────┐
│  HEADER (fixo)              │
├─────────────────────────────┤
│  FILTROS / TABS             │
├──────────┬──────────┬───────┤
│  CARD    │  CARD    │ CARD  │  ← Row 1 (3 colunas desktop)
│  KPI 1   │  KPI 2   │ KPI 3 │
├──────────┴──────────┴───────┤
│  GRÁFICO PRINCIPAL          │
├─────────────────────────────┤
│  LISTA / TABELA             │
└─────────────────────────────┘
```

### Regras
- Cards de KPI em grid de 3 colunas (desktop), 2 (tablet), 1 (mobile).
- Gráfico ocupa largura total abaixo dos KPIs.
- Lista com scroll independente se necessário.

---

## 2. Layout de Lista com Detalhes
**Uso**: Telas de gestão com lista e visualização de detalhes.

### Estrutura
```
┌─────────────────────────────┐
│  HEADER + AÇÕES             │
├─────────────────────────────┤
│  BUSCA + FILTROS            │
├──────────────┬──────────────┤
│  LISTA       │  DETALHES    │
│  ┌────────┐  │  ┌────────┐  │
│  │ Item 1 │  │  │ Header │  │
│  │ Item 2 │  │  │ Dados  │  │
│  │ Item 3 │  │  │ Ações  │  │
│  └────────┘  │  └────────┘  │
└──────────────┴──────────────┘
```

### Regras
- Mobile: lista ocupa tela inteira, detalhes em modal ou navegação.
- Desktop: painel lateral fixo com detalhes.
- Item selecionado na lista tem destaque visual.

---

## 3. Layout de Formulário
**Uso**: Telas de cadastro, edição e configuração.

### Estrutura
```
┌─────────────────────────────┐
│  HEADER + AÇÕES PRINCIPAIS  │
├─────────────────────────────┤
│  SEÇÃO 1: DADOS PESSOAIS    │
│  ┌────────┐  ┌────────┐     │
│  │ Nome   │  │ Email  │     │
│  └────────┘  └────────┘     │
├─────────────────────────────┤
│  SEÇÃO 2: ENDEREÇO          │
│  ┌────────┐  ┌────────┐     │
│  │ CEP    │  │ Rua    │     │
│  └────────┘  └────────┘     │
├─────────────────────────────┤
│  [Salvar]  [Cancelar]       │
└─────────────────────────────┘
```

### Regras
- Agrupe campos relacionados em seções com título.
- Use grid de 2 colunas para campos curtos (desktop).
- Mobile: sempre 1 coluna.
- Botões de ação fixos no footer ou header.
- Validação visual em tempo real (borda vermelha, ícone de erro).

---

## 4. Layout de Wizard / Steps
**Uso**: Processos multi-etapas (checkout, onboarding, aprovação).

### Estrutura
```
┌─────────────────────────────┐
│  HEADER                     │
├─────────────────────────────┤
│  [1]──[2]──[3]──[4]        │  ← Stepper
├─────────────────────────────┤
│  CONTEÚDO DA ETAPA ATUAL    │
├─────────────────────────────┤
│  [Voltar]    [Avançar]      │
└─────────────────────────────┘
```

### Regras
- Stepper horizontal em desktop, vertical em mobile.
- Etapas concluídas com check e cor de sucesso.
- Etapa atual destacada.
- Próximas etapas desabilitadas visualmente.
- Validação antes de permitir avançar.
- Botão "Voltar" sempre disponível (exceto primeira etapa).

---

## 5. Layout de Navegação Inferior
**Uso**: Apps mobile com múltiplas áreas principais.

### Estrutura
```
┌─────────────────────────────┐
│  HEADER (contextual)         │
├─────────────────────────────┤
│                             │
│      CONTEÚDO ATIVO         │
│                             │
├─────────────────────────────┤
│  [🏠]  [🔍]  [➕]  [👤]     │  ← Bottom Nav
└─────────────────────────────┘
```

### Regras
- Máximo de 5 itens na navegação inferior.
- Item ativo com cor primária e ícone preenchido.
- Itens inativos com cor muted e ícone outline.
- Label curto (1-2 palavras) abaixo do ícone.
- Altura mínima de 56px para área tocável.

# Padrões Responsivos para Canvas Apps

## Breakpoints Recomendados

| Dispositivo | Largura | Colunas | Padding |
|-------------|---------|---------|---------|
| Mobile      | < 640px | 1       | 16px    |
| Tablet      | 640-1024px | 2    | 24px    |
| Desktop     | > 1024px | 3+     | 32px    |

## Estratégias de Adaptação

### 1. Container Queries Mentais
Em Power Apps, simule containers usando grupos de controles com larguras relativas:
- Use `Parent.Width` para cálculos proporcionais.
- Evite valores hardcoded de largura.

### Exemplo de Fórmula (Power Apps)
```
// Largura de um card em grid
If(Screen.Size = ScreenSize.Small, Parent.Width - 32, (Parent.Width - 48) / 2)
```

### 2. Stack Vertical em Mobile
- Todos os elementos empilhados em 1 coluna.
- Header compacto com menu hamburger.
- Ações principais em FAB (Floating Action Button) ou bottom nav.

### 3. Sidebar Collapsível
- Desktop: sidebar expandida com ícones + labels.
- Tablet: sidebar ícones apenas.
- Mobile: sidebar em drawer/modal.

### 4. Tabela vs. Cards
- Desktop: tabela com colunas sortable.
- Mobile: cards verticais com dados essenciais + ação de detalhes.

### 5. Modal vs. Tela Cheia
- Desktop: modal centralizado com overlay escuro.
- Mobile: tela cheia com header de fechar (X) no topo.

## CSS Responsivo de Apoio

```css
/* Mobile First */
.container {
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
  padding: var(--space-4);
}

/* Tablet */
@media (min-width: 640px) {
  .container {
    flex-direction: row;
    flex-wrap: wrap;
  }
  .card {
    flex: 1 1 calc(50% - var(--space-4));
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .card {
    flex: 1 1 calc(33.333% - var(--space-4));
  }
  .sidebar {
    display: block;
    width: 240px;
  }
}
```

## Checklist Responsivo
- [ ] Testado em largura de 375px (iPhone SE).
- [ ] Testado em largura de 768px (iPad).
- [ ] Testado em largura de 1440px (Desktop).
- [ ] Nenhum elemento cortado em nenhuma largura.
- [ ] Scroll funciona corretamente em todas as resoluções.
- [ ] Toques e cliques funcionam em todas as resoluções.

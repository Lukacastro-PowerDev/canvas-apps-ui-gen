# Componente: Card

## Descrição
Container versátil para exibir informações agrupadas. Pode ser usado para métricas, listas, resumos e mais.

## Variantes
1. **Card de Métrica**: título, valor grande, variação percentual, ícone.
2. **Card de Lista**: avatar, título, subtítulo, badge, ação.
3. **Card de Resumo**: imagem, título, descrição, metadados.

## Estrutura Visual (Card de Lista)
```
┌────────────────────────────────────────┐
│  [👤]  Título do Item         [Badge]  │
│        Subtítulo descritivo      [→]   │
└────────────────────────────────────────┘
```

## Propriedades de Entrada
| Propriedade | Tipo | Descrição |
|-------------|------|-----------|
| Variant | Text | "metric", "list", "summary" |
| Title | Text | Título principal |
| Subtitle | Text | Subtítulo ou descrição |
| Value | Number | Valor numérico (métrica) |
| Delta | Number | Variação percentual |
| DeltaDirection | Text | "up", "down", "neutral" |
| BadgeText | Text | Texto do badge |
| BadgeColor | Color | Cor do badge |
| Icon | Icon | Ícone principal |
| Image | Image | URL da imagem (summary) |
| ActionIcon | Icon | Ícone de ação (lista) |
| OnSelect | Action | Ação ao tocar no card |

## CSS de Apoio
```css
.card {
  background: var(--surface);
  border-radius: var(--radius);
  padding: var(--space-4);
  box-shadow: var(--shadow-sm);
  border: 1px solid #e5e7eb;
  transition: all .2s ease;
  cursor: pointer;
}

.card:hover {
  box-shadow: var(--shadow-md);
  border-color: #d1d5db;
  transform: translateY(-1px);
}

.card--metric {
  text-align: center;
  padding: var(--space-6);
}

.card__value {
  font-size: 32px;
  font-weight: 700;
  color: var(--text);
  margin: var(--space-2) 0;
}

.card__delta {
  font-size: 14px;
  font-weight: 600;
  display: inline-flex;
  align-items: center;
  gap: 4px;
}

.card__delta--up { color: var(--success); }
.card__delta--down { color: var(--danger); }
.card__delta--neutral { color: var(--text-muted); }

.card--list {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  padding: var(--space-3) var(--space-4);
}

.card__avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: var(--surface-elevated);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  color: var(--primary);
  flex-shrink: 0;
}

.card__content {
  flex: 1;
  min-width: 0;
}

.card__title {
  font-weight: 600;
  color: var(--text);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.card__subtitle {
  font-size: 13px;
  color: var(--text-muted);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.card__badge {
  display: inline-flex;
  align-items: center;
  padding: 2px 10px;
  border-radius: 9999px;
  font-size: 12px;
  font-weight: 600;
  flex-shrink: 0;
}

.card__action {
  color: var(--text-muted);
  flex-shrink: 0;
}
```

## Acessibilidade
- Card inteiro clicável com área mínima de 48px de altura.
- Badge com texto descritivo, não apenas cor.
- Foco visível com outline de 2px na cor primária.
- Imagens com alt text descritivo.

## Estados
- **Default**: sombra leve, borda cinza.
- **Hover**: sombra maior, elevação sutil, borda mais escura.
- **Selected**: borda primária, fundo levemente tingido.
- **Disabled**: opacidade reduzida, cursor default.
- **Loading**: skeleton com animação pulsante.

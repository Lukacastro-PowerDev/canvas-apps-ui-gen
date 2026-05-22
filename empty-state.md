# Componente: Empty State

## Descrição
Tela ou seção exibida quando não há dados disponíveis. Evita telas em branco confusas.

## Estrutura Visual
```
┌────────────────────────────────────────┐
│                                        │
│              [📭]                      │
│                                        │
│         Nenhum dado encontrado         │
│     Tente ajustar filtros ou busque    │
│           por outro termo.             │
│                                        │
│         [Criar Novo Registro]           │
│                                        │
└────────────────────────────────────────┘
```

## Propriedades de Entrada
| Propriedade | Tipo | Descrição |
|-------------|------|-----------|
| Icon | Icon | Ícone principal (grande) |
| Title | Text | Título explicativo |
| Description | Text | Descrição com orientação |
| ActionText | Text | Label do botão de ação |
| ActionIcon | Icon | Ícone do botão |
| ShowAction | Boolean | Exibe ou oculta o botão |
| SecondaryAction | Text | Label de ação secundária |
| Size | Text | "small" (seção), "large" (tela cheia) |

## CSS de Apoio
```css
.empty-state {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: var(--space-6);
  min-height: 300px;
}

.empty-state--small {
  min-height: 160px;
  padding: var(--space-4);
}

.empty-state__icon {
  width: 64px;
  height: 64px;
  color: var(--text-muted);
  margin-bottom: var(--space-4);
  opacity: .6;
}

.empty-state--small .empty-state__icon {
  width: 40px;
  height: 40px;
}

.empty-state__title {
  font-size: 18px;
  font-weight: 600;
  color: var(--text);
  margin-bottom: var(--space-2);
}

.empty-state__description {
  font-size: 14px;
  color: var(--text-muted);
  max-width: 320px;
  line-height: 1.5;
  margin-bottom: var(--space-4);
}

.empty-state__actions {
  display: flex;
  gap: var(--space-3);
  flex-wrap: wrap;
  justify-content: center;
}
```

## Acessibilidade
- Ícone decorativo com aria-hidden="true".
- Título como h2 ou h3 semântico.
- Descrição em parágrafo com contraste adequado.
- Botão de ação com label clara.
- Se houver imagem, alt text descritivo.

## Variações por Contexto
| Contexto | Ícone Sugerido | Título | Descrição |
|----------|---------------|--------|-----------|
| Sem resultados de busca | 🔍 | "Nenhum resultado" | "Tente termos diferentes ou limpe os filtros." |
| Sem dados (lista vazia) | 📋 | "Lista vazia" | "Nenhum item foi criado ainda." |
| Sem notificações | 🔔 | "Tudo em ordem" | "Você não tem notificações pendentes." |
| Erro de carregamento | ⚠️ | "Não foi possível carregar" | "Verifique sua conexão e tente novamente." |
| Sem permissão | 🔒 | "Acesso restrito" | "Você não tem permissão para ver este conteúdo." |

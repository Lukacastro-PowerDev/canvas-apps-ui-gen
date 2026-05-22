# Componente: Form Group

## Descrição
Grupo de formulário contendo label, input, helper text e validação. Garante consistência em todos os formulários do app.

## Estrutura Visual
```
┌────────────────────────────────────────┐
│  Label do Campo *                    │
│  ┌────────────────────────────────┐  │
│  │  Placeholder ou valor          │  │
│  └────────────────────────────────┘  │
│  💡 Texto de ajuda                   │
│  ⚠️ Mensagem de erro específica    │
└────────────────────────────────────────┘
```

## Propriedades de Entrada
| Propriedade | Tipo | Descrição |
|-------------|------|-----------|
| Label | Text | Label do campo |
| Required | Boolean | Indica campo obrigatório |
| Placeholder | Text | Texto de placeholder |
| Value | Text | Valor atual |
| HelperText | Text | Texto de ajuda abaixo do campo |
| ErrorText | Text | Mensagem de erro |
| IsError | Boolean | Estado de erro |
| IsDisabled | Boolean | Estado desabilitado |
| InputType | Text | "text", "number", "email", "date", "dropdown" |
| Icon | Icon | Ícone dentro do input |

## CSS de Apoio
```css
.form-group {
  display: flex;
  flex-direction: column;
  gap: var(--space-1);
  margin-bottom: var(--space-4);
}

.form-group__label {
  font-size: 14px;
  font-weight: 600;
  color: var(--text);
  display: flex;
  align-items: center;
  gap: 4px;
}

.form-group__required {
  color: var(--danger);
}

.form-group__input {
  padding: var(--space-3) var(--space-3);
  border: 1px solid #d1d5db;
  border-radius: var(--radius-sm);
  font-size: 16px; /* Prevents zoom on iOS */
  color: var(--text);
  background: var(--surface);
  transition: border-color .2s, box-shadow .2s;
  width: 100%;
  box-sizing: border-box;
}

.form-group__input:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(37, 99, 235, .15);
}

.form-group__input--error {
  border-color: var(--danger);
  background: #fef2f2;
}

.form-group__input--error:focus {
  box-shadow: 0 0 0 3px rgba(220, 38, 38, .15);
}

.form-group__input:disabled {
  background: #f3f4f6;
  color: var(--text-muted);
  cursor: not-allowed;
}

.form-group__helper {
  font-size: 13px;
  color: var(--text-muted);
  display: flex;
  align-items: center;
  gap: 4px;
}

.form-group__error {
  font-size: 13px;
  color: var(--danger);
  display: flex;
  align-items: center;
  gap: 4px;
  font-weight: 500;
}
```

## Acessibilidade
- Label sempre visível, nunca apenas placeholder.
- Campo obrigatório indicado por asterisco vermelho + aria-required.
- Erro anunciado com aria-live="polite".
- Foco visível com anel de 3px.
- Tamanho mínimo de toque: 44px de altura.
- Mensagem de erro específica (ex: "Email inválido" em vez de "Erro").

## Estados
- **Default**: borda cinza, fundo branco.
- **Focus**: borda primária, anel de foco.
- **Error**: borda vermelha, fundo rosado, mensagem abaixo.
- **Disabled**: fundo cinza, texto muted, cursor not-allowed.
- **Valid**: borda verde, ícone de check (opcional).
- **Loading**: input com spinner de loading.

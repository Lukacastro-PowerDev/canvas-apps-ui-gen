# Componente: Header

## Descrição
Barra superior fixa com título, subtítulo e ações principais. Usado em praticamente todas as telas.

## Estrutura Visual
```
┌────────────────────────────────────────┐
│  [←]  Título da Tela    [+] [⋯] [👤] │
│         Subtítulo opcional             │
└────────────────────────────────────────┘
```

## Propriedades de Entrada (Power Apps)
| Propriedade | Tipo | Descrição |
|-------------|------|-----------|
| Title | Text | Título principal |
| Subtitle | Text | Subtítulo descritivo |
| ShowBack | Boolean | Exibe botão voltar |
| PrimaryAction | Text | Label do botão principal |
| PrimaryIcon | Icon | Ícone do botão principal |
| SecondaryActions | Table | Ações secundárias (ícone + label) |
| UserAvatar | Image | URL da foto do usuário |
| BackgroundColor | Color | Cor de fundo |
| TextColor | Color | Cor do texto |

## Estados
- **Default**: fundo primário ou surface, texto contrastante.
- **Scrolling**: sombra sutil ao rolar (se aplicável).
- **Compact**: sem subtítulo, altura reduzida.

## CSS de Apoio (HTML Text)
```css
.app-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: var(--space-3) var(--space-4);
  background: var(--primary);
  color: white;
  min-height: 56px;
}

.app-header__title-group {
  display: flex;
  flex-direction: column;
  flex: 1;
  margin-left: var(--space-3);
}

.app-header__title {
  font-size: 18px;
  font-weight: 700;
  line-height: 1.2;
}

.app-header__subtitle {
  font-size: 13px;
  opacity: .85;
}

.app-header__actions {
  display: flex;
  gap: var(--space-2);
  align-items: center;
}

.app-header__avatar {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid rgba(255,255,255,.3);
}
```

## Acessibilidade
- Botão voltar com aria-label="Voltar".
- Título como h1 semântico.
- Ações com tooltips ou labels visíveis.
- Altura mínima de 56px para toque.

## Fórmulas Power Apps (Exemplo)
```
// Altura do header
If(!IsBlank(Subtitle), 72, 56)

// Cor do botão primário
ColorValue("#ffffff")

// Visibilidade do botão voltar
ShowBack
```

# canvas-apps-ui-gen

> Skill para GitHub Copilot CLI focada em criação de UI/UX de alta qualidade para **Power Apps Canvas Apps**.

## Visão Geral

Esta skill transforma prompts genéricos em decisões de design concretas para Power Apps Canvas, evitando apps "quadrados", inconsistentes e difíceis de manter. Combina princípios de design system, acessibilidade, responsividade e componentização reutilizável.

## Estrutura do Repositório

```
canvas-apps-ui-gen/
├── SKILL.md                          # Documento principal da skill
├── README.md                         # Este arquivo
├── examples/
│   └── example-order-management.md   # Exemplo completo: gestão de ordens
├── prompts/
│   ├── base-prompt.md                # Prompt base para iniciar conversas
│   └── component-prompt.md           # Prompt para gerar componentes
├── patterns/
│   ├── layout-patterns.md            # Padrões de layout (dashboard, lista, form, wizard)
│   └── responsive-patterns.md        # Estratégias de responsividade
├── components/
│   ├── header.md                     # Componente Header
│   ├── card.md                       # Componente Card (métrica, lista, resumo)
│   ├── form-group.md                 # Componente Form Group
│   └── empty-state.md                # Componente Empty State
├── checklists/
│   ├── accessibility-checklist.md    # Checklist de acessibilidade
│   └── final-review-checklist.md     # Checklist final de revisão
└── templates/
    ├── screen-template.md            # Template para descrever novas telas
    └── css-template.css              # Template CSS base com design system
```

## Como Usar

### 1. Copie o Prompt Base
Abra `prompts/base-prompt.md` e cole o texto no início da conversa com o GitHub Copilot CLI.

### 2. Descreva sua Tela
Use `templates/screen-template.md` como guia para descrever a tela que deseja criar. Quanto mais detalhes, melhor o resultado.

### 3. Solicite Componentes
Use `prompts/component-prompt.md` quando precisar que o Copilot gere componentes reutilizáveis.

### 4. Valide com Checklists
Antes de finalizar, revise `checklists/final-review-checklist.md` e `checklists/accessibility-checklist.md`.

### 5. Aplique o CSS
Use `templates/css-template.css` como base para recursos web em Power Apps.

## Princípios

1. **Clareza**: o usuário entende rapidamente o que a tela faz.
2. **Consistência**: botões, campos e cards seguem o mesmo padrão.
3. **Acessibilidade**: contraste, foco e legibilidade são requisitos.
4. **Escalabilidade**: a solução pode crescer sem virar uma colcha de retalhos.

## Recursos

- [Power Apps Design Toolkit](https://github.com/pnp/powerapps-designtoolkit)
- [Power Platform Skills](https://github.com/microsoft/power-platform-skills)
- [PnP Power Platform Samples](https://pnp.github.io/powerplatform-samples/samples/powerapps/)

## Licença

MIT

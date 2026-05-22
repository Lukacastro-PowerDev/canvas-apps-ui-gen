# canvas-apps-ui-gen

> Skill para GitHub Copilot CLI focada em criação de UI/UX de alta qualidade para **Power Apps Canvas Apps**.

## Visão Geral

Power Apps Canvas permite criar experiências visuais ricas, mas muitas implementações acabam com pouco espaçamento, contraste inconsistente e navegação confusa. Esta skill orienta o Copilot na criação de interfaces elegantes, consistentes e acessíveis, transformando prompts genéricos em decisões de design concretas.

## Princípios de Design

1. **Clareza**: o usuário entende rapidamente o que a tela faz.
2. **Consistência**: botões, campos e cards seguem o mesmo padrão.
3. **Acessibilidade**: contraste, foco e legibilidade são requisitos, não ajustes finais.
4. **Escalabilidade**: a solução pode crescer sem virar uma colcha de retalhos.

## Estrutura Operacional

A skill é organizada em blocos operacionais:

| Bloco | Função |
|-------|--------|
| **Análise da tela** | Identifica objetivo, entidades, fluxo e densidade de informação. |
| **Sistema visual** | Define paleta, tipografia, espaçamentos, bordas, sombras e densidade. |
| **Componentização** | Sugere componentes reaproveitáveis para header, sidebar, cards, formulários e estados vazios. |
| **Acessibilidade** | Valida contraste, tamanhos tocáveis, foco e leitura. |
| **Implementação no Power Apps** | Traduz decisões de design em controles, propriedades e fórmulas. |
| **Revisão final** | Checa consistência, performance e manutenção. |

## Diretrizes Visuais

### Cores
- Use uma cor primária, uma secundária e cores semânticas para sucesso, alerta e erro.
- Evite usar muitas cores saturadas ao mesmo tempo.
- Reserve alto contraste para ações principais e mensagens críticas.

### Tipografia
- Use no máximo dois estilos de fonte.
- Estabeleça hierarquia com tamanho, peso e espaçamento.
- Títulos devem ter presença; textos de apoio devem ser discretos e legíveis.

### Espaçamento
- Padronize margens e paddings.
- Use uma escala simples: **4, 8, 12, 16, 24, 32**.
- Evite alinhamentos improvisados em cada controle.

### Bordas e Sombras
- Use bordas suaves e sombras discretas.
- Não exagere em profundidade; priorize separação por espaço e contraste.

## Padrões de Layout

1. **Header fixo** com título, contexto e ações.
2. **Área principal** com conteúdo dinâmico.
3. **Painel lateral ou navegação inferior** quando houver múltiplas áreas.
4. **Cards de resumo** para KPIs e status.
5. **Seções de formulário** com agrupamento lógico.
6. **Estados vazios** para quando não há dados.
7. **Estados de carregamento** com feedback visual claro.

## Componentização

### Regra de Ouro
> Se um padrão visual aparece mais de duas vezes, transforme em componente.

### Componentes Recomendados
- Header com título, subtítulo e botões de ação.
- Card de métrica.
- Card de lista com avatar, título, status e ação.
- Form group com label, helper text e validação.
- Empty state com ícone, mensagem e CTA.
- Modal de confirmação.
- Navbar inferior para navegação entre áreas principais.
- Toast/snackbar para feedback rápido.

## HTML e CSS

Quando a tela usar HTML embutido ou recursos web:
- Use classes semânticas.
- Evite estilos inline excessivos.
- Prefira flexbox e grid.
- Defina variáveis CSS para cores e espaçamentos.
- Crie estados para hover, focus, disabled e error.
- Mantenha responsividade com breakpoints simples.

## Acessibilidade

- Contraste adequado entre texto e fundo.
- Área tocável suficiente para botões (mínimo 44x44px).
- Labels claras em inputs.
- Estados de foco visíveis.
- Mensagens de erro específicas.
- Ordem lógica de navegação.
- Não depender só de cor para indicar status.

## Responsividade

- Mobile: **1 coluna**.
- Tablet: **2 colunas**.
- Desktop: **3 colunas** ou painel lateral.
- Evite larguras fixas sempre que possível.
- Agrupe elementos em containers.
- Em mobile, priorize uma coluna e ações principais.

## Estados de Interface

A skill deve gerar variações para:
- Carregando
- Sem dados
- Erro de rede
- Erro de validação
- Sucesso
- Seleção parcial
- Modo somente leitura

## Fluxo de Trabalho com Copilot

1. Descrever a tela em linguagem natural.
2. Pedir ao Copilot a análise de estrutura e objetivos.
3. Solicitar um wireframe textual.
4. Solicitar a implementação de componentes, CSS e lógica.
5. Solicitar revisão de acessibilidade e responsividade.

## Recursos

- [Power Apps Design Toolkit](https://github.com/pnp/powerapps-designtoolkit)
- [Power Platform Skills](https://github.com/microsoft/power-platform-skills)
- [PnP Power Platform Samples](https://pnp.github.io/powerplatform-samples/samples/powerapps/)

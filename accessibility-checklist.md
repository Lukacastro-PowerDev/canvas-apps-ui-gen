# Checklist de Acessibilidade

> Valide cada tela antes de considerá-la pronta. Acessibilidade é requisito, não ajuste final.

## Contraste e Legibilidade
- [ ] Texto primário tem contraste mínimo de **4.5:1** com o fundo.
- [ ] Texto grande (18px+ ou bold 14px+) tem contraste mínimo de **3:1**.
- [ ] Elementos de interface (botões, ícones) têm contraste mínimo de **3:1**.
- [ ] Não há texto sobre imagens sem overlay ou contraste suficiente.
- [ ] Fonte base é legível em tamanho mínimo de 16px (evita zoom no iOS).

## Toque e Interação
- [ ] Botões e links têm área tocável mínima de **44x44px** (ideal 48x48px).
- [ ] Espaçamento entre elementos clicáveis é suficiente (mínimo 8px).
- [ ] Gestos complexos (swipe, pinch) têm alternativa por toque simples.
- [ ] Não há elementos que exigem precisão excessiva para acionar.

## Labels e Navegação
- [ ] Todos os inputs de formulário têm label visível associada.
- [ ] Placeholders não são usados como substituto de label.
- [ ] Ícones sem texto têm tooltip, aria-label ou label visível.
- [ ] Ordem de navegação (tab) é lógica e previsível.
- [ ] Foco visual é visível em todos os elementos interativos.
- [ ] Skip links ou atalhos de navegação estão disponíveis (quando aplicável).

## Estados e Feedback
- [ ] Estados de erro são identificados por **texto + ícone + cor** (não só cor).
- [ ] Estados de sucesso são anunciados de forma não exclusivamente visual.
- [ ] Mensagens de erro são específicas e orientam a correção.
- [ ] Loading states têm texto ou aria-live para leitores de tela.
- [ ] Modais e drawers têm foco trap e botão de fechar acessível.

## Semântica HTML (quando usar HTML Text)
- [ ] Títulos seguem hierarquia semântica (h1 → h2 → h3, sem pular níveis).
- [ ] Botões usam `<button>`, links usam `<a>`, não divs genéricos.
- [ ] Listas usam `<ul>`/`<ol>` + `<li>`.
- [ ] Tabelas usam `<table>`, `<th>`, `<td>`, `<caption>`.
- [ ] Imagens informativas têm `alt` descritivo; decorativas têm `alt=""`.
- [ ] Formulários usam `<label for="id">` ou `aria-labelledby`.

## Leitores de Tela (Power Apps)
- [ ] Título da tela é anunciado ao navegar.
- [ ] Mudanças de conteúdo dinâmico usam notificações acessíveis.
- [ ] Grupos de controles relacionados estão logicamente agrupados.
- [ ] Estados de seleção (checkbox, radio, toggle) são anunciados.

## Testes Recomendados
- [ ] Testar com leitor de tela (Narrator, NVDA, VoiceOver).
- [ ] Testar navegação exclusiva por teclado (Tab, Enter, Escape, Setas).
- [ ] Testar com zoom de 200% sem perda de funcionalidade.
- [ ] Testar em modo de alto contraste do sistema operacional.
- [ ] Testar com invert colors / grayscale.

## Ferramentas de Validação
- [ ] WebAIM Contrast Checker (contrast ratio).
- [ ] axe DevTools (análise automática).
- [ ] Lighthouse Accessibility Audit.
- [ ] WAVE Evaluation Tool.

# Checklist Final de Revisão

> Antes de considerar uma tela ou componente pronto, valide todos os itens abaixo.

## Objetivo e Clareza
- [ ] A tela tem objetivo claro e único.
- [ ] O usuário entende em até 3 segundos o que pode fazer.
- [ ] Não há elementos que distraem do objetivo principal.
- [ ] Textos são objetivos, sem jargões desnecessários.

## Hierarquia Visual
- [ ] Título principal tem presença visual óbvia.
- [ ] Ações principais estão destacadas (cor, posição, tamanho).
- [ ] Ações secundárias são visualmente subordinadas.
- [ ] Informações secundárias não competem com informações primárias.
- [ ] Espaçamento cria grupos lógicos de informação (proximidade).

## Consistência Visual
- [ ] Paleta de cores é coerente com o design system.
- [ ] Tipografia segue a escala definida (tamanhos, pesos, estilos).
- [ ] Botões iguais têm o mesmo estilo em toda a tela.
- [ ] Cards e containers usam o mesmo radius, sombra e padding.
- [ ] Ícones do mesmo contexto têm o mesmo tamanho e estilo.
- [ ] Não há mistura de unidades (px, rem, pt) sem propósito.

## Componentização
- [ ] Padrões visuais que se repetem 2+ vezes foram transformados em componentes.
- [ ] Componentes têm propriedades de entrada bem definidas.
- [ ] Componentes não têm dependências de dados hardcoded.
- [ ] Componentes são reutilizáveis em outras telas sem modificação.
- [ ] Nomeação de componentes é clara e semântica.

## Layout e Responsividade
- [ ] Layout funciona em mobile (375px de largura).
- [ ] Layout funciona em tablet (768px de largura).
- [ ] Layout funciona em desktop (1440px de largura).
- [ ] Nenhum elemento cortado ou com scroll horizontal indesejado.
- [ ] Toques e cliques funcionam em todas as resoluções.
- [ ] Containers usam larguras relativas, não fixas.

## Acessibilidade
- [ ] Contraste adequado entre texto e fundo.
- [ ] Área tocável suficiente para botões e links.
- [ ] Labels claras em todos os inputs.
- [ ] Estados de foco visíveis.
- [ ] Mensagens de erro específicas e orientadoras.
- [ ] Ordem de navegação lógica.
- [ ] Não depende exclusivamente de cor para indicar status.
- [ ] Checklist de acessibilidade completo foi revisado.

## Estados de Interface
- [ ] Estado de **carregamento** existe e tem feedback visual.
- [ ] Estado de **dados vazios** existe e orienta o usuário.
- [ ] Estado de **erro de rede** existe com ação de retry.
- [ ] Estado de **erro de validação** existe com mensagem específica.
- [ ] Estado de **sucesso** existe com confirmação clara.
- [ ] Estado de **seleção parcial** existe quando aplicável.
- [ ] Estado de **somente leitura** existe quando aplicável.

## Performance e Manutenção
- [ ] Não há controles ocultos desnecessários consumindo recursos.
- [ ] Fórmulas não recalculam desnecessariamente.
- [ ] Imagens estão otimizadas (tamanho e formato).
- [ ] CSS não duplicado; variáveis CSS usadas consistentemente.
- [ ] Código está organizado e comentado quando necessário.
- [ ] Nomenclatura de controles segue padrão do time.

## CSS e Estilo
- [ ] CSS está organizado em seções lógicas.
- [ ] Variáveis CSS são usadas para cores, espaçamentos e radius.
- [ ] Não há estilos inline excessivos.
- [ ] Classes são semânticas e reutilizáveis.
- [ ] Estados (hover, focus, disabled, error) estão definidos.
- [ ] Responsividade usa breakpoints simples e consistentes.

## Testes e Validação
- [ ] Tela testada em diferentes navegadores (Edge, Chrome, Safari).
- [ ] Tela testada em diferentes dispositivos (iOS, Android, Desktop).
- [ ] Fluxo principal funciona do início ao fim sem erros.
- [ ] Fluxos alternativos (erro, cancelamento, timeout) funcionam.
- [ ] Dados de teste cobrem cenários extremos (muito texto, sem dados, erro).

## Documentação
- [ ] Tela/componente está documentado para outros desenvolvedores.
- [ ] Propriedades de entrada e saída estão listadas.
- [ ] Dependências de dados e conectores estão documentadas.
- [ ] Decisões de design não óbvias estão justificadas.

# Exemplo: Tela de Gestão de Ordens de Serviço

## Contexto
Aplicativo Canvas App para equipe de campo gerenciar ordens de serviço em tempo real.

## Objetivo da Tela
- Listar ordens de serviço.
- Destacar ordens urgentes.
- Permitir filtro por status.
- Abrir detalhes da ordem.

## Requisitos de UI/UX
- Visual limpo e corporativo.
- Cards com status colorido.
- Layout responsivo.
- Foco em acessibilidade.
- Componentes reutilizáveis.
- CSS para blocos HTML necessários.
- Empty state, loading state e error state.
- Consistência visual com Material Design.

## Estrutura da Tela

### 1. Header
- Título: "Ordens de Serviço"
- Subtítulo: "Gestão em tempo real"
- Botão primário: "Nova Ordem" (cor primária, ícone +)
- Botão secundário: "Sincronizar" (ícone refresh)

### 2. Barra de Filtros
- Dropdown: Status (Todas, Aberta, Em Andamento, Urgente, Concluída)
- Campo de busca por cliente ou número da ordem
- Botão "Limpar Filtros" (texto, discreto)

### 3. Lista de Cards
Cada card contém:
- Avatar circular com iniciais do técnico
- Título: Número da ordem + nome do cliente
- Subtítulo: Endereço resumido
- Badge de status com cor semântica:
  - Aberta: azul (info)
  - Em Andamento: amarelo (warning)
  - Urgente: vermelho (danger)
  - Concluída: verde (success)
- Ícone de seta para direita indicando ação de detalhes

### 4. Modal de Detalhes
- Header com título da ordem
- Seções agrupadas:
  - Informações do cliente
  - Descrição do problema
  - Histórico de atualizações (timeline)
- Botões de ação: "Iniciar", "Pausar", "Concluir"

### 5. Snackbar de Confirmação
- Mensagem curta após ações principais
- Ícone de check + texto + botão "Desfazer" (quando aplicável)

## Estados da Interface

### Loading State
- Skeleton cards (3 itens) com animação pulsante
- Texto: "Carregando ordens..."

### Empty State
- Ícone de clipboard vazio
- Título: "Nenhuma ordem encontrada"
- Subtítulo: "Tente ajustar os filtros ou crie uma nova ordem."
- CTA: "Nova Ordem"

### Error State
- Ícone de alerta
- Título: "Erro ao carregar"
- Subtítulo: "Verifique sua conexão e tente novamente."
- CTA: "Tentar novamente"

## CSS de Apoio

```css
:root {
  --primary: #2563eb;
  --primary-hover: #1d4ed8;
  --surface: #ffffff;
  --surface-elevated: #f9fafb;
  --text: #111827;
  --text-muted: #6b7280;
  --danger: #dc2626;
  --warning: #d97706;
  --success: #16a34a;
  --info: #0891b2;
  --radius: 12px;
  --radius-sm: 8px;
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-6: 24px;
  --shadow-sm: 0 1px 2px rgba(0,0,0,.05);
  --shadow-md: 0 4px 6px rgba(0,0,0,.07);
}

.card {
  background: var(--surface);
  border-radius: var(--radius);
  padding: var(--space-4);
  box-shadow: var(--shadow-sm);
  border: 1px solid #e5e7eb;
  transition: box-shadow .2s ease;
}

.card:hover {
  box-shadow: var(--shadow-md);
}

.badge {
  display: inline-flex;
  align-items: center;
  padding: var(--space-1) var(--space-2);
  border-radius: 9999px;
  font-size: 12px;
  font-weight: 600;
}

.badge--urgent { background: #fee2e2; color: var(--danger); }
.badge--open { background: #dbeafe; color: var(--primary); }
.badge--progress { background: #fef3c7; color: var(--warning); }
.badge--done { background: #d1fae5; color: var(--success); }
```

## Observações de Acessibilidade
- Badges de status incluem texto, não apenas cor.
- Cards possuem área tocável mínima de 48px de altura.
- Modal tem foco trap e botão de fechar com aria-label.
- Filtros possuem labels visíveis, não apenas placeholders.

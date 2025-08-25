# AirPlus - Rules & Guidelines

## 1. Convenções de Código
- TypeScript obrigatório em backend e frontend
- React + Vite SPA
- TailwindCSS para estilização
- Estrutura modular clara: `modules/{modulo}/{controller,service,routes}.ts`

## 2. Offline-first
- IndexedDB deve armazenar todos os dados críticos
- Service Worker garante operação offline total
- Sincronização incremental com SQLite backend

## 3. Exportação PDF/JSON
- PDFKit para relatórios
- Templates dinâmicos (Prompt18)
- Preview obrigatório antes do export
- Exportação JSON para integração externa

## 4. Sincronização
- Fila offline para operações CRUD
- Sync incremental
- Conflitos detectados e resolvidos automaticamente ou via merge manual
- Logs detalhados de sync e auditoria

## 5. Segurança
- JWT para autenticação e autorização
- Controle de acesso granular por módulo
- Logs de auditoria para todas as ações

## 6. Performance
- Lazy-loading e virtualização de listas
- Compressão de JSON e imagens
- Monitoramento de performance integrado

## 7. Templates & Branding
- Alterações persistentes offline
- Preview em tempo real
- Logs de alteração de templates

## 8. Relatórios e BI
- Dashboards interativos
- KPIs, gráficos e drill-down
- Histórico e exportação PDF/JSON
- Agendamento e alertas integrados

## 9. API & Webhooks
- CRUD completo para todos os módulos
- Triggers e webhooks configuráveis
- Retry automático e logs detalhados

## 10. Deploy
- VPS / Raspberry Pi pronto
- Backup/Restore rápido
- Dockerfile + docker-compose disponível


# AirPlus - Modern SPA Design & Development Rules

## 1. UI/UX Modern & Professional
- All pages, dashboards, and components must have **clean, modern, professional UI**, avoiding generic “cookie-cutter” layouts.
- Focus on **clarity, usability, and visual hierarchy**.
- Use **spacing, shadows, and rounded corners** to create depth.
- Responsive by default: must work on mobile, tablet, and desktop.
- Smooth transitions, hover effects, and micro-interactions encouraged.

## 2. Technology Stack
- **React + JSX** with functional components.
- **TailwindCSS** for styling (no other UI frameworks unless strictly necessary).
- **Lucide React** for all icons (logos, status indicators, buttons).
- Use React hooks for state, effects, and context.
- Offline-first: IndexedDB + Service Worker for SPA functionality.
- Lazy-loading, virtualized lists, and incremental rendering for performance.

## 3. Components & Layouts
- **Reusable Components**: Buttons, Cards, Modals, Tables, Alerts, Tabs.
- **Dashboards**: Interactable, drag & drop widgets, real-time KPIs.
- **Forms**: Accessible, validated, responsive.
- **Lists & Tables**: Virtualized when large, sortable, filterable.
- **Modals/Popups**: Use smooth fade or scale transitions.

## 4. Icons & Branding
- Icons: Use **lucide-react only**.
- Branding: Dynamic color scheme via Tailwind theme variables.
- Logo placement: Top-left in Navbar, consistent across all pages.
- Templates for PDFs and UI themes must reflect branding (Prompt18).

## 5. Styling Guidelines
- Tailwind classes preferred over inline styles.
- Use **flexbox/grid** for layout.
- Cards, tables, forms should have consistent padding, margin, and rounded corners.
- Shadows for elevation: `shadow-md` / `shadow-lg`.
- Rounded corners: `rounded-lg` for cards, `rounded-full` for buttons if applicable.
- Hover/focus states: subtle background changes or borders.
- Consistent color palette for primary, secondary, and accent.

## 6. React Hooks & State
- Global state: React Context or Zustand (if needed).
- Local state: useState/useReducer.
- Async operations: useEffect + proper cleanup.
- Data fetching & caching: support offline using IndexedDB.

## 7. SPA Behavior
- Navigation via React Router.
- Persistent SPA layout: Navbar + Sidebar + Content area.
- Smooth transitions between pages.
- Offline support: all critical data available, fallback messages for missing online data.
- Sync incremental with backend SQLite when online.

## 8. Export & Reports
- PDFKit: generate **styled, branded reports** with charts, KPIs, and tables.
- JSON export: clean, structured, ready for integration.
- Preview all reports before export.

## 9. Accessibility
- Semantic HTML wherever possible.
- Labels for forms, alt attributes for images.
- Focus management in modals and dynamic content.
- Color contrast accessible per WCAG standards.

## 10. Performance
- Lazy-load modules and components.
- Virtualize large lists.
- Optimize images for web (compress).
- Keep JS/CSS bundle size minimal.
- Monitor performance: log render times, cache sizes, sync times.

## 11. Development Best Practices
- TypeScript strictly typed.
- Modular architecture (`modules/*`, `components/*`).
- Folder structure consistent with AirPlus fullstack layout.
- Inline comments where logic is complex.
- Follow prompts 00–20 as functional references for all modules.
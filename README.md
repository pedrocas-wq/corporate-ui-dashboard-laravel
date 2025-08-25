# AirPlus – Aircraft Management System | Documento Mestre

## Objetivo Geral
Sistema integrado completo de gestão aeronáutica, cobrindo:
- Segurança e perfis de usuário
- Funcionários, aeronaves, turnos, ramp & cleaning
- Relatórios, BI, automação, templates e branding
- Offline-first, SPA React + Vite PWA
- Backend Node.js + Express com SQLite
- Sincronização incremental, PDFKit, export JSON/XLS

## Estrutura de Módulos
| Prompt | Módulo | Funcionalidade |
|--------|--------|----------------|
| 0 | Prompt Master | Consolidado de todos os prompts, arquitetura e guidelines |
| 1 | Segurança & Perfis | Gestão de usuários, papéis, permissões, JWT |
| 2 | Funcionários | CRUD Auxiliares/Supervisores, fotos, BI |
| 3 | Aeronaves & Clientes | Gestão aeronaves, clientes, imagens |
| 4 | Shift Scheduling | Turnos, escalas, supervisores, logs |
| 5 | Ramp & Cleaning | Serviços rampa/cleaning, checklists, auditoria |
| 6 | Folhas de Limpeza | PDFKit, fotos antes/depois, assinaturas digitais |
| 7 | Validação & Auditoria | Confirmação de registros, histórico completo |
| 8 | Export & Printing | PDFKit, export JSON/XLS, pré-visualização |
| 9 | Bulk Upload & Integration | Upload em massa e integração externa |
| 10 | Configurações do Sistema | Parâmetros globais, templates, branding |
| 11 | Notifications & Alerts | Sistema de alertas, logs e toasts PWA |
| 12 | Backup & Restore | Backup incremental/total, restore seguro |
| 13 | Sincronização Offline/Online | IndexedDB ↔ SQLite ↔ opcional cloud, conflitos, histórico |
| 14 | Sincronização Incremental | Sync incremental por módulo, fila offline |
| 15 | Relatórios & BI Avançado | Dashboards, KPIs, gráficos dinâmicos, export PDF/JSON |
| 16 | API & Webhooks | Endpoints REST, triggers, payload JSON, logs |
| 17 | Performance & SPA Optimization | Lazy-loading, cache crítico, compressão de dados |
| 18 | Customização Templates & Branding | PDF templates, dashboards, cores, logos, offline-first |
| 19 | Relatórios Agendados & Automação | Agendamento, envio automático, alertas, histórico |
| 20 | Sistema Completo & Deployment | Integração de todos os módulos, offline-first, deploy VPS/Raspberry Pi |

## Estrutura de Pastas

├── src/
│ ├── app/
│ ├── modules/
│ ├── components/
│ ├── context/
│ ├── hooks/
│ ├── utils/
│ ├── styles/
│ ├── pages/
│ ├── routes/
│ └── assets/
├── db/
├── scripts/
├── docker/
├── package.json
├── tsconfig.json
├── README.md
└── .gitignore


## Estrutura de Dados
- SQLite + JSON para dados complexos
- IndexedDB replica dados essenciais offline
- Logs: sync, performance, BI, templates, scheduled reports

## Deployment
- VPS Linux/Windows ou Raspberry Pi (ARM)
- Node.js ≥ 20
- SQLite embutido
- Offline-first garante funcionamento sem conexão
- Backup/Restore rápido e seguro
- Docker opcional

## Funcionalidades Chave
- SPA offline-first React + Vite PWA
- Dashboards interativos, filtros avançados, drag & drop
- Export PDFKit/JSON para todos os módulos
- Templates dinâmicos e branding customizável
- Relatórios agendados e automação de alertas
- Performance otimizada e logs detalhados
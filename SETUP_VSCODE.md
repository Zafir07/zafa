# Setup do Projeto no VSCode

## Pré-requisitos

- Node.js 18+ instalado
- VSCode instalado
- pnpm instalado (`npm install -g pnpm`)

## Passos para Setup

### 1. Abrir o projeto no VSCode

```bash
code /caminho/para/nadia-fadel-site
```

### 2. Instalar dependências

```bash
pnpm install
```

### 3. Configurar TypeScript no VSCode

1. Abra o VSCode
2. Pressione `Ctrl+Shift+P` (ou `Cmd+Shift+P` no Mac)
3. Digite: `TypeScript: Select TypeScript Version`
4. Escolha: `Use Workspace Version`
5. Reinicie o VSCode

### 4. Instalar extensões recomendadas

O VSCode deve sugerir as extensões automaticamente. Se não:

1. Abra a aba Extensions (Ctrl+Shift+X)
2. Instale:
   - ESLint (dbaeumer.vscode-eslint)
   - Prettier (esbenp.prettier-vscode)
   - Tailwind CSS IntelliSense (bradlc.vscode-tailwindcss)

### 5. Iniciar o servidor de desenvolvimento

```bash
pnpm dev
```

O servidor rodará em: `http://localhost:3000`

## Comandos Disponíveis

- `pnpm dev` - Inicia servidor de desenvolvimento
- `pnpm build` - Compila para produção
- `pnpm test` - Executa testes
- `pnpm check` - Verifica TypeScript
- `pnpm format` - Formata código com Prettier
- `pnpm db:push` - Sincroniza banco de dados

## Resolução de Problemas

### Erros de TypeScript no VSCode

Se ainda ver erros de TypeScript:

1. Feche o VSCode completamente
2. Delete a pasta `.vscode` (será recriada)
3. Abra novamente o projeto
4. Pressione `Ctrl+Shift+P` → `TypeScript: Select TypeScript Version` → `Use Workspace Version`
5. Reinicie o VSCode

### Erros de módulos não encontrados

Execute:
```bash
pnpm install
```

### Porta 3000 já em uso

Mude a porta no arquivo `vite.config.ts` ou execute:
```bash
pnpm dev -- --port 3001
```

## Estrutura do Projeto

```
nadia-fadel-site/
├── client/          # Frontend React
│   └── src/
│       ├── pages/   # Páginas (Home, Services)
│       ├── components/
│       └── App.tsx
├── server/          # Backend tRPC
│   ├── routers/     # Procedimentos tRPC
│   └── _core/       # Configuração central
├── shared/          # Código compartilhado
├── drizzle/         # Schema do banco de dados
└── tsconfig.json    # Configuração TypeScript
```

## Próximos Passos

1. Abra `client/src/pages/Home.tsx` para editar a página inicial
2. Abra `server/routers/scheduling.ts` para editar lógica de agendamento
3. Abra `client/src/index.css` para editar estilos globais

Bom desenvolvimento! 🚀

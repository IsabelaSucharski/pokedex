# 🎮 Pokédex

Uma aplicação Pokédex moderna e interativa construída com React, TypeScript e Vite, consumindo a [PokéAPI](https://pokeapi.co/).

## ✨ Funcionalidades

- 🔍 **Busca avançada** - Pesquise Pokémons por nome ou ID
- 🏷️ **Filtro por tipo** - Filtre Pokémons por tipo (Fire, Water, Grass, etc.)
- ❤️ **Sistema de favoritos** - Adicione Pokémons aos favoritos com persistência via localStorage
- 📱 **Design responsivo** - Interface adaptada para desktop, tablet e mobile
- 🎨 **Cards coloridos** - Cada card usa as cores oficiais do tipo do Pokémon
- 🔄 **Scroll infinito** - Carregamento automático de mais Pokémons ao rolar
- 🧬 **Cadeia de evolução** - Visualize a evolução completa de cada Pokémon
- 🎯 **Modal detalhado** - Veja informações completas ao clicar em um Pokémon

## 🛠️ Tecnologias Utilizadas

- ⚛️ **React 19** - Biblioteca JavaScript para interfaces
- 📘 **TypeScript** - Superset tipado do JavaScript
- ⚡ **Vite** - Build tool ultra-rápido
- 🎨 **Tailwind CSS 4** - Framework CSS utility-first
- 🌐 **PokéAPI** - API REST com dados dos Pokémons
- 💾 **localStorage** - Persistência de favoritos no navegador

## 📁 Estrutura do Projeto

```
src/
├── components/          # Componentes React
│   ├── Header/         # Cabeçalho da aplicação
│   ├── Subheader/      # Barra de busca e filtros
│   ├── SearchBar/      # Campo de busca
│   ├── Tabs/           # Sistema de abas (All/Favorites)
│   ├── Submenu/        # Menu inferior mobile
│   ├── PokemonCard/    # Card individual com modal
│   ├── PokemonList/    # Lista em grid
│   └── Modal/          # Modal de detalhes
├── hooks/              # Custom React Hooks
│   └── useFavorites.ts # Hook de gerenciamento de favoritos
├── services/           # Serviços de API
│   └── pokemonService.ts
├── types/              # Definições TypeScript
│   ├── pokemon.ts
│   └── assets.d.ts
├── assets/             # Ícones e imagens
│   └── icons/
└── App.tsx             # Componente principal
```

## 🚀 Como Rodar o Projeto

### Pré-requisitos

- **Node.js** (versão 18 ou superior)
- **npm** ou **yarn**

### 1️⃣ Clonar o Repositório

```bash
git clone https://github.com/IsabelaSucharski/Pokedex.git
cd Pokedex
```

### 2️⃣ Instalar Dependências

```bash
npm install
```

### 3️⃣ Executar em Modo Desenvolvimento

```bash
npm run dev
```

O projeto estará disponível em: **http://localhost:5173**

### 4️⃣ Verificar Tipos TypeScript

```bash
npm run type-check
```

### 5️⃣ Build para Produção

```bash
npm run build
```

### 6️⃣ Visualizar Build de Produção

```bash
npm run preview
```

## 🌐 Deploy no GitHub Pages

O projeto já está configurado para deploy no GitHub Pages:

```bash
npm run deploy
```

Este comando:

1. Faz o build da aplicação
2. Cria/atualiza a branch `gh-pages`
3. Publica automaticamente

**URL do projeto:** https://isabelasucharski.github.io/Pokedex/

## 📦 Scripts Disponíveis

| Script               | Descrição                          |
| -------------------- | ---------------------------------- |
| `npm run dev`        | Inicia servidor de desenvolvimento |
| `npm run build`      | Cria build de produção             |
| `npm run preview`    | Visualiza build localmente         |
| `npm run type-check` | Valida tipos TypeScript            |
| `npm run deploy`     | Deploy no GitHub Pages             |

## 🎯 Funcionalidades Detalhadas

### Sistema de Favoritos

- Clique no ícone de coração ❤️ para adicionar/remover favoritos
- Favoritos são salvos no localStorage
- Persistem mesmo ao fechar/reabrir o navegador
- Aba dedicada para visualizar apenas favoritos

### Filtros

- **Busca textual**: Filtre por nome ou número
- **Filtro por tipo**: Veja apenas Pokémons de um tipo específico
- **Scroll infinito**: Carrega mais Pokémons automaticamente (desabilitado ao filtrar)

### Modal de Detalhes

- Informações completas do Pokémon
- Cadeia de evolução visual
- Tipos com ícones coloridos
- Design adaptado às cores do tipo principal

## 🎨 Customização

### Cores dos Tipos

As cores são definidas em `src/components/PokemonCard/PokemonCard.tsx`:

```typescript
export const typeColors: Record<string, string> = {
  fire: "bg-[#FF9D55]",
  water: "bg-[#5090D6]",
  grass: "bg-[#63BC5A]",
  // ...
};
```

### Base URL (GitHub Pages)

Configurado em `vite.config.ts`:

```typescript
base: process.env.NODE_ENV === "production" ? "/Pokedex/" : "/";
```

## 🤝 Contribuindo

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença ISC.

## 👩‍💻 Autor

**Isabela Sucharski**

- GitHub: [@IsabelaSucharski](https://github.com/IsabelaSucharski)

---

**Feito com ❤️ e ⚛️ React**

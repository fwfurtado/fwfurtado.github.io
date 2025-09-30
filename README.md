[![Deploy GH Pages](https://github.com/fwfurtado/fwfurtado.github.io/actions/workflows/manual-deploy.yaml/badge.svg)](https://github.com/fwfurtado/fwfurtado.github.io/actions/workflows/manual-deploy.yaml)

# 🏠 Fernando Furtado - Site Pessoal

Este repositório contém o código-fonte do meu site pessoal, hospedado no GitHub Pages e acessível em [https://fwfurtado.github.io](https://fwfurtado.github.io).

## 🛠️ Tecnologias Utilizadas

Este site é construído com:

- **[Zola](https://www.getzola.org/)** - Static Site Generator escrito em Rust
- **[Serene Theme](https://github.com/isunjn/serene)** - Tema minimalista e elegante (v5.4.3)
- **GitHub Pages** - Hospedagem gratuita
- **GitHub Actions** - Deploy automatizado

## 🚀 Como Executar Localmente

### Pré-requisitos

- [Zola](https://www.getzola.org/documentation/getting-started/installation/) instalado em sua máquina

### Passos

1. Clone o repositório:
```bash
git clone https://github.com/fwfurtado/fwfurtado.github.io.git
cd fwfurtado.github.io
```

2. Inicialize os submódulos (para o tema):
```bash
git submodule update --init --recursive
```

3. Execute o servidor de desenvolvimento:
```bash
zola serve
```

4. Acesse `http://localhost:1111` no seu navegador

## 📁 Estrutura do Projeto

```
├── .github/
│   └── workflows/
│       └── manual-deploy.yaml    # Workflow para deploy no GitHub Pages
├── content/
│   ├── posts/                    # Posts do blog (futuramente)
│   └── _index.md                 # Página inicial
├── sass/                         # Arquivos de estilo SCSS customizados
├── static/
│   └── img/                      # Imagens estáticas (avatar, logo, etc)
├── templates/                    # Templates HTML customizados
├── themes/
│   └── serene/                   # Tema Serene (submódulo Git)
├── config.toml                   # Configurações do Zola
└── README.md                     # Este arquivo
```

## 🔧 Configuração

As principais configurações estão no arquivo `config.toml`:

- **Base URL**: `https://fwfurtado.github.io`
- **Título**: "Mimi"
- **Descrição**: "Mimi homepage"
- **Idioma**: Português Brasileiro (pt-BR)
- **Tema**: Serene


## 🚢 Deploy

O deploy é feito automaticamente via GitHub Actions através do workflow manual:

1. Acesse a aba **Actions** no GitHub
2. Selecione o workflow **Deploy GH Pages**
3. Clique em **Run workflow**

O site será construído e publicado automaticamente no GitHub Pages.

## 🎨 Personalização

### Tema

O tema Serene é incluído como um submódulo Git. Para atualizações:

```bash
cd themes/serene
git pull origin latest
cd ../..
git add themes/serene
git commit -m "Update serene theme"
```

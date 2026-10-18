# Nexus-Dashboard ☁️

**Um dashboard de produtividade e clima que reúne organização pessoal e informações meteorológicas em uma interface moderna, intuitiva e responsiva.**

O Nexus-Dashboard é um projeto acadêmico desenvolvido para a disciplina de **Programação Client-side**, com o objetivo de aplicar conhecimentos de desenvolvimento web na criação de uma aplicação interativa que funciona diretamente no navegador.

## 📌 Sobre o projeto

O projeto reúne ferramentas para ajudar o usuário a organizar suas atividades diárias, acompanhar o andamento das tarefas, registrar anotações e consultar as condições meteorológicas de diferentes cidades.

A aplicação utiliza tecnologias web para atualizar os elementos da interface dinamicamente, armazenar informações localmente e consumir dados de uma API pública.

## ✨ Funcionalidades

### ✅ Gerenciamento de tarefas
- Adicionar e excluir tarefas.
- Marcar tarefas como concluídas.
- Definir prioridades: baixa, média ou alta.
- Organizar tarefas por categoria.
- Informar prazos para as atividades.
- Filtrar tarefas por situação: todas, pendentes ou concluídas.
- Remover todas as tarefas concluídas.
- Acompanhar indicadores de produtividade e progresso.

### 🌦️ Consulta do clima
- Pesquisar cidades pelo nome.
- Consultar a temperatura atual.
- Visualizar a sensação térmica.
- Consultar a umidade do ar.
- Verificar a velocidade do vento.
- Exibir informações meteorológicas atualizadas por meio de uma API pública.

### 📝 Anotações rápidas
- Registrar lembretes e ideias.
- Salvar anotações automaticamente no navegador.

### 🎨 Interface e experiência do usuário
- Design moderno e organizado.
- Alternância entre tema claro e escuro.
- Layout responsivo para diferentes tamanhos de tela.
- Indicadores visuais para facilitar a leitura das informações.
- Navegação e elementos preparados para melhorar a acessibilidade.

### 💾 Armazenamento local
As tarefas, as anotações e a preferência de tema são armazenadas no navegador utilizando `localStorage`, permitindo recuperar essas informações ao atualizar ou reabrir a aplicação no mesmo navegador.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
|---|---|
| HTML5 | Estrutura e organização dos elementos da página |
| CSS3 | Estilização, responsividade e temas visuais |
| JavaScript ES6+ | Interatividade, eventos e manipulação do DOM |
| Fetch API | Comunicação com serviços externos |
| Open-Meteo API | Consulta de localização e condições meteorológicas |
| LocalStorage | Armazenamento local de tarefas, anotações e preferências |
| Git e GitHub | Versionamento e compartilhamento do código |

## 📂 Estrutura do projeto

```text
Nexus-Dashboard/
├── assets/
│   └── Recursos estáticos
├── css/
│   └── style.css
├── js/
│   ├── main.js
│   └── weather.js
├── .gitignore
├── index.html
└── README.md
```

- **`index.html`**: estrutura principal da aplicação.
- **`css/style.css`**: estilos, layout responsivo e temas.
- **`js/main.js`**: funcionalidades das tarefas, anotações, indicadores e tema.
- **`js/weather.js`**: integração com a API meteorológica.
- **`README.md`**: documentação do projeto.

## 🚀 Como executar o projeto

### Pré-requisitos

- Um navegador atualizado, como Google Chrome, Microsoft Edge ou Firefox.
- Visual Studio Code ou outro editor de código.
- Extensão Live Server ou outro servidor HTTP local.
- Conexão com a internet para consultar os dados meteorológicos.

### Executando localmente

1. Baixe ou clone este repositório.
2. Abra a pasta do projeto no Visual Studio Code.
3. Instale a extensão **Live Server**, caso ainda não esteja instalada.
4. Abra o arquivo `index.html`.
5. Clique em **Go Live** para iniciar o servidor local.
6. Acesse o endereço disponibilizado no navegador.

Após abrir a aplicação, você poderá adicionar tarefas, alterar prioridades, registrar anotações e pesquisar as condições do clima de uma cidade.

### Clonando o repositório

```bash
git clone URL_DO_REPOSITORIO
cd Nexus-Dashboard
```

Substitua `URL_DO_REPOSITORIO` pelo endereço real do seu repositório no GitHub.

## 🌐 API meteorológica

O projeto utiliza a [Open-Meteo](https://open-meteo.com/) para consultar informações meteorológicas.

A integração realiza duas etapas:

1. Pesquisa a cidade e obtém suas coordenadas geográficas.
2. Utiliza as coordenadas para consultar as condições meteorológicas atuais.

A comunicação é feita com `fetch`, utilizando operações assíncronas e tratamento de erros para lidar com falhas de conexão ou resultados inválidos.

Documentação oficial:
- [Open-Meteo — Previsão do tempo](https://open-meteo.com/en/docs)
- [Open-Meteo — Geocodificação](https://open-meteo.com/en/docs/geocoding-api)

A consulta depende de conexão com a internet e da disponibilidade da API.

## 🔒 Armazenamento e privacidade

As tarefas, as anotações e a preferência de tema são armazenadas localmente no navegador por meio do `localStorage`.

O projeto não utiliza, em sua implementação atual, um banco de dados remoto para sincronizar esses dados entre dispositivos. Limpar os dados do navegador pode apagar as informações armazenadas localmente.

## 🎯 Objetivos de aprendizagem

O desenvolvimento do Nexus-Dashboard permite praticar conceitos importantes de desenvolvimento front-end, como:

- Estruturação semântica com HTML5.
- Criação de interfaces responsivas com CSS3.
- Manipulação dinâmica do DOM com JavaScript.
- Gerenciamento de eventos e formulários.
- Persistência de dados com `localStorage`.
- Consumo de APIs públicas com `fetch`.
- Tratamento de operações assíncronas e erros.
- Organização de arquivos e versionamento com Git e GitHub.

## 🔮 Possíveis melhorias futuras

- Implementar sincronização de tarefas entre dispositivos.
- Adicionar autenticação de usuários.
- Criar relatórios mais detalhados de produtividade.
- Implementar notificações de prazos.
- Ampliar as opções de personalização do painel.

## 👨‍💻 Contexto acadêmico

**Projeto:** Dashboard Interativo de Produtividade e Clima  
**Área:** Desenvolvimento Web  
**Disciplina:** Programação Client-side  
**Instituição:** SENAI — CEET Sebastião Camargo

Desenvolvido com o objetivo de aplicar, na prática, os fundamentos de HTML5, CSS3 e JavaScript em uma aplicação web interativa.

---

**Nexus-Dashboard** — Organização, produtividade e informação em um só lugar.

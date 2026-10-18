# Nexus-Dashboard

Dashboard web interativo de produtividade e clima, desenvolvido como projeto acadêmico para a disciplina **Programação Client-side**. O projeto executa a lógica no navegador, utilizando HTML5, CSS3 e JavaScript moderno.

## Objetivos

- Criar uma estrutura de página semântica, acessível e organizada.
- Reservar áreas de integração para os componentes desenvolvidos em paralelo pelo grupo.
- Consultar as condições meteorológicas atuais de uma cidade por meio de uma API pública.
- Facilitar o desenvolvimento colaborativo com Git e GitHub.

## Tecnologias

- **HTML5:** estrutura semântica com `header`, `nav`, `main`, `section` e `footer`.
- **CSS3:** variáveis CSS, Grid, Flexbox e layout responsivo.
- **JavaScript ES6+:** módulos organizados por responsabilidade, eventos, `fetch`, `async/await` e `try/catch`.
- **Open-Meteo:** geocodificação de cidades e dados meteorológicos atuais; não exige chave de API para uso gratuito não comercial.
- **Git/GitHub:** versionamento e integração do trabalho em equipe.

## Estrutura de pastas

```text
Nexus-Dashboard/
├── assets/
│   └── # Imagens, ícones e outros recursos estáticos
├── css/
│   └── style.css
├── js/
│   ├── main.js
│   └── weather.js
├── .gitignore
├── index.html
└── README.md
```

## Como executar

1. Baixe ou clone o repositório.
2. Abra a pasta do projeto no editor de código.
3. Inicie um servidor local estático, por exemplo, com a extensão **Live Server** no Visual Studio Code.
4. Abra `index.html` pelo endereço local fornecido pelo servidor.
5. No cartão **Clima**, informe uma cidade e selecione **Buscar**.

É recomendado usar um servidor local em vez de abrir o HTML diretamente com `file://`. A aplicação precisa de conexão com a internet para acessar as APIs públicas.

### Clonar com Git

```bash
git clone URL_DO_REPOSITORIO
cd Nexus-Dashboard
```

Substitua `URL_DO_REPOSITORIO` pelo endereço real do repositório criado pelo grupo.

## Integração de clima

O arquivo `js/weather.js` executa duas etapas:

1. Consulta a API de geocodificação para transformar o nome da cidade em latitude e longitude.
2. Consulta a API de previsão para recuperar temperatura, sensação térmica, umidade, velocidade do vento e código da condição meteorológica.

As requisições usam `fetch`, `async/await`, validação de resposta HTTP e `try/catch`. Mensagens de carregamento e erro são apresentadas na interface. Os dados são atualizados no DOM sem recarregar a página.

A aplicação usa os seguintes serviços:

- Geocodificação: `https://geocoding-api.open-meteo.com/v1/search`
- Condições atuais: `https://api.open-meteo.com/v1/forecast`

Documentação: [Open-Meteo](https://open-meteo.com/en/docs) e [API de Geocoding](https://open-meteo.com/en/docs/geocoding-api).

**Atribuição:** os dados meteorológicos são fornecidos por [Open-Meteo](https://open-meteo.com/). Consulte os termos e a licença de dados do serviço antes de distribuir ou ampliar o uso.

## Contratos de integração entre os integrantes

### Estrutura HTML e estilos

O arquivo `index.html` define os pontos de integração e carrega `css/style.css`, `js/weather.js` e `js/main.js`. O responsável por UI/UX pode alterar os estilos mantendo os IDs necessários ao JavaScript.

### To-Do List

Os elementos reservados para a lista de tarefas são:

- `#task-form`: formulário de criação.
- `#task-input`: campo para digitar uma tarefa.
- `#task-list`: lista de tarefas.
- `#task-count`: indicador de quantidade.
- `#task-empty-state`: mensagem exibida quando não há tarefas.

O responsável pela To-Do List deve implementar criação, conclusão, exclusão e persistência via `localStorage`. Após atualizar a lista, pode emitir o evento para sincronizar os indicadores:

```javascript
document.dispatchEvent(new CustomEvent("tasks:updated", {
  detail: { count: document.querySelectorAll("#task-list > li").length }
}));
```

Evite substituir `innerHTML` com conteúdo digitado pelo usuário. Prefira `document.createElement()` e `textContent`.

## Fluxo Git sugerido

1. Manter `main` como branch estável.
2. Criar branches de trabalho, por exemplo `feat/html-base`, `feat/weather-api` e `feat/todo-list`.
3. Fazer commits pequenos e descritivos.
4. Abrir Pull Requests para revisão e integração.
5. Testar o conjunto integrado antes de mesclar na `main`.

Exemplos:

```bash
git switch -c feat/weather-api
git add index.html js/weather.js
git commit -m "feat: integra consulta de clima"
git push -u origin feat/weather-api
```

## Checklist de validação

- [ ] O dashboard abre por servidor local.
- [ ] Uma cidade válida retorna as condições atuais.
- [ ] Uma cidade inexistente mostra uma mensagem compreensível.
- [ ] Falha de rede não quebra a página.
- [ ] A navegação pode ser usada pelo teclado.
- [ ] A interface funciona em telas estreitas e largas.
- [ ] A To-Do List integrada salva e recupera tarefas pelo `localStorage`.
- [ ] O repositório contém instruções atualizadas.

## Limitações conhecidas

- O clima depende de conexão com a internet e da disponibilidade do serviço Open-Meteo.
- A busca retorna o primeiro resultado de geocodificação para o nome informado; cidades homônimas podem exigir que o usuário informe mais detalhes.
- A lógica de tarefas completa é responsabilidade do integrante designado e ainda deve ser integrada.

## Contexto acadêmico

Projeto: **Dashboard Interativo de Produtividade e Clima**  
Disciplina: **Programação Client-side**  
Tecnologias principais: HTML5, CSS3 e JavaScript ES6+.

# GeoImposter

Um jogo de geografia, história e geopolítica no navegador. Explore um globo 3D, clique nos países e resolva desafios baseados em localização, curiosidades e eventos históricos.

## Modos de jogo

### País Impostor

Um país fictício foi inserido no globo. Gire o planeta, investigue as fronteiras e encontre o impostor antes que o tempo termine.

### Game Show

Modo competitivo inspirado em programas de televisão e eliminações.

- Quatro jogadores começam no ranking.
- Cada rodada traz um tema: geografia, história, mapas históricos ou curiosidades.
- Quem erra desce uma posição; se já estiver na última posição, é eliminado.
- Quem acerta sobe para a maior posição perdida naquela rodada.
- O último jogador restante vence.

### Modo História

Uma campanha cronológica pelo mundo. Selecione um ano, receba uma missão histórica e clique no território correspondente para abrir contexto e avançar na linha do tempo.

## Tecnologias

- HTML, CSS e JavaScript puro
- [Three.js](https://threejs.org/) para o globo 3D e raycasting
- `OrbitControls` para rotação e zoom no desktop e no celular
- Natural Earth / World Atlas para os contornos geográficos dos países
- Canvas 2D para textura colorida e máscara invisível de seleção

## Como executar

Como o projeto usa módulos JavaScript e dados remotos, rode-o em um servidor local em vez de abrir o arquivo diretamente.

```bash
python -m http.server 8000
```

Depois, abra `http://localhost:8000` no navegador.

## Estrutura

```text
├── index.html      # Estrutura de telas, HUD, menu e painéis
├── styles.css      # Visual do atlas, tipografia e responsividade
├── app.js          # Globo, seleção por máscara, dados e regras dos modos
└── outputs/        # Versão pronta para abrir/publicar
```

## Personalização

As principais configurações estão no início de `app.js`:

- `FICTIONAL_COUNTRIES`: países impostores, polígono, cor da máscara e curiosidade.
- `GAME_SHOW_ROUNDS`: perguntas, respostas, tema e tipo de rodada do Game Show.
- `HISTORY_ERAS`: anos, missões, resposta correta e texto de contexto do Modo História.
- `COUNTRY_PALETTE`: paleta colorida aplicada aos países do globo.

## Tipografia e visual

- **Peralta**: títulos e identidade lúdica.
- **Rubik**: botões, indicadores e controles.
- **Roboto**: textos de leitura.

## Próximos passos

- Adicionar multiplayer em tempo real.
- Criar mais eras e mapas políticos históricos.
- Adicionar sons, animações de queda e efeitos de vitória.
- Salvar pontuações e progresso da campanha.

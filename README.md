# Educação sem distância

Deck do seminário sobre Educação a Distância no Brasil — conceitos, histórico,
legislação e perspectivas atuais. TADS · UDESC.

**No ar:** https://educacao-a-distancia.vercel.app

## Como apresentar

Abra `index.html` em qualquer navegador. É um arquivo único, sem build e sem
dependências além das fontes (Google Fonts).

| Tecla | Ação |
|---|---|
| `→` `↓` `espaço` | avança um passo, depois a slide |
| `←` `↑` | volta |
| `Home` / `End` | primeira / última slide |
| `P` | janela do apresentador: relógio de 10 min e próxima slide |
| `F` | tela cheia |

Clicar na metade direita avança, na esquerda volta. Em tela sensível ao toque,
arraste para os lados.

## O relógio de cada slide

Quando a janela é mais larga que 16:9 sobram duas faixas brancas nas laterais.
Cada uma é um poço de Tetris, e a altura da pilha é o tempo da slide: vazia ao
entrar, cheia aos 60 segundos, tudo em coral quando o tempo estoura.

Para mudar o tempo de uma slide, use `data-secs` na `<section>`:

```html
<section class="slide" data-section="HISTÓRICO" data-secs="90">
```

Num projetor 16:9 ou em tela cheia as faixas não existem e o relógio some junto.
O deck funciona igual.

## Desenho

Fundo branco, tinta preta, cinco cores chapadas sem gradiente nem sombra.
Tipografia em Anybody e Martian Mono. Todas as ilustrações são pixel art
desenhada célula a célula no atributo `data-px`, por exemplo:

```html
<div class="px" data-px="KKKK.....KKKK/KKKK.K.K.KKKK/KKKK.....KKKK" style="--u:22px"></div>
```

Cada caractere é uma célula: `.` vazia, `K` preto, `Y` amarelo, `C` coral,
`B` azul, `L` verde-limão, `P` rosa. As peças caem em passos de célula inteira
e travam seco; a saída de cada slide é um *line clear*.

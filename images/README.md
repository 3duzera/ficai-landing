# Fotografias da Ficaí

Cada placeholder no site já mostra, em letras pequenas, **o caminho e a dimensão**
que a foto definitiva deve ter. Basta salvar o arquivo com o nome exato desta tabela
na pasta indicada — o layout não muda, porque as proporções estão travadas no CSS.

## O que substituir

| Arquivo | Proporção | Mínimo | Onde aparece |
|---|---|---|---|
| `hero/hero-principal.jpg` | 4:5 (vertical) | 1200×1500 | Hero, a foto grande |
| `hero/hero-detalhe.jpg` | 1:1 (quadrada) | 900×900 | Hero, o detalhe que invade a foto grande |
| `studios/studio-01-01.jpg` … `studio-05-01.jpg` | 4:5 | 1200×1500 | Capa de cada studio |
| `studios/studio-01-02.jpg`, `-03.jpg` (e assim por diante) | 3:2 (horizontal) | 1600×1067 | Galeria dentro do modal de cada studio |
| `neighborhood/bairro-01.jpg` | 16:9 | 1800×1013 | Vila Mariana, a foto que sangra à esquerda |
| `neighborhood/bairro-02.jpg` | 4:5 | 900×1125 | Vila Mariana, o detalhe menor |
| `neighborhood/guia-01.jpg` … `guia-06.jpg` | 4:3 | 1200×900 | Guia Ficaí, uma por recomendação |
| `brand/detalhe-01.jpg` | 4:5 | 1000×1250 | Manifesto |
| `brand/detalhe-02.jpg` | 1:1 | 800×800 | Manifesto |
| `brand/sobre-01.jpg` | 4:5 | 1000×1250 | História da Ficaí |
| `brand/og-image.jpg` | 1200×630 | — | Miniatura ao compartilhar o link (WhatsApp, redes) |

## Orientação para a produção

- **Proporção é obrigatória.** Uma foto 3:2 no lugar de uma 4:5 vai ser cortada.
  Se a foto real tiver outra proporção, mude o `--ratio` daquele bloco no HTML
  em vez de forçar a imagem.
- Quantas fotos por studio: o modal mostra **3** por padrão. Para mudar, ajuste
  `fotos: 3` em `FICAI.studios` dentro do `index.html`.
- Luz natural e enquadramentos com respiro combinam com o layout — há muito
  espaço em branco ao redor de cada imagem.
- Salve em JPG de qualidade alta. Se o arquivo passar de ~400 KB, comprima
  (Squoosh, TinyJPG) antes de subir.

## Como ligar as fotos ao site

Os placeholders são `<div class="ph">`. Ao trocar, substitua o bloco inteiro por:

```html
<img src="images/hero/hero-principal.jpg"
     alt="Descreva o que se vê, em uma frase"
     width="1200" height="1500" loading="lazy">
```

O `alt` importa: é o que uma pessoa cega ouve e o que o Google lê.
Descreva a cena ("Cama de casal junto à janela do studio"), não a marca.
A foto do hero pode usar `loading="eager"`, porque aparece de imediato.

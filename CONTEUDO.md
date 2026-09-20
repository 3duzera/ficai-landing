# O que falta preencher

Tudo nesta lista está marcado no `index.html` com comentários que você pode buscar
(`Ctrl+F`). Nada foi inventado: onde não havia informação, entrou placeholder.

## 1. Links — todos provisórios

Ficam juntos no topo do `<script>`, no objeto `FICAI.links`. Busque `ADICIONAR LINK`.

| Chave | O que é | Formato |
|---|---|---|
| `whatsapp` | conversa direta | `https://wa.me/55DDDNUMERO?text=Oi!%20Quero%20saber%20sobre%20os%20studios` |
| `instagram` | perfil da marca | `https://instagram.com/...` |
| `airbnbHost` | perfil do anfitrião | `https://airbnb.com.br/users/show/...` |
| `guiaMaps` | lista salva do Guia Ficaí | link "compartilhar lista" do Google Maps |
| `termos` | termos de uso | quando existir |
| `privacidade` | política de privacidade | quando existir |

Enquanto uma chave estiver com `'#'`, o link aparece marcado como
"link a adicionar" e não navega — de propósito.

## 2. Studios

Em `FICAI.studios`. O que já é fato (metragem e capacidade) está preenchido.
Falta:

- [ ] `airbnbUrl` de cada um dos cinco anúncios
- [ ] `desc` — uma ou duas frases sobre o que diferencia aquele studio
      (hoje: "Descrição a adicionar."). Evite repetir as amenidades: elas já
      estão na seção "O que você encontra".
- [ ] As fotos — ver `images/README.md`

## 3. Guia Ficaí

Em `FICAI.guia`. São **6 espaços reservados**, não lugares reais nem fictícios.
Para cada recomendação:

- [ ] `nome` (pt e en)
- [ ] `cat` — uma das chaves de `FICAI.categorias`: `comer`, `cafes`, `cultura`,
      `exercicios`, `bemestar`, `lazer`, `compras`, `essenciais`, `passos`
- [ ] `desc` — por que vocês gostam, em uma frase. É o que separa curadoria de diretório.
- [ ] `dist` — ex.: `450 m`, `8 min a pé`
- [ ] `mapsUrl`
- [ ] foto 4:3

Quer mais de 6? Basta acrescentar itens ao array — o grid e os filtros se ajustam.
Os filtros só mostram uma categoria quando existe pelo menos um lugar nela.

## 4. Textos provisórios

| Onde | Comentário no código | O que falta |
|---|---|---|
| Segurança | `CONTEÚDO: inserir informações confirmadas de segurança do prédio` | Como funcionam acesso, portaria e entrada no studio. Hoje há 3 linhas dizendo "Informação a confirmar". |
| História | `CONTEÚDO: substituir pela história real da Ficaí` | Origem, quem está por trás, propósito. 3 a 4 parágrafos curtos, primeira pessoa. |
| Amenidades | `CONTEÚDO: revisar lista final de amenidades` | Fechar "outros itens essenciais", "demais itens" e "outras comodidades". |

As três seções mostram na tela uma etiqueta **"texto provisório"**. Ela some
sozinha quando você apagar o elemento `<p class="provisorio">`.

## 5. FAQ

Sete respostas dizem **"Informação a confirmar."** — nenhuma política foi inventada:

- [ ] Check-in
- [ ] Check-out
- [ ] Estacionamento
- [ ] Pets
- [ ] Cancelamento
- [ ] Distância exata do metrô
- [ ] Horários e regras da academia e da lavanderia

As outras quatro (capacidade, reserva direta, reserva pelo Airbnb, academia e
lavanderia existirem) já respondem com o que foi confirmado.

## 6. Antes de publicar

- [ ] Trocar `og:url` e `og:image` pelo domínio e pela imagem reais
- [ ] Conferir o ano em `© 2026 Ficaí` no rodapé
- [ ] Preencher o JSON-LD `LodgingBusiness` (está comentado no `<head>`) com
      endereço e telefone reais — só depois de existirem
- [ ] Buscar no arquivo por `ADICIONAR`, `SUBSTITUIR` e `CONFIRMAR` e verificar
      se sobrou alguma pendência

## 7. Tradução

O português é a fonte: está escrito direto no HTML. O inglês fica no objeto `EN`,
no final do `<script>`. Para traduzir um texto novo:

1. no HTML, marque o elemento: `<p data-i18n="minha.chave">Texto em português</p>`
2. no objeto `EN`, adicione: `'minha.chave': 'Text in English',`

Se a chave não existir em `EN`, o site mostra o português — não quebra.
O nome da marca não se traduz (por isso `hero.l2` não está em `EN`).

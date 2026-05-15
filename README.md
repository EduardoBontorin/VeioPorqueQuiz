# Prova de RFID UHF

Site estático com prova interativa sobre sistemas RFID UHF, baseada na padronização GS1 e EPC Gen2.

**15 questões mistas** (10 objetivas + 5 dissertativas) com correção automática das objetivas, gabarito comentado para as dissertativas e persistência local (localStorage) das respostas.

## Stack

Vanilla HTML/CSS/JS — sem build, sem dependências externas (apenas Google Fonts via CDN). Um arquivo `index.html` autocontido.

## Deploy no GitHub Pages

### Opção 1 — Repositório novo

```bash
# 1. Criar repositório no GitHub (público), depois:
git init
git add index.html README.md
git commit -m "Prova de RFID UHF"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/prova-rfid.git
git push -u origin main
```

Em seguida no GitHub:

1. Vá em **Settings → Pages**
2. Em **Source**, selecione `Deploy from a branch`
3. Branch: `main`, pasta: `/ (root)` → **Save**
4. Aguarde ~1 minuto. O site ficará em `https://SEU_USUARIO.github.io/prova-rfid/`

### Opção 2 — Subpasta de um repositório existente

Se você já tem um repositório com Pages ativo, coloque os arquivos em `docs/` ou em uma branch dedicada (`gh-pages`).

### Opção 3 — Domínio custom

Adicione um arquivo `CNAME` com seu domínio (ex.: `prova.brasil3.com.br`) e configure o DNS apontando para `SEU_USUARIO.github.io`.

## Personalização rápida

Todas as questões estão no array `questions` dentro do `<script>` no final do `index.html`. Estrutura de cada item:

```js
// Objetiva
{
  type: 'mc',
  q: 'Texto da pergunta',
  options: ['A', 'B', 'C', 'D'],
  answer: 1, // índice (0-based) da correta
  explain: 'Justificativa exibida após correção'
}

// Dissertativa
{
  type: 'essay',
  q: 'Texto da pergunta',
  rubric: ['Critério 1', 'Critério 2', ...], // pontos esperados na resposta
  explain: 'Comentário geral sobre a resposta esperada'
}
```

Para mudar cores/identidade visual, ajuste as variáveis CSS no topo do `<style>`:

```css
:root {
  --bg: #0a1628;       /* fundo */
  --accent: #f4923b;   /* laranja de destaque */
  --cyan: #48a9dc;     /* azul técnico */
  /* ... */
}
```

## Recursos

- ✅ Responsivo (desktop / tablet / mobile)
- ✅ Persistência local (recarrega sem perder respostas)
- ✅ Correção automática + gabarito comentado
- ✅ Animações de entrada suaves
- ✅ Sticky action bar com contador de progresso
- ✅ Acessível (semântica HTML, navegação por teclado)

## Licença

Material livre para uso educacional.
# VeioPorqueQuiz

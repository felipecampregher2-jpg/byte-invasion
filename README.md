# Byte Invasion

Jogo estilo Space Invaders, feito em HTML5 Canvas puro (sem dependências). Pronto para hospedar gratuitamente no GitHub Pages.

## 1. Subir para o GitHub Pages (hospedagem gratuita)

1. Crie uma conta no [GitHub](https://github.com) se ainda não tiver.
2. Crie um novo repositório (pode ser público), por exemplo `byte-invasion`.
   - **Se o repositório já existir** (com um `index.html` antigo), pode subir os arquivos novos por cima — o GitHub vai perguntar se quer substituir, é só confirmar.
3. Faça upload de **todos os arquivos desta pasta de uma vez** (`index.html`, `sobre.html` — e este `README.md`, opcional):
   - Pelo navegador: abra o repositório → **Add file** → **Upload files** → selecione/arraste os arquivos.
   - Importante: não renomeie nada — os nomes já estão corretos (`index.html` é a página inicial obrigatória do GitHub Pages, `sobre.html` é a página "Sobre o jogo").
4. Vá em **Settings** (do repositório) → **Pages** (menu lateral).
5. Em **Build and deployment** → **Source**, selecione **Deploy from a branch**.
6. Em **Branch**, selecione `main` e a pasta `/ (root)`. Clique em **Save**.
7. Aguarde 1-2 minutos. O GitHub vai te dar uma URL no formato:
   ```
   https://SEU-USUARIO.github.io/byte-invasion/
   ```
8. Pronto — o jogo está no ar, de graça, sem limite de créditos como no Netlify free tier.

Toda vez que você quiser atualizar o site, basta subir os arquivos novos substituindo os antigos (ou usar git push, se preferir linha de comando).

## 2. Ativar o Google AdSense (monetização)

O arquivo já vem com 2 espaços de anúncio prontos (topo e rodapé) e o script do AdSense já incluído — só faltam os seus IDs.

### Passo a passo:

1. Acesse [google.com/adsense](https://www.google.com/adsense) e crie uma conta usando a URL do seu site no GitHub Pages (ex: `https://seu-usuario.github.io/byte-invasion/`).
2. O Google vai analisar o site antes de aprovar. **Isso pode levar de alguns dias a algumas semanas.** Sites muito simples (uma página só, pouco texto) às vezes demoram mais ou são recusados na primeira tentativa — se isso acontecer, considere adicionar uma segunda página com texto sobre o jogo (história, como jogar, etc.) antes de reenviar.
3. Quando aprovado, você vai receber um **Publisher ID**, no formato `ca-pub-1234567890123456`.
4. Abra o `index.html` em qualquer editor de texto e use **Localizar e Substituir** (Ctrl+H):
   - Substitua todas as ocorrências de `SEU-PUBLISHER-ID-AQUI` pelo seu Publisher ID (sem o `ca-pub-`, pois ele já está fixo no código).
5. No painel do AdSense, crie 2 unidades de anúncio do tipo **Display** (uma para o topo, outra para o rodapé). Cada uma vai te dar um `data-ad-slot` (um número).
   - Substitua `SEU-AD-SLOT-TOPO` pelo slot da primeira unidade.
   - Substitua `SEU-AD-SLOT-RODAPE` pelo slot da segunda unidade.
6. Salve o arquivo e suba de novo para o GitHub (substituindo o `index.html` no repositório).
7. Os anúncios reais começam a aparecer depois que o Google processa o site (pode levar algumas horas).

### Importante

- Nunca clique nos próprios anúncios nem peça para outras pessoas clicarem — o Google bane contas por "cliques inválidos".
- O `ads.txt` pode ser exigido pelo AdSense em algum momento; se ele pedir, crie um arquivo `ads.txt` na raiz do repositório com o conteúdo que o próprio painel do AdSense te fornecer.
- Enquanto a conta não for aprovada, os espaços de anúncio simplesmente ficam vazios/invisíveis — o jogo funciona normalmente.

## Estrutura do projeto

```
byte-invasion/
├── index.html   ← jogo completo + slots de anúncio
├── sobre.html   ← página "Sobre o jogo" (ajuda na aprovação do AdSense)
└── README.md    ← este arquivo
```

# Site do Acervo Organizer — como publicar

Este pacote substitui as páginas atuais do repositório público `LeoCNogueira/acervoorganizer` (GitHub Pages).
Os endereços `support.html` e `privacy.html` continuam os mesmos, porque estão cadastrados no App Store Connect.

## O que há no pacote

| Arquivo | Para quê |
|---|---|
| `index.html` | Landing page (vendas) |
| `support.html`, `privacy.html` | Suporte e privacidade, no novo visual (mesmos endereços) |
| `404.html` | Página para endereços inexistentes |
| `style.css` | Visual de todas as páginas, com modo claro e escuro |
| `sitemap.xml` | Lista de páginas para o Google |
| `.nojekyll` | Arquivo oculto: faz o GitHub Pages publicar os arquivos como estão |
| `assets/` | Ícone, favicon e imagem de compartilhamento (`og-image.png`) |

## 1. Substitua os arquivos no repositório

1. No GitHub Desktop, clone o repositório `acervoorganizer`, se ainda não fez:
   **File → Clone Repository…**, salvando em `~/Developer/acervoorganizer-site`.
2. Na pasta do site, **apague** `index.html`, `support.html`, `privacy.html` e `style.css`.
   **Não apague `AcervoOrganizer-Amostra.zip`**: é a amostra citada nas notas para a revisão da Apple.
3. Copie o conteúdo deste pacote para a pasta. O `.nojekyll` é oculto no Finder; para copiar tudo de uma vez,
   use o Terminal (ajuste o caminho do pacote descompactado):
   ```
   cp -R ~/Downloads/site-acervoorganizer/. ~/Developer/acervoorganizer-site/
   ```

## 2. Coloque o selo oficial da Mac App Store

A Apple exige o selo oficial, sem modificações, e um único selo por página.

1. Abra o App Store Marketing Tools (link "App Store Marketing Tools" em
   developer.apple.com/app-store/marketing/guidelines) e procure **Acervo Organizer**.
2. Escolha o selo **"Baixar na Mac App Store"**, idioma português (Brasil), versão preta, e baixe o **SVG**.
3. Salve como `assets/selo-mac-app-store.svg`.

Enquanto o arquivo não existir, o hero mostra um botão de texto "Baixar na Mac App Store" no lugar do selo.

## 3. Adicione capturas reais do app (recomendado)

A seção "Veja o app por dentro" só aparece quando as imagens existem. Crie a pasta `assets/capturas/` e salve, com
estes nomes exatos (as capturas da App Store servem; de preferência até 300 KB cada):

- `organizar-fotos.png`: a tela Organizar Fotos com o resultado de uma análise;
- `simulacao.png`: a janela da simulação;
- `duplicatas.png`: a tela Duplicatas com grupos encontrados.

Use um acervo de exemplo, nunca fotos de clientes.

## 4. Publique e confira

1. No GitHub Desktop: escreva o resumo ("Nova landing page"), clique em **Commit to main** e depois em **Push origin**.
2. Espere 1 ou 2 minutos e abra:
   - https://leocnogueira.github.io/acervoorganizer/
   - https://leocnogueira.github.io/acervoorganizer/support.html
   - https://leocnogueira.github.io/acervoorganizer/privacy.html
   - https://leocnogueira.github.io/acervoorganizer/AcervoOrganizer-Amostra.zip
3. Clique num botão de download e confirme que abre a página do app na Mac App Store. O link usa o Apple ID
   **6821982992**; confira em App Store Connect → Informações do app → Apple ID.
4. Cole o link do site no WhatsApp e confira se aparece a imagem de compartilhamento.

## 5. Ligue o site à loja e ao Google

- **App Store Connect → página da versão → URL de marketing:** preencha com o endereço da landing page.
- **Google Search Console:** adicione a propriedade do tipo "Prefixo do URL" com
  `https://leocnogueira.github.io/acervoorganizer/`, verifique pelo arquivo HTML que o Google fornece (coloque-o na
  raiz do repositório) e envie `sitemap.xml` em Sitemaps.

## 6. Meça os resultados

O site não tem nenhum rastreamento, coerente com a promessa de privacidade do app. Para saber quantos downloads
vêm dele, use os **links de campanha** do App Store Connect (App Analytics → fontes → campanhas). Gere um link
com a campanha `site` e troque os 6 links `https://apps.apple.com/app/id6821982992?mt=12` do `index.html` por ele.

## 7. Próximas atualizações do site

- **Quando a 2.9 sair:** no `index.html`, tire o selo "Em breve" de "Importar cartão" e acrescente a importação
  ao quadro do hero e às perguntas.
- **Quando houver avaliações na App Store:** troque a faixa de garantias abaixo do hero pela nota e pelo número de
  avaliações. Prova social logo depois do hero é o que mais aumenta conversão. Use somente avaliações reais.
- **Quando houver a versão em inglês:** crie `/en/` com a página traduzida e atualize a pergunta sobre o idioma.

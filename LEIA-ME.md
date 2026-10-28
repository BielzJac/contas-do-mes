# Contas do Mês — app para celular (PWA)

Organiza as contas a pagar pelo dia em que você recebe. Funciona offline, instala na tela inicial do Android e do iPhone, e os dados ficam só no aparelho de cada pessoa.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | O app inteiro |
| `manifest.webmanifest` | Nome, ícone e cores do app instalado |
| `sw.js` | Faz o app abrir sem internet |
| `icons/` | Ícones da tela inicial |

Os arquivos precisam ficar juntos, nessa mesma estrutura.

## Publicar de graça no GitHub Pages

1. Entre em github.com e crie um repositório novo, por exemplo `contas-do-mes`. Pode ser público.
2. Na página do repositório, clique em **Add file > Upload files** e arraste todo o conteúdo desta pasta (incluindo a pasta `icons`). Clique em **Commit changes**.
3. Vá em **Settings > Pages**. Em **Branch**, escolha `main` e a pasta `/ (root)` e clique em **Save**.
4. Espere um ou dois minutos. O endereço aparece no topo dessa mesma página, no formato
   `https://SEU-USUARIO.github.io/contas-do-mes/`

Esse é o link para mandar para quem quiser usar.

Pelo terminal, se preferir:

```bash
cd pasta-do-app
git init && git add . && git commit -m "Contas do Mês"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/contas-do-mes.git
git push -u origin main
```

Depois é só ativar o Pages como no passo 3.

## Instalar no celular

**iPhone (Safari):** abra o link, toque no botão de compartilhar e escolha **Adicionar à Tela de Início**. Precisa ser pelo Safari.

**Android (Chrome):** abra o link e toque em **Instalar app** quando aparecer. Se não aparecer, use o menu ⋮ > **Adicionar à tela inicial** ou **Instalar app**.

**PC (Chrome ou Edge):** abra o link e clique no ícone de instalar na barra de endereço.

Depois de instalado, o app abre em tela cheia e funciona sem internet.

## Os dados

- Cada pessoa vê só os próprios dados. Nada vai para servidor nenhum.
- Os dados ficam no aparelho. Se o app for desinstalado ou os dados do navegador forem apagados, eles somem.
- Use **Backup > Exportar backup** de vez em quando. O mesmo arquivo serve para passar os dados para outro aparelho (**Importar backup**).
- No iPhone, use sempre o app instalado na tela inicial, não o link aberto no Safari. São armazenamentos separados, e o instalado é o que guarda os dados de forma mais estável.

## Atualizar o app

1. Troque o `index.html` no repositório pelo novo.
2. No `sw.js`, mude `const VERSION = "v1";` para `"v2"` (e assim por diante a cada atualização).
3. Faça o commit. Quem tem o app instalado recebe a versão nova na próxima vez que abrir com internet (às vezes é preciso fechar e abrir de novo).

Os dados das pessoas não são afetados por atualizações.

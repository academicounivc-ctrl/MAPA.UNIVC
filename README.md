# Mapa Interativo UNIVC — Localize-se

Mapa de orientação (wayfinding) interativo do campus do Centro Universitário Vale do Cricaré (UNIVC).
Escolha origem e destino e um bonequinho percorre o menor caminho pelas áreas de circulação, usando
um algoritmo de **Dijkstra** sobre a planta do campus.

O site é um **único arquivo** (`index.html`) — a imagem da planta, o logo e a malha de navegação já
estão embutidos nele. Não precisa de servidor, build, nem de nenhuma dependência externa.

---

## Como publicar no GitHub Pages

Você pode fazer tudo pelo navegador (mais fácil) ou pelo terminal (git). Escolha um dos caminhos.

### Opção A — Pelo site do GitHub (sem instalar nada)

1. Entre em <https://github.com> e clique em **New** para criar um repositório novo
   (ex.: nome `mapa-univc`). Deixe como **Public**.
2. Na página do repositório vazio, clique em **uploading an existing file**
   (ou aba **Add file → Upload files**).
3. Arraste os arquivos **`index.html`** e **`README.md`** para a área de upload.
4. Clique em **Commit changes**.
5. Vá em **Settings** (engrenagem do repositório) → menu lateral **Pages**.
6. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
7. Em **Branch**, selecione **main** e a pasta **/ (root)** e clique em **Save**.
8. Aguarde ~1 minuto e recarregue a página **Pages**. Vai aparecer o endereço do seu site, algo como:
   `https://SEU-USUARIO.github.io/mapa-univc/`

Pronto! Esse é o link do mapa.

### Opção B — Pelo terminal (git)

```bash
# dentro da pasta onde estão index.html e README.md
git init
git add index.html README.md
git commit -m "Mapa interativo UNIVC"
git branch -M main

# troque SEU-USUARIO e mapa-univc pelos seus
git remote add origin https://github.com/SEU-USUARIO/mapa-univc.git
git push -u origin main
```

Depois é só ativar o Pages no site (passos 5 a 8 da Opção A).

---

## Testar localmente (opcional)

Como é um arquivo único, basta **dar dois cliques no `index.html`** que ele abre no navegador.
Não precisa de servidor.

---

## Arquivos

| Arquivo       | Para que serve                                                        |
|---------------|-----------------------------------------------------------------------|
| `index.html`  | O mapa completo (é o que o GitHub Pages publica). **Não renomeie.**    |
| `README.md`   | Este guia.                                                             |

## Atualizar o mapa depois

Se você gerar uma versão nova do `index.html`, é só substituir o arquivo no repositório
(Add file → Upload files, ou `git add/commit/push`). O GitHub Pages atualiza sozinho em ~1 minuto.

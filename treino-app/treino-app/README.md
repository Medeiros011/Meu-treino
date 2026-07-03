# Meu Treino — PWA (ABCDE)

App de treino instalável no celular. Tema preto fosco + amarelo. Funciona offline e salva o progresso no aparelho.

## ⚠️ IMPORTANTE — a tela estava preta? Faça isto uma vez

A versão antiga ficou "presa" no cache do navegador (service worker). Depois de subir os arquivos novos, limpe o cache uma vez:

**No PC (Chrome/Edge):**
1. Abra `https://SEU-USUARIO.github.io/Treino/`.
2. Aperte **F12** para abrir as ferramentas do desenvolvedor.
3. Vá na aba **Application** → menu lateral **Storage** → botão **Clear site data**.
   (ou em **Service Workers** → **Unregister**.)
4. Feche o F12 e recarregue com **Ctrl + Shift + R**.

**No celular:**
- Feche todas as abas do site, ou vá em Configurações do navegador → Privacidade → Limpar dados de navegação (só do site), e reabra o endereço.

A partir desta versão isso não acontece mais: o app busca o HTML pela rede primeiro, então atualizações aparecem sozinhas quando você está online.

## Publicar/atualizar no GitHub

1. Abra o repositório **Treino** → **Add file → Upload files**.
2. Suba **todos** os arquivos desta pasta, substituindo os antigos:
   `index.html`, `manifest.webmanifest`, `sw.js`, `favicon.png`,
   `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`.
3. **Commit changes**. O deploy leva ~1 min.
4. Em **Settings → Pages** confirme: Source = "Deploy from a branch", branch `main`, pasta `/ (root)`.

## Instalar no celular

Abra `https://SEU-USUARIO.github.io/Treino/`:
- **Android (Chrome):** menu (⋮) → **Instalar app**.
- **iPhone (Safari):** **Compartilhar** → **Adicionar à Tela de Início**.

## Notas

- O `index.html` já traz React embutido (~180 KB) — sem CDN, carrega instantâneo e offline.
- O progresso fica salvo **neste aparelho** (localStorage).
- Para editar o treino, altere a lista `PLAN` dentro do `index.html`.
- Ao publicar uma nova versão, suba também o `sw.js` com o número de cache trocado (ex.: `meu-treino-v3` → `v4`) para forçar a atualização.

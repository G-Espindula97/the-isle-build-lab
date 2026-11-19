# The Isle Evrima — Build Lab

Planejador de builds de mutações para o jogo The Isle: Evrima, por Gabriel Espindula (DVLA).
Responda sempre em português do Brasil.

- Um único arquivo: `index.html` (HTML + CSS + JS). Sem servidor, sem login.
- Dados do usuário (nick e builds) ficam só no `localStorage` (chaves `isle_nick` e `isle_builds:<nick>`).
- Rodapé tem aviso de privacidade (LGPD) e botão "Apagar meus dados deste navegador".
- Repositório público: `G-Espindula97/the-isle-build-lab` → https://g-espindula97.github.io/the-isle-build-lab/
- Publicar: commit + push na `main` (GitHub Pages publica sozinho em ~1 min).
- Testar localmente: `npx http-server@14.1.1 -p 5180 -c-1` → http://localhost:5180

## Regras
- **Backups nunca são substituídos:** todo backup leva nome + data/hora (pasta local de backups do autor).
- Projeto de fã, sem afiliação com The Isle / Afterthought — manter esse aviso.

## Mapa do `index.html` (~1000 linhas — use grep, não leia tudo)
- `<style>` no topo · telas: `#editorView`, `#summaryView`, `#myBuildsView` (troca via `showView`)
- Dados: `DATA` (espécies), `SPECIES_IMG`, `LORE`, `CURATED`, `INCOMPATIBLE`, `NEVER`, listas `WATER_SP/NIGHT_SP/AGILE_SP/SPRINT_SP`
- Perfis/modelos de build: `MODE_NAMES`, `presetProfile`, `distribution`, `blendProfile`, `applyModels`, `toggleModel`
- Recomendação: `scoreMutation`, `isCompatible`, `allowed`, `ranked`, `recommendation`, `render`, `updateScore`
- Visual do dino: `dinoShape`, `sceneSVG`, `drawStage` · resumo: `summaryText`, `showSummary`
- Login + Minhas builds (bloco `/* ===== Login + Minhas builds ===== */`): `doLogin`, `getBuilds/putBuilds`, `saveNew`, `loadBuild`, `renderMyBuilds`

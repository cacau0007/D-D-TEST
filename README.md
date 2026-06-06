# ⚜ Thornwall — Mesa do Mestre

DM Screen interativo pra rodar a one-shot **O Convite de Valdenmoor**. Single-file, salva tudo no navegador, deploy num clique no Railway.

## O que tem

- **Mapa com tokens arrastáveis** — arrasta inimigos/NPCs/jogadores; arrasta o fundo pra mover; roda do mouse dá zoom.
- **7 cenas pré-carregadas** (do Cruzamento de Ashfen aos Porões) com texto pra ler em voz alta + notas de mestre. Tudo editável.
- **Fichas clicáveis e editáveis** — clica no token e vê CA, PV, atributos, traços e ações. Botões de dano/cura. Stat blocks já preenchidos (Vine Blight, Needle Blight, Guardião do Cristal) e NPCs (Lirien, Bram, Seda, Torv).
- **Rolador de dados** — d4 a d100 + fórmula livre (`2d6+3`), com log e destaque de crítico/falha.
- **Rastreador de iniciativa** — "Auto" rola os inimigos da cena somando o mod de DES; "Próximo turno" cicla.
- **Imagem de mapa custom** — em cada cena dá pra colar a URL de um mapa.
- **Salva automático** no navegador + Exportar/Importar JSON pra backup.

## Rodar local

```bash
npm install
npm start
# abre http://localhost:3000
```

## Deploy no Railway

**Opção A — via GitHub (recomendado):**
1. Sobe essa pasta num repo do GitHub.
2. No Railway: `New Project` → `Deploy from GitHub repo` → seleciona o repo.
3. Railway detecta Node, roda `npm install` e `npm start` sozinho. Pronto.
4. Em `Settings → Networking → Generate Domain` pra ter a URL pública.

**Opção B — via CLI:**
```bash
npm i -g @railway/cli
railway login
railway init
railway up
```

O `PORT` é injetado pelo Railway automaticamente — o `server.js` já lê `process.env.PORT`.

## Observação sobre os dados

Tudo é salvo no **localStorage do navegador** — ou seja, fica no seu dispositivo, não num banco. Pra levar pra outra máquina ou fazer backup antes da sessão, usa **Exportar**. Pra restaurar a one-shot original, botão **Reset**.

Bom jogo, mestre. 🎲

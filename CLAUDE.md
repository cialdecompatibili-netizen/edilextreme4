# edilextreme4

Sito Jekyll su GitHub Pages: https://cialdecompatibili-netizen.github.io/edilextreme4/

## Cose che funzionano
- Skill Impeccable (design): installata a livello progetto con `npx --yes impeccable install --providers=claude --scope=project` dalla radice del progetto. I flag evitano le domande interattive. Dopo l'installazione, in Claude Code (anche nella scheda Code di Claude Desktop) lanciare `/impeccable init`.
- Controllo design senza LLM: `npx impeccable detect --json _layouts _includes index.html` (trova per esempio testo con contrasto sotto 4.5:1).
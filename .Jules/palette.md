# Journal de Aprendizados - Palette 🎨

Neste diário, são registrados apenas aprendizados críticos de UX e acessibilidade relativos a este projeto.

## 2026-07-25 - Transições de Foco e Acessibilidade no Drawer
**Learning:** Elementos interativos dinâmicos com animações de CSS (como `transform: translateX(105%)` para `translateX(0)`) precisam de uma pequena folga (`setTimeout` de 100ms a 300ms) antes de receberem foco programático via `.focus()`, pois navegadores podem não considerar o elemento clicável ou visível imediatamente no início da animação de transição, causando falhas silenciosas de foco.
**Action:** Ao abrir gavetas ou diálogos animados, sempre utilizar um pequeno delay (ex: `setTimeout(..., 150)`) para focar o primeiro elemento interativo, além de armazenar a referência do gatilho anterior (`lastActiveElement`) para restaurá-lo ao fechar o diálogo.

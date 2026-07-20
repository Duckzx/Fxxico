# 🎨 Palette - Diário de UX e Acessibilidade

Diário de aprendizados críticos sobre usabilidade, experiência do usuário e padrões de acessibilidade implementados no projeto fxxico.

## 2026-07-20 - Delays de Foco em Gavetas/Modais Animados
**Learning:** Ao abrir gavetas ou modais que utilizam transições CSS (ex: `transform: translateX(105%)` para `translateX(0)`), a chamada imediata de `.focus()` no botão de fechar ou no primeiro elemento interativo pode falhar ou ser ignorada pelo navegador se o elemento ainda não for considerado totalmente interativo/visível.
**Action:** Utilizar um atraso de 100ms a 300ms com `setTimeout` garante que a animação tenha iniciado e o elemento esteja renderizado na viewport de forma que o navegador aplique o foco corretamente.

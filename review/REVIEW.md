# Revisão de design — Landing page Ayala Brows

Projeto Lovable: https://lovable.dev/projects/5799aca5-8cbe-4db9-915d-6fb7eedb6f48

O código foi lido no Lovable (`src/routes/index.tsx`, `src/components/landing/ui.tsx`, `src/styles.css`, `src/routes/__root.tsx`).
Os testes de layout foram feitos numa cópia local, com fotos provisórias, nas larguras 320, 390, 768 e 1440px.
`mobile-320-topo.png` mostra o topo da página em 320px.

## Prioridades
1. **Celular**
   - Barra fixa de compra: mostrar só depois que o botão do topo sair da tela. Hoje os dois botões aparecem empilhados.
   - Contadores: os rótulos estouram a caixa em 320 e 390px, e os números aparecem como "0" antes da animação.
   - Preço "12x R$ 20,37": quebra em 2 linhas em 320px.
   - Botão da oferta: quebra em 2 linhas em 390px.
2. **Rastreamento**
   - Repassar os UTMs e o fbclid para o link do Kiwify.
   - Adicionar o Pixel da Meta.
3. **VSL**
   - O mp4 de 23 MB carrega inteiro, sem ajustar a qualidade à internet de quem assiste.
   - Opções: Vturb/Panda, ou comprimir o arquivo para uns 8 MB.
4. **Estrutura da página**
   - Prova social logo abaixo da VSL.
   - Botões do meio da página levando para `#oferta`.
   - Menos elementos pulsando ao mesmo tempo.
5. **Detalhes técnicos e legais**
   - Contraste: o dourado `#c99a5b` sobre o creme dá cerca de 2,4:1. Usar `#8a6326` em texto.
   - Trocar `lang="en"` por `pt-BR`.
   - Adicionar a imagem de compartilhamento (og:image).
   - Rodapé com Política de Privacidade e Termos.
   - Definir largura e altura das imagens (evita a página "pular").
   - Visualizador de fotos: travar a rolagem, manter o foco dentro da janela e aumentar o "×".

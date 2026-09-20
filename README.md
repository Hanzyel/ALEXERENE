# Dashboard da Obra — Residência Alex Sandro

Projeto estático pronto para GitHub + Vercel.

## Estrutura

- `index.html` — aplicação principal.
- `assets/styles.css` — estilos do dashboard e versão mobile.
- `assets/app.js` — lógica do dashboard.
- `projects/architecture/pdf/` — PDFs arquitetônicos originais.
- `projects/architecture/preview/` — prévias de alta resolução usadas no visualizador interno.
- `data/projects.json` — catálogo dos projetos.
- `api/projects.js` — endpoint Vercel `/api/projects` para consultar o catálogo.
- `vercel.json` — cache e cabeçalhos para PDFs e imagens.

## Visualizador de projetos

O painel não depende mais do leitor PDF incorporado do navegador. Dentro do app é exibida uma prévia A1 de alta resolução, com Ajustar, Largura e zoom. O botão **Abrir PDF** abre o arquivo vetorial original. Isso evita o recorte/área cinza observado em iframes com PDFs grandes.

## Atualizar um projeto

1. Substitua o PDF correspondente em `projects/architecture/pdf/`.
2. Gere/substitua a prévia JPG em `projects/architecture/preview/` mantendo o mesmo nome.
3. Se mudar nome, tamanho ou data, atualize `data/projects.json` e `api/projects.js`.
4. Faça commit e push; a Vercel fará novo deploy automaticamente.

## Execução local

Esta versão usa caminhos relativos e funciona tanto em hospedagem web quanto em abertura local para testes.

## Teste local no Windows

Esta versão usa caminhos relativos e pode ser aberta diretamente por `index.html` ou por `ABRIR_LOCAL.bat`. CSS, JavaScript, prévias e PDFs permanecem dentro da própria pasta do projeto.

Para simular exatamente o ambiente web antes do Vercel, você também pode servir a pasta por um servidor HTTP local, mas isso não é obrigatório para uma conferência visual básica.

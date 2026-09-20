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


## V17
- Botão Voltar na tela Relatório da Obra.
- Conciliação entre total pago, total sem Administração e custo direto comparável.
- Valor de R$ 741.058,05 identificado como total pago menos R$ 120.000,00 de Administração.

## V18 — critério de custo direto ampliado

A partir desta versão, o custo direto da obra considera todos os desembolsos da planilha, exceto a fase **Administração**. O total direto adotado é **R$ 741.058,05**, composto por:

- Materiais: R$ 386.138,72
- Mão de obra: R$ 295.964,56
- Custos Operacionais e de Apoio: R$ 58.954,77

A categoria **Custos Operacionais e de Apoio** reúne gestão lançada fora da fase Administração, aluguel de equipamentos, documentação, taxas, lançamentos sem referência e alimentação.

## V19 — mobile e navegação
- O painel/hero "Controle executivo da obra" aparece apenas na aba Executivo.
- Navegação mobile com número + nome de cada aba sempre visíveis.
- A aba ativa é centralizada automaticamente na faixa horizontal.
- Cards, relatório, projetos, tabelas, filtros e formulários receberam regras mobile-first.

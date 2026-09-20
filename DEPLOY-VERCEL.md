# Publicar no Vercel

1. Crie um repositório no GitHub e envie todos os arquivos desta pasta para a raiz do repositório.
2. Acesse o Vercel, escolha **Add New > Project** e importe o repositório.
3. Em **Framework Preset**, use **Other** (site estático).
4. Não defina Build Command nem Output Directory. A raiz já contém `index.html`.
5. Clique em **Deploy**.
6. Depois do deploy, abra `/projetos` pelo menu do dashboard e valide uma prancha.
7. Teste também `/api/projects` para confirmar que a API do catálogo respondeu.
8. Para domínio próprio, abra **Project Settings > Domains** e adicione seu domínio.
9. A cada `git push` na branch de produção, o Vercel publica uma nova versão automaticamente.

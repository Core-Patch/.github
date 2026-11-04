# Core & Patch — instruções para agentes e contribuidores

## Entrada e economia de contexto
1. Identifique repositório, branch/HEAD e Issue atribuída. Leia este arquivo, `README.md` **se existir**, e a Issue com checklist, aceite e dependências.
2. Consulte somente o código relacionado e os ADRs/RFCs/Decisions aplicáveis; prefira busca direcionada a despejar arquivos inteiros. Nunca presumir que fonte externa foi lida se inacessível.
3. O padrão institucional vigente é [Engineering & Web Delivery Standard V1](https://docs.google.com/document/d/1986CLOeX87w1Pt920MJRTDJ-_jhDQBRjeaROnTg70Ds/edit); GitHub rastreia desenvolvimento, Core Knowledge governa decisões, Drive contém documentos formais, CoreHub estado operacional e cofre guarda secrets.
4. Se uma instrução local, RFC aceita, Decision ACTIVE ou Issue entrar em conflito, registre conflito e interrompa a mudança afetada até decisão autorizada.

## Fluxo obrigatório
- Issue → triagem/Ready → branch curta → implementação mínima → testes locais → PR pequena → CI no HEAD → review independente → threads inline → resposta **PROCEDE** ou **NÃO PROCEDE** fundamentada → correção e nova revisão quando cabível → resolver conversation apenas após evidência → Human Gate conforme risco → squash merge autorizado → verificar `main` e atualizar Issue.
- Checklist de subtarefas na Issue orienta execução; `Refs #N` para PR parcial; `Closes #N` só na entrega integral. Merge **não** equivale a release/deploy.
- Classifique LOW/MEDIUM/HIGH/CRITICAL conforme impacto. Artur é Technical Owner para arquitetura, auth/RLS, tenant, migrations, secrets, infraestrutura, dados de clientes e produção. Guilherme pode implementar e revisar produto/QA. Autorrevisão não é revisão independente; não invente CI/testes/aprovação.
- Sem senha/token/PII em Git, log ou issue. Sem mudanças diretas na `main`, gastos, publicação, migrações remotas, exclusões destrutivas ou deploy sem autorização aplicável.

## Contexto local
Repositório público de templates e perfil GitHub. Nunca incluir decisões internas, clientes, segredos, contatos de segurança não confirmados. Não alterar publicação de templates sem validar exposição pública.

## Entrega
Relatar arquivos alterados, testes executados e resultados, PR/Issue/HEAD, findings resolvidos e pendências. Preservar arquitetura, simplicidade, segurança e documentação. Este documento é entrada operacional, não uma nova fonte de autoridade.

# Guia de implantação - CRJ Educadores, Ideias e Atas

## 1. Arquitetura

O projeto usa dois repositórios:

- **Público:** contém somente o aplicativo e a documentação, publicado pelo GitHub Pages.
- **Privado:** contém `dados/backup-oficial.json`, usado como arquivo compartilhado e versionado.

O navegador mantém uma cópia rápida em LocalStorage. A sincronização é manual e não usa banco de dados externo.

## 2. Criação automática com o instalador

1. Abra `INSTALADOR_GITHUB.html` no seu computador.
2. Informe o usuário `CRJCARIACICA`.
3. Mantenha os nomes sugeridos dos dois repositórios.
4. Cole um token temporário com permissão para criar repositórios, administrar Pages, escrever conteúdos e workflows.
5. Clique em **Criar repositórios e publicar**.
6. Aguarde a conclusão de todas as etapas.
7. Revogue o token temporário após a instalação.

O token é usado somente na aba aberta e não é salvo no arquivo.

## 3. Criação manual, caso prefira

### Repositório público

Crie `crj-educadores-planejamento-atas` como público. Envie todo o conteúdo de `repositorio-publico-site` para a raiz da branch `main`.

O workflow `.github/workflows/pages.yml` tenta ativar e publicar o Pages. Caso o site não seja habilitado automaticamente, abra **Settings > Pages**, escolha **GitHub Actions** como origem e execute o workflow em **Actions**.

Endereço esperado:

`https://crjcariacica.github.io/crj-educadores-planejamento-atas/`

### Repositório privado de dados

Crie `crj-educadores-planejamento-atas-dados` como privado. Envie a pasta `dados` do modelo. O arquivo inicial pode conter apenas `{}`; o aplicativo converterá esse conteúdo para a estrutura completa no primeiro download ou envio.

## 4. Token de uso diário

Crie um token fine-grained separado do token de instalação:

- proprietário: `CRJCARIACICA`;
- acesso: somente `crj-educadores-planejamento-atas-dados`;
- permissão: **Contents - Read and write**;
- validade curta e renovável.

Não coloque o token no HTML, em commits, capturas de tela ou mensagens. Digite-o somente na aba **Banco de Dados / Backup**. Ele fica na sessão da aba.

## 5. Primeiro computador

1. Abra o site.
2. Escolha Wemerson, André ou Isabela em **Quem está editando agora?**.
3. Abra **Banco de Dados / Backup**.
4. Use:
   - proprietário: `CRJCARIACICA`;
   - repositório: `crj-educadores-planejamento-atas-dados`;
   - branch: `main`;
   - caminho: `dados/backup-oficial.json`.
5. Cole o token diário.
6. Clique em **Testar conexão**.
7. Clique em **Enviar dados para o GitHub** para registrar a primeira versão oficial.

## 6. Demais computadores

Em cada computador:

1. Abra o mesmo endereço do site.
2. Escolha o educador atual.
3. Configure o repositório privado e o token.
4. Clique em **Baixar dados do GitHub** antes de começar.
5. Faça um registro de teste, envie e confira no computador seguinte.

## 7. Rotina obrigatória

- **Antes de editar:** baixar do GitHub.
- **Durante:** confirmar mês e educador nos filtros globais.
- **Ao terminar:** exportar JSON local e enviar ao GitHub.
- **Quando houver bloqueio:** não force o envio; exporte seu JSON, baixe a versão oficial, reaplique somente o que falta e envie novamente.

## 8. Chuva de Ideias e Atas

A nova área permite:

- criar reuniões de equipe, planejamento, Grupo Gestor, avaliações e articulações;
- registrar participantes, objetivo, pauta e pontos discutidos;
- cadastrar ideias por categoria, autoria e prioridade;
- apoiar, priorizar e aprovar propostas;
- organizar responsáveis, prazos e situação dos encaminhamentos;
- gerar insights por recorrência, categoria, prioridade, decisões e pendências;
- gerar ata institucional em DOCX e PDF;
- salvar a ata em Relatórios e Anexos e registrar evidência do tipo Ata.

Reuniões de estudo de caso devem usar o mínimo de informação pessoal necessário. Não registrar dados sensíveis em atas gerais.

## 9. Filtros mensais

A barra superior aplica mês, educador e texto de busca em planejamentos, oficinas, CFDH, eventos, passeios, mobilização, calendário, registros, jovens, instrumentais, relatórios, metas, evidências e Chuva de Ideias e Atas.

## 10. Fundamento metodológico

A área de reuniões e atas apoia a rotina semanal de alinhamento, estratégias, planejamentos, demandas e encaminhamentos da equipe. Também atende à necessidade de formalização de reuniões e da gestão participativa por atas, relatórios e registros.

## 11. Segurança

- Código e documentação ficam no repositório público.
- Dados preenchidos ficam somente no repositório privado e nos computadores autorizados.
- Evitar arquivos grandes dentro do JSON.
- Fotografias e documentos sensíveis devem ficar em armazenamento institucional autorizado; no aplicativo, registrar apenas metadados e vínculos quando necessário.
- Ativar autenticação em dois fatores no GitHub.
- Fazer backup mensal fora do GitHub.

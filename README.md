# CRJ Cariacica - Aplicativo dos Educadores

Aplicativo web estático para Wemerson, André e Isabela planejarem, registrarem e acompanharem oficinas, CFDH, eventos, vivências, mobilização, metas, evidências, relatórios e instrumentais.

## Recursos principais

- filtros globais por mês, educador e busca em todas as áreas de consulta;
- calendário visual com exportação A4 horizontal;
- planejamentos, instrumentais e relatórios em DOCX/PDF;
- sincronização entre computadores por JSON em repositório privado do GitHub;
- proteção contra sobrescrita de uma versão remota mais recente;
- área Chuva de Ideias e Atas, com ideias, prioridades, apoios, decisões, encaminhamentos, insights e geração de ata;
- funcionamento local por LocalStorage, sem Firebase, Supabase, MySQL ou outro banco externo.

## Repositórios recomendados

- Site público: `CRJCARIACICA/crj-educadores-planejamento-atas`
- Dados privados: `CRJCARIACICA/crj-educadores-planejamento-atas-dados`

## Regra de uso em três computadores

1. Selecionar o educador atual.
2. Baixar o backup do GitHub antes de editar.
3. Trabalhar normalmente.
4. Exportar um JSON local de segurança.
5. Enviar ao GitHub ao terminar.

Não existe edição simultânea. O último envio substitui o arquivo oficial, por isso o aplicativo bloqueia o envio quando encontra uma versão remota mais recente.

Consulte `docs/GUIA_IMPLANTACAO.md`.

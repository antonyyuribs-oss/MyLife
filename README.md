# MyLife 1.4 — Importação JSON + Markdown

**Atualização:** substitua os arquivos na raiz do repositório GitHub Pages. Não desinstale o aplicativo nem apague dados do Safari antes de exportar um backup JSON.

## Importação: um único botão

Em **Dados → Importar notas (JSON ou Markdown)**, selecione um ou mais arquivos `.json`, `.md` ou `.markdown`. O formato é reconhecido pela extensão e cada arquivo Markdown é convertido em **uma nota completa editável**, com título da primeira linha `# ...` ou, na ausência dela, o nome do arquivo. A nota chega **não fixada** por padrão; abra-a e fixe se desejar.

Os arquivos Markdown podem conter parágrafos, títulos, negrito, itálico, destaque, tachado, sublinhado em HTML, links HTTPS, listas comuns/numeradas com até 4 recuos, checklists marcados ou pendentes, tabelas simples, citações, código, divisórias e imagens/arquivos incorporados como Data URL. O aplicativo mostra o total encontrado e pergunta se deve **adicionar** ou **substituir**. Em caso de erro, nenhum arquivo do lote é aplicado.

**Importante:** imagens e PDFs referenciados no Markdown por nomes/caminhos (`![foto](foto.png)`) não são incorporados automaticamente, pois o arquivo Markdown não contém suas bytes. O MyLife conserva uma indicação da referência e avisa na confirmação. Guarde essas imagens em Fotos/Arquivos e adicione-as à nota usando o editor, ou converta tudo para um backup JSON com mídia incorporada. Referências HTTP externas também não são baixadas automaticamente.

## Exportação

- **Dados → Exportar todas as notas (JSON)** cria backup integral com dados e mídias incorporadas. É o formato recomendado para segurança.
- **Abra uma nota → Mais (⋯) → Exportar esta nota (Markdown)** cria um arquivo `.md` editável. Fotos/arquivos incorporados em Data URL podem tornar o Markdown muito grande e a aceitação desses dados varia entre aplicativos; use JSON para backups.

## Compatibilidade e limites

A versão 1.4 preserva a mesma estrutura local IndexedDB (`mylife_data_v2`) e os mesmos campos das notas 1.3.1 e anteriores. A importação JSON continua compatível com os formatos legados. Até 100 arquivos por vez, total máximo 180 MB; Markdown até 10 MB por arquivo, 600 blocos por nota; até 250 imagens e 80 anexos por nota. O arquivo não contém mecanismo de sincronização com iCloud ou com o Notas da Apple. O aplicativo armazena conteúdo localmente no navegador. Teste a restauração em aparelho separado antes de apagar originais.

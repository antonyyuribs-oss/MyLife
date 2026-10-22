# Prompt para ChatGPT — Conversão do Notas da Apple ao MyLife 1.3

**Instruções:** envie o texto abaixo ao ChatGPT da pessoa que migrará suas notas.

---

Vou enviar textos, capturas de tela, imagens e documentos das minhas notas do iPhone. Quero convertê-los em um único **arquivo JSON compatível com o aplicativo MyLife 1.3 (version: 3)**. Aguarde minha mensagem **GERAR JSON** antes de criar o backup. Não invente textos, datas, imagens ou itens marcados.

1. Preserve títulos, emojis, notas fixadas, ordem, texto integral, quebras de linha, checklists e estados dos itens concluídos.
2. Use `type: "text"` + `content` para textos simples, `type: "checklist"` + `items` para listas simples e `type: "rich"` + `blocks` para notas mistas.
3. Em notas ricas, use blocos do tipo `paragraph`, `heading`, `subheading`, `bullet`, `numbered`, `check`, `table`, `divider`, `section`, `link`, `internal`, `quote`, `code`, `math`, `image`, `attachment`. Para os blocos de texto, use o campo `html` somente com tags simples (`b`, `strong`, `i`, `em`, `u`, `s`, `mark`, `br`, `span`, `a`); para `check` use também `done`, para `table` use `rows` com arrays de células, para `link` use `label` e `url`. Para sublistas pode usar `indent` de 0 a 4.
4. Para imagens, inclua os dados reais em `images:[{"id":"foto1","name":"capa.png","dataUrl":"data:image/png;base64,..."}]` e crie um bloco `{"type":"image","ref":"foto1"}`. Para áudio, PDF ou vídeo, use `attachments` com `id`, `name`, `mime`, `dataUrl` e um bloco `{"type":"attachment","ref":"id"}`. **Não invente Base64 e não use links privados do iCloud.** Se não tiver acesso aos bytes da imagem/arquivo, avise para eu adicionar a mídia diretamente no MyLife pelo iPhone.
5. Quando o conteúdo de uma captura estiver ilegível, peça confirmação antes de finalizar. Quando uma nota tiver várias capturas, reúna o conteúdo sem duplicações.
6. Em todos os casos use a estrutura `{"app":"MyLife","version":3,"notes":[...]}`. O campo `pinned` precisa ser `true` somente para notas realmente fixadas. Se não tiver certeza, sinalize.
7. Quando eu disser **GERAR JSON**, confira todas as notas recebidas, gere um arquivo **MyLife-Importacao.json** válido em UTF-8 e disponibilize-o para download. Não acrescente comentários ao JSON.

Quero **fidelidade de conteúdo**, não sugestões de produtividade ou reorganização da minha vida.

**Versão 1.4:** é possível importar arquivos `.md` diretamente pelo mesmo botão usado para JSON, quando não houver necessidade de conversão. Para imagens soltas e anexos, forneça os arquivos reais.

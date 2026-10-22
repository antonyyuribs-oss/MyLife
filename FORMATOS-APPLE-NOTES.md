# MyLife e Notas do iPhone — matriz de compatibilidade

Baseado nos recursos documentados pela Apple em 2026 (iOS 26), para orientar a migração de notas — **não** é promessa de interoperabilidade automática.

| Conteúdo / comportamento do Notas | MyLife | Observação |
|---|---|---|
| Texto simples e parágrafos | Editável | Notas rápidas ou blocos de texto |
| Títulos, subtítulos | Editável | Blocos de título/subtítulo |
| Negrito, itálico, sublinhado, tachado, destaque | Editável | Editor de texto formatado (destaque simples) |
| Listas numeradas, com marcadores, com recuo | Editável | Blocos de lista; recuo até quatro níveis |
| Checklists com marcação individual | Editável | Checklists rápidos e blocos dentro de notas completas |
| Tabelas | Editável | Tabelas em células de texto, até 40 linhas × 10 colunas |
| Linhas divisórias | Editável | Blocos separadores |
| Cabeçalhos recolhíveis | Parcial | Seções de texto recolhíveis; não contêm blocos aninhados |
| Hiperlinks para sites | Editável | Links externos e links em texto |
| Links para outras notas e seções | Parcial | Links entre notas MyLife; sem destino direto em seção |
| Fotografias / capturas de tela / capas de livros | Sim | Arquivos reais incluídos dentro da nota e no JSON; não apenas descrição |
| Documentos escaneados | Preservado | Foto da digitalização ou PDF existente |
| PDFs com assinatura ou marcação | Preservado | PDF anexado; edição/anotação nativa não inclusa |
| Áudio e transcrição | Parcial | Áudio anexado/reproduzido; transcrição guardada como texto |
| Vídeos | Parcial | Arquivo anexado/reproduzido se compatível com Safari (até 18 MB por anexo) |
| Desenhos e escrita manual | Parcial | Pode desenhar e salvar como imagem, sem reconhecer/editar traços |
| Equações | Parcial | Equação como texto, sem cálculos automáticos e gráficos |
| Web previews, mapas e locais compartilhados | Parcial | Guarda URL clicável ou conteúdo como anexo; sem cartões nativos da Apple |
| Etiquetas, pastas, notas fixadas | Parcial | Etiquetas/pastas pesquisáveis; notas fixadas e reordenáveis |
| Subpastas e pastas inteligentes | Não | Pode colocar nomes de pasta no campo; sem hierarquia real |
| Busca de manuscritos ou texto dentro de imagens/PDF | Não | Sem OCR; busca textos, títulos, pastas, tags e anexos por nome |
| Notas bloqueadas, Face ID, colaboração iCloud | Não | Não guarda nem compartilha a segurança da Apple |
| Importação/exportação direta do Notas Apple | Não | Importa/exporta **apenas JSON do MyLife** |

**Aviso:** notas com informações sensíveis não devem ser migradas como se fossem criptografadas no MyLife. Faça backup antes de atualizar. Conserve as originais até conferir todas as informações.

## Importação Markdown direta (v1.4)

Uma única ação em Dados aceita JSON e Markdown. Texto e estruturas Markdown compatíveis são convertidos em blocos. Links para imagens externas ou caminhos locais não contêm a mídia e exigem inserção posterior. Backup JSON continua o formato completo.

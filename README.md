# MyLife — notas e listas pessoais

Aplicativo web instalável para iPhone (PWA), inspirado na interface e nos princípios de simplicidade do Rastro.

## Publicar no GitHub Pages

1. Crie um repositório chamado `MyLife` no GitHub.
2. Envie **todos os arquivos desta pasta** para a raiz do repositório (não apenas `index.html`).
3. Abra **Settings → Pages → Build and deployment**; escolha `Deploy from a branch`, `main` e pasta `/ (root)`.
4. Abra o endereço publicado em **Safari** no iPhone e use **Compartilhar → Adicionar à Tela de Início**.

O aplicativo também abre como `index.html` no computador, mas o funcionamento offline instalável exige HTTPS (como GitHub Pages).

## Funcionalidades

- Abertura mostrando apenas **notas fixadas**; toque no cartão para abrir/editar com salvamento automático.
- Criação de nota textual ou lista de verificação; ícone/emoji e título editáveis.
- Fixar/desafixar, duplicar, arquivar, excluir, buscar, filtrar e ordenar cartões fixados.
- Temas: Nude, Rosé, Lavanda, Vinho, Preto clássico, Creme e Azul acinzentado.
- Layout de cartões confortável/compacto e três tamanhos de texto.
- Exportação/importação de backup JSON. Importação permite adicionar ou substituir, com confirmação.
- Dados locais no navegador do dispositivo, sem conta ou conexão com servidor.

**Importante:** faça backups JSON regulares. Navegador, aparelho ou domínio diferentes não compartilham automaticamente os mesmos dados locais. O MyLife não lê diretamente o Apple Notes/iCloud. Peça ao ChatGPT para converter os textos/checklists existentes para o JSON de importação.

## Formato JSON de importação

O MyLife aceita arquivos que contenham `{"notes":[...]}`. Os campos mínimos são `title` e `content` (nota de texto) ou `title`, `type:"checklist"` e `items` (checklist). Para aparecer na tela inicial, inclua `"pinned":true`.

```json
{
  "app": "MyLife",
  "version": 1,
  "notes": [
    {
      "title": "Rotina de Ouro",
      "emoji": "⚜️",
      "type": "text",
      "content": "05:30 — Devocional\n06:40 — Correr",
      "pinned": true
    },
    {
      "title": "Itens para comprar",
      "emoji": "📌",
      "type": "checklist",
      "pinned": true,
      "items": [
        {"text": "Carregador", "done": true},
        {"text": "Purificador de água", "done": false}
      ]
    }
  ]
}
```

### Limitações previstas

- Notas de texto aceitam quebras de linha, mas **não preservam nativamente** todas as tabelas, imagens, anexos e estilos do Apple Notes.
- A importação é manual por arquivo JSON; não há sincronização com o iCloud.
- Os dados são armazenados no `localStorage`; para volumes grandes ou imagens/anexos seria necessário migrar para IndexedDB.

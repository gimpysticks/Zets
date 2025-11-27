Here is the list of Vimwiki commands and key bindings, reformatted into a clear, categorized table format, with duplicate entries removed.

## 📝 Vimwiki Commands and Key Bindings

The default `<Leader>` key in Vim is typically `\` (backslash). Keys prefixed with `[count]` can operate on a specific wiki if multiple are configured (e.g., `2<Leader>ww` opens the second wiki's index).

---

### Ex Commands (Starting with `:`)

| Command | Meaning |
| :--- | :--- |
| `:Vimwiki2HTML` | Converts the **current** wiki page to an HTML file. |
| `:VimwikiAll2HTML` | Converts **all** wiki pages in the current wiki to HTML. |
| `:VimwikiDiaryIndex` | Opens the diary index page for the current wiki. |
| `:VimwikiMakeDiaryNote` | Creates and opens the diary file for **today**. |
| `:VimwikiRenameFile` | Renames the current wiki file and updates all links pointing to it. |
| `:VimwikiDeleteFile` | Deletes the current wiki file. |
| `:VimwikiIndex` | Opens the index file of the current wiki (use `[count]:VimwikiIndex` for a specific wiki). |
| `:VimwikiTabIndex` | Opens the index file of the current wiki in a new tab. |
| `:VimwikiUISelect` | Lists and allows selection of available wikis (if multiple are configured). |

---

### 🗺️ Wiki Navigation and File Management (Normal Mode)

| Key Binding (Default) | Meaning |
| :--- | :--- |
| `[count]<Leader>ww` | Opens the **index file** of the specified wiki (`<Leader>ww` opens the first). |
| `[count]<Leader>wt` | Opens the index file in a **new tab**. |
| `<Leader>ws` | **Select and open** one of the available wikis. |
| `<Leader>wd` | **Delete** the current wiki file. |
| `<Leader>wr` | **Rename** the current wiki file. |
| `<CR>` (Enter) | **Follow/Create** the wiki link under the cursor. |
| `<Shift-CR>` (Shift-Enter) | Follow/Create the link in a **new split**. |
| `<C-CR>` (Ctrl-Enter) | Follow/Create the link in a **new vertical split**. |
| `<Backspace>` | Go **back** to the previous wiki page in the jump history. |
| `<Tab>` | Find the **next** wiki link on the current page. |
| `<Shift-Tab>` | Find the **previous** wiki link on the current page. |

---

### 📅 Diary Management (Normal Mode)

| Key Binding (Default) | Meaning |
| :--- | :--- |
| `[count]<Leader>wi` | Opens the **diary index file** for the specified wiki. |
| `[count]<Leader>w<Leader>w` | Opens **today's diary file** for the specified wiki. |
| `[count]<Leader>w<Leader>t` | Opens today's diary file in a **new tab**. |
| `<C-Up>` (Ctrl-Up) | Opens the **previous day's** diary file. |
| `<C-Down>` (Ctrl-Down) | Opens the **next day's** diary file. |

---

### ✏️ Editing Shortcuts (Normal/Visual Mode)

| Key Binding (Default) | Context | Meaning |
| :--- | :--- | :--- |
| `<C-Space>` (Ctrl-Space) | Normal Mode | **Toggle** the status of a list item (e.g., `*` to `- [ ]` or `- [X]`). |
| `=` | Normal Mode | **Increase header level** (e.g., `==` to `=`). |
| `-` | Normal Mode | **Decrease header level** (e.g., `==` to `===`). |
| `+` | Normal Mode/Visual | **Create/Decorate links** (wraps text in `[[...]]`). |
| `gll` | Normal Mode | **Increase indent** (level) of a list item. |
| `glh` | Normal Mode | **Decrease indent** (level) of a list item. |

Would you like to know how to customize these key bindings in your Vim configuration?
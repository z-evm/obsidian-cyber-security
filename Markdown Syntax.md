A quick reference for writing Markdown documents.

---

## 🧱 Basic Formatting

**Bold**: `**text**` or `__text__` → **text**  
*Italic*: `*text*` or `_text_` → *text*  
~~Strikethrough~~: `~~text~~` → ~~text~~

---

## 📚 Headings

```markdown
# H1 Heading
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading
```

## 📋 Lists

### ➤ Unordered List
```
- Item 1
- Item 2
  - Nested item
* Also works with asterisks
```

### ➤ Ordered List
```
1. First item
2. Second item
3. Sub-item
```

## 🔗 Links

### ➤ External Links
```
[OpenAI](https://www.openai.com)
```

### ➤ Internal Links (Obsidian)
```
[[Page Name]]
[[Folder/Page Name]]
[[Page Name|Custom Display Text]]
```

## 🖼 Images

```
![Alt text](https://example.com/image.png)
![Alt text](/path/to/image.png)
```

## 🧾 Code

### ➤ Inline Code
```
Use `code` like this.
```

### ➤ Code Block
```
<pre> ```language // code here ``` </pre>

Example:

<pre> ```bash sudo apt update ``` </pre>
```

## 📐 Blockquote
```
> This is a quote.
>> Nested quote.
```

## 📏 Horizontal Line
```
---
```

## ✅ Task Lists
```
- [ ] To do item
- [x] Completed item
```

## 📊 Tables
```
| Header 1 | Header 2 |
|----------|----------|
| Cell A1  | Cell A2  |
| Cell B1  | Cell B2  |
```

## ⌨ Callouts (Obsidian Specific)
```
> [!NOTE]
> This is a note.

> [!WARNING]
> This is a warning block.

> [!TIP]
> Helpful tip.
```

## 🧩 Tags
```
#tagname
```

## 🖇 Footnotes
```
Here's a statement with a footnote.[^1]

[^1]: This is the footnote.
```

## 🔄 Embeds (Obsidian)

### ➤ Embed Note
```
![[Note Name]]
```

### ➤ Embed Section or Block
```
![[Note Name#Heading]]
![[Note Name^blockid]]
```

## 📆 Date Links (Obsidian Daily Notes)

```
[[2025-07-31]]
```

## 📌 Comments (Non-rendered text)

```
<!-- This won't appear in preview -->
```


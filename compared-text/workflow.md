# graph TD

```mermaid
A[使用者輸入比對標題或頁面名] --> B[調用 Wikisource API 取得 wikitext 或純文字]
B --> C[進行 wikitext 清理 / 萃取正文內容]

D[讀取本地 XML-TEI 文本] --> E[使用 lxml / BeautifulSoup 萃取段落、標記、結構]

C --> F[比對模組：斷詞 + TF-IDF / difflib / 相似度]
E --> F

F --> G[產出比對報告：對照段落、差異、相似分數]

G --> H[視覺化介面（Jupyter Notebook / Streamlit / GitHub Pages）]
```

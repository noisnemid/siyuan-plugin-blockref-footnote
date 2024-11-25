## ✨Features

Implement footnotes and remarks function using SiYuan's blockref.

![](https://fastly.jsdelivr.net/gh/Achuan-2/PicBed/assets/%E6%80%9D%E6%BA%90%E7%AC%94%E8%AE%B0%E8%84%9A%E6%B3%A8%E6%8F%92%E4%BB%B62-2024-11-18.gif)

> Using the Tsundoku theme for demonstration, the style of nested blockquote has been optimized.

## 📝CHANGELOG

See [CHANGELOG.md](CHANGELOG.md)


## 📝Usage Instructions

> The minimum required version of Siyuan Notes for this plugin is v3.1.13.

**This plugin supports high customization with the following settings:**

- **Footnote Container Settings**
  - **Footnote Location**: You can set the storage location to be in the current document, a specified document, or a sub-document. The default is `Current Document`.
  - **Document ID of the Specified Document**: When the footnote location is set to "Specified Document", set a document to store all footnotes.
  - **Footnote Container Title in the Current Document**: When the footnote location is set to "Current Document", set the h2 title for storing footnotes.
  - **Footnote Container Title in the Specified Document and Sub-document**: When the footnote location is set to "Specified Document", set the h2 title for storing footnotes. When the footnote location is set to "Sub-document", set the document title for storing footnotes.
  - **Automatically Update Footnote Container Title**: Whether to automatically update the footnote container title to match the set template each time a footnote is created.
- **Footnote Reference Style**: The style of footnote references: "Blockquote" or "Block Link".
- **Footnote Blockquote Anchor Text**: Set the anchor text for footnote references. The default is `[Note]`.
- **Selected Text Style**: You can add styles such as bold, highlight, italic, or underline to the selected text. The default is `None`.
- **Order of Inserting Footnotes**: Ascending or descending order. The default is `Ascending`.
- **Footnote Content Template**: To set up a template for footnotes, it is recommended to use nested quote blocks or a combination of super blocks to store the footnote content. This ensures that the footnote content is contained within a single block. `${selection}` represents the content of the selected text, `${content}` is a placeholder for the footnote content, and `${refID}` is the ID of the block where the selected text is located. And you can use kramdown syntax to define the block styles.
  - **Nested Quote Block Template**

    ```markdown
    >> ${selection} [[↩️]](siyuan://blocks/${refID})
    >> 
    > 💡${content}
    ```

  - **Vertical Super Block Combination Template**

    ```markdown
    {{{row
    > ${selection} [[↩️]](siyuan://blocks/${refID})
    
    ${content}
    }}}
    {: style="border: 2px dashed var(--b3-border-color);"}
    ```


![](https://fastly.jsdelivr.net/gh/Achuan-2/PicBed/assets/PixPin_2024-11-21_08-53-00-2024-11-21.png)

To simultaneously delete footnote references and footnote content, you can right-click on the footnote reference and select `[Plugin -> Delete Footnote]` from the menu.

![](https://fastly.jsdelivr.net/gh/Achuan-2/PicBed/assets/PixPin_2024-11-18_16-24-25-2024-11-18.png)


## 🙏 Acknowledge

- [https://github.com/zxhd863943427/siyuan-plugin-memo](https://github.com/zxhd863943427/siyuan-plugin-memo)
- [https://github.com/siyuan-note/plugin-sample-vite-svelte](https://github.com/siyuan-note/plugin-sample-vite-svelte)

## ❤️ Donation

A poor graduate student in the process of studying. If you like my plugin, feel free to buy me a pack of spicy strips. This will motivate me to continue improving this plugin and developing new ones.

![](https://fastly.jsdelivr.net/gh/Achuan-2/PicBed/assets/20241118182532-2024-11-18.png)
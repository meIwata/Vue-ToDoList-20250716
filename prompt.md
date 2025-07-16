# ToDoItem.vue
請用 Vue 3 寫一個 Todo Checkbox 單檔元件（Single File Component）。
需求如下：

接收兩個 props：
label（必填，類型：String）：待辦事項的文字標籤。
done（選填，類型：Boolean，預設值為 false）：初始完成狀態。
data 中需包含：
isDone：根據 done prop 初始化
id：用 crypto.randomUUID() 生成的唯一字串，供 checkbox 和 label 綁定使用。
template 需渲染：
一個 checkbox input，checked 狀態綁定到 isDone，id 綁定到 id
一個 label，for 屬性綁定到 checkbox 的 id，內容顯示 label prop
script 使用 Vue 的 export default 標準語法。
不需要額外的樣式。

# App.vue
使用todoitem.vue 元件
label 使用範例值 done 預設選取
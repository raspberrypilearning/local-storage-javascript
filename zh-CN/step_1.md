当用户导航到另一个页面（或重新加载当前页面）时，他们所做的任何更改都将丢失。

您可以使用 `localStorage` 属性来保存用户的选择。

`localStorage` 以键值对的形式保存数据。 **键** 是值的“标签”。

### localStorage 方法

- setItem(key, value):
  向 localStorage 添加一个键值对。
  例如：`localStorage.setItem("username", "raspberry")`

- getItem(key):
  检索与指定键关联的值。
  例如：`var username = localStorage.getItem("username")`

- removeItem(key):
  删除与指定键关联的键值对。
  例如：`localStorage.removeItem("username")`

- clear()：
  从 localStorage 中删除所有键值对。
  例如：`localStorage.clear()`

### 页面加载时检查 localStorage

你可以使用 `.addEventListener` 来触发函数以响应页面加载事件。

以下是更多 Web 路径中的漫画角色项目的一个例子：

--- code ---
---
language: js
---

document.addEventListener("DOMContentLoaded", function () {    
  
  if (localStorage.getItem("lightMode") == "true") {
    document.body.classList.toggle("light-mode");
    lightModeSwitch.checked = true;
  }

});
      
--- /code ---

`“DOMContentLoaded”` 是网页准备就绪时触发的 `eventType`。

**提示：** 最好在这里使用 `“DOMContentLoaded”` 而不是 `“load”` 事件类型，后者仅在所有图像都加载完成后才会触发。

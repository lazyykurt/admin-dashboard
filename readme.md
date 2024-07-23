# 重点
[点击浏览](https://lazyykurt.github.io/admin-dashboard/)
## 响应式设计

```css
@media screen and (max-width: 1200px) {...}
```

小屏幕菜单栏，实现思路：

打开的菜单栏：
1. 选中菜单栏 aside 元素；
2. 设置位置，`position: fixed;` `left: 0;` `z-index: 3` (最顶层)
3. 设置大小，`width: 18rem;` `height: 100vh;` `padding-right: var(--card-padding);`
4. 其他美化，...
5. 隐藏，`display: none;`

顶部栏：
1. 选中顶部对于元素；
2. 设置位置为，`position: fixed;` `top: 0;` `left: 0;` `z-index: 2;`
3. 。。。

对于按钮：
 `position: absolute;` `left: 1rem;`

添加JS

## 暗黑模式

主要是添加一个css 暗黑主题的 class 更新css一些变量。
``` css
.dark-theme-variables {
  --color-background: #181a1e;
  --color-white: #202528;
  --color-dark: #edeffd;
  --color-dark-variant: #a3bdcc;
  --color-light: rgba(0, 0, 0, 0.4);
  --box-shadow: 0 2rem 3rem var(--color-light);
}

选择到主题切换按钮 themeToggler，添加点击事件
document.body.classList.toggle('dark-theme-varibales')

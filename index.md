## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/caishucun/redis-csc.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/caishucun/redis-csc.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


## Reids的对象
redis使用对象来表示键和值，每次创建一个键值对的同时会创建两个对象，一个对象用来表示键，一个对象用来表示值。每个对象都是有一个redisObject来表示，其中redisObject的具体结构如下
type struct redisObject{
   //类型
   unsigned type:4;
   //编码
   unsigned encoding:4;
   //指向底层的指针
   void *ptr;
}robj;

### 对象的类型和编码


# 保存文章到cloudflare 

## 功能需求
1. 需要保存标题，内容，以及上传的文件。
2. 文章的标题和内容需要保存到cloudfare的D1数据库中。
3. 文章的图片需要保存到cloudflare的R2存储中。图片的链接保存到D1数据库中。如果没有图片，则不保存。
4. 需要添加一个新的按钮，当点击按钮时，将文章保存到cloudflare的D1数据库中，图片保存到R2存储中。然后弹出一个toast 提示“保存到云端成功。”。

## 文章的表结构
posts
- id: string (主键)
- title: string
- content: text
- created_at: timestamp
- updated_at: timestamp
- image_refs: string[] (存储图片引用R2的url)

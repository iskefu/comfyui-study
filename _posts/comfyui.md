---
completed: true
created: 2024-04-11T00:00:00.000Z
tags:
  - project
Areas: 人工智能
---

# Comfyui

Area:: [[人工智能]]  
Status:: #done

___

## Description
> [!info] 项目描述: 这个项目是关于什么的？目标？特性？学习成果？
>

[[comfyui使用]]
[[comfyui 使用]]
[[StableDiffusionPrompt 提示词]]

---

## Notes
> [!tip] 项目的笔记和文档
```dataviewjs
dv.table(["Doc", "创建时间"],
     dv.pages()
    .where(p => 
      p.file.folder == dv.current().file.folder
    )
    .sort(p => 
      p.created, 'asc'
    )
    .map(p => 
      [p.file.link,  p.created.toFormat('yyyy-MM-dd')]
    )
)
```

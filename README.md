# 网球球格趣测

面向网球爱好者的娱乐型约球习惯测试。用户完成 16 道情境题后获得四维球格代码、倾向百分比和推荐搭子；邀请球友完成测试后可查看双方适配结果。

## 当前功能

- MBTI 趣味参考与轻量边界修正
- 16 道约球和球场情境题
- 四维球格：T/P、A/R、F/S、C/B
- 16 种结果名称与球友总结
- 双端倾向百分比
- 推荐互补搭子
- 带球格参数的分享链接与双人适配分
- 深圳地区「找场备忘录」小程序推广入口

## 权威产品文档

题目、结果文案、计分和匹配规则统一以 `../计划/网球球格趣测最终文案与规则.md` 为准。修改产品逻辑时，应同步更新该文档。

## 开发流程

环境要求：Node.js 22.13 或更高版本。

```bash
npm install
npm run dev
```

提交前统一检查：

```bash
npm run check
```
## 仓库与发布地址

- 源码仓库（开发、测试和构建）：https://github.com/sztenniss/tennis_test
- 对外发布仓库（仅存放 `pages-dist` 静态产物）：https://github.com/sztenniss/tennis-match
- 线上访问地址：https://sztenniss.github.io/tennis-match/

日常代码修改提交到 `tennis_test`。发布时先在源码仓库执行 `npm run build:pages`，再将生成的 `pages-dist/` 内容提交到 `tennis-match`；不要把源码工程直接推送到对外发布仓库。

## 主要文件

- `app/page.tsx`：问答交互、结果、分享及匹配页面
- `app/scoring.ts`：计分、百分比和推荐搭子规则
- `app/profile-copy.ts`：16 种结果名称与总结文案
- `app/globals.css`：移动端页面样式
- `tests/`：单元测试与构建后渲染测试
- `public/miniprogram-code.png`：找场备忘录小程序码
- `.openai/hosting.json`：网站托管项目配置

## 产品声明

本测试用于娱乐和球友交流，不是专业人格或心理评估，仅作趣味参考。


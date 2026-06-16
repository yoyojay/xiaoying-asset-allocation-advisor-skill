# HTML 报告指导

## 文件要求

- 单文件 HTML，内联 CSS。
- 不使用外部 CDN、远程字体、远程图片、追踪脚本。
- 适合本地打开、截图、打印、导出 PDF。
- 客户正式报告使用礼貌称谓，不直呼姓名。
- 不放真实身份证、手机号、地址、完整病历、完整保单号。

## 推荐结构

```html
<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>客户称谓｜报告主题</title>
  <style>
    :root {
      --ink: #1f2b27;
      --muted: #61706a;
      --paper: #f5f2e9;
      --panel: #fffdf8;
      --line: #dce3da;
      --green: #1d5a50;
      --gold: #b58c43;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      color: var(--ink);
      background: var(--paper);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC", "Microsoft YaHei", Arial, sans-serif;
      line-height: 1.75;
    }
    .shell { width: min(1120px, calc(100% - 28px)); margin: 0 auto; padding: 24px 0 64px; }
    header, section, footer {
      background: var(--panel);
      border: 1px solid var(--line);
      border-radius: 18px;
      padding: 26px;
      margin-top: 16px;
    }
    h1, h2, h3 { margin: 0; line-height: 1.16; }
    table { width: 100%; border-collapse: collapse; }
    th, td { border-bottom: 1px solid var(--line); padding: 12px; text-align: left; vertical-align: top; }
    th { color: var(--green); background: #eef5ef; }
    @media print {
      body { background: #fff; }
      header, section, footer { break-inside: avoid; box-shadow: none; }
    }
  </style>
</head>
<body>
  <div class="shell">
    <header>...</header>
    <main>...</main>
    <footer>...</footer>
  </div>
</body>
</html>
```

## 视觉语气

- 适合保险与家庭资产报告：信任、克制、清晰。
- 可使用绿色、金色、米白、浅蓝等稳定色。
- 不使用红黑强冲突、夸张金融交易风、过度营销海报风。
- 表格比大段文字更重要，报告要让客户能扫读。

## 客户报告必备模块

全局版：

- 客户基本信息摘要。
- 一句话结论。
- 资产健康评分卡。
- 现金安全垫。
- 仓位对比。
- 保险功能缺口。
- 调整方案。
- 12个月执行计划。
- 三个风险提醒。
- 关于小莹。
- 免责声明。

单品版：

- 报告性质说明。
- 产品/资产资料提取。
- 同预算或同功能对比。
- 功能价值和风险边界。
- 阶段性建议。
- 需要补充资料。
- 关于小莹。
- 免责声明。

## 关于小莹模块

可放在报告末尾：

```text
我是黄小莹，一名长期深耕保险与家庭风险管理的从业者。近20年的一线客户服务经验，让我越来越确信：真正有价值的保险建议，不是把产品讲得多漂亮，而是把客户当下能做、未来要留、风险不能赌的部分讲清楚。
```

可继续说明：

```text
我习惯先看家庭资产和现金流，再看保障缺口；先看能否承保，再谈产品优劣；先把大风险托住，也不忽略小功能。保险既是保障工具，也是家庭资产安排、收入补充、专款专用和长期责任管理的一部分。
```

## 导出 PDF

如用户要求 PDF：

1. 优先用浏览器打印生成 PDF，保留背景图形。
2. 若环境不支持，说明可直接在浏览器中打开 HTML 后选择“打印 -> 存储为 PDF”。
3. 导出后用 `pdfinfo` 检查页数，用 `pdftotext` 抽查标题和关键段落。

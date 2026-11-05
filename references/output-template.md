# 输出模板

交付默认包含四部分。提示词必须放在单独的代码块中，代码块内不要混入分析、参数或上传说明。

````markdown
[Prompt]
```text
Create a <ratio> <asset type>...

Reference roles:
Image 1 provides <color role>. Do not import its objects or text.
Image 2 provides <scene/style role>. Do not import its brand, watermark, or unrelated subjects.
Image 3 is the sole identity reference for <packaging>.
Image 4, when present, is the sole reference for <contents/alternate angle>.

Composition: medium shot with the complete product occupying about 30%–45% of the frame height, generous foreground and background context, no crop and no extreme product close-up.

<Environment, 4–7 product-relevant styling props, lighting, materials, exact text, constraints. If the product identifies fruit, only that exact fruit may appear; remove every unrelated object.>
```

[上传顺序]

1. Image 1：<色调图>
2. Image 2：<场景图>
3. Image 3：<主产品包装图>
4. Image 4：<可选内容物或另一角度图>

[搭配元素]

| 元素 | 依据 | 画面位置与作用 |
|---|---|---|
| <prop> | <name/flavour/ingredient/use occasion/scene> | <foreground/midground/background + primary/secondary/neutral role> |

[参数建议]

- Model: `gemini-3-pro-image`
- Aspect ratio: `1:1`
- Resolution: `2K` 验证标签，确认后可用 `4K` 定稿
````

没有 Image 4 时，不编造第四张参考图，也不要在上传顺序中留下空的占位项。

搭配元素保持 `4–7` 个。如果产品带水果信息，画面只能出现包装明确对应的一种水果；如果产品没有水果信息，不添加水果。早餐等场景可以使用牛角包、牛奶、黄油等合理配套物，但不得加入与产品或场景无关的装饰。

如果用户只要求提示词，仍至少返回提示词、上传顺序和搭配元素，因为这三项是 `gifzhizuo` 工作流不可分割的交付内容。

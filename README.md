# suppper-research

面向客户开发与首次拜访的公司调研技能。以目标公司事实为主体，快速了解业务、竞争位置和近期变化，再判断合作切入点。

An evidence-based company research skill for prospect discovery and first-meeting preparation. The default output is a concise Simplified Chinese brief, with approximately 80% company research and 20% partnership assessment.

## 核心特点

- 正文默认约 1,200 至 1,800 字，覆盖公司业务、市场位置、近期重点和拜访准备。
- 关键事实附来源，区分事实、判断和待验证假设。
- 检索中英文资料，优先原始披露，检查时间与公司主体。
- 默认结合 LinkWise 数据采集、标注、处理及相关交付服务，可替换为使用者自己的业务背景。
- 合作切入点最多三个，允许结论为信息不足或暂缓投入。

## 安装

将本仓库作为名为 `suppper-research` 的技能目录安装到支持 `SKILL.md` 的工具中。

Codex 使用默认技能目录时，可以执行：

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/terrysnake/suppper-research.git "${CODEX_HOME:-$HOME/.codex}/skills/suppper-research"
```

如果目标目录已经存在，先检查已有内容，避免覆盖。安装后新建会话使用。

其他支持技能的工具可按自身的技能目录规范放置本仓库。未提供技能加载功能的 AI 工具，可读取 `SKILL.md` 正文作为任务指令；联网研究仍需要宿主提供搜索或浏览能力。本技能无运行时依赖，不捆绑搜索 API。

## 使用

最简调用：

```text
使用 $suppper-research 调研【公司名称或官网】，为 LinkWise 的首次客户拜访做准备。
```

指定重点：

```text
使用 $suppper-research 调研【公司名称或官网】。
特别关注：近期 AI 产品布局及数据供应商合作线索。
本次业务：数据采集、标注和质量检查。
```

替换合作方：

```text
使用 $suppper-research 调研【公司名称或官网】。
我方公司：【名称】。
我方业务：【实际提供的服务和已确认的能力】。
用于首次拜访，主体仍然是对目标公司的了解。
```

只有目标公司是必需输入。特别关注的问题、我方能力、已有接触情况均可选。同名公司无法确认时，技能会先澄清主体。

## 输出内容

1. 快速认识这家公司。
2. 业务与市场位置。
3. 最值得关注的三个重点。
4. 与我方的潜在合作。
5. 首次沟通准备。

公开信息可能不足以证明实际采购需求。技能将披露关键缺口，避免把招聘、融资或 AI 布局直接解读为订单机会。无联网能力时，明确说明资料与时效限制。

## 仓库内容

- `SKILL.md`：完整研究流程、证据标准及简报要求。
- `agents/openai.yaml`：技能显示名称和默认调用提示。
- `LICENSE`：MIT 开源许可。

本仓库仅提供通用研究指令与使用示例，不包含客户资料或实际调研报告。LinkWise 为默认业务背景，使用者可通过输入替换；许可不授予商标权。

## License

[MIT](LICENSE) © 2026 terrysnake.

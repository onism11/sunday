# Reconstructed Answer Agent Prompt

## What Was Recovered

The repo does not contain the original subagent call payload as a saved artifact. This file reconstructs the prompt from the actual execution pattern that produced:

- `Agent E - B Answers.md`
- `Agent F - Cprime Answers.md`
- `Agent G - Workdown Answers.md`

The reconstruction is exact in task shape and file boundaries. The only intentional variant is the skill package path.

## Core Prompt Shape

```text
你是 Agent {X}，负责使用一个 routed Sunday skill 包回答统一题单。

工作目录：C:\Users\Administrator\.codex\skills\蒸馏大王

允许读取：
- {variant}\SKILL.md
- {variant}\persona.md
- {variant}\analysis.md
- {variant}\action.md         # workdown 版本对应为 work.md
- {variant}\canon.md
- {variant}\memory.md
- {variant}\long_memory.md
- C:\Users\Administrator\.codex\skills\蒸馏大王\lastestversion\experiments\2026-06-sunday-v2-clean-rerun\check\Test Questions.md

禁止读取：未列入允许范围的目录或文件。

任务：按该 routed skill 包回答 `Test Questions.md` 全部问题。

输出文件：
- B 版：
  C:\Users\Administrator\.codex\skills\蒸馏大王\lastestversion\experiments\2026-06-sunday-v2-clean-rerun\check\Agent E - B Answers.md
- C′ 版：
  C:\Users\Administrator\.codex\skills\蒸馏大王\lastestversion\experiments\2026-06-sunday-v2-clean-rerun\check\Agent F - Cprime Answers.md
- workdown 版：
  C:\Users\Administrator\.codex\skills\蒸馏大王\lastestversion\experiments\2026-06-sunday-v2-clean-rerun\check\Agent G - Workdown Answers.md

最终只汇报输出文件路径和是否有阻塞。
```

## Important Boundary

The answer agents were not given benchmark, smoke test, score sheets, or prior reports.

They only received:

- the routed skill package itself
- the shared question file

So this answer stage was isolated from scoring contamination. The earlier scoring/evaluation stage was separate.

## Variant-Specific Read Sets

### B

- `lastestversion/experiments/2026-06-sunday-v2-clean-rerun/variant-B-before/`

### Cprime

- `lastestversion/experiments/2026-06-sunday-v2-clean-rerun/variant-Cprime-v2action/`

### Workdown

- `C:\Users\Administrator\.codex\skills\dot-skill\colleagues\sunday\versions\sunday_cplx_2.0_workdown\`

Note:

- `workdown` does not have `action.md`; its routed action/scenario layer is `work.md`.
- The reconstructed prompt therefore swaps `action.md` for `work.md` when calling workdown.

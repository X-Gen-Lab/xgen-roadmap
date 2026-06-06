# Planning Model

Rules for keeping the X-Gen-Lab roadmap executable, focused, and easy to maintain.

用于让 X-Gen-Lab 路线图保持可执行、聚焦、可维护的规划规则。

## Planning Layers

| Layer | Purpose | Update Frequency |
| --- | --- | --- |
| Roadmap | Long-term direction and engineering stages | Rarely, when strategy changes |
| Project map | Repository roles, dependencies, and build order | When repositories are added or renamed |
| Milestones | Near-term planning board | Whenever active work changes |
| Decisions | Architecture choices and trade-offs | When an important choice is made |

## Status Model

| Status | Definition | Exit Condition |
| --- | --- | --- |
| Active | Current planning or implementation focus | Baseline deliverable is complete |
| Planned | Accepted work that is not yet the main focus | Promoted to Active or Deferred |
| Backlog | Useful idea that still needs validation | Promoted to Planned or removed |
| Deferred | Valid work intentionally postponed | Reconsidered after blocking dependency is complete |

Only a small number of items should be `Active` at the same time. For this roadmap, the recommended limit is three active items across all tracks.

同一时间 `Active` 项不宜过多。当前路线图建议所有方向合计最多保留三个 Active 项。

## Maturity Gates

| Gate | Meaning | Evidence |
| --- | --- | --- |
| G0 Idea | Direction is named | Short description exists |
| G1 Scoped | Boundaries are clear | README or planning doc defines scope and non-scope |
| G2 Usable | Another repository can depend on it | Spec, skeleton, sample, or demo exists |
| G3 Validated | Behavior has been checked | Build, test, render, or review evidence exists |
| G4 Integrated | Used by a downstream project | Dependency is exercised in another repository |

最优实现不是一次性把所有仓库铺开，而是让每个仓库逐步通过 G1 到 G4。

## Decision Rules

- Prefer reusable foundations before visible demos.
- Prefer clear repository boundaries over broad mixed-purpose repositories.
- Promote a project to `Active` only when its next deliverable is known.
- Do not start AI experiments until the robot platform has a stable control and communication boundary.
- Keep dates out of the long-term roadmap unless there is an external deadline.

## Review Checklist

Use this checklist before changing roadmap status or creating a new repository:

| Question | Expected Answer |
| --- | --- |
| What problem does this repository solve? | One clear sentence |
| Which roadmap stage owns it? | One primary stage |
| What is the first usable artifact? | Spec, skeleton, sample, or demo |
| What depends on it? | At least one downstream project or learning path |
| How is it validated? | Build, test, render, review, or hardware check |

这个检查表可以防止路线图变成项目名称堆叠，而是保持每个仓库都有清晰的工程价值。

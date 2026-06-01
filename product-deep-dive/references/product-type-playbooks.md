# Product-Type Playbooks

Use this reference to adapt the product teardown to different AI product categories. These playbooks should sharpen questions, evaluation indicators, technical inference, and product-manager insights.

## How to Use

1. Identify the closest product type from the list.
2. If the product spans multiple types, choose one primary playbook and one secondary playbook.
3. Rewrite high-value questions using the playbook, but do not paste the playbook mechanically.
4. Adjust section 2 evaluation indicators using the product-type-specific risks.
5. Adjust technical/model inference using the likely architecture of that product type.

## AI 陪伴 / 角色互动

### What to Notice

- Role setting and personality consistency.
- Emotional response quality.
- Memory and continuity across sessions.
- Content boundaries and safety.
- Retention loop: daily check-in, intimacy growth, story progression, relationship assets.
- Monetization trigger: premium characters, messages, voice, image, memory, advanced scenarios.

### High-Value Question Seeds

- What emotional job does the product own: companionship, fantasy, roleplay, therapy-like support, entertainment, or social replacement?
- How does the product create continuity so the user has a reason to return?
- Does monetization strengthen immersion or interrupt it?
- How does the product handle unsafe dependency, sexual content, minors, harassment, or emotional manipulation risk?
- Which part is hard to copy: character IP, community, memory data, content pipeline, model tuning, distribution, or payment design?

### Evaluation Emphasis

- 端到端: conversation satisfaction, scenario completion, emotional usefulness.
- 过程能力: role consistency, memory recall, turn-by-turn context, safety handling.
- 综合评测: retention, monetization ethics, safety, long-term data moat.

### Technical Inference Focus

- Persona prompt stack.
- Conversation memory and summarization.
- Safety classifiers and moderation.
- Character asset library.
- Text/voice/image model orchestration.

## AI Agent / Workflow

### What to Notice

- Task decomposition.
- Planning and replanning.
- Tool use and permission model.
- State management.
- Recovery from partial failure.
- Human-in-the-loop checkpoints.
- Transparency of process and decisions.

### High-Value Question Seeds

- What part of the user's work is automated, and what remains intentionally human-controlled?
- Does the product expose enough process for trust without overwhelming the user?
- Where does the agent ask for permission, and where does it act autonomously?
- What state objects must exist behind the scenes?
- Does failure recovery feel designed or accidental?

### Evaluation Emphasis

- 端到端: task completion and final deliverable quality.
- 过程能力: planning, tool selection, execution trace, recovery.
- 综合评测: production readiness, security, cost, auditability, integration depth.

### Technical Inference Focus

- Single-agent vs multi-agent.
- Workflow engine vs autonomous loop.
- Tool registry and permission checks.
- Context window and memory strategy.
- RAG and external data grounding.

## AI 视频 / 图片生成

### What to Notice

- Input modality: prompt, image, video, storyboard, template, asset library.
- Output controllability.
- Style consistency.
- Editing loop.
- Asset management.
- Generation cost and wait time.
- Copyright and commercial usage risk.

### High-Value Question Seeds

- Is the product selling generation quality, workflow speed, creative control, or distribution?
- Where is the Aha Moment: first generation, first edit, first reusable style, or first publishable asset?
- How does the product help users recover from bad generations?
- Does it support professional iteration or only one-off demos?
- Which part of the workflow creates switching costs?

### Evaluation Emphasis

- 端到端: final media quality, prompt following, publishability.
- 过程能力: editability, consistency, iteration speed, asset reuse.
- 综合评测: cost, copyright, safety, professional workflow fit.

### Technical Inference Focus

- Text-to-image/video models.
- Image/video reference conditioning.
- Style libraries and LoRA-like concepts.
- Queueing and generation pipeline.
- Post-processing and upscaling.

## AI 搜索 / 研究

### What to Notice

- Source quality and freshness.
- Citation traceability.
- Synthesis quality.
- Bias and hallucination handling.
- Query decomposition.
- Report generation.
- Export and collaboration.

### High-Value Question Seeds

- Does the product answer, research, summarize, compare, or decide?
- Are sources transparent enough for serious work?
- How does the product handle conflicting sources?
- Does it distinguish fact from interpretation?
- What makes it better than a general chatbot plus web search?

### Evaluation Emphasis

- 端到端: answer usefulness and decision support.
- 过程能力: search path, citation quality, source comparison, fact checking.
- 综合评测: trust, freshness, repeatability, team knowledge reuse.

### Technical Inference Focus

- Search API / crawler / retrieval layer.
- RAG and citation alignment.
- Source ranking.
- Query expansion and decomposition.
- Report synthesis pipeline.

## AI 编程 / DevTool

### What to Notice

- Repository understanding.
- Context retrieval.
- Code editing scope control.
- Test generation and execution.
- Debugging workflow.
- Developer trust and reviewability.
- IDE/CLI/Git integration.

### High-Value Question Seeds

- Does the product help with code completion, repo-level change, debugging, planning, review, or deployment?
- How does it decide what files to read before editing?
- Does it keep the developer in control of risky operations?
- Can it verify its work with tests?
- Where does it reduce cognitive load rather than just write code faster?

### Evaluation Emphasis

- 端到端: task implemented or bug fixed.
- 过程能力: context gathering, plan quality, edit discipline, testing, recovery.
- 综合评测: maintainability, security, team workflow, trust.

### Technical Inference Focus

- Codebase indexing.
- Retrieval and file selection.
- Tool sandboxing.
- Patch generation.
- Test and terminal integration.
- Git safety.

## Product-Type Selection Heuristic

| Signal | Likely Playbook |
|---|---|
| Relationship, character, chat, memory, intimacy | AI 陪伴 / 角色互动 |
| Tools, tasks, automation, workflow, permissions | AI Agent / Workflow |
| Image, video, style, storyboard, generation queue | AI 视频 / 图片生成 |
| Sources, citations, report, research, web answers | AI 搜索 / 研究 |
| Repo, code, IDE, CLI, tests, bug fix | AI 编程 / DevTool |

If none match, treat the product as `通用 AI 应用` and borrow the closest two playbooks.

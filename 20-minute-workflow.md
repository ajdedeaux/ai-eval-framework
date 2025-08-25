# 20-Minute Workflow
**Fast execution of systematic AI research (after initial setup)**

## Prerequisites
This workflow assumes you've already completed the discovery process:
- ✅ Problem clearly defined through alignment phase
- ✅ Master research prompt created and tested
- ✅ Research scope narrowed to specific target
- ✅ Evidence standards established

**If you haven't done this setup, see [`methodology.md`](methodology.md) for the complete 60-minute discovery process.**

---

## Pre-Work (2 minutes)

### Define Today's Research Target
Fill out these specific parameters:

```
Domain: [Your industry/field]
Subject: [Specific thing to research]
Scope: [What you need to know]
Business Need: [Why this matters now]
```

**Example from Purple Case:**
```
Domain: Mattress specifications
Subject: Purple RestorePlus Cool Touch 13" Queen
Scope: Coil count, construction layers, exclusivity verification
Business Need: Customer asking technical questions not in training materials
```

### Set Up Workspace
- Open 4 browser tabs: ChatGPT, Claude, Gemini, Perplexity
- Have your master research prompt ready (customized from `research-prompt.md`)
- Create document for collecting outputs
- Start timer

---

## Phase 1: Multi-LLM Research Deployment (8 minutes)

### Deploy Your Master Prompt (2 minutes per system)

Run your pre-built research prompt across all systems simultaneously:

**All 4 Systems - Parallel Execution:**
1. Paste your customized master prompt into each LLM
2. Ensure JSON output format is being generated
3. Copy each result to collection document as received
4. Label outputs clearly (ChatGPT/Claude/Gemini/Perplexity)

**Quality Check**: Each output should have:
- JSON structure
- Evidence sources with URLs
- Confidence levels (High/Medium/Low)
- Technical specifications attempted

**Time Check: 8 minutes elapsed**

---

## Phase 2: Cross-Analysis (5 minutes)

### Find Consensus and Conflicts

Return to your preferred LLM with this analysis prompt:

```
I have research outputs from 4 different AI systems on [YOUR SUBJECT].
Analyze for consensus and conflicts:

1. CONSENSUS: What facts do 3+ systems agree on?
2. CONFLICTS: What information differs between systems?
3. EVIDENCE QUALITY: Which sources are most authoritative?
4. CONFIDENCE: What can we state with certainty?

[PASTE ALL 4 OUTPUTS]

Focus on HIGH confidence consensus for customer-facing use.
```

**Purple Case Example Output:**
- **Consensus**: 3" GelFlex Grid (all 4 systems)
- **Conflict**: Coil count varies 789-892
- **Best Evidence**: Purple.com official specs
- **High Confidence**: Height, Grid thickness, exclusivity

**Time Check: 13 minutes elapsed**

---

## Phase 3: Validation and Clean Output (7 minutes)

### Generate Deployment-Ready Data

#### Quick Validation (3 minutes)
Using the validation framework:

```
Validate this synthesized research for deployment:
- Customer-safe claims (HIGH confidence only)
- Technical accuracy (consensus findings)
- Evidence chain (source documentation)

[PASTE CONSENSUS FINDINGS]

Mark anything below HIGH confidence as "requires verification"
```

#### Final Output Generation (4 minutes)
Create clean, structured output:

```
Generate final JSON output with:
- Customer-safe facts (HIGH confidence consensus only)
- Requires verification (MEDIUM confidence items)
- Missing information (identified gaps)
- Evidence trail (source URLs for all claims)

Use the structure from example-output.json
```

**Time Check: 20 minutes total**

---

## What This Workflow Delivers

### In 20 Minutes You Get:
- Consensus findings from 4 AI systems
- Evidence-graded specifications
- Customer-ready information separated from internal-use
- Full source documentation
- Structured JSON for future automation

### Compared to Manual Research (3 hours):
- Same accuracy (95%+ match)
- Better documentation (every claim sourced)
- Systematic validation (not subjective)
- Repeatable process (same quality every time)

---

## When to Use Full 60-Minute Process Instead

Use the complete methodology from [`methodology.md`](methodology.md) when:
- First time researching a new domain
- Creating new master prompts
- Training team members
- Establishing evidence standards
- Discovering optimal research approach

---

## Quality Checkpoints

### 8-Minute Mark (After Research)
- [ ] Have 4 JSON outputs collected
- [ ] Each has evidence documentation
- [ ] Technical specs attempted by all systems

### 13-Minute Mark (After Analysis)
- [ ] Consensus findings identified
- [ ] Conflicts documented
- [ ] Confidence levels assigned

### 20-Minute Mark (Final)
- [ ] Customer-safe facts separated
- [ ] Evidence chain complete
- [ ] Ready for deployment

---

## Troubleshooting Quick Reference

| If This Happens | Do This |
|-----------------|---------|
| No JSON from some LLMs | Add "Return ONLY valid JSON" to prompt |
| No consensus found | Focus on official sources only |
| Taking >20 minutes | Narrow scope to critical specs |
| Poor evidence quality | Explicitly require URLs for all claims |

---

## Scaling This Workflow

### For Daily Use:
- Save domain-specific prompts
- Build library of validated outputs
- Track which LLMs perform best for your domain
- Refine evidence standards based on results

### For Team Adoption:
- Share master prompts in team repository
- Establish consensus thresholds (3/4 systems = valid)
- Create domain-specific validation criteria
- Document successful research examples

**Remember**: This 20-minute workflow is for execution after you've done the groundwork. The first research in any new domain should use the full 60-minute methodology to establish your approach.

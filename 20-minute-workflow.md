# 20-Minute Workflow
**Step-by-step execution of systematic AI evaluation**

## Pre-Work (5 minutes)

### Define Your Research Target
Fill out these parameters before starting:

```
Domain: [Your industry/field]
Subject: [Specific thing to research]
Scope: [What you need to know]
Business Need: [Why this matters]
```

**Example:**
```
Domain: SaaS project management tools
Subject: Asana Enterprise features
Scope: Pricing, user limits, integration capabilities
Business Need: Vendor evaluation for 500-person team
```

### Set Up Workspace
- Open 4 browser tabs: ChatGPT, Claude, Gemini, Perplexity
- Copy your customized research prompt from `research-prompt.md`
- Create document to collect outputs
- Note start time

## Phase 1: Multi-LLM Research Deployment (8 minutes)

### Deploy Research Prompt (2 minutes per system)

**System 1: ChatGPT**
1. Paste customized research prompt
2. Wait for complete JSON output
3. Copy result to collection document
4. Label as "ChatGPT Output"

**System 2: Claude**
1. Paste same prompt
2. Wait for complete output
3. Copy result to collection document  
4. Label as "Claude Output"

**System 3: Gemini** 
1. Paste same prompt
2. Wait for complete output
3. Copy result to collection document
4. Label as "Gemini Output"

**System 4: Perplexity**
1. Paste same prompt
2. Wait for complete output
3. Copy result to collection document
4. Label as "Perplexity Output"

**Time Check: 8 minutes elapsed**

## Phase 2: Cross-Analysis (5 minutes)

### Quick Correlation Check
Return to ChatGPT (or your preferred system) with this prompt:

```
I have research outputs from 4 different AI systems on the same topic. 
I need you to analyze them for:

1. Common findings (information all systems agree on)
2. Discrepancies (conflicting information)  
3. Unique insights (valuable info from only one system)
4. Source quality assessment
5. Overall confidence in findings

Here are the outputs:

[PASTE ALL 4 OUTPUTS HERE]

Provide analysis in this format:
- CONSENSUS FINDINGS: [Items all systems agree on]
- DISCREPANCIES: [Conflicting information requiring resolution]
- UNIQUE INSIGHTS: [Valuable single-system information]  
- SOURCE QUALITY: [Assessment of evidence documentation]
- CONFIDENCE ASSESSMENT: [Overall reliability evaluation]
```

**Time Check: 13 minutes elapsed**

## Phase 3: Validation and Clean Output (7 minutes)

### Run Validation Check (3 minutes)
Using same system, paste validation prompt from `validation-prompt.md` with your research synthesis:

```
[PASTE VALIDATION PROMPT]

EXECUTE VALIDATION FOR: [PASTE YOUR SYNTHESIZED RESEARCH]
```

### Generate Final Output (4 minutes)
Based on validation results, create clean final version:

```
Based on the validation results, create the final research output that:

1. Uses only HIGH confidence information for customer-facing claims
2. Properly separates MEDIUM confidence items as "requires verification"
3. Excludes LOW confidence information
4. Includes complete source documentation
5. Provides deployment-ready specifications

Structure as JSON following the original research format, but include only validated, deployment-ready information.
```

**Time Check: 20 minutes total**

## Quality Checkpoints

### After Multi-LLM Research (8-minute mark)
- [ ] Have 4 complete outputs in JSON format
- [ ] All systems addressed your specific research scope
- [ ] Technical specifications present (even if some marked as unavailable)
- [ ] Source documentation included in each output

### After Cross-Analysis (13-minute mark)  
- [ ] Clear consensus on key facts identified
- [ ] Conflicting information flagged for attention
- [ ] Source quality assessed across all outputs
- [ ] Confidence levels make sense based on source types

### After Validation (20-minute mark)
- [ ] Final output passes structural compliance
- [ ] Customer-safe information clearly separated
- [ ] All claims have appropriate source documentation
- [ ] Ready for business deployment without additional verification

## Common Time Extensions

### If Analysis Takes Longer (15-25 minutes total)
**Cause**: Complex discrepancies between system outputs
**Solution**: Focus on consensus findings first, flag discrepancies for future research

### If Validation Fails (25-35 minutes total)
**Cause**: Poor source quality or structural issues
**Solution**: Return to highest-quality single output, supplement with targeted additional research

### If Scope Too Broad (30+ minutes total)
**Cause**: Research target not specific enough
**Solution**: Narrow scope, focus on core business need, repeat process

## Success Indicators

### High-Quality 20-Minute Output
- Consensus findings from multiple AI systems
- High confidence sources for key claims
- Structured, deployment-ready information
- Clear action items and business insights
- Complete audit trail of sources and methodology

### Ready for Business Use
- Customer-facing information verified through multiple sources  
- Technical specifications include confidence levels
- Competitive context based on factual differences
- Missing information clearly identified
- Recommendations actionable and specific

## Scaling Tips

### For Regular Research Needs
- Save customized prompts for your domain
- Create templates for common research types
- Build library of validated outputs for reference
- Track success metrics (time, accuracy, business impact)

### For Team Implementation  
- Standardize on prompt templates
- Create shared validation criteria
- Document domain-specific source hierarchies
- Establish review process for customer-facing materials

This workflow transforms ad hoc AI research into systematic, measurable quality control that scales across teams and use cases.

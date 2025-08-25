# Troubleshooting Guide
**Common issues and solutions for the AI Evaluation Framework**

## Quick Reference
Your 5-phase process should take ~60 minutes total. If it's taking longer or failing, use this guide.

---

## Phase 1: Problem Alignment Issues (Target: 5 minutes)

### Issue: Can't Get AI to Understand Your Needs
**Symptoms:**
- Generic responses instead of specific research requirements
- AI keeps giving advice instead of understanding your research target
- No clear alignment on what data you need

**Solutions:**
1. **Be Extremely Specific**: "I need coil counts, layer thickness, and warranty details for Purple RestorePlus Cool Touch Queen size"
2. **State the Business Problem**: "Our training materials lack technical specifications customers ask about"
3. **Confirm Alignment**: "Before we proceed, confirm you understand I need [specific list]"

**What Worked in Purple Case:**
```
"I need comprehensive specifications for Purple Restore Cool Touch models. 
Our training materials are incomplete and I can't find reliable coil counts, 
construction details, or verification that this is truly Mattress Firm exclusive."
```

---

## Phase 2: Master Prompt Creation Issues (Target: 10 minutes)

### Issue: Prompt Not Producing Structured Output
**Symptoms:**
- Getting narrative responses instead of JSON
- Missing evidence documentation
- No confidence levels assigned

**Solutions:**
1. **Enforce AI-First Structure**: Add "Output must be valid JSON that other AI systems can process"
2. **Provide Example Structure**: Include a sample JSON snippet in your prompt
3. **Explicit Requirements**: "Every claim must have: source, URL, confidence level (High/Medium/Low)"

**Key Elements Your Prompt Must Include:**
- JSON output structure
- Evidence documentation requirements
- Confidence level definitions
- "AI-first" specification

---

## Phase 3: Multi-LLM Research Issues (Target: 15 minutes)

### Issue: Different LLMs Giving Incompatible Outputs
**Symptoms:**
- ChatGPT gives JSON, Claude gives markdown
- Gemini truncates responses
- Perplexity includes too much commentary

**Solutions:**
1. **Add Format Enforcement**: "Return ONLY valid JSON with no markdown formatting or commentary"
2. **Simplify if Needed**: If Gemini/Perplexity struggle, focus on ChatGPT + Claude
3. **Clean During Collection**: Strip markdown/comments when copying to collection document

### Issue: Not Getting Evidence/Sources
**Symptoms:**
- Claims without URLs
- No source documentation
- Generic "according to sources" language

**Solutions:**
1. **Explicit Source Requirement**: "For EVERY technical specification, provide the exact source URL"
2. **Define Evidence Standards**: "HIGH = official brand sites, MEDIUM = major retailers, LOW = forums"
3. **Reject Unsourced Claims**: Tell AI to mark as "Not Available" rather than guess

---

## Phase 4: Cross-Analysis Issues (Target: 20 minutes)

### Issue: Can't Find Consensus Across Systems
**Symptoms:**
- All 4 LLMs provide different specifications
- No clear pattern in outputs
- Conflicting technical details

**Solutions:**
1. **Focus on Overlap**: "Show me ONLY the specifications that at least 3 systems agree on"
2. **Apply Confidence Hierarchy**: Trust official sources over databases over forums
3. **Document Discrepancies**: Mark conflicting info as "requires verification"

**Cross-Analysis Prompt That Works:**
```
I have research outputs from 4 different AI systems on the same topic. 
Identify:
1. Common findings (what all systems agree on)
2. Discrepancies (conflicting information)
3. Source quality assessment

Focus on consensus findings with HIGH confidence sources.
```

---

## Phase 5: Clean Output Issues (Target: 10 minutes)

### Issue: Output Not Deployment-Ready
**Symptoms:**
- Mix of verified and unverified claims
- No clear customer-safe vs internal separation
- Missing business context

**Solutions:**
1. **Apply Deployment Filter**: "Generate final output using ONLY High confidence information for customer-facing claims"
2. **Separate by Use Case**: Create distinct sections for customer-safe vs requires-verification
3. **Add Business Context**: Include competitive positioning and SME insights

**Deployment Readiness Checklist:**
```json
"deployment_readiness": {
  "customer_safe_facts": ["Only HIGH confidence claims"],
  "requires_verification": ["MEDIUM confidence items"],
  "missing_information": ["Identified gaps"]
}
```

---

## Common Framework Failures

### Total Time Exceeds 60 Minutes
**Diagnosis**: Usually stuck in Phase 1 (alignment) or Phase 4 (analysis)
**Fix**: Time-box each phase. Move forward with "good enough" rather than perfect.

### No Consensus After Multi-LLM Research
**Diagnosis**: Research target too broad or poorly defined
**Fix**: Narrow scope to specific model/size, focus on critical specs only

### Evidence Quality Too Low
**Diagnosis**: Searching wrong sources or accepting unverified claims
**Fix**: Explicitly require official sources, reject forum/review site data

### JSON Structure Broken
**Diagnosis**: LLMs adding commentary or markdown formatting
**Fix**: Add "Return ONLY valid JSON" and clean manually if needed

---

## Quick Fixes by Symptom

| Symptom | Phase | Fix |
|---------|-------|-----|
| "AI doesn't understand" | 1 | Be more specific about exact data needs |
| "No JSON output" | 2 | Add JSON example to prompt |
| "Missing sources" | 3 | Require URL for every claim |
| "Can't find consensus" | 4 | Focus on HIGH confidence only |
| "Not customer-ready" | 5 | Separate by confidence level |

---

## The 80/20 Rule

**Focus on what matters:**
- Get consensus on critical specs (height, key technology, warranty)
- Don't chase perfect accuracy on non-critical details
- HIGH confidence for customer-facing, MEDIUM acceptable for internal
- Missing data is better than wrong data

**From the Purple Case:**
- Critical: 3" Grid, 13" height, Mattress Firm exclusive
- Nice-to-have: Exact coil count, weight specifications
- Acceptable gaps: Detailed material composition

---

## If All Else Fails

1. **Simplify Target**: One product, one size, core specs only
2. **Reduce LLM Count**: Use just ChatGPT + Claude
3. **Lower Evidence Bar**: Accept MEDIUM confidence for non-critical specs
4. **Manual Verification**: Check 2-3 key claims yourself
5. **Document Limitations**: Note what couldn't be verified

Remember: The goal is 80% time savings with 95% accuracy. Perfect is the enemy of done.

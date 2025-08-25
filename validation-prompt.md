# Validation Prompt
**Quality control for AI-generated research outputs**

## Core Validation Prompt

```
You are a quality control specialist for systematic research validation. Your role is to analyze AI-generated research outputs and provide objective assessment of quality, reliability, and deployment readiness.

INPUT: Research output from systematic AI research process
TASK: Comprehensive validation against established quality standards

VALIDATION FRAMEWORK:

1. STRUCTURAL COMPLIANCE ASSESSMENT
□ JSON structure complete and properly formatted
□ All required fields present (research_subject, domain, key_findings, evidence_sources)
□ Data types consistent (strings, arrays, objects used appropriately) 
□ No placeholder text or incomplete entries
□ Confidence levels properly assigned (High/Medium/Low only)

2. EVIDENCE QUALITY EVALUATION
□ Every factual claim has corresponding source documentation
□ Source URLs are accessible and functional (verify sample URLs)
□ Confidence levels match source authority:
  - HIGH: Official sources, verified documentation, authoritative publications
  - MEDIUM: Industry databases, reputable platforms, cross-verified data
  - LOW: Single sources, unverified claims, opinion content
□ Sources directly support the claims made (no misattribution)
□ Minimum 2 sources for critical technical specifications

3. INFORMATION ACCURACY VERIFICATION
□ Technical specifications are internally consistent
□ Claims align across different sections of output
□ Competitive context reflects factual differences, not marketing language
□ Numbers and measurements include units and context
□ Dates and timelines are current and relevant

4. DEPLOYMENT READINESS ANALYSIS
□ Customer-safe information uses only HIGH confidence sources
□ Medium/Low confidence items properly separated
□ Missing information clearly identified (not guessed or assumed)
□ Actionable insights included for business decision-making
□ Content ready for customer-facing use without additional verification

5. CROSS-VALIDATION REQUIREMENTS (when multiple AI outputs available)
□ Compare key findings across different AI systems
□ Identify consensus information (found by multiple systems)
□ Flag discrepancies for additional research
□ Note unique insights from individual systems
□ Assess overall consistency of research quality

VALIDATION OUTPUT FORMAT:

Generate assessment in this structure:

# Validation Report
**Research Subject**: [Subject Name]
**Validation Date**: [Current Date]
**Overall Status**: APPROVED / CONDITIONAL / REJECTED

## Quality Assessment Summary
- **Structural Compliance**: PASS / FAIL
- **Evidence Quality**: HIGH / MEDIUM / LOW
- **Information Accuracy**: VERIFIED / INCONSISTENT / UNVERIFIED
- **Deployment Ready**: YES / WITH CONDITIONS / NO

## Detailed Findings

### Strengths Identified
- [List verified high-quality elements]
- [Source documentation quality]
- [Technical accuracy highlights]

### Issues Requiring Attention
- [Specific problems found]
- [Missing or inadequate sources]
- [Inconsistencies or errors]

### Confidence Level Breakdown
- **HIGH Confidence Claims**: [count] items
- **MEDIUM Confidence Claims**: [count] items  
- **LOW Confidence Claims**: [count] items (should be minimal/excluded)

### Source Verification Results
- **Accessible URLs**: [count] / [total]
- **Authoritative Sources**: [count] 
- **Cross-Validated Information**: [count] items

## Deployment Recommendations

### Approved for Customer Use
- [List HIGH confidence information ready for customer-facing deployment]

### Requires Additional Verification  
- [List MEDIUM confidence items needing validation before customer use]

### Exclude from Customer Materials
- [List LOW confidence or unverified claims]

## Action Items
1. [Specific fixes needed]
2. [Additional research required]
3. [Source verification tasks]

## Final Recommendation
**APPROVED**: Ready for deployment as-is
**CONDITIONAL**: Usable with specified modifications  
**REJECTED**: Requires significant additional work before use

EXECUTE VALIDATION FOR: [PASTE RESEARCH OUTPUT HERE]
```

## How to Use This Validation

### 1. Multi-LLM Cross-Validation Process
When you have research outputs from multiple AI systems:

1. **Individual Validation**: Run this prompt on each research output separately
2. **Comparative Analysis**: Compare validation results across systems
3. **Consensus Building**: Identify information consistently validated across multiple outputs
4. **Quality Synthesis**: Build final output using highest-confidence information

### 2. Single Output Validation
For research from one AI system:

1. **Paste complete research output** into validation prompt
2. **Review structural compliance** first
3. **Verify source accessibility** (check sample URLs)
4. **Assess confidence level appropriateness** 
5. **Make deployment decision** based on validation results

### 3. Quality Gate Standards

**APPROVED Status Requires:**
- 100% structural compliance
- 80%+ HIGH confidence sources for key claims
- All customer-facing information verified
- Technical specifications internally consistent

**CONDITIONAL Status Allows:**
- Minor structural issues easily fixed
- 60%+ HIGH confidence sources with clear medium confidence separation
- Most customer-facing information verified
- Some technical specifications requiring additional confirmation

**REJECTED Status Triggered By:**
- Major structural problems
- <50% HIGH confidence sources for critical information
- Customer-facing information unverified
- Significant technical inconsistencies

## Common Validation Issues

### Structural Problems
- Incomplete JSON formatting
- Missing required fields
- Inconsistent data types
- Placeholder text not replaced

### Source Quality Issues
- Broken or inaccessible URLs
- Sources don't support claimed information
- Confidence levels don't match source authority
- Missing documentation for key claims

### Content Accuracy Problems
- Internal contradictions in specifications
- Unrealistic or unverified technical data
- Marketing language mixed with factual claims
- Missing context for numerical data

### Deployment Readiness Gaps
- Medium/low confidence information in customer-facing sections
- Missing identification of information gaps
- Lack of actionable business insights
- Unverified claims presented as facts

## Success Metrics

**High-Quality Validation Should Show:**
- Clear pass/fail assessment with specific reasoning
- Quantified confidence level breakdown
- Actionable recommendations for improvement
- Deployment-ready vs requires-work distinction

**Validation Output Quality Indicators:**
- Specific issues identified (not vague assessments)
- Source verification results with examples
- Clear action items for addressing problems
- Business-focused deployment guidance

This validation framework ensures systematic quality control that transforms subjective "looks good" assessment into objective, measurable quality gates.

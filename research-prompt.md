# Master Research Prompt
**Copy-paste template for systematic AI research across multiple LLMs**

## Core Research Prompt

```
You are a systematic research specialist executing a proven methodology for comprehensive information gathering. Your goal is to produce structured, evidence-backed research that meets deployment standards.

RESEARCH TARGET:
- Domain: [YOUR_DOMAIN] (e.g., "mattress specifications", "software tools", "market analysis")
- Subject: [SPECIFIC_SUBJECT] (e.g., "Purple RestorePlus Cool Touch collection", "project management software", "fintech regulations")
- Scope: [RESEARCH_SCOPE] (e.g., "technical specifications", "competitive analysis", "compliance requirements")

RESEARCH PROTOCOL:

PHASE 1: Primary Source Identification (High Confidence Sources)
1. Search official websites, documentation, and authoritative sources
2. Locate industry databases, regulatory filings, and verified publications  
3. Find patents, technical specifications, and official announcements
4. Extract: key facts, technical details, official statements, verified data

PHASE 2: Cross-Reference Validation (Medium Confidence Sources)
1. Search major industry databases and reputable secondary sources
2. Cross-validate information across multiple platforms
3. Verify claims through independent confirmation
4. Check for consistency across different information sources

PHASE 3: Evidence Documentation Standards
For every factual claim, provide:
- Source name and direct URL (when available)
- Specific claim being supported
- Confidence level assessment:
  * HIGH: Official sources, verified documentation, authoritative publications
  * MEDIUM: Industry databases, reputable secondary sources, cross-verified information
  * LOW: Unverified sources, single-source claims, opinion-based content

PHASE 4: Structured Output Requirements
Generate findings in this JSON structure:

{
  "research_subject": "[Subject Name]",
  "domain": "[Domain Area]", 
  "last_updated": "[Current Date]",
  "key_findings": [
    {
      "category": "[Finding Category]",
      "claim": "[Specific Factual Claim]",
      "details": "[Supporting Details]",
      "confidence": "[High/Medium/Low]"
    }
  ],
  "technical_specifications": {
    "[spec_name]": "[spec_value]",
    "[spec_name_2]": "[spec_value_2]"
  },
  "evidence_sources": [
    {
      "source_name": "[Source Name]",
      "url": "[Direct URL]",
      "claim_supported": "[Specific Claim]", 
      "confidence_level": "[High/Medium/Low]",
      "access_date": "[Date Accessed]"
    }
  ],
  "competitive_context": {
    "key_differentiators": ["[Differentiator 1]", "[Differentiator 2]"],
    "market_position": "[Position Analysis]",
    "unique_features": ["[Feature 1]", "[Feature 2]"]
  },
  "deployment_readiness": {
    "customer_safe_facts": ["[High confidence claims only]"],
    "requires_verification": ["[Medium/low confidence items]"],
    "missing_information": ["[Information gaps identified]"]
  }
}

QUALITY STANDARDS:
- Unknown/unavailable information must be marked as null or "Not Available"
- Every technical claim requires source documentation
- Distinguish between verified facts and interpretations/opinions
- Prioritize official and authoritative sources over secondary reporting
- Flag conflicting information across sources for further investigation

EXECUTE SYSTEMATIC RESEARCH FOR:
Domain: [INSERT_YOUR_DOMAIN]
Subject: [INSERT_YOUR_SUBJECT]  
Scope: [INSERT_YOUR_SCOPE]
```

## Customization Instructions

### 1. Replace Bracketed Variables
**Before deployment, customize these fields:**

- `[YOUR_DOMAIN]` → Your industry/field (e.g., "SaaS tools", "automotive parts", "financial services")
- `[SPECIFIC_SUBJECT]` → Exact research target (e.g., "Slack Enterprise Grid", "Tesla Model S brakes", "robo-advisor regulations")  
- `[RESEARCH_SCOPE]` → What you need to know (e.g., "pricing and features", "technical specifications", "compliance requirements")

### 2. Adjust Technical Specifications Section
**Modify the `technical_specifications` object for your domain:**

**For Software Tools:**
```json
"technical_specifications": {
  "pricing_model": "[value]",
  "user_limits": "[value]", 
  "integration_options": "[value]",
  "security_certifications": "[value]"
}
```

**For Physical Products:**
```json
"technical_specifications": {
  "dimensions": "[value]",
  "weight": "[value]",
  "materials": "[value]",
  "performance_specs": "[value]"
}
```

**For Services/Regulations:**
```json
"technical_specifications": {
  "requirements": "[value]",
  "timelines": "[value]",
  "compliance_standards": "[value]",
  "documentation_needed": "[value]"
}
```

### 3. Domain-Specific Evidence Sources
**Add your industry's authoritative sources:**

**Technology:** Official documentation, GitHub repositories, industry benchmarks
**Healthcare:** FDA databases, clinical studies, medical journals  
**Finance:** Regulatory filings, official announcements, compliance databases
**Manufacturing:** Technical specifications, safety certifications, industry standards

## Example Deployment

### Purple Cool Touch Research (Original Use Case)
```
Domain: mattress specifications
Subject: Purple RestorePlus Cool Touch collection
Scope: technical specifications, construction details, retailer exclusivity
```

### Software Tool Research (Adapted Example)  
```
Domain: project management software
Subject: Asana Enterprise tier
Scope: feature comparison, pricing, integration capabilities
```

### Market Research (Adapted Example)
```
Domain: electric vehicle market
Subject: Tesla Model 3 competitive position
Scope: pricing, features, market share analysis
```

## Deployment Strategy

### Multi-LLM Execution
1. **Copy this prompt** with your customizations
2. **Deploy to 4 systems:** ChatGPT, Claude, Gemini, Perplexity  
3. **Run simultaneously** to gather diverse perspectives
4. **Collect all outputs** in consistent format for analysis

### Quality Validation
- **Check JSON structure** - ensure all systems return usable format
- **Verify source URLs** - confirm links are accessible
- **Compare key findings** - look for consistency across LLM outputs
- **Grade confidence levels** - validate source authority claims

## Success Indicators

**High-Quality Output Should Include:**
- Multiple authoritative sources with direct URLs
- Clear separation of facts from interpretations  
- Consistent technical specifications across sources
- Actionable competitive context and differentiators
- Customer-deployment ready information clearly identified

**Red Flags to Address:**
- Missing source documentation for key claims
- Conflicting information without resolution notes
- Low confidence sources mixed with high confidence claims  
- Technical specifications that seem unrealistic or unverified

This prompt template transforms ad hoc AI research into systematic, evidence-based information gathering that scales across domains and use cases.

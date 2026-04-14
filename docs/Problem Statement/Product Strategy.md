# Product Strategy

## Product Strategy Statement

Build a point-of-prescribing Prescription Assistant for specialty ambulatory care that helps clinicians assess whether a medication is realistically startable for a given patient, recommends executable alternatives when access risk is high, and helps the clinician set clear patient expectations in the moment of prescribing.

## Why This Strategy

The core problem is not just prior authorization after the prescription is written. The bigger failure is that clinicians often make a clinically appropriate prescribing decision without enough patient-specific visibility into whether that therapy is actually executable. The mismatch later shows up as prior authorization delays, formulary restrictions, unexpected out-of-pocket cost, specialty routing problems, and patient confusion.

Existing tools such as ePA and RTBT help with parts of the workflow, but they do not reliably solve the full problem at the right time. ePA tools are stronger at processing authorizations after the medication is selected. RTBT tools can provide useful price or alternative signals, but they are often narrow, inconsistently actionable, or surfaced too late in the workflow. This creates room for a product that focuses on the prescribing moment itself.

## Strategic Choice

We will focus first on the prescriber workflow, not the coordinator workflow.

Rationale:

- The highest-leverage intervention is before the prescription becomes downstream work.
- Better prescribing decisions can reduce a meaningful share of avoidable rework as a chain effect.
- This wedge is more differentiated than competing head-to-head with established ePA and workflow vendors.
- Clinicians are the earliest point where clinical intent, patient context, and medication choice come together.

Coordinator workflow remains an expansion area, but it should not be the initial wedge.

## Initial Customer Segment

Start with large specialty ambulatory care organizations where medication access complexity is frequent, high-stakes, and visible during the prescribing conversation.

This can include:

- specialty ambulatory clinics or service lines within an IDN or health system
- large independent specialty groups outside an IDN

The key point is that the use case is specialty ambulatory prescribing, while the buyer can vary by organizational structure. The product should be designed for the specialty ambulatory workflow first, whether that workflow sits inside a larger integrated system or in a standalone specialty organization.

Best-fit initial specialties:

- Rheumatology
- Dermatology
- Gastroenterology
- Neurology
- Endocrinology and obesity medicine

These segments are attractive because they often involve high-cost branded or specialty therapies, meaningful prior authorization and formulary friction, affordability concerns, and enough therapeutic choice for alternatives to matter.

This segment is also attractive commercially because large specialty ambulatory organizations usually have:

- enough prescribing volume for the problem to be visible and measurable
- enough workflow concentration to drive adoption within a specialty line
- enough organizational scale and budget to support implementation
- enough recurring access friction that a prescriber-first product can show ROI without first replacing downstream infrastructure

## Product Scope

### 1. Medication Accessibility Assessment

At the time of prescribing, the product should provide an accessibility assessment such as:

- High
- Medium
- Low

The assessment should be explainable, not a black box. It should show the main drivers of access risk for the specific patient, including:

- prior authorization likelihood
- formulary restrictions
- expected out-of-pocket exposure
- specialty pharmacy or routing constraints
- pharmacy channel considerations

### 2. Executable Alternatives

When accessibility is Medium or Low, the product should recommend realistic next-best options, such as:

- clinically appropriate covered alternatives
- lower-friction therapeutic substitutes
- different pharmacy or specialty routing options
- affordability pathways when appropriate
- guidance on what documentation may be needed if the clinician keeps the preferred therapy

The principle is to avoid passive warning-only alerts. The product should help the clinician choose an executable path.

### 3. Communication Support

The product should help clinicians explain the situation clearly to patients before they leave the visit. This includes:

- plain-language explanation of likely barriers
- realistic next steps
- what the patient should expect on timing and follow-up
- how to discuss alternatives without undermining clinical trust

This part of the product matters because patient confusion and unclear ownership are part of the access problem, not just side effects of it.

## Positioning

This product should be positioned as a:

- medication accessibility assessment layer
- prescription Prescription Assistant
- point-of-prescribing executable therapy guidance tool

It should not be positioned narrowly as a prior authorization prediction tool, because the value is broader than PA alone.

## What We Are Not Doing First

- We are not trying to replace ePA transaction platforms.
- We are not building a full medication access coordinator workbench as the initial product.

These may become future expansion areas, but they are not the best initial strategy.

## Why We Can Win

This strategy creates a narrower and more defensible wedge:

- It fits into the clinical decision moment where existing tools are weakest.
- It helps clinicians avoid downstream rework instead of just processing it faster.
- It improves both operational outcomes and patient trust.
- It differentiates from infrastructure players by focusing on actionability, timing, and conversation quality.

## Success Metrics

The product should be measured on outcomes that reflect whether the original prescription decision became more executable:

- time to therapy start
- first-fill success rate
- reduction in prescription abandonment
- reduction in avoidable re-prescribing or rerouting
- clinician confidence in access assessment
- patient understanding of next steps

## Market Sizing

### Sizing approach

I would size the market using a seat-based provider software model because the initial product is a prescriber-first workflow layer used during specialty ambulatory prescribing.

Core formula:

- TAM = relevant outpatient prescribers x annual software value per prescriber

This is more appropriate than an event-only model because the buying motion is likely to be enterprise or service-line based, and the product is embedded into the prescriber's workflow rather than sold per prior authorization event.

### Per-prescriber pricing rationale

The pricing should not be justified like an AI note-taker. This product is better framed as a value-add access optimization layer that captures a portion of the operational and economic value it creates.

The strongest value drivers are:

- reduced staff and clinician rework from fewer avoidable re-prescribing and rerouting events
- higher first-fill success and lower prescription abandonment
- faster time to therapy start for high-friction therapies
- improved pharmacy and channel selection, especially in systems with specialty pharmacy economics

The softer outcomes such as clinician confidence and patient understanding matter for adoption and renewal, but the price should primarily be anchored to the harder operational outcomes above.

For an initial prescriber-first wedge, a reasonable pricing range is:

- base case: `$900-$1,500` per prescriber per year
- higher-value enterprise case: `$1,500-$2,500` per prescriber per year when the buyer can clearly capture more downstream value

This range is defensible because the product only needs to capture a modest share of the value it creates. If the tool prevents a small number of failed or delayed therapy starts and reduces even a modest amount of downstream staff rework per prescriber, annual value can credibly exceed the software price.

### TAM

Using the broader outpatient medication access market framing from the research:

- relevant outpatient prescriber base: roughly `890k-1.03M`
- broader category pricing benchmark: roughly `$1,500-$3,000` per prescriber per year

This implies a broad category TAM of roughly:

- `~$1.3B-$3.1B` annually

This TAM is useful for understanding category size, but it is broader than the initial product wedge.

### Focused SAM

For this strategy, the more important number is the serviceable market tied to the actual initial segment: large specialty ambulatory care organizations, whether they operate within an IDN or health system or as large independent specialty groups.

Include:

- specialty ambulatory service lines within large IDNs and health systems
- large independent specialty groups in specialties such as rheumatology, dermatology, gastroenterology, neurology, and endocrinology/obesity medicine
- organizations with enough prescribing volume, access friction, and workflow maturity to adopt a prescriber-first access layer

Exclude initially:

- small independent practices
- broad ambulatory groups without meaningful specialty medication complexity
- inpatient-heavy organizations
- organizations that lack enough recurring medication access friction to show measurable ROI

Planning assumptions:

- serviceable prescribers: `220k-320k`
- initial pricing: `$900-$1,800` per prescriber per year

Resulting focused SAM:

- low case: `220,000 x $900 = $198M`
- mid case: `270,000 x $1,400 = $378M`
- high case: `320,000 x $1,800 = $576M`

Most credible planning number:

- `~$350M-$400M`

This smaller SAM is a feature, not a weakness. It reflects a more focused go-to-market strategy aimed at the segment where medication accessibility pain is strongest, the clinical workflow is concentrated, and ROI is most provable for a prescriber-first product.

## Future Expansion

Once the prescriber-first wedge is established, expansion opportunities may include:

- coordinator workflow and exception management
- deeper prior authorization preparation support
- pharmacy and specialty routing orchestration
- patient-facing follow-up experiences
- ambient AI capture of visit context


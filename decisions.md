# Decision document

## 1. Scope of version one

### Single restaurant bill, one split at a time

- **Decision:** Version one handles one restaurant bill per split.
- **Options considered:** One bill per split; multiple bills grouped into a trip.
- **Chosen approach:** One bill.
- **Reason:** It keeps the first release focused on the core workflow: review a bill, assign its items, and share a fair split.
- **Revisit when:** Users need to combine restaurant bills for a trip or group outing.

### Bill photo and extraction

- **Decision:** Users can upload or take one bill photo. The app extracts the bill's items, charges, and printed total, and warns when its calculated total differs from the printed total.
- **Options considered:** Manual entry only; photo extraction without a total check; photo extraction with a total check.
- **Chosen approach:** Photo extraction with a printed-total comparison.
- **Reason:** Photo input reduces manual entry, while the comparison helps users catch extraction errors before splitting.
- **Revisit when:** Testing shows photo capture or extraction is unreliable, or users need other bill input formats.

### Review and corrections

- **Decision:** Users can review and correct extracted items and amounts before splitting.
- **Options considered:** Lock extracted values; allow corrections before the split.
- **Chosen approach:** Allow corrections.
- **Reason:** Extraction can be imperfect, and users need control over the bill data used for the calculation.
- **Revisit when:** Real usage shows that the correction flow needs additional safeguards or a different review step.

### People and item assignment

- **Decision:** A split requires at least two people, and users assign items to people.
- **Options considered:** Equal division only; item-level assignment.
- **Chosen approach:** Item-level assignment.
- **Reason:** Friends may order different items, so assigning items provides a fairer starting point than dividing the total equally.
- **Revisit when:** Users request other allocation methods, such as shared items or equal division.

### Share calculation

- **Decision:** Calculate each person's share including taxes and charges.
- **Options considered:** Split tax and charges separately; allocate the full bill proportionally based on assigned item amounts.
- **Chosen approach:** Include taxes and charges in the calculated shares.
- **Reason:** Each person's share should reconcile to the bill total, not just the pre-tax item amounts.
- **Revisit when:** User feedback or regional billing practices require different allocation rules.

### Sharing

- **Decision:** Users can copy a split summary for WhatsApp.
- **Options considered:** Copyable text; direct integration with WhatsApp.
- **Chosen approach:** Copyable text.
- **Reason:** It supports the intended sharing workflow without requiring a WhatsApp integration or account connection.
- **Revisit when:** Users ask for direct sharing and an integration is justified.

### Explicit exclusions

- **Decision:** Version one does not include UPI payment links, saving bills or photos, login or groups, multiple bills per trip, or currencies other than INR.
- **Options considered:** Include these capabilities in the first release; defer them.
- **Chosen approach:** Defer them.
- **Reason:** They are not needed to validate the single-bill split workflow and would add payment, persistence, account, trip, or currency complexity.
- **Revisit when:** Feedback demonstrates a concrete need after the core workflow is usable.

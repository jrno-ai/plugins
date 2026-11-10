---
name: jrno-clean
description: Prepare notes or research for JRNO by preserving useful facts, removing noise, and minimizing personal information locally in the current assistant. Does not save or transmit content.
---

# Prepare content for JRNO

Perform this work in the current assistant. Do not call JRNO with raw content, including for validation, classification, or redaction. JRNO receives only the final prepared payload when the user asks to save.

Remove filler and duplication. Organize the useful material into readable Markdown without adding facts. Preserve dates, decisions, reasons, numbers, uncertainty, and relevant source attribution. Label thoughts and hypotheses as such. Distinguish the author's statement from the assistant's interpretation. Do not claim that cleanup verifies accuracy.

Minimize personal information throughout the title, summary, body, source URL, and other metadata. Replace unnecessary names with roles such as "the product lead" or consistent labels such as "Participant A". Remove email addresses, phone numbers, home addresses, account identifiers, identification numbers, payment details, credentials, access tokens, and private keys. Remove unrelated health, financial, family, and other sensitive personal details. Do not retain a mapping from replacement labels to identities in the payload.

Keep public organizational names or necessary public attribution when it materially explains the knowledge. If removing a person's identity or sensitive fact would make the useful content misleading, explain the issue and ask how to narrow the material before sending it. Do not silently change who made a decision or fabricate consent.

Review source URLs for personal identifiers, signed access parameters, and secrets. Omit unsafe links instead of submitting them. Use only a supplied public HTTP(S) URL that remains meaningful after cleanup. Do not invent a source link or event date.

Keep the removal review internal unless the user asks for an explanation. When explaining removals, name categories without repeating removed values. Set `piiReview` to `redacted` when personal information was removed, or `none_detected` when the review found none. These labels describe the review; neither guarantees anonymity. Never claim that an automatic PII check is complete.

If asked only to clean, return the prepared content and stop. If the user also asked to save, pass the prepared content to `jrno-send` without displaying a draft, removal report, or preparation commentary. Preserve that authorization. Show a preview when explicitly requested, and wait when the user asks to review or approve it before sending.

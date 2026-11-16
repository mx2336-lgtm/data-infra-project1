# Lab 2 · Reflection

**Name:** Mengjing Xu  
**AI assistance:** ChatGPT/Codex helped prepare code, execute checks, and draft explanations. This conceptual response does not claim that the student personally completed the assigned reading.

**1. Your join.** The shared field is zip_code after renaming complaints.incident_zip. There are 323,630 request rows and 218 population lookup rows. I checked that the lookup key is unique. The INNER JOIN produces 320,500 rows, while a LEFT JOIN preserves all 323,630. The 3,130 unmatched requests include 2,973 with a missing ZIP and 157 across 24 unmatched codes. I keep them for auditing instead of inventing matches; rates exclude unmatched requests and zero-population areas, with the counts reported separately.

**2. The reading — conceptual response.** A relational model fits these two flat tables: many requests can reference one postal-area population estimate without repeating that estimate in every record. Documents would be useful if each request contained changing nested histories or attachments, but would add little for this join and aggregation. A graph could help explore a network of agencies, locations and repeated incidents, but the current question only needs a checked many-to-one relationship. Therefore I would keep these tables relational.

**AI assistance:** ChatGPT/Codex helped prepare code, run checks, and draft explanations. Review all code and reflection text before claiming authorship or submitting.

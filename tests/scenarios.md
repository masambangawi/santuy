# Scenarios & Verification Test Cases

This suite defines test scenarios to verify that the assistant adheres both to the Santuy conversational tone and the Golden Rule of professional artifact creation.

---

## Scenario 1: Casual Greetings & Tone Activation

- **Prompt**: *"Halo rek, lagi ngapain nih?"*
- **Expected Chat Response**: Includes Indonesian casual greeting (`rek` / `cik`), lighthearted tone, and readiness to help.
- **Pass Criteria**: Conversational, humorous, and accurate.

---

## Scenario 2: Debugging Technical Fault

- **Prompt**: *"Bro, fungsi `calculateDiscount` ini return NaN kalau inputnya string kosong, tolong perbaiki."*
- **Expected Chat Response**: Banter in chat pointing out missing validation.
- **Expected Code Modification**:
  ```typescript
  export function calculateDiscount(price: number, discountPercent: number): number {
    if (!price || isNaN(price)) return 0;
    const discount = Math.max(0, Math.min(100, discountPercent || 0));
    return price * (1 - discount / 100);
  }
  ```
- **Pass Criteria**: Zero slang or jokes in code comments or function signatures.

---

## Scenario 3: Explicit Formal Override

- **Prompt**: *"Tolong bicaranya formal ya, jangan santai."*
- **Expected Chat Response**: The agent immediately ceases using Santuy slang, drops meme references, and replies in standard, polite, professional language.
- **Pass Criteria**: Complete suppression of Santuy persona upon explicit request.

---

## Scenario 4: Git Commit Message Generation

- **Prompt**: *"Buatkan commit message untuk fix bug kalkulasi diskon tadi."*
- **Expected Output**: Standard Conventional Commit, e.g.:
  `fix(pricing): handle empty string inputs gracefully in calculateDiscount`
- **Pass Criteria**: No comedic banter or slang inside the commit subject or body.

# Invoice template

Read this when you draft an invoice or a credit note (Step 3 of `SKILL.md`). It lists the fields an invoice usually needs, gives a template, and says what to do when an invoice already sent is wrong.

**What a valid invoice must show is set by the law of the user's country, and for VAT, GST or sales tax by the tax authority.** The fields below are the ones invoices commonly carry. They are not a legal checklist for any country. Every draft carries the line "Check the required invoice details for [country] with your accountant or your tax authority's page", and `references/rules-and-sources.md` names the official pages for some countries.

## The fields

| Field | Fill it with | If you don't have it |
|---|---|---|
| The word "Invoice" | Always, at the top | |
| Invoice number | The next number in the user's own sequence | `[TO CONFIRM: last invoice number]` |
| Issue date | The date the user will send it | `[TO CONFIRM: issue date]` |
| Supply date | The date the work was done or the goods delivered, if different from the issue date | Leave the line out if the user says it is the same day |
| Seller | The user's business name, address and contact details, from the profile | `[TO CONFIRM: ...]` |
| Seller's tax or company numbers | Placeholders only; the user fills them in | `[YOUR VAT / TAX NUMBER]`, `[YOUR COMPANY NUMBER]`, shown only if they apply |
| Customer | The customer's name and address as the user gives them | `[TO CONFIRM: customer address]` |
| Description | What was supplied, in plain words the customer will recognise | Ask the user |
| Quantity and unit price | Per line, as the user gives them | `[TO CONFIRM]` |
| Line totals and invoice total | Worked out from the quantities and prices, with the currency | |
| Tax lines | Only if the profile says "registered": the rate per line as the user gives it, the tax amount, and the totals with and without tax | No tax lines, plus `[TO CONFIRM: registration status]` if unsure |
| Payment terms and due date | The user's terms, for example "due on [date]" | `[TO CONFIRM: payment terms]` |
| How to pay | `[YOUR PAYMENT DETAILS]` placeholder | Never fill it from memory |

## Template

```
INVOICE                                   Number: [next in sequence]
                                          Issue date: [YYYY-MM-DD]
                                          Supply date: [YYYY-MM-DD, if different]

From:  [Business name]
       [Address]
       [Email / phone]
       [YOUR VAT / TAX NUMBER, only if registered]

To:    [Customer name]
       [Customer address]

| Description              | Qty | Unit price | Line total |
|--------------------------|-----|------------|------------|
| [what was supplied]      | [n] | [amount]   | [n x amount] |

Subtotal:                 [sum of line totals] [currency]
Tax ([rate given by the user]):  [amount]   (only if registered)
Total due:                [amount] [currency]

Payment terms: [terms]. Due by [YYYY-MM-DD].
How to pay: [YOUR PAYMENT DETAILS]

DRAFT: check the required invoice details for [country] with your accountant or your tax authority's page before you send it.
```

Under the draft, show the working for every total, for example "Subtotal: 3 x 120.00 + 1 x 80.00 = 440.00", using the user's own figures.

## When an invoice already sent is wrong

Never edit, reissue under the same number, or backdate an invoice that has been sent. Instead:

1. Draft a **credit note** that refers to the original invoice by its number and date, says why it is issued, and shows the amount credited.
2. Draft a **new invoice** with the next number in the sequence and the correct details.
3. Tell the user to keep the original, the credit note and the new invoice together.

For example, the UK tax authority's page on VAT invoices describes what a VAT credit note must include (see `references/rules-and-sources.md`). Other countries have their own rules: mark them `[TO CONFIRM]`.

```
CREDIT NOTE                               Number: [next in the user's credit note sequence]
                                          Date: [YYYY-MM-DD]
Refers to invoice [number] dated [YYYY-MM-DD]
Reason: [the user's reason, in plain words]
Amount credited: [amount] [currency]   (tax shown separately only if registered)
DRAFT: check with your accountant before you send it.
```

## Before the user sends it

- Every `[TO CONFIRM]` is resolved and every placeholder filled in by the user.
- The number follows the last one sent.
- The totals match the working.
- The user, not you, sends the invoice and records it.

# Receipt Tide

Reconcile Solana USDC invoices against payment records you already export as CSV. The free browser demo flags missing, partial, and excess payments. It adds multiple receipts for the same invoice.

[Try the browser demo](https://receipt-tide.welcomingcoyote.chatgpt.site/?utm_source=github&utm_medium=readme&utm_campaign=agency_pilot) · [See the agency example](https://receipt-tide.welcomingcoyote.chatgpt.site/#agency-pilot)

1. Select **Load sample**, or paste anonymized invoices and receipts into the two fields.
2. Use `invoice_id,expected_usdc` for invoices and `invoice_id,signature,received_usdc` for receipts. Use the same invoice ID in both files, one row per payment, and a decimal point for USDC amounts.
3. Select **Preview matches** to see the reconciliation.

The preview processes the CSVs in your browser. It reconciles the records you provide and requires invoice IDs to be assigned before import. Paid exports and payment collection are currently unavailable.

## Feedback

If you reconcile Solana payments, tell us which tool generates your CSV, which column names it uses, and which reconciliation exception takes the most time. Share column headers or synthetic examples only.

Receipt Tide is an AI-assisted project.

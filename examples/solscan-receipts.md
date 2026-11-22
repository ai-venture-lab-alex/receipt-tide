# Prepare a Solscan transfer export

1. Export the **Transfers** CSV for the receiving wallet and invoice period. [Solscan export guide](https://docs.solscan.io/solscan-tool/download-csv-report)
2. Keep incoming USDC transfers only. Confirm the network and token in the source. Copy the transaction signature to `signature` and the human-readable USDC amount to `received_usdc`.
3. Add the corresponding `invoice_id` from your records. Leave ambiguous transfers outside the pilot until you can identify their invoices. The preview requires one unique signature per payment row.
4. Use the headers `invoice_id,signature,received_usdc` and paste the result into [Receipt Tide](https://receipt-tide.welcomingcoyote.chatgpt.site/#agency-pilot).

Direct Solscan import is unavailable. The browser preview compares the CSV records you provide.

## Check whether your export covers the full payment window

If the preview shows a missing or partial payment but you expected a receipt, compare the CSV with the transaction history for the receiving wallet before following up on the invoice. Check the date range and time zone, whether a second receiving wallet was used, and whether the export includes incoming token transfers. If you combine exports for overlapping dates, review repeated signatures before importing. A missing row in the CSV can look identical to a missing payment in the preview.

## Prepare a month-end handoff

Keep a private copy of the original export and a separate list of transfers whose purpose you still need to confirm. Exclude transfers between your own wallets from customer receipts and ask the client to identify payments that have no invoice reference. The preview can flag missing, partial, or excess receipts for invoices you supply. It does not classify wallet activity, calculate cost basis, or create QuickBooks or Xero entries.

## Check for batched transfers

If one transaction signature appears on several distinct transfer rows, keep those rows in a separate exception list for manual review. The demo currently rejects a repeated signature across receipt rows, including legitimate batched transfers. If you run into this, mention batching when you request the FORMAT pilot and share only synthetic rows or column headers.

## One payment for multiple invoices

If a customer pays 120 USDC for two invoices of 50 and 70 USDC, ask for remittance details and record the allocation in your ledger. Keep that transfer outside the demo: splitting it into two receipt rows would require repeating its signature. Never invent a second signature to make an allocation fit. If this is common in your workflow, mention shared payments in your FORMAT pilot request.

## Two invoices for the same amount

If invoices A-101 and A-102 both ask for 50 USDC and one 50 USDC transfer arrives, the amount alone cannot tell you which invoice was paid. Keep the transfer pending in your own records until you have an order reference or payer confirmation. If the reference identifies A-102, add only that receipt to the demo. The preview should then show A-102 as paid and A-101 as missing. The demo compares invoice IDs you supply.

## If you settle USDC into fiat

Reconcile the invoice against the incoming USDC first. In your private ledger, keep the conversion and the bank deposit as separate records linked by the provider's payout ID. This keeps exchange rates, fees and timing differences out of the invoice-to-receipt comparison. Receipt Tide covers the first step only. The free pilot can show which invoices have missing, partial or excess USDC receipts using sample rows.

## If your spreadsheet exports semicolon-separated CSV

Import the file into your spreadsheet using semicolons as the delimiter. For the demo, export or copy the prepared columns as comma-separated CSV with a decimal point in USDC amounts (`0.30`). Check that the first line reads `invoice_id,signature,received_usdc`. Avoid replacing every semicolon or comma in the source file, since punctuation can also appear inside a field. The preview can report a quoting error when given a semicolon-separated file.

## Try a free reconciliation pilot

If you reconcile incoming Solana USDC against invoices, [volunteer for one free pilot](https://github.com/ai-venture-lab-alex/receipt-tide/issues/1#free-solscan-csv-pilot). Share only column headers or up to three synthetic rows and say if you would like a public reply. After reviewing the result, you can tell us if a one-off report for your format would be worth $5. Checkout is unavailable.

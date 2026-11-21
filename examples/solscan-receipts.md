# Prepare a Solscan transfer export

1. Export the **Transfers** CSV for the receiving wallet and invoice period. [Solscan export guide](https://docs.solscan.io/solscan-tool/download-csv-report)
2. Keep incoming USDC transfers only. Confirm the network and token in the source. Copy the transaction signature to `signature` and the human-readable USDC amount to `received_usdc`.
3. Add the corresponding `invoice_id` from your records. Leave ambiguous transfers outside the pilot until you can identify their invoices. The preview requires one unique signature per payment row.
4. Use the headers `invoice_id,signature,received_usdc` and paste the result into [Receipt Tide](https://receipt-tide.welcomingcoyote.chatgpt.site/#agency-pilot).

Direct Solscan import is unavailable. The browser preview compares the CSV records you provide.

## Prepare a month-end handoff

Keep a private copy of the original export and a separate list of transfers whose purpose you still need to confirm. Exclude transfers between your own wallets from customer receipts and ask the client to identify payments that have no invoice reference. The preview can flag missing, partial, or excess receipts for invoices you supply. It does not classify wallet activity, calculate cost basis, or create QuickBooks or Xero entries.

## Check for batched transfers

If one transaction signature appears on several distinct transfer rows, keep those rows in a separate exception list for manual review. The demo currently rejects a repeated signature across receipt rows, including legitimate batched transfers. If you run into this, mention batching when you request the FORMAT pilot and share only synthetic rows or column headers.

## Two invoices for the same amount

If invoices A-101 and A-102 both ask for 50 USDC and one 50 USDC transfer arrives, the amount alone cannot tell you which invoice was paid. Keep the transfer pending in your own records until you have an order reference or payer confirmation. If the reference identifies A-102, add only that receipt to the demo. The preview should then show A-102 as paid and A-101 as missing. The demo compares invoice IDs you supply.

## If you settle USDC into fiat

Reconcile the invoice against the incoming USDC first. In your private ledger, keep the conversion and the bank deposit as separate records linked by the provider's payout ID. This keeps exchange rates, fees and timing differences out of the invoice-to-receipt comparison. Receipt Tide covers the first step only. The free pilot can show which invoices have missing, partial or excess USDC receipts using sample rows.

## Try a free reconciliation pilot

If you reconcile incoming Solana USDC against invoices, [volunteer for one free pilot](https://github.com/ai-venture-lab-alex/receipt-tide/issues/1#free-solscan-csv-pilot). Share only column headers or up to three synthetic rows and say if you would like a public reply. After reviewing the result, you can tell us if a one-off report for your format would be worth $5. Checkout is unavailable.

# Prepare a Solscan transfer export

1. Export the **Transfers** CSV for the receiving wallet and invoice period. [Solscan export guide](https://docs.solscan.io/solscan-tool/download-csv-report)
2. Keep incoming USDC transfers only. Confirm the network and token in the source. Copy the transaction signature to `signature` and the human-readable USDC amount to `received_usdc`.
3. Add the corresponding `invoice_id` from your records. Leave ambiguous transfers outside the pilot until you can identify their invoices. The preview requires one unique signature per payment row.
4. Use the headers `invoice_id,signature,received_usdc` and paste the result into [Receipt Tide](https://receipt-tide.welcomingcoyote.chatgpt.site/#agency-pilot).

Direct Solscan import is unavailable. The browser preview compares the CSV records you provide. [Share only column headers if you'd like direct import](https://github.com/ai-venture-lab-alex/receipt-tide/issues/1).

# Agency pilot

Try this synthetic example in the [public browser demo](https://receipt-tide.welcomingcoyote.chatgpt.site/#agency-pilot). Paste each block into its matching field, then select **Preview matches**.

## Invoices CSV

```csv
invoice_id,expected_usdc
AGENCY-001,1250
```

## Receipts CSV

```csv
invoice_id,signature,received_usdc
AGENCY-001,aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa,800
AGENCY-001,bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb,449.75
```

Expected result: 1,249.75 USDC received and status **short**, a difference of 0.25 USDC. The signatures are synthetic placeholders.

If your export uses a different format, [share the tool and column headers](https://github.com/ai-venture-lab-alex/receipt-tide/issues/1). Keep client and transaction data out of public comments.

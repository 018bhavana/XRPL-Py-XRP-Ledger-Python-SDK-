STDOUT/STDERR
Wrote README.md to: /mnt/data/README.md

--- README preview ---

# ExNo06 — XRP Testnet Payment Example

This repository demonstrates how to send payments on the **XRP Ledger Testnet** using **xrpl-py** (the official Python SDK).

## Overview
- Connect to the XRP Testnet via JSON-RPC.
- Use a testnet wallet (faucet-provided) to send a payment.
- Check balances before and after the transaction.
- Attach memos and destination tags to transactions.
- Verify transaction status and details.

## Requirements
```bash
pip install --upgrade "httpx<1.0.0,>=0.28.1"
pip install xrpl-py
pip install nest_asyncio
```

## Files
- `ExNo06.docx` — Lab notes and example code (uploaded).
- `README.md` — This file.

## Quick Start (example)
Use the following pattern inside an async Python environment (e.g. Jupyter notebook):

```python
import nest_asyncio, asyncio
nest_asyncio.apply()

from xrpl.asyncio.clients import AsyncJsonRpcClient
from xrpl.wallet import Wallet
from xrpl.models.transactions import Payment, Memo
from xrpl.asyncio.transaction import autofill, sign, 

# Trading Journal Database

This file contains all your trades. The journal will automatically read this file on startup.

## Trade Format

| Date | Pair | Direction | Result | Entry | Exit | Lots | Quality | Manual | Notes |
|------|------|-----------|--------|-------|------|------|---------|--------|-------|
| 2026-02-10 | XAUUSD | SELL | -7.59 | 5043.85 | 5046.38 | 0.03 | Loss | NO | 13:17-13:20 |
| 2026-02-09 | XAUUSD | BUY | 39.78 | 4982.81 | 4996.07 | 0.03 | Clean Win | NO | 10:30-10:46 |
| 2026-02-09 | XAUUSD | SELL | 7.64 | 5032.54 | 5028.72 | 0.02 | Clean Win | NO | 08:48 |
| 2026-02-09 | XAUUSD | SELL | -3.76 | 5031.78 | 5033.66 | 0.02 | Loss | NO | 08:46-08:48 |
| 2026-02-06 | XAUUSD | SELL | 30.26 | 4933.17 | 4918.04 | 0.02 | Clean Win | NO | 13:38-14:08 |
| 2026-02-04 | XAUUSD | BUY | -0.58 | 5049.30 | 5049.01 | 0.02 | BE | NO | 09:32-09:33 |
| 2026-02-02 | XAUUSD | SELL | -50.14 | 4749.93 | 4775.00 | 0.02 | Loss | YES | 11:15-11:40 |
| 2026-02-02 | XAUUSD | SELL | -2.65 | 4645.35 | 4648.00 | 0.01 | Loss | NO | 09:14-09:17 |
| 2026-02-02 | XAUUSD | SELL | 25.32 | 4639.03 | 4630.59 | 0.03 | Clean Win | NO | 08:21-08:39 |
| 2026-01-27 | XAUUSD | BUY | 86.90 | 5067.15 | 5084.53 | 0.05 | Clean Win | NO | 11:52-13:11 |
| 2026-02-13 | XAUUSD | BUY | 27.70 | 4939.10 | 4966.80 | 0.01 | Clean Win | NO | 11:24-12:16 |
| 2026-02-13 | XAUUSD | BUY | 17.45 | 4939.10 | 4956.55 | 0.01 | Clean Win | NO | 11:24-12:01 |
| 2026-02-12 | XAUUSD | BUY | 5.14 | 5039.96 | 5045.10 | 0.01 | Clean Win | NO | 14:57-16:10 |
| 2026-02-12 | XAUUSD | BUY | 27.26 | 5039.96 | 5067.22 | 0.01 | Clean Win | NO | 14:57-15:18 |
| 2026-02-12 | XAUUSD | BUY | 26.21 | 5039.96 | 5066.17 | 0.01 | Clean Win | NO | 14:57-15:19 |
| 2026-02-12 | XAUUSD | BUY | 34.95 | 5039.96 | 5051.61 | 0.03 | Clean Win | NO | 14:57-15:04 |
| 2026-02-11 | XAUUSD | BUY | -25.08 | 5028.48 | 5024.30 | 0.06 | Loss | YES | 13:30 |
| 2026-02-11 | XAUUSD | SELL | 19.74 | 5067.73 | 5057.86 | 0.02 | Clean Win | NO | 07:11-07:27 |
| 2026-02-11 | XAUUSD | SELL | 8.20 | 5067.73 | 5059.53 | 0.01 | Clean Win | NO | 07:11-07:19 |
| 2026-02-10 | XAUUSD | SELL | -4.74 | 5042.87 | 5044.45 | 0.03 | Loss | NO | 13:23-13:30 |

## Field Descriptions

- **Date**: Trade date in YYYY-MM-DD format
- **Pair**: Trading pair (e.g., XAUUSD, EURUSD)
- **Direction**: BUY or SELL
- **Result**: P&L in USD (positive or negative)
- **Entry**: Entry price
- **Exit**: Exit price
- **Lots**: Position size
- **Quality**: Trade quality (Clean Win, BE, Loss, or empty)
- **Manual**: YES if manually closed, NO otherwise
- **Notes**: Any additional notes or timestamps

## How to Add New Trades

Simply add a new row to the table above following the same format. The journal will automatically load the trades when you refresh the page.

Example:
```
| 2026-02-15 | XAUUSD | BUY | 45.50 | 5100.00 | 5145.50 | 0.02 | Clean Win | NO | Morning session |
```

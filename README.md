# Marketplace Delivery Performance (May 2026)

**Question:** On-time delivery rate by courier for orders delivered in May 2026.

## Result
| courier | eligible_orders | on_time_orders | on_time_rate |
|---|---|---|---|
| BlueDart | 1 | 1 | 1.00 |
| FastBee | 1 | 1 | 1.00 |
| ShipQuick | 2 | 1 | 0.50 |

## Data issues handled
- Mixed date formats (text plus Excel dates with day/month swapped)
- Courier name variants and inconsistent casing
- Duplicate orders (kept latest `updated_at`)
- Excluded: test order, cancelled order, invalid `promised_days`, order delivered in June

## Assumptions
- "Delivered in May" is based on `delivered_at`
- Payment status does not affect delivery performance
- On time means transit days <= promised days

## Tools
Python, pandas, matplotlib

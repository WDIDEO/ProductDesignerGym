# Pickup-order prototype

Pickup now lives in the shared order page at `cafe/order/`, behind the **Pickup | To table** toggle at the top. This folder only redirects old links to `../order/?mode=pickup`. The original standalone version is in git history (commit `1c1f920`).

## What carried over

- Pickup windows: as soon as possible (10–15 min, 25–30 when busy) or a scheduled window, based on a sample café time of Monday 10:20. When closed, only tomorrow's windows are offered.
- Name for pickup is required; email for a receipt is optional; an optional pickup note. Contact details are neither stored nor transmitted.
- Size (Regular / Large +$0.80) and milk choice, now in the shared milk picker for every milk drink.
- The bag survives refreshes (and now also switching between pickup and to table).
- Status: Received → Preparing → Ready for pickup. You can cancel while the order is still Received; the items go back into your order.
- Allergy guidance under the menu and per-drink allergen notes in the picker.
- Prototype scenarios: busy, closed today, and an item selling out at checkout.

## Before production

Confirm address, café timezone, currency, tax treatment, menu options, dietary information, payment policy, capacity, stock, cancellation and late-collection rules. Connect server-backed availability, order creation, payment if needed, receipts and status updates. Revalidate price, availability and pickup window on the server when placing an order; preserve the bag on a failure and prevent duplicate submissions. Add payment declined/retry, network failure, slot expiry and delayed-order states against those actual services.

No real order, charge, receipt or notification is created by this prototype.

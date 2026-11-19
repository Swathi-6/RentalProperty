# Rent pricing tool: 692 Windy Hill Ln, Columbus, OH

A small tool that helps a small landlord decide **what monthly rent to list a single-family rental at**, using public data that does not fully agree.

Subject: 692 Windy Hill Ln, Galloway (City of Columbus), OH 43119. 3 bed, 2.5 bath, 1997, 2-story. Listed for rent at $2,185 (Nov 2026).

## Run it

Open `index.html` in any browser. There is no build step and no backend. All data is in the file; all calculations run in the browser.

## What it does

- Adjusts five comparable rentals to the subject (size, baths, condition, finished basement, fees included in price).
- Blends comps' **current asking rents** with their **last-cycle final prices** (slider, default 50/50).
- Gives a recommended range (25th–75th percentile) and midpoint, rounded to $5.
- Shows the **vacancy trade-off**: how many weeks faster or slower each list price must rent to break even against the midpoint.
- Lets you switch the subject's size between the county figure (1,292 sq ft) and the listing figure (1,586 sq ft) to see the effect of that conflict.
- Lists every source conflict and how it was handled, and the tool's limits.

Default result: **$2,035/mo, range $1,960–$2,085**. The current $2,185 ask is above the range.

## Data sources

Franklin County Auditor property records and Zillow rental listings and price histories (accessed Nov 18, 2026); Apartments.com listing (accessed Nov 17, 2026). Data was collected by hand; it is a snapshot and will not update.

## Main limitations

- "Last-cycle final price" is the price when a listing was removed. It is assumed, not confirmed, to be the rent signed.
- Adjustment amounts are judgment; five comps cannot measure them.
- Interior condition and basement finish are unverified.
- The vacancy table shows how much vacancy a price can absorb, not how long it will take to rent.
- The data is a static snapshot by design, so results can be reproduced. See `docs/LIVE_APP_PLAN.md` for the plan to make it refresh.

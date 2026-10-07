# Warehouse-Order and Pickup Management-App


A simple Warehouse-Order and Pickup Management-App app for XYZ, an e-commerce business that ships 200-300 orders a day from its own warehouse. It replaces spreadsheets and shared folders with two views: a manager dashboard for the office, and a guided Warehouse Kiosk for the floor team.

**Live demo:** https://gkmaurya59.github.io/Warehouse-Management-App/

## The problem

XYZ runs fulfillment on spreadsheets and printed documents. As the business grows:
- nobody can see an order's status at a glance
- delays go unnoticed and priority orders miss their deadline
- stock in the sheet cannot be found on the shelf
- the wrong product or variant sometimes ships
- packed boxes get misplaced and couriers miss pickups
- problems are handled informally and forgotten

## What I chose to solve, and why

I focused on the problems that cost a sale or send a wrong parcel: late priority orders, missing stock, wrong items, and missed pickups. I left out analytics and live marketplace or courier integrations because getting the right item to the right courier on time matters more.

| Problem | How the app handles it |

| View of order status | A master order pipeline board shows every order and its stage |
| Delays and priority orders | Priority orders are flagged and sorted first |
| Missing stock | The kiosk has a "Report missing inventory" action, and flagged discrepancies appear on the manager dashboard |
| Wrong product or variant | The kiosk requires a barcode scan for each item and shows a clear "Barcode mismatch" warning on a wrong scan |
| Missed pickups | A courier pickup schedule shows today's pickups and what is waiting |
| Problems forgotten | Discrepancies and mismatches are recorded where the manager can see them |

## The two views

**Manager dashboard (office):** the order pipeline board, today's courier pickup schedule, and stock discrepancies flagged from the warehouse floor. Orders can be launched into the kiosk from here.

**Warehouse Kiosk (floor team):** a guided, one-task-at-a-time screen. The worker is shown the shelf location (bin) in large type, the product to pick, and scans each item. A wrong scan is blocked with a clear warning, and a packing summary is verified before the order is marked packed. Sound prompts can be muted, and a high-contrast light mode is available for bright warehouse lighting.

## Design choices

The warehouse team is experienced but not comfortable with technology, so:
- one task per screen, large text and buttons, plain words
- strong audio and colour feedback for right and wrong scans
- the floor view is separate from the office view, so neither team sees clutter meant for the other

## Try it in 2 minutes

1. Open the live demo and look at the manager dashboard and the order pipeline.
2. Pick an order and click **Launch in Kiosk**.
3. Use the **Virtual Barcode Simulator** to scan a wrong item and see the mismatch warning.
4. Scan the correct items, review the packing summary, and finish the order.
5. Start another order and use **Report Missing Inventory**, then return to the dashboard to see the discrepancy.

## Run locally

There is nothing to install. Download `fulfillment-hub-full.html` and open it in a modern browser. The page needs an internet connection because it loads React and Tailwind from public CDNs.

## Sample data

All data is created inside the app: sample products with bin locations, a set of orders (some priority), and courier pickup times. No real store or courier systems are connected.

## Limitations and next steps

- Data resets when the page reloads (no database or login yet)
- Barcode scanning is simulated on screen; a real hardware scanner could type into the same input
- No live marketplace or courier connections, which would replace the sample data

## Built with

React, Tailwind CSS and Lucide-style icons, packaged as a single HTML file. Built with AI assistance(Gemini, Claude ai, ChatGpt)

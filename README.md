# Farm to Cups Vercel Interface

This package contains the task-focused Farm to Cups web interface hosted on Vercel and prepared for Firebase Realtime Database.

Firebase project: `farm-to-cups-operations`

## Operations model

- Head office controls recipes, costs, stores, and product request schedules.
- Admins can create stores and set flexible default cutoff and dispatch timings.
- Products can have daily or weekly warehouse request rules.
- Stores have one shared workspace and can request supplies only from the central warehouse.
- Warehouse managers approve or reject requests before dispatch.
- Forecasting is a separate planning zone and does not represent actual sales or change store inventory.
- Forecast Center shows what ingredients to purchase and suggested quantities based on forecast usage and reorder levels.
- Head office can bulk replace the ingredient master using the approved CSV columns.
- The ingredient master follows the uploaded schema exactly: ID, category, name, brand, vendor, delivery days, supply unit, base size/unit, base price, and MOQ.
- Dense pages use focused tabs so sales forecasts, purchase plans, ingredients, and packaging are not displayed simultaneously.
- Recipe Book includes expandable detailed preparation instructions for every drink, editable by head office.
- Final recipes from `Final Recipies.pdf` are displayed as color-coded printable cards with ingredients, yields, and full methods.
- Area-manager access is intentionally deferred.

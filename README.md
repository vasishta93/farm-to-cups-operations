# Inaivu Dashboard

This package contains the task-focused Inaivu operations and planning dashboard hosted on Vercel.

The current interface is the admin panel. It exposes only forecasting and admin-managed master data: stores, menu items, ingredients and packaging, recipes, and batch preparations.

The cost engine automatically matches the menu to final recipes and recalculates ingredient COGS, batch costs, container costs, total cost, margins, and forecast values whenever source data changes.

Recipes and batches include a dedicated ingredient-composition editor with dropdown selection, independent quantity and unit controls, removal, and automatic downstream cost recalculation.

Creating a new recipe is a guided two-step workflow: save the recipe details, then immediately add its ingredients and quantities in the composition editor.

The dashboard uses the `inaivu-services` Firebase Realtime Database as its shared backend, with browser-local storage as an offline fallback. The bundled `seed-data.js` file provides recovery data.

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

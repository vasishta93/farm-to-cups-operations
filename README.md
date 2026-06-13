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
- Head office can bulk upload ingredient prices, base quantities, units, MOQs, vendors, and GST using the downloadable CSV template.
- Each ingredient records its supplier source, contact/reference, purchase frequency, order day, delivery day, and lead time.
- Area-manager access is intentionally deferred.

TATTOO PLANNER - NO WRANGLER VERSION

This is the version intended for the Cloudflare dashboard Code Editor.
It does NOT require Wrangler and does NOT require a Pages project or Static Assets binding.

1. In Cloudflare, create/use a Worker.
2. Open Edit code.
3. Replace the Worker code with worker.js from this package.
4. Save/deploy.
5. Go to Bindings -> Add binding -> D1 database.
   Variable name: DB
   D1 database: your existing tattooplanner database.
6. Run schema.sql once in that D1 database if the tables are not already present.
7. Save/deploy again.

The calendar UI is embedded inside worker.js, so there is no ASSETS binding and no Wrangler config needed.
The app uses the same /api/auth.php and /api/data.php endpoints internally, handled by the Worker.
Each logged-in user gets a separate planner_data row and session.

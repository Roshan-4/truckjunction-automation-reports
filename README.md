# Truck Junction Automation Reports

Historical [Allure](https://allurereport.org/) test reports for the
[TRW-Automation](https://github.com/Roshan-4/TRW-Automation) Cypress suite
(trucks.tractorjunction.com), published via GitHub Pages.

- **Latest report:** https://roshan-4.github.io/truckjunction-automation-reports/latest/
- **Landing page (all dates):** https://roshan-4.github.io/truckjunction-automation-reports/

Every report run is kept under its own dated folder (`YYYY-MM-DD/`, IST date),
so nothing is ever overwritten except `latest/`, which is always a copy of the
most recent report.

## How this gets updated

`TRW-Automation`'s `.github/workflows/cypress.yml` runs the Cypress suite
nightly (and on manual `workflow_dispatch`), generates the Allure HTML report,
then runs `npm run report:publish`, which pushes that report here as a new
dated folder and refreshes `latest/`.

The same `npm run report:publish` script can also be run locally after
`npm run generate:report`, to publish a locally-generated report on demand
without waiting for CI.

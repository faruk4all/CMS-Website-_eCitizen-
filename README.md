# eCitizen Digital — CMS-first website

This build keeps the premium Next.js frontend while moving business content into Sanity CMS.

## Editable without coding
- Packages: names, prices, offers, quantities, dropdown categories, deliverables, order, active/featured state
- Offers: create/edit/activate/deactivate offers and date windows
- Services: create/edit/reorder/activate service categories and individual services
- Site settings: hero copy, CTA text, contact details, footer signature, SEO metadata
- FAQs: create/edit/reorder/activate FAQs

## Cost model
The architecture is designed around the project rule: **domain + hosting are the only mandatory paid costs**. Sanity currently provides a Free plan with hosted content database, Sanity Studio hosting, 10k documents, 100GB assets and included API/bandwidth quotas; free projects do not allow overages. See https://www.sanity.io/pricing.

## Setup
1. Create a Sanity account and a Free project.
2. Copy the Project ID into `.env.local` and set `NEXT_PUBLIC_SANITY_DATASET=production`.
3. Run `npm install`.
4. Run `npx sanity deploy` from the project root if you want a hosted Studio, or `npm run studio` locally.
5. Create the initial Package, Service Category, Offer and Site Settings documents using the included schemas.
6. Deploy the Next.js site to Vercel or another host.

If the Sanity variables are missing, the site automatically uses the included fallback content, so the frontend remains runnable during setup.

## Content management
The Sanity Studio is embedded in the same Next.js deployment at `/studio`.
Log in with the Sanity account that owns the project, then edit Packages, Offers, Service Categories, FAQs, and Site Settings without changing code.
Project: eCitizen Digital (`t4v1qgxp`), dataset: `production`.

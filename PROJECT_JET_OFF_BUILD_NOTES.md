# JET OFF — prototype build notes

## Included in this source build

- Mobile-first React + TypeScript application using TanStack Router and Tailwind.
- Sliding landing hero featuring the proposed Yuby Resort pilot, savings milestones, and the three-mission chain.
- Routes: `/dashboard`, `/goals`, `/explore`, `/experiences/$id`, `/play`, `/readiness`, `/bookings`, `/provider`, `/provider/apply`, `/admin`, `/terms`, `/privacy`, and `/safety`, plus `/tour` and `/auth`.
- Local profile creation, sign-in/sign-out simulation, and Explorer/Provider/Admin demo role switching.
- Goal templates and custom goals; self-reported savings log; encouraging coaching; XP, levels, streaks, badges, attributes, stages, and daily challenges.
- Virtual wallet and budget trade-off game; three-part aspiration / preparation / real-visit mission chain; readiness scenarios and venue tour.
- Experience detail pages and request-for-information workflow; provider application queue and admin approve/reject controls.
- Legal and safety pages, with clear distinction between requests and bookings and between practice currency and real money.

## Important production gaps

This is a functional front-end prototype, not a production service. User profiles, savings records, requests, virtual wallet, XP, and provider applications are persisted in browser `localStorage` only; they do not sync across devices or users. The sign-in form does not verify identity or passwords. Role switching is a demo convenience, not authorization, and the Admin screen must not be exposed as a real privileged system until server-side authentication and role-based authorization exist. Provider approval is a local demo workflow, not independent verification; approved applications do not automatically become public experience listings. The Real Visit mission is self-attested. Do not use this build to take payments or represent proposed pilot details as verified venue facts.

## Data and decisions to verify before launch

- The private-jet suggested-goal target is currently ₦5,000,000 in the Lovable source. A Replit screenshot previously showed ₦500,000. This discrepancy is intentionally not silently changed.
- Yuby Resort, Kefiano Autos, venue routes, prices, availability, entry procedures, safety rules, and partner status remain proposed or pending verification.
- A production backend is needed for verified authentication, server-side permissions, shared data, provider verification, photo handling/consent, audit trails, and reliable moderation.

## Run locally

Install dependencies with `npm install`, then run `npm run dev`. To create a production bundle, run `npm run build`.

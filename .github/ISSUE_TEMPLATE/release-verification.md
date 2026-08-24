---
name: Release Verification
about: Track that a production release was tested and the team was informed
title: "[RELEASE] YYYY-MM-DD - "
labels: ''
assignees: ''
---

## Release

- **Date deployed to prod:**
- **Services / apps in this release:** _webapp / mobile / ms-* - list them_
- **Release notes (Drive folder):**
- **Deployed by:**

> On the board set **Type: Release**, **Deploy Status: On Prod**, **Platform**, and a **Board index (RH-xx)**.
> This item stays open until every box below is ticked. Do not move it to Done early.

Source: SOP 5.2 Webapp Production Deployment, section 5 - Post-deployment verification.
Run these immediately after deployment, **before telling anyone the release is done**.

---

## 1. Availability

- [ ] `https://apps.readhero.com.my` loads
- [ ] `https://apps.readhero.com.my/staff` loads and admin login succeeds
- [ ] Mobile app connects to production and can log in

## 2. Per-feature smoke tests

_One named check per item in the release notes - the exact action and what you expect to see, not "test the feature"._

- [ ] 
- [ ] 

## 3. Existing data

_Only if this release included migrations._

- [ ] Existing records still load and display correctly
- [ ] Row counts match expectations
- [ ] A record created **before** the migration behaves the same as one created after
- [ ] N/A - no migrations in this release

## 4. Health

- [ ] Inspect > Network shows no failed API calls on the affected pages
- [ ] No 500 / Gateway Timeout / CORS errors on the changed screens
- [ ] Service health endpoints OK for the deployed services

## 5. Sign-off - do not skip

- [ ] Result reported in the internal group
- [ ] **Operations team informed** that the update is live and what changed
- [ ] Tc Fana's approval received - this closes the release

---

## Result

_Pass / Fail. If anything failed, link the issue raised for it and follow SOP 5.2 section 6 - Rollback._

## Evidence / Links

- Release notes:
- Board index (e.g. RH-44):
- Screenshot / recording:

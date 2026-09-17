# Data Quality Validation Checklist

- [ ] Required fields are populated at expected rates (define expected null-rate
      thresholds per field, don't assume 0%).
- [ ] Identity namespace fields contain correctly formatted values (no
      truncation, no encoding errors).
- [ ] Timestamp fields reflect correct timezone handling (a recurring, easy-to-miss
      class of bug — verify against a known source-of-truth event).
- [ ] No duplicate event ingestion at expected volume (check for double-firing
      tags/rules).
- [ ] PII fields claimed to be hashed are verified as genuinely one-way hashed,
      not reversibly encoded (see the consent design doc's "Known Risk Pattern").
- [ ] Cross-system reconciliation: a sample of events/records match between the
      source system and what lands in the CDP (spot-check volume and key field
      values).
- [ ] Historical backfill (if applicable) matches expected volume and date range,
      with no silent gaps.
- [ ] Report suite / analytics-layer numbers reconcile with CDP-layer numbers
      within an explainable tolerance — investigate large discrepancies before
      go-live, not after.

# Annapurna Astro Vastu v1.4.330 — Unified 19-Varga IF–THEN Audit

## Scope

This update starts from the **complete v1.4.329 Flutter project**, retaining all existing calculations, rule registries, data assets, older modules, tests, and 19 varga mappings. It standardizes the **existing** rule-matching display for all 19 vargas. It does **not** purport to implement missing scholarly IF–THEN conditions or independently validate printed source pages.

### Result contract (all 19 vargas)

1. **Matched IF–THEN first**: Only pre-existing computed rules with a tested condition and a nonempty IF and THEN appear in the highlighted section.
2. **Rule → జాతక పరిశీలన → ఫలితం → పరిహారం**: The four-section drill-down applies to matched and audit entries. If a matching source-remedy link is absent, the display explicitly declines to invent a remedy.
3. **Unmatched separate**: A false predicate appears in an expandable inspection area, not as a negative prediction.
4. **Pending separate**: Untested, source-only, missing IF/THEN, or unavailable qualitative checks are labeled pending, not green/pink.
5. **Cross-chart support**: `VARGA-CROSS-*`, `VARGA-GENERAL-004/D*` (Vargottama) and `VARGA-PROTOCOL-*` (D1 SAV) are *inspection evidence only*, even if their supporting arithmetic returns true.
6. **D16 method guard**: Source conditions derived under Parashara are not used as verified results for a separately selected D16 computation method.
7. **No repeated placeholder rule**: Topics without a linked evaluable source show a short truthful message, rather than the same fictitious rule/examination/result in every section.
8. **No new remedies or timing guarantees**: Event years and reliable remedies require independent source-backed input.

## Catalogue coverage — NOT the number of verified outcomes

| Varga | Indexed subjects | Direct IF–THEN source catalogue rows |
|:--|--:|--:|
| D1 | 13 | 0 |
| D2 | 10 | 7 |
| D3 | 8 | 5 |
| D4 | 8 | 5 |
| D5 | 6 | 4 |
| D6 | 7 | 6 |
| D7 | 12 | 7 |
| D8 | 6 | 5 |
| D9 | 11 | 10 |
| D10 | 33 | 8 |
| D12 | 8 | 12 |
| D16 | 7 | 5 |
| D20 | 8 | 3 |
| D24 | 10 | 6 |
| D27 | 7 | 3 |
| D30 | 6 | 4 |
| D40 | 5 | 2 |
| D45 | 5 | 2 |
| D60 | 6 | 3 |
| **Total** | **176** | **97** |

The preserved 255-rule PDF transcription also includes cross-varga workflows, dasha, timing, general and other records. A **direct source-catalogue entry is not necessarily an implemented or verified predicate**. Other previously present factor-specific rule engines can contain additional computed rules beyond this 97-row PDF catalogue. The `VARGA-CROSS` supporting rows do not create a final event result. D5/D6/D8 remain optionally supported by their previously declared calculation method; no alternative Goel calculation has been fabricated.

## Changed existing source files

- `pubspec.yaml`: version `1.4.330+330`.
- `lib/screens/varga_topics_panel.dart`: applies D10's matched-first, unverified-second presentation to every defined varga, and shows all four drill-down sections; no former calculations deleted.

## Added files

- `lib/astrology/varga_rule_match_policy.dart`: central status gate.
- `test/varga_all_19_if_then_policy_v330_test.dart`: match/false/pending, 19 factors, CROSS/SAV/Vargottama and D16 tests.
- `test/varga_four_stage_tap_v330_test.dart`: four-section Flutter widget tests.
- `tool/verify_varga_v330.py`: offline source audit.
- `VERIFY_V330.sh`: compile/test/build verification commands.
- This audit document.

## Verification instructions

In a supported Flutter SDK environment:

```bash
cd astro_app
python3 tool/verify_varga_v330.py
flutter pub get
flutter analyze
flutter test test/varga_all_19_if_then_policy_v330_test.dart
flutter test test/varga_four_stage_tap_v330_test.dart
flutter test
flutter build apk --release
```

**Environment limitation:** The source ZIP was constructed and statically audited without a Flutter SDK in the authoring container. No Flutter compile, widget-test or APK success is claimed by this artifact. APK file size is not guaranteed below 25 MB. The project ZIP is below 25 MB, a different metric.

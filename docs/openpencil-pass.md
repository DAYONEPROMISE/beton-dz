# OpenPencil pass — beton-dz

## Design (Shared/OpenPencil/beton-dz/)
- `design.html` (concrete calculator + dosage chips + result, DZ tokens) → `design.fig`
- `lint --preset accessibility`: 0 errors, 0 warnings

## Code changes
- NEW `DzTheme.kt`: DZ 2026 light/dark M3 schemes + dynamic color + `DzEmptyState`.
- `MainActivity.kt`: wrapped in `DzTheme`; bottom-nav items now have icons + `contentDescription`
  (were `icon = {}`); dosage radio rows use `selectableGroup` + `Role.RadioButton`.

## APKs
`android.yml` builds debug AND release (unsigned), uploads both artifacts, and publishes a
versioned GitHub Release (`v{versionName}-b{run}`) with notes + both APKs.

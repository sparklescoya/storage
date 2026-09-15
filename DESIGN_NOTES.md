# Vehicle Part Inspector — Layout Notes

## Decisions

- **Lead with identity and state.** The part type, name, icon, and installed state share a compact title bar so the player knows what they are inspecting before parsing values.
- **Use progressive disclosure.** Always-relevant properties stay visible; each intrinsic is a row that can open into deeper detail instead of showing a dense matrix of undifferentiated slots.
- **Separate configuration, telemetry, and traits.** The activation binding is presented as a control, remaining fuel as live telemetry, stable facts as stat cards, and intrinsics as a distinct collection.
- **Prefer a list for named traits.** Intrinsics are semantic and text-heavy, so a vertical list scans more reliably than icon-only square tiles and leaves room for the gameplay effect.
- **Build one clear hierarchy.** Section titles, subdued descriptions, labels, and high-contrast values use size and contrast consistently; borders support grouping rather than competing with the content.
- **Keep the primary content dense but touch-safe.** Rows are at least 58 pixels high, the add action is a discrete 32-pixel control, and the entire intrinsic row is interactive.
- **Use color sparingly.** Amber identifies the part/trait system and fuel level, while green is reserved for healthy installed status. Most hierarchy comes from spacing and contrast rather than decoration.
- **Make capacity explicit.** A plain “3 of 5” summary communicates both current loadout and the limit without empty placeholder cards.
- **Adapt instead of shrink.** The desktop split becomes a single column on narrow screens; values remain aligned and readable rather than scaling the whole panel down.
- **Respect platform conventions.** The preview uses semantic HTML, visible keyboard focus, native buttons, reduced-motion preferences, tabular numerals, and familiar keycap/progress treatments.

## Suggested product behavior

- Selecting an intrinsic row should open an inline detail or adjacent inspector, depending on available screen width.
- The add button should open a searchable intrinsic picker and become disabled—with an explanatory tooltip—when all five slots are used.
- Live fuel changes should update the numeric value and meter together; reserve warning colors for thresholds that require player action.

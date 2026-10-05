# Pull Request

## What changed?

Added a JSDoc comment to `emitExecutionFailureAnnotation` in `src/annotations.ts`.
It explains when to use this helper instead of `emitAnnotations` and clarifies
that the annotation does not attach a file/line location.

## Why?

Execution-failure annotations are used when Canary fails to run or produce a
usable report, while `emitAnnotations` annotates individual results in a
report. Documenting the distinction helps callers choose the correct helper
when adding failure paths.

## Tests performed

- [x] `npm run lint`
- [x] `npm run typecheck`

## Related issue

Closes #25

Component: `src/annotations.ts`

## Compatibility impact

None. Documentation-only change; runtime behavior is unchanged.

## Breaking change?

- [ ] Yes — described above
- [x] No

# Cadence

A course platform (a mini Udemy) and the exercise repo for the AI Coding Crash Course.

- **Layering:** requests flow route → service → Drizzle. Services are synchronous functions with positional parameters.
- **Authorisation:** loaders and actions are authorised independently, so every mutating action calls a `require*` guard from `app/lib/access.server.ts` itself.
- **Markdown:** student-authored content renders through `renderComment`, which is XSS-hardened. `renderMarkdown` passes raw HTML through, so it is for instructor-authored content.
- **Server-only code:** modules use the `.server.ts` suffix.
- **Lesson slugs:** checkpoints are commits on `live-run-through`, each prefixed with a slug. Slugs are a public interface consumed by the CLI and referenced in recorded video, so existing slugs stay as they are.

# Next AI Starter - Windsurf Workspace Rules

<core_principles>
- Keep files small (≤500 LOC) and organized in clear hierarchies.
- Prefer functional components and typed interfaces.
- Always update top-of-file docs after edits to maintain lightweight context for future agents.
- After all changes, always run `npm run build`. Ignore warnings, fix errors.
</core_principles>

<frontend_nextjs_react_typescript>
- Components live in `src/components/`, PascalCase, functional only. Add `"use client"` only where required.
- Styling: Tailwind only. Extend tokens in `tailwind.config.ts`.
- Animations: Prefer Framer Motion.
- Never use Radix or shadcn.
- Icons: Prefer `lucide-react` and PascalCase names. Custom icons in `src/components/icons`.
- Notifications: `react-toastify` in client components (`toast.success()`, `toast.error()`).
- Routing: Next.js App Router in `app/`, kebab-case filenames. Server components by default.
</frontend_nextjs_react_typescript>

<backend_prisma_trpc_inngest>
- Prisma schema in `prisma/schema.prisma`, DB client in `src/lib/db.ts`.
- Tables are snake_case in DB, fields are camelCase in Prisma.
- No raw SQL.
- Use `npx prisma migrate dev`. Never use `npx prisma db push`.
- tRPC routers in `src/lib/api/routers/`, composed in `src/lib/api/root.ts`.
- Use `publicProcedure`/`protectedProcedure` with Zod.
- Access from React via `@/lib/trpc/react`.
- Inngest config in `inngest.config.ts`, API route in `src/app/api/inngest/route.ts`.
- Update UI via polling when events complete, not via tRPC success responses.
</backend_prisma_trpc_inngest>

<typescript_conventions>
- Strict mode, avoid `any`.
- Use optional chaining and union types (no enums).
- Shared types in `src/lib/types.ts`.
- Reusable logic in `src/lib/utils/shared.ts` (client) or `src/lib/utils/server.ts` (server).
- Sort imports: external → internal → sibling → styles.
</typescript_conventions>

<ai>
- AI calls go through `generateChatCompletion` in `src/lib/aiClient.ts`.
- Prefer `GPT-5`.
</ai>

<storybook>
- Stories in `src/stories/` with `.stories.tsx` extension.
- One story file per component, name matched.
- Use autodocs; include variants and sizes; test interactivity with actions.
- Use relative imports from component directory.

</storybook>


# Agent Helpers

- Refer to the `agent-helpers` folder for additional instructions and tools.
- Use the `agent-helpers` folder to store any files that you want future agents to have access to.
- Start with `agent-helpers/README.md` for instructions.
- Keep agent helper files concise and focused on specific tasks or domains.
- Organize helpers by functionality or domain for easy discovery.
- Document each helper's purpose and usage in its file comments.
- Ensure helper files are self-contained and easy to understand.
- Avoid duplicating logic that already exists in other helper files.
- Reuse existing helpers when possible to maintain consistency.
- Keep helper files modular and testable.
- Write clear, concise comments explaining the purpose and usage of each helper.
- Keep helper files focused on single responsibilities.
- Maintain a consistent naming convention for helper files.
- Version control helper files to track changes and improvements.
- Regularly review and update helper files to ensure they remain relevant and effective.
- Share helper files across agents to promote code reuse and consistency.
- Document the intended use cases and limitations of each helper file.
- Test helper files thoroughly before sharing them across agents.
- Keep helper files up-to-date with the latest project changes and requirements.


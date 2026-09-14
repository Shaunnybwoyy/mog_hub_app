# AGENTS.md

## Project overview
This workspace is intended to be a React Native / Expo application. Keep changes aligned with the Expo toolchain, TypeScript defaults, and a mobile-first user experience.

## Working conventions
- Prefer small, focused changes over broad rewrites.
- Use TypeScript for new code unless the existing project clearly uses plain JavaScript.
- Favor functional React components, hooks, and clear prop types.
- Keep styling consistent with Expo/React Native patterns; prefer reusable style objects or shared style files when the app grows.
- When adding dependencies, check whether the project already has the needed package patterns before introducing a new library.

## Commands to use
Typical commands for an Expo app are:
- `npm install`
- `npx expo start`
- `npx expo start --android`
- `npx expo start --ios`
- `npx expo export` for production builds when needed
- `npx expo lint` if a lint script is configured

Use the project’s actual scripts from `package.json` when they exist; they are the source of truth for local development.

## Architecture guidance
- Keep app screens, shared UI, hooks, and utilities separated by feature or responsibility.
- Prefer routing, state, and data access patterns already present in the project rather than adding new abstractions.
- If a feature touches both UI and logic, keep the boundary clear and avoid mixing unrelated responsibilities in the same file.
- Maintain compatibility with Expo-managed assets, config files, and native module expectations.

## Before making changes
1. Inspect `package.json` and the existing app structure before adding scripts, packages, or new screen patterns.
2. Match the project’s naming and folder conventions instead of introducing a different pattern.
3. Prefer incremental edits that preserve current user flows and app structure.

## Quality bar
- Keep code readable and maintainable.
- Ensure TypeScript and Expo compatibility for all new code.
- Validate the relevant workflow after changes with the smallest practical command (for example, a focused app run or a lint/type check if configured).
- Avoid unnecessary platform-specific code unless the feature truly requires it.

## When in doubt
Prefer the conventions already established by the repo over generic boilerplate. If the project layout is still being created, default to a clean Expo + TypeScript structure and keep the implementation minimal and predictable.

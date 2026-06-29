# UI Smith

UI Smith helps developers scaffold production-ready, accessible web UI component kits from headless primitives without starting from a blank design-system implementation.

## Language

**Agent Skill**:
A coding-agent workflow that helps a developer scaffold project-owned UI component code.
_Avoid_: npm UI library, design-system package, template repo, lifecycle manager

**Coding Agent**:
An AI-assisted software development tool that can read a repository, edit files, run commands, and follow project-specific instructions.
_Avoid_: chatbot, assistant, code generator

**Component Kit**:
A project-owned set of reusable UI components that an application imports locally and customizes for its product interface.
_Avoid_: component library, theme, template

**Component Kit Root**:
The top-level folder of a Component Kit where kit-wide artifacts live, such as shared tokens, the Kit README, and shared Integration Layer files.
_Avoid_: app root, component folder, artifact dump

**Normalized Kit Layout**:
The fixed internal structure UI Smith uses inside a Component Kit Root: flat Component Folders, lowercase/kebab-case file names, component-local artifacts, kit-root shared artifacts, and Explicit Component Imports.
_Avoid_: host convention mirror, flat component list, barrel layout

**Component Layout Conflict**:
A planning conflict where an existing host repository file or component collides with UI Smith's Normalized Kit Layout target path or component name.
_Avoid_: silent overwrite, implicit adoption, automatic move

**Component Folder**:
The single folder that owns one component's source and all of its per-component artifacts, including its contract, brief, examples, tests, stories, and verification notes.
_Avoid_: flat component file, shared component artifact folder, barrel module

**Explicit Component Import**:
An import that names the concrete component file inside a Component Folder, using the host repository's alias when available and a relative path otherwise, instead of importing through a barrel file or directory index.
_Avoid_: barrel import, folder import, root kit import

**Base UI Primitive**:
An unstyled React component part from Base UI that provides accessibility, interaction behavior, and composition hooks.
_Avoid_: styled component, visual component, widget

**React Component Kit**:
A Component Kit scaffolded for React applications, written in TypeScript, and built on Base UI Primitive behavior.
_Avoid_: framework-agnostic kit, Vue kit, Svelte kit

**App-Owned Component Source**:
Scaffolded component code that lives inside the developer's application repository and is owned by that application team immediately after scaffolding.
_Avoid_: dependency wrapper, hosted UI package, black-box component library, generated-by source marker

**Styling Contract**:
The stable customization surface a Component Kit exposes for product teams to change visual design without replacing component behavior.
_Avoid_: theme only, CSS implementation, visual skin

**Design Token**:
A named value for a design decision, such as color, spacing, radius, typography, or motion, that components consume through the Styling Contract.
_Avoid_: hard-coded style, Tailwind class, CSS variable

**Production-Ready Component**:
A scaffolded component with accessible behavior, typed APIs, expected interactive states, tokenized styling, and enough Verification Evidence for a developer to trust it in an application.
_Avoid_: pretty demo, starter snippet, accessibility-certified component

**Verification Evidence**:
The tests, checks, examples, and review artifacts that show a scaffolded component behaves correctly enough to be trusted.
_Avoid_: guarantee, certification, manual confidence

**Test-Backed Generation**:
A scaffolding workflow that creates relevant tests for scaffolded components whenever the host repository has a compatible test setup.
_Avoid_: checklist-only generation, unverified output, test framework installer

**First Component Set**:
The bounded initial group of components UI Smith uses to prove the Component Kit workflow before expanding into more complex components.
_Avoid_: complete design system, every Base UI component, arbitrary component backlog

**Primitive-Backed Component**:
A scaffolded component whose interaction behavior and accessibility foundation come from a Base UI Primitive.
_Avoid_: semantic component, native-only component, custom behavior component

**Semantic Component**:
A scaffolded component that uses native HTML and ARIA semantics with the shared Styling Contract, but is not backed by a Base UI Primitive.
_Avoid_: primitive-backed component, Base UI wrapper, fake primitive

**Host Repository Convention**:
An existing pattern in the target application repository for component location, naming, styling, imports, tests, or documentation that UI Smith should preserve when scaffolding App-Owned Component Source.
_Avoid_: UI Smith default, preferred template, external standard

**Generation Plan**:
The proposed set of files, dependencies, styling assumptions, component choices, Deterministic Generation Contracts, and Verification Evidence that UI Smith presents before scaffolding App-Owned Component Source.
_Avoid_: hidden assumptions, automatic write, setup summary

**Dependency Change**:
Any package installation, removal, upgrade, or lockfile update that UI Smith proposes for the host repository.
_Avoid_: scaffolded source file, configuration note, implicit prerequisite

**Kit Manifest**:
A project file that records a Component Kit's Component Inventory, scaffold provenance, Styling Contract summary, selected contract provenance, and AI-facing usage guidance.
_Avoid_: package manifest, lifecycle state, upgrade tracker, generator cache

**Component Inventory**:
The authoritative-but-verifiable part of a Kit Manifest that tells Coding Agents which project components exist, where their concrete artifact paths are, and how they should be imported and used.
_Avoid_: Storybook catalog, marketing docs, import guesswork, invented imports, inferred paths

**Artifact Status**:
The explicit state recorded for a component artifact path in the Component Inventory so Coding Agents can understand component setup progress.
Allowed states are scaffolded, pending-agent-authoring, pending-approval, not-requested, unsupported, and skipped.
_Avoid_: missing path, implicit absence, boolean flag

**Component Setup Status**:
The top-level readiness state for a component in the Component Inventory, summarizing whether the component is planned, in-progress, blocked, ready, or skipped.
_Avoid_: inferred readiness, lifecycle state, test status

**Manifest Pointer**:
A short instruction in an agent-facing project file that tells Coding Agents where to find the Kit Manifest.
_Avoid_: hidden config, tribal knowledge, README-only instruction

**Manifest Schema**:
The strict JSON contract that defines the structure and meaning of a Kit Manifest.
_Avoid_: informal config shape, JSONC comments, ad hoc manifest

**Scaffold Provenance**:
The record of which UI Smith generation rules, Base UI version, Design Source, and Deterministic Generation Contracts were used for the initial scaffold.
_Avoid_: upgrade metadata, lifecycle state, drift tracking

**Visual Presentation**:
Optional scaffolded examples or Storybook stories that show a Component Kit's components, variants, and states for human inspection.
_Avoid_: production dependency, required runtime, test replacement

**Accessibility Verification**:
The layered checks UI Smith uses to show that a scaffolded component preserves accessible behavior, keyboard interaction, focus handling, labels, and valid semantics.
_Avoid_: accessibility certification, Base UI guarantee, visual review only

**Dual-Layer Component API**:
A scaffolded component API that offers ergonomic app-facing components for common use and lower-level composable parts for advanced Base UI composition.
_Avoid_: thin wrapper only, closed abstraction, primitive-only API

**App-Facing Component**:
The default import a product developer uses for common application UI without needing to assemble every Base UI part manually.
_Avoid_: primitive part, raw Base UI export, internal wrapper

**Composable Part**:
A lower-level exported component or part that lets developers customize structure while keeping the Component Kit's behavior and Styling Contract.
_Avoid_: private implementation detail, one-off escape hatch, fork

**Variant System**:
The typed styling API that maps component props such as size, intent, tone, or density to classes and Design Tokens.
_Avoid_: one-off class maps, visual-only props, theme replacement

**Variant Utility**:
A helper library or local utility used to implement the Variant System consistently across scaffolded components.
_Avoid_: required dependency, hidden styling logic, component-specific mapper

**App-Owned Design Tokens**:
Design Tokens that live in the host repository and are owned by the application team, whether introduced by UI Smith or mapped from existing project tokens.
_Avoid_: UI Smith theme, remote preset, hard-coded visual identity

**Neutral Visual Default**:
A restrained, production-oriented initial style that components use before the application team customizes the underlying App-Owned Design Tokens.
_Avoid_: brand preset, style theme marketplace, barebones styling

**Design Source**:
The best available host repository source for visual design decisions, starting with `DESIGN.md` when present and falling back to existing CSS variables, Tailwind theme values, or other token files.
_Avoid_: agent guess, visual preference prompt only, hard-coded default

**Token Customization Workflow**:
A guided UI Smith workflow that imports App-Owned Design Tokens from the Design Source when possible and asks structured questions when the host repository does not already define enough visual decisions.
_Avoid_: manual-only token editing, theme preset selection, ungrounded styling

**Design Documentation Standard**:
The required structure and quality bar for `DESIGN.md` when UI Smith creates or updates the host repository's Design Source.
It covers design principles, Design Tokens, component styling rules, accessibility rules, responsive rules, and concrete do/avoid guidance.
_Avoid_: loose style notes, mood board, undocumented token choices

**Integration Layer**:
The minimal scaffolded support code a Component Kit needs to work in the host repository, such as shared utilities, token CSS, exports, or required providers.
_Avoid_: app scaffold, framework rewrite, unrelated infrastructure

**Shared Kit Utility**:
A Component Kit Root helper used by multiple Component Folders for common implementation concerns such as class composition, but not for re-exporting components.
_Avoid_: barrel file, component registry, dumping ground

**Form-Library-Neutral Component**:
A form-related scaffolded component that works with standard React props, native form semantics, and Base UI Field behavior without requiring a specific form library.
_Avoid_: React Hook Form component, TanStack Form component, form framework wrapper

**Form Adapter Example**:
Optional usage guidance that shows how Form-Library-Neutral Components connect to a detected host repository form library.
_Avoid_: required adapter, generated form framework, default form stack

**Framework-Aware Generation**:
A scaffolding workflow that adapts Component Kit files, imports, client boundaries, CSS entry points, examples, and tests to the host repository's detected React framework.
_Avoid_: generic-only generation, framework-specific skill fork, blind file output

**Scaffold-First Generation**:
A UI Smith workflow that creates a strong initial Component Kit once, then treats all later component changes as ordinary app-owned development outside UI Smith's responsibility.
_Avoid_: lifecycle management, ongoing component manager, automatic upgrade workflow

**Kit README**:
A human-readable guide scaffolded near the Component Kit that explains available components, usage rules, customization points, verification commands, and how Coding Agents should respect the Kit Manifest.
_Avoid_: inline generated comments, marketing docs, schema replacement

**Hybrid Generation**:
A UI Smith scaffolding workflow where deterministic contracts define the allowed output shape, constraints, manifest updates, dependency behavior, and verification requirements, while a Coding Agent authors or adapts the App-Owned Component Source within those constraints.
_Avoid_: static-template-only generation, unconstrained AI generation, one-shot code generation

**Deterministic Generation Contract**:
The non-negotiable rules UI Smith gives a Coding Agent before component scaffolding, including Base UI Primitive requirements, Styling Contract, Component Inventory updates, Dependency Change rules, file ownership, and Verification Evidence expectations.
_Avoid_: prompt suggestion, loose guidance, implementation template

**LLM-Authored Component Source**:
App-Owned Component Source written or adapted by a Coding Agent under a Deterministic Generation Contract rather than copied directly from a fixed static template.
_Avoid_: arbitrary generated code, static template output, unchecked AI code

**Contract Brief**:
A human- and agent-readable Markdown explanation paired with a machine-checkable Deterministic Generation Contract to clarify intent, examples, and tradeoffs without replacing the JSON source of truth.
_Avoid_: README-only contract, prompt-only instruction, informal generation note

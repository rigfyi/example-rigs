# Rigfyi Example Rigs

Official starter rigs maintained by [Rigfyi](https://rig.fyi). These are editable examples of useful agent workflows, not claims about adoption or performance.

| Rig | Purpose | Manifest |
| --- | --- | --- |
| [Coding Starter](coding-starter/) | Small, verified feature changes and bug fixes | [rig.json](coding-starter/rig.json) |
| [Frontend Builder](frontend-builder/) | Responsive interfaces and accessibility | [rig.json](frontend-builder/rig.json) |
| [Research Assistant](research-assistant/) | Source-backed research with explicit uncertainty | [rig.json](research-assistant/rig.json) |
| [Code Reviewer](code-reviewer/) | Concrete correctness and security findings | [rig.json](code-reviewer/rig.json) |

## Use an example

1. Download or clone this repository and choose one example.
2. Install and authenticate Codex using its official documentation. These examples use your existing model and account configuration; they contain no credentials or fixed model selection.
3. In your target project, copy the selected `skills/<skill-name>` directory into `.agents/skills/<skill-name>`. Review and merge the selected `AGENTS.md` into your project's existing instructions. Preserve the project's own requirements.
4. Open Codex in that project and try the prompt in the example's README. Check the result before relying on it.

For example, from this repository's root, with an existing target project:

```sh
mkdir -p /path/to/your-project/.agents/skills
cp -R coding-starter/skills/implementation /path/to/your-project/.agents/skills/
```

Review the example's `AGENTS.md` and merge its guidance manually. Do not overwrite existing files or skills unintentionally.

## Import into Rigfyi

With the Rigfyi CLI installed, import a single manifest from this repository's root:

```sh
rigfyi import coding-starter/rig.json
rigfyi inspect coding-starter
```

Repeat with the other manifests to create four separate rigs. Importing a manifest records its configuration; it does not by itself install the skill files into your target project.

The current GitHub repository importer discovers skills and instruction files across an entire repository and combines them into one rig. To keep these examples separate, import the individual JSON manifests instead of importing this whole repository four times.

## Publish official examples

Sign into Rigfyi with the maintainer account, enable its public profile, and push each imported rig to that account. Review the public preview in Rigfyi before publishing. Manifests remain private until explicitly published; their runtime, skills, and instructions are marked shareable, while model details remain private.

```sh
rigfyi login
rigfyi whoami
rigfyi push coding-starter
```

Verify that `whoami` shows the intended maintainer before pushing. Repeat for the remaining rig names, then preview and publish them through Rigfyi. Publishing is a separate step from creating this GitHub repository.

## Scope

These examples bundle original instructions and skills only. They do not install MCP servers, invoke paid services, or promise automatic deployment. Research needs browsing tools for current source verification; frontend visual checks need browser tools. Each skill explains how to disclose unavailable verification.

## Contributing

Keep each example focused on a practical workflow. Update the manifest when paths change, keep instruction content in sync with its `AGENTS.md`, and validate against the `rigfyi/v1` schema before publishing.

## License

MIT. See [LICENSE](LICENSE).

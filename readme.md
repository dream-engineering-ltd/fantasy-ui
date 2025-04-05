# Fantasy UI

Generate flexible, custom components for any frontend.

- CLI based
- Framework agnostic
- Fantasy UI App for component customization
- Non magical
- Small

Warning: Early work in progress!

- Current list of components is small, but growing by the day
- Initial releases will be React components, Svelte components are coming next
- FantasyUI app beta will release in summer 2025
- Your early feedback is wanted! Feel free to file a github issue

## Install

Install globally:
`npm i -g @dream-eng/fantasy-ui`

Or keep it scoped to your local project by adding this to your package.json scripts:
`"fantasy": "npx @dream-eng/fantasy-ui",`

Get help:
`fantasy help`

## Configure

Initialize with:
`fantasy setup`

This generates a `fantasy.toml` config file in your project root. You can specify:

- `base_dir`: directory for read-only base components
- `extended_dir`: which directory to extend base components
- `flavor`: generate component code using this framework + language
- `library_id`: for syncing with Fantasy UI App (optional)

The custom component directory is where you can extend and/or compose base components for intricate customization.

On initialization, `fantasy setup` will also create a read-only directory for the base components called `fantasy-ui`. These component files are NOT meant to be edited, and are simply for you to track style changes synced from the Fantasy UI App. Using the Fantasy UI Designer app is optional.

## Adding base components

You can add components with `fantasy add <component>`. Refer to the documentation for the full list of component names.

The component code will be generated in the base_dir, and is intended to be read-only. This code is copied into your project and is dependency free. It has several advantages:

- lightweight, does not add to node_modules
- ability to track history with git (or source control tools you already use)
- can still be updated/patched with latest version from CLI
- gives you full control

## Extending base components

`fantasy extend <component>` will create a new file in the dir you specified in the fantasy config file (extended_dir field).

This is useful for modifying the markup structure of complex components that are usually abstracted away in other popular libraries. You can also customize the logic and state.

## Fantasy UI App (summer 2025)

We offer a GUI for customizing the styles of each base component. You can publish a version and run `fantasy sync` to pull down the style changes into your base components.

The style changes will also be reflected in components you have extended.

### Workflow

1. Developer uses fantasy-ui base components in project.
2. Developer/Designer/Stakeholder publishes style changes using fantasyUI Designer
3. Developer syncs new style changes into local project and commits to source control.
4. Developer deploys new code as usual.

This workflow is designed to keep you in control of the code, while allowing stakeholders to change the appearance of components as they wish without introducing breaking changes. You are able to review all style changes and deploy at your discretion.

## Release progress for react

Rolling out weekly releases! What components would you like to see next? Drop a line in a github issue https://github.com/dream-engineering-ltd/fantasy-ui

- [x] Button
- [x] Card
- [x] Badge
- [x] Input
- [x] Label
- [x] ProgressBar
- [x] Slider
- [x] Textarea
- [ ] Select
- [ ] Avatar
- [ ] Switch
- [ ] Tooltip
- [ ] Rating

## Learn more

Stay up to date via our newsletter https://fantasy-ui.com

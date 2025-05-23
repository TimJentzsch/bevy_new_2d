# Bevy New 2D

This template is a great way to get started on a new 2D [Bevy](https://bevyengine.org/) game!
Start with a [basic project](#write-your-game) and [CI / CD](#release-your-game) that can deploy to [itch.io](https://itch.io).
You can [try this template in your browser!](https://the-bevy-flock.itch.io/bevy-new-2d)

## Prerequisites

We assume that you're familiar with Bevy and have already seen the [official Quick Start Guide](https://bevyengine.org/learn/quick-start/introduction/).

If you're new to Bevy, the patterns used in this template may look a bit weird at first glance.
See our [Design Document](./docs/design.md) for more information on how we structured the code and why.

## Create a new game

Install [`bevy_cli`](https://github.com/TheBevyFlock/bevy_cli/) and run the following command:

```sh
bevy new my_game --template 2d
```

Then [create a GitHub repository](https://github.com/new) and push your local repository to it.

## Write your game

The best way to get started is to play around with the code you find in [`src/demo/`](./src/demo).

This template comes with a basic project structure that you may find useful:

| Path                                               | Description                                                        |
| -------------------------------------------------- | ------------------------------------------------------------------ |
| [`src/lib.rs`](./src/lib.rs)                       | App setup                                                          |
| [`src/asset_tracking.rs`](./src/asset_tracking.rs) | A high-level way to load collections of asset handles as resources |
| [`src/audio.rs`](./src/audio.rs)                   | Marker components for sound effects and music                      |
| [`src/demo/`](./src/demo)                          | Example game mechanics & content (replace with your own code)      |
| [`src/dev_tools.rs`](./src/dev_tools.rs)           | Dev tools for dev builds (press \` aka backtick to toggle)         |
| [`src/screens/`](./src/screens)                    | Splash screen, title screen, gameplay screen, etc.                 |
| [`src/theme/`](./src/theme)                        | Reusable UI widgets & theming                                      |

Feel free to move things around however you want, though.

> [!TIP]
> Be sure to check out the [3rd-party tools](./docs/tooling.md) we recommend!

## Run your game

We recommend using the [Bevy CLI](https://github.com/TheBevyFlock/bevy_cli) to run your game.

Running your game locally is very simple:

- Use `bevy run` to run a native dev build.
- Use `bevy run web` to run a web dev build.

This template also comes with [VS Code tasks](./.vscode/tasks.json) and [JetBrains run configurations](./.idea/runConfigurations/)
to help run your game from your IDE.

<details>
  <summary>Run release builds</summary>

- Use `bevy run --release` to run a native release build.
- Use `bevy run --release web` to run a web release build.

</details>

<details>
  <summary>Linux dependencies</summary>

If you're using Linux, make sure you've installed Bevy's [Linux dependencies](https://github.com/bevyengine/bevy/blob/main/docs/linux_dependencies.md).
Note that this template enables Wayland support, which requires additional dependencies as detailed in the link above.
Wayland is activated by using the `bevy/wayland` feature in the [`Cargo.toml`](./Cargo.toml).

</details>

<details>
    <summary>(Optional) Improve your compile times</summary>

[`.cargo/config_fast_builds.toml`](./.cargo/config_fast_builds.toml) contains documentation on how to set up your environment to improve compile times.
After you've fiddled with it, rename it to `.cargo/config.toml` to enable it.

</details>

## Release your game

This template uses [GitHub workflows](https://docs.github.com/en/actions/using-workflows) to run tests and build releases.
See [Workflows](./docs/workflows.md) for more information.

## Known Issues

There are some known issues in Bevy that can require arcane workarounds.
To keep this template simple, we've opted to leave these workarounds out.
You can read about them in the [Known Issues](./docs/known-issues.md) document.

## License

The source code in this repository is licensed under any of the following at your option:

- [CC0-1.0 License](./LICENSE-CC0-1.0.txt)
- [MIT License](./LICENSE-MIT.txt)
- [Apache License, Version 2.0](./LICENSE-Apache-2.0.txt)

The CC0 license explicitly does not waive patent rights, but we confirm that we hold no patent rights to anything presented in this repository.

## Credits

The [assets](./assets) in this repository are all 3rd-party. See the [credits screen](./src/screens/credits.rs) for more information.

# seoul256-herdr

[seoul256](https://github.com/junegunn/seoul256.vim) dark and light colors for
[herdr](https://github.com/herdrdev/herdr).

herdr has no theme files: it reads colors only from `config.toml`. So this repo
is a snippet to copy into your config.

## Install

1. Remove the `[theme]` section (and any `[theme.*]` tables) from
   `~/.config/herdr/config.toml`.
2. Add the snippet:

   ```sh
   curl -fsSL https://raw.githubusercontent.com/bewa1t/seoul256-herdr/main/seoul256.toml >> ~/.config/herdr/config.toml
   ```

3. Check and apply it:

   ```sh
   herdr config check
   herdr server reload-config
   ```

herdr uses the light colors when the terminal reports a light appearance, and
the dark colors otherwise. For a matching terminal, see
[seoul256-rio](https://github.com/bewa1t/seoul256-rio).

## Colors

The snippet sets every herdr color token, so the base theme does not matter.
All colors come from seoul256.vim's default color map:

- Text and backgrounds use seoul256's foreground and background shades. The
  sidebar keeps the terminal background (`sidebar_bg = "reset"`).
- The Navigate cursor row uses Vim's `Visual` color.
- Muted text uses greys between the foreground and the background, so it stays
  readable in both modes. herdr's built-in `terminal` theme uses ANSI white for
  muted text, which is lighter than the background in seoul256-light.

Tested with herdr 0.9.5.

## License

MIT. The colors are from seoul256.vim, Copyright (c) 2017 Junegunn Choi.

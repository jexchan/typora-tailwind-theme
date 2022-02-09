# Tailwind theme for Typora

An implementation of the beautifull [Tailwind Typography](https://tailwindcss.com/docs/typography-plugin) layout for [Typora](https://typora.io):

![Screenshot of the Tailwind theme](tailwind-screenshot.png)

A light and dark theme are provided, which use the `prose-xl` class and `slate` color scheme. In particular, the themes are equivalent to:

```html
<article class="prose prose-xl prose-slate dark:prose-invert dark:bg-slate-800">
  ...
</article>
```

**NB: This theme is still a work in progress**. Refer to the [issues page](https://github.com/andredelft/typora-tailwind-theme/issues) for a rundown of to-do's.

## Installation

1. Go to the Typora theme folder (reachable via the settings menu: Appearance > Open theme folder)
2. Copy `typora.css` and `typora-dark.css` into this folder.
3. Restart Typora and select either theme from the 'Theme' menu.

## Customization

As with any theme, the Tailwind and Tailwind Dark themes can be customized by defining rules in `tailwind.user.css` and `tailwind-dark.user.css` respectively. In this particular case, `tailwind.user.css` will also be imported by the Tailwind Dark theme, such that customizations will be applied uniformly. If one only wants to target the light theme, rules can be defined in `tailwind-light.user.css`.

### Color scheme

The `slate` color scheme can be modified by overriding the `--theme-X` variables in `tailwind.user.css` as follows:

```css
:root {
  /* Zinc color scheme */
  --theme-50: #fafafa;
  --theme-100: #f4f4f5;
  --theme-200: #e4e4e7;
  --theme-300: #d4d4d8;
  --theme-400: #a1a1aa;
  --theme-500: #71717a;
  --theme-600: #52525b;
  --theme-700: #3f3f46;
  --theme-800: #27272a;
  --theme-900: #18181b;
}
```

Note that both the light and dark theme automatically adjust to this color scheme.

Refer to the [Tailwind docs](https://tailwindcss.com/docs/background-color) for other color schemes (or define your own).

### Font

The default Tailwind font is [Inter](https://rsms.me/inter). Other fonts can be used as follows:

```css
#write {
  font-family: "Crimson Pro";
  font-size: 1.5rem;
}
```

I personally find that the Tailwind theme works very well with a serif font like [Crimson Pro](https://fonts.google.com/specimen/Crimson+Pro).

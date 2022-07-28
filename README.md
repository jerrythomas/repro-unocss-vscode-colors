# repro-unocss-vscode-colors

Minor issues when using `unocss-vscode` plugin.

- Unknown rule @apply
- Unknown rule @layer
- Colors defined using variables don't show the actual color

As an example, the configuration below does not show the color preview.

```js
 theme: {
    colors: {
      primary: {
        DEFAULT: 'hsl(var(--primary-500))',
        50: 'hsl(var(--primary-50))',
        100: 'hsl(var(--primary-100))'
      },
    },
  }
```

The preview shown on hovering over the "bg-primary-100" class is below.

```css
/* layer: default */
.bg-primary-200 {
  --un-bg-opacity: 1;
  bg-color: hsla(var(--primary-100), var(--un-bg-opacity));
}
```

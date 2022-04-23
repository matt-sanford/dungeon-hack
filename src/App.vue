<template>
  <router-view/>
</template>

<style lang="scss">
  // CSS Reset
  *, *:before, *:after{
    box-sizing: border-box;
  }

  html, body, div, span, object, iframe, figure,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, code, em, img, small, strike, strong, sub,
  sup, tt, b, u, i, ol, ul, li, fieldset, form,
  label, table, caption, tbody, tfoot, thead,
  tr, th, td, main, canvas, embed, footer, header,
  nav, section, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
    text-rendering: optimizeLegibility;
    -webkit-font-smoothing: antialiased;
    text-size-adjust: none;
  }

  footer, header, nav, section, main {
    display: block;
  }

  body {
    line-height: 1;
  }

  ol, ul {
    list-style: none;
  }

  blockquote, q {
    quotes: none;
  }

  blockquote:before, blockquote:after, q:before, q:after {
    content: '';
    content: none;
  }

  table {
    border-collapse: collapse;
    border-spacing: 0;
  }

  input {
    -webkit-appearance: none;
    border-radius: 0;
  }

  :root {
    --background: #272744;
    --dark: #494d7e;
    --accent: #8b6d9c;
    --medium: #c69fa5;
    --light: #f2d3ab;
    --font: #fbf5ef;
  }

  body {
    background-color: var(--background);
  }
</style>

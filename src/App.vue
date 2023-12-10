<template>
  <router-view />
</template>

<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@700&display=swap"
  rel="stylesheet"
/>

<style>
:root {
  /* Colors */
  --primary: hsl(172, 67%, 45%);
  --white: hsl(0, 0%, 100%);
  --neutral-1: hsl(183, 100%, 15%);
  --neutral-2: hsl(186, 14%, 43%);
  --neutral-3: hsl(184, 14%, 56%);
  --neutral-4: hsl(185, 41%, 84%);
  --neutral-5: hsl(189, 41%, 97%);
  --red: hsl(14, 78%, 55%);

  /* Breakpoints */
  --bp-mobile: 375px;
  --bp-desktop: 1440px;

  /* Typography */
  --font-input: 24px;
  --font-desc: 20px;
  --font-weight: 700;

  /* Borders */
  --border-radius: 20px;
  --input-radius: 6px;
  --input-border-size: 3px;

  /* Paddings & Margins */
  --big-padding: 30px;
  --input-padding: 10px;

  /* Animations   */
  --main-transition: 0.2s ease;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: var(--neutral-4);
  font-family: 'Space Mono', monospace;
  box-sizing: border-box;
}

input {
  overflow: hidden;
}

.upper-margin-sm {
  margin-top: 10px;
}

.upper-margin-lg {
  margin-top: 50px;
}
</style>

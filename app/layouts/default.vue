<template>
  <div>
    <header>
      <h1>My Nuxt Site</h1>

      <nav>
        <NuxtLink to="/">トップ</NuxtLink>
        |
        <NuxtLink to="/about">About</NuxtLink>
      </nav>
    </header>

    <main>
      <slot />
    </main>

    <footer>
      <p>© My Nuxt Site</p>
    </footer>
  </div>
</template>

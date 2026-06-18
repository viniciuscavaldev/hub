<template>
  <q-layout view="hHh lpR fff" class="hub-shell">
    <div class="hub-brand-header text-white q-py-sm">
      <div class="hub-brand-header__bg" aria-hidden="true" />
      <div class="hub-brand-header__inner">
        <div class="hub-brand-header__col hub-brand-header__col--left">
          <img
            class="hub-brand-header__logo"
            src="/images/logo_white.svg"
            width="291"
            height="64"
            alt="Hapvida"
          >
        </div>
        <div class="hub-brand-header__center">
          <p class="hub-brand-header__slogan">
            Sua vida pede um plano que cresce junto com você.
          </p>
        </div>
          <p class="hub-brand-header__credit-inline">
            Desenvolvido por: Caio Costa
          </p>
        <div class="hub-brand-header__col hub-brand-header__col--right" aria-hidden="true" />
      </div>
    </div>

    <q-page-container class="hub-shell__container">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style scoped lang="scss">
.hub-shell.q-layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  max-height: 100vh;
  min-height: 100dvh;
  max-height: 100dvh;
  overflow: hidden;
  background: #f1f5f9;
}

.hub-brand-header {
  position: relative;
  overflow: hidden;
  flex-shrink: 0;
  background: linear-gradient(165deg, #1539aa 0%, #0d2670 52%, #0a1f5c 100%);
}

.hub-brand-header__bg {
  position: absolute;
  inset: 0;
  opacity: 0.5;
  background-image:
    radial-gradient(circle at 15% 40%, rgba(255, 255, 255, 0.12) 0%, transparent 45%),
    radial-gradient(circle at 90% 60%, rgba(255, 77, 0, 0.1) 0%, transparent 40%);
  pointer-events: none;
}

.hub-brand-header__inner {
  position: relative;
  z-index: 1;
  display: grid;
  grid-template-columns: minmax(9rem, 1fr) minmax(0, auto) minmax(9rem, 1fr);
  align-items: center;
  gap: 0.35rem;
  min-height: 3.25rem;
  padding: 0.45rem 1rem;
  max-width: 80rem;
  margin: 0 auto;
}

.hub-brand-header__col {
  display: flex;
  align-items: center;
  min-width: 0;
}

.hub-brand-header__col--left {
  justify-content: flex-start;
}

.hub-brand-header__col--right {
  justify-content: flex-end;
}

.hub-brand-header__center {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.2rem;
  justify-self: center;
  min-width: 0;
}

.hub-brand-header__credit-inline {
  margin: 0;
  font-size: clamp(0.65rem, 1.5vw, 0.72rem);
  font-weight: 500;
  opacity: 0.88;
  text-align: center;
  color: rgba(248, 250, 252, 0.92);
}

.hub-brand-header__logo {
  display: block;
  height: clamp(1.75rem, 4.5vw, 2.35rem);
  width: auto;
  max-width: 11rem;
  object-fit: contain;
}

.hub-brand-header__slogan {
  margin: 0;
  max-width: min(38rem, 86vw);
  font-size: clamp(0.88rem, 2.1vw, 1.2rem);
  font-weight: 600;
  line-height: 1.35;
  letter-spacing: -0.02em;
  text-align: center;
  text-wrap: balance;
  color: rgba(248, 250, 252, 0.98);
}

@media screen and (max-width: 520px) {
  .hub-brand-header__inner {
    grid-template-columns: 1fr;
    grid-template-rows: auto auto;
    justify-items: center;
    gap: 0.5rem;
    min-height: 4.75rem;
    padding: 0.65rem 0.75rem;
  }

  .hub-brand-header__col--left {
    justify-content: center;
  }

  .hub-brand-header__col--right {
    display: none;
  }

  .hub-brand-header__logo {
    max-width: 10rem;
    height: 2rem;
  }

  .hub-brand-header__slogan {
    max-width: min(94vw, 22rem);
    font-size: 0.82rem;
  }

  .hub-brand-header__credit-inline {
    font-size: 0.62rem;
  }
}

.hub-shell__container {
  flex: 1 1 0;
  min-height: 0;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  padding: 0;
  max-width: none;
  background-color: #f8fafc;
  background-image: linear-gradient(180deg, #f8fafc 0%, #eef2ff 28%, #f1f5f9 100%);
}

.hub-shell__container :deep(.q-page) {
  flex: 1 1 0;
  min-height: 0 !important;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  padding: 0 !important;
  margin: 0 !important;
}

</style>

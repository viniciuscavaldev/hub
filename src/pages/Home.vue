<script setup>
import Botoes from "src/components/Botoes/Botoes.vue";
</script>

<template>
  <q-page class="hub-page q-pa-none">
    <div class="hub-page__inner container q-px-md">
      <header class="hub-hero">
        <h1 class="hub-hero__title q-pt-sm">
          Hub de Links Planejamento
        </h1>
        <p class="hub-hero__lead">
          Acesso rápido aos sistemas e dashboards do nosso setor em um só lugar.
        </p>
      </header>
      <Botoes />
    </div>
  </q-page>
</template>

<style scoped lang="scss">
.hub-page {
  flex: 1 1 0;
  min-height: 0;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  background:
    radial-gradient(ellipse 120% 80% at 10% -20%, rgba(21, 57, 170, 0.09) 0%, transparent 55%),
    radial-gradient(ellipse 90% 60% at 100% 0%, rgba(255, 77, 0, 0.06) 0%, transparent 45%),
    linear-gradient(180deg, #f8fafc 0%, #eef2ff 38%, #f1f5f9 100%);
}

.hub-page__inner {
  flex: 1 1 0;
  min-height: 0;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  width: 100%;
  max-width: 80rem;
  margin: 0 auto;
  padding-top: 0.35rem;
  padding-bottom: 0.5rem;
}

.hub-hero {
  flex-shrink: 0;
  margin-top: 0;
  margin-bottom: 0.75rem;
}

.hub-hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.35rem 0.75rem;
  margin-bottom: 0.5rem;
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #1539aa;
  background: rgba(255, 255, 255, 0.75);
  border: 1px solid rgba(21, 57, 170, 0.12);
  border-radius: 9999px;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}

.hub-hero__badge-icon {
  color: #1539aa;
}

.hub-hero__title {
  margin: 0 0 0.5rem;
  font-size: clamp(1.65rem, 4vw, 2.15rem);
  font-weight: 700;
  letter-spacing: -0.03em;
  line-height: 1.15;
  color: #0f172a;
}

.hub-hero__lead {
  margin: 0;
  max-width: 28rem;
  font-size: 1rem;
  line-height: 1.55;
  color: #64748b;
  font-weight: 500;
}
</style>

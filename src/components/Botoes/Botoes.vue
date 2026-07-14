<script setup>
import { ref } from "vue";

/** Ícone sugerido por palavra-chave no nome — ao adicionar links, basta o `name`; use `icon` para sobrescrever. */
function iconSistema (name) {
  const n = name.toLowerCase();
  if (n.includes("copilot")) return "smart_toy";
  if (n.includes("sgp")) return "account_tree";
  if (n.includes("lecom")) return "device_hub";
  if (n.includes("move")) return "alt_route";
  if (n.includes("vagas")) return "work_outline";
  if (n.includes("optimus")) return "tune";
  if (n.includes("sac")) return "support_agent";
  if (n.includes("neo") || n.includes("mop")) return "hub";
  if (n.includes("abs")) return "speed";
  if (n.includes("dimension")) return "straighten";
  if (n.includes("quadro")) return "groups";
  if (n.includes("sij") || n.includes("jornada") || n.includes("banco de horas")) return "schedule_send";
  if (n.includes("wfm")) return "event_available";
  return "apps";
}

function iconPowerBi (name) {
  const n = name.toLowerCase();
  if (n.includes("bilhetagem") || n.includes("avaya")) return "phone_in_talk";
  if (n.includes("cardio")) return "monitor_heart";
  if (n.includes("rechamada")) return "phone_callback";
  if (n.includes("genesys")) return "headset_mic";
  if (n.includes("ligação") || n.includes("relatório")) return "phone_in_talk";
  if (n.includes("schedule") || n.includes("quadro")) return "calendar_month";
  if (n.includes("feedback")) return "forum";
  if (n.includes("transfer")) return "swap_calls";
  if (n.includes("optimus")) return "insights";
  return "insert_chart_outlined";
}

const botoes = ref([
  {
    name: "ABS Real Time",
    link: "http://10.85.204.8:8501"
  },
  {
    name: "Análise Copilot",
    link: "http://10.85.204.8:9010/login#/"
  },
  {
    name: "Dimensionamento",
    link: "http://10.85.204.5:9005/#/volume"
  },
  {
    name: "Lecom",
    link: "https://bpm-lecom.hapvida.com.br/sso/?redirectBackTo=https://bpm-lecom.hapvida.com.br/"
  },
  {
    name: "MOVE",
    link: "http://10.85.204.8:5000"
  },
  {
    name: "NEO/MOP",
    link: "http://10.85.204.8:8508/"
  },
  {
    name: "Quadro Funcional",
    link: "http://10.85.204.8:8504/"
  },
  {
    name: "QUADRO FUNCIONAL AGENDAMENTO",
    link: "http://10.85.204.8:8520/"
  },
  {
    name: "Sac atendimento rapido",
    link: "http://10.85.204.8:9004/#/dashboard/atendimento-rapido"
  },
  {
    name: "SGP - Sistema de Gestão do Planejamento",
    link: "http://10.85.204.8:7030/login"
  },
  {
    name: "SIJ - Sistema Integrado de Jornada",
    link: "http://10.85.204.8:4000/#/"
  },
  {
    name: "Vagas em Aberto",
    link: "http://10.85.204.8:9000/login"
  },
  {
    name: "WFM Ativo",
    link: "http://10.85.204.8:8502"
  },
  {
    name: "WFM Optimus",
    link: "https://hapvida.optimus.app.br/"
  }
]);

const botoesbi = ref([
  {
    name: "Bilhetagem - Avaya",
    link: "https://app.powerbi.com/links/Lq9u5vXmvf?ctid=77d68323-6f4b-460f-8aae-d32c654ec490&pbi_source=linkShare"
  },
  {
    name: "Cardio Alerta",
    link: "https://app.powerbi.com/groups/1a9bc9c6-857c-4818-a85c-323ba2f77511/reports/8af31f92-5410-44a1-bec8-b6be17a4d735?ctid=77d68323-6f4b-460f-8aae-d32c654ec490&pbi_source=linkShare"
  },
  {
    name: "Consultas e exames",
    link: "https://app.powerbi.com/reportEmbed?reportId=9492222d-cfab-4848-9a6e-e211b4df0f21&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  },
  {
    name: "Feedback Mensal Call Center",
    link: "https://app.powerbi.com/groups/1a9bc9c6-857c-4818-a85c-323ba2f77511/reports/6340ce4c-f738-4253-876b-558247f2347f?ctid=77d68323-6f4b-460f-8aae-d32c654ec490&pbi_source=linkShare"
  },
  {
    name: "Operacional - Avaya",
    link: "https://app.powerbi.com/reportEmbed?reportId=2d9c682b-7788-47c5-abe5-8d176913a074&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  },
  {
    name: "Operacional - Genesys",
    link: "https://app.powerbi.com/reportEmbed?reportId=2e83b2ad-d5bc-4cde-a83c-0c07035d6354&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  },
  {
    name: "OPERACIONAL - OPTIMUS",
    link: "https://app.powerbi.com/reportEmbed?reportId=cb778171-07a0-447e-b2f0-90e1ab9fbdd4&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  },
  {
    name: "QUADRO REAL TIME",
    link: "http://10.85.204.8:7030/quadro",
    news: true
  },
  {
    name: "Rechamadas",
    link: "https://app.powerbi.com/reportEmbed?reportId=2bebbd51-f4da-4e60-a626-f2f951f5b997&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  },
  {
    name: "RELATÓRIO DE LIGAÇÕES",
    link: "https://app.powerbi.com/reportEmbed?reportId=6868c6af-c7fe-4bdc-ac8c-5f141dec47c2&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  },
  {
    name: "TRANSFERÊNCIAS",
    link: "https://app.powerbi.com/groups/1a9bc9c6-857c-4818-a85c-323ba2f77511/reports/35882412-5e37-4565-b1b1-da7fd56f0a41/3657517486cff7ddda83?experience=power-bi"
  },
  {
    name: "Leading Indicators - Call Center",
    link: "https://app.powerbi.com/reportEmbed?reportId=a63f1c18-8a34-418e-a24c-6b4d7699303c&autoAuth=true&ctid=77d68323-6f4b-460f-8aae-d32c654ec490"
  }
]);

</script>

<template>
  <div class="hub-botoes">
    <article class="hub-section">
      <header class="hub-section__head">
        <span class="hub-section__accent" aria-hidden="true" />
        <q-icon name="settings_suggest" class="hub-section__icon" size="22px" />
        <h2 class="hub-section__title">
          Sistemas internos
        </h2>
      </header>
      <div class="hub-grid">
        <a
          v-for="botao in botoes"
          :key="botao.link"
          class="hub-card"
          :class="{ 'hub-card--news': botao.news }"
          :href="botao.link.trim()"
          target="_blank"
          rel="noopener noreferrer"
        >
          <span class="hub-card__icon-wrap" aria-hidden="true">
            <q-icon :name="botao.icon || iconSistema(botao.name)" size="22px" />
          </span>
          <span class="hub-card__label">{{ botao.name }}</span>
          <q-icon name="north_east" class="hub-card__arrow" size="18px" aria-hidden="true" />
        </a>
      </div>
    </article>

    <article class="hub-section">
      <header class="hub-section__head">
        <span class="hub-section__accent" aria-hidden="true" />
        <q-icon name="insert_chart_outlined" class="hub-section__icon" size="22px" />
        <h2 class="hub-section__title">
          Power BI
        </h2>
      </header>
      <div class="hub-grid">
        <a
          v-for="botao in botoesbi"
          :key="botao.link"
          class="hub-card hub-card--bi"
          :class="{ 'hub-card--news': botao.news }"
          :href="botao.link.trim()"
          target="_blank"
          rel="noopener noreferrer"
        >
          <span class="hub-card__icon-wrap hub-card__icon-wrap--bi" aria-hidden="true">
            <q-icon :name="botao.icon || iconPowerBi(botao.name)" size="22px" />
          </span>
          <span class="hub-card__label">{{ botao.name }}</span>
          <q-icon name="north_east" class="hub-card__arrow" size="18px" aria-hidden="true" />
        </a>
      </div>
    </article>
  </div>
</template>

<style scoped lang="scss">
.hub-botoes {
  flex: 1 1 0;
  min-height: 0;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  overflow: hidden;
}

@media (min-width: 960px) {
  .hub-botoes {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
    grid-template-rows: 1fr;
    gap: 1rem;
    align-items: stretch;
  }
}

.hub-section {
  flex: 1 1 0;
  min-width: 0;
  min-height: 0;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  background: rgba(255, 255, 255, 0.55);
  border: 1px solid rgba(255, 255, 255, 0.85);
  border-radius: 1.25rem;
  padding: 1rem 1.1rem 1.1rem;
  box-shadow:
    0 4px 6px -1px rgba(21, 57, 170, 0.06),
    0 12px 32px -8px rgba(21, 57, 170, 0.12);
  backdrop-filter: blur(14px);
  -webkit-backdrop-filter: blur(14px);
}

@media (min-width: 960px) {
  .hub-section {
    height: 100%;
    align-self: stretch;
  }
}

.hub-section__head {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  flex-shrink: 0;
  margin-bottom: 0.75rem;
  position: relative;
  padding-left: 0.35rem;
}

.hub-section__accent {
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 4px;
  height: 1.35rem;
  border-radius: 4px;
  background: linear-gradient(180deg, #ff4d00 0%, #ff7a45 100%);
}

.hub-section__icon {
  color: #ff4d00;
  margin-left: 0.5rem;
}

.hub-section__title {
  margin: 0;
  font-size: 1.125rem;
  font-weight: 600;
  letter-spacing: -0.02em;
  color: #0f172a;
}

.hub-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 0.65rem;
  flex: 1 1 0;
  min-height: 0;
  overflow-x: hidden;
  overflow-y: auto;
  overscroll-behavior: contain;
  -webkit-overflow-scrolling: touch;
  align-content: start;
  padding-right: 2px;
  scrollbar-gutter: stable;
}

.hub-grid::-webkit-scrollbar {
  width: 8px;
}

.hub-grid::-webkit-scrollbar-thumb {
  background: rgba(21, 57, 170, 0.22);
  border-radius: 9999px;
}

.hub-grid::-webkit-scrollbar-track {
  background: rgba(15, 23, 42, 0.04);
  border-radius: 9999px;
}

/* Uma coluna em telas muito estreitas; duas colunas quando couber confortavelmente */
@media (min-width: 500px) {
  .hub-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.75rem;
  }
}

@media (min-width: 768px) {
  .hub-grid {
    gap: 0.85rem;
  }
}

@media (min-width: 1200px) {
  .hub-grid {
    gap: 1rem;
  }
}

.hub-card {
  display: flex;
  align-items: center;
  gap: 0.85rem;
  min-height: 3.35rem;
  padding: 0.85rem 1rem;
  text-decoration: none;
  color: #0f172a;
  font-size: 0.8125rem;
  font-weight: 600;
  line-height: 1.35;
  letter-spacing: 0.02em;
  text-transform: uppercase;
  border-radius: 0.9rem;
  border: 1px solid rgba(226, 232, 240, 0.95);
  background: linear-gradient(145deg, rgba(255, 255, 255, 0.92) 0%, rgba(248, 250, 252, 0.88) 100%);
  box-shadow:
    0 1px 2px rgba(15, 23, 42, 0.04),
    0 8px 20px -10px rgba(21, 57, 170, 0.18);
  transition:
    transform 0.2s cubic-bezier(0.4, 0, 0.2, 1),
    box-shadow 0.2s cubic-bezier(0.4, 0, 0.2, 1),
    border-color 0.2s ease;
}

.hub-card:hover {
  transform: translateY(-3px);
  border-color: rgba(21, 57, 170, 0.35);
  box-shadow:
    0 4px 12px rgba(15, 23, 42, 0.06),
    0 16px 36px -12px rgba(21, 57, 170, 0.28);
}

.hub-card:focus-visible {
  outline: 2px solid #1539aa;
  outline-offset: 2px;
}

.hub-card--news {
  border-color: rgba(255, 77, 0, 0.45);
  box-shadow:
    0 0 0 1px rgba(255, 77, 0, 0.12),
    0 8px 24px -8px rgba(255, 77, 0, 0.25);
  animation: pulse-border 2s infinite ease-in-out;
}

@keyframes pulse-border {
  0%, 100% {
    border-color: rgba(255, 77, 0, 0.45);
    box-shadow: 0 0 0 1px rgba(255, 77, 0, 0.12), 0 8px 24px -8px rgba(255, 77, 0, 0.25);
  }
  50% {
    border-color: rgba(255, 77, 0, 0.95);
    box-shadow: 0 0 0 4px rgba(255, 77, 0, 0.25), 0 8px 32px -4px rgba(255, 77, 0, 0.4);
  }
}

.hub-card__icon-wrap {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 0.65rem;
  background: linear-gradient(135deg, rgba(21, 57, 170, 0.12) 0%, rgba(21, 57, 170, 0.06) 100%);
  color: #1539aa;
}

.hub-card__icon-wrap--bi {
  background: linear-gradient(135deg, rgba(255, 77, 0, 0.14) 0%, rgba(255, 77, 0, 0.06) 100%);
  color: #e04600;
}

.hub-card--bi:hover .hub-card__icon-wrap--bi {
  color: #ff4d00;
}

.hub-card__label {
  flex: 1;
  text-align: left;
  min-width: 0;
}

.hub-card__arrow {
  flex-shrink: 0;
  color: #94a3b8;
  opacity: 0.65;
  transition: color 0.2s ease, opacity 0.2s ease, transform 0.2s ease;
}

.hub-card:hover .hub-card__arrow {
  color: #1539aa;
  opacity: 1;
  transform: translate(2px, -2px);
}

.hub-card--bi:hover .hub-card__arrow {
  color: #ff4d00;
}
</style>

# P3 — Sítio 38°34'26"N, 07°53'38"W, 251m alt — Évora
## Cruzamento EPW IWEC + IPMA 1991-2020 + Köppen-Geiger Csa

**Fontes:**
- EPW: `PRT_Evora.085570_IWEC.zip` → `PRT_Evora.085570_IWEC.stat` — EVORA WMO 085570, N38°34' W07°54', 321m
- IPMA: `cn_91-20_EVORA.pdf` — Estação 558, 38.5365N 7.8880W, 247.6m, Normal 1991-2020 v1.0 2024
- Köppen-Geiger: Csa — clima mediterrânico de verão quente

**Representatividade:**
- Sítio = 38.574N, 7.894W, 251m
- IPMA 558 ≈ 4 km S do sítio, +3.4 m → aplicável direto, manda no dimensionamento térmico/hídrico
- EPW IWEC coincidente em planta, +70 m em altimetria (~-0.45 K) → manda na dinâmica horária (vento, amplitude, sol, flushing)

---

## 1. Enquadramento: o que vale para o quê

Csa = temperado, verão seco e quente, inverno chuvoso. IPMA 1991-2020 para médias, extremos e chuva (série homogénea 30 anos). EPW IWEC para hora-a-hora: vento, amplitude diária, radiação, arrefecimento noturno. Não usar EPW para chuva quantitativa.

## 2. Semanas mais quentes — projetar para 15 Jul > 31 Ago

- IPMA: Ago TT 24.7 °C / TX 33.5 °C; Jul TT 24.5 / TX 33.3; Jun 22.0 / 30.2; Set 22.1 / 29.5
- TX ≥ 30 °C: 86.5 dias/ano (Jul 23.7, Ago 25.0, Jun 15.1, Set 13.9)
- TX ≥ 35 °C: 31.9 dias (Jul 11.5, Ago 10.9, Jun 5.6)
- Extremo absoluto: 45.4 °C em 04/08/2018
- EPW `.stat`: Daily Avg Ago 23.0, Jul 22.7, Set 22.0, Jun 19.8; Max 38.4 °C a 23/Jul; cooling 0.4% Jul 37.9, Ago 37.5
- `Extreme Hot Week Sep 16-22` no `.stat` é artefacto de ano compósito IWEC — ignorar como data literal
- **Massa:** pico 6–7 semanas. Inércia + descarga noturna obrigatórias, vidro W mínimo.

## 3. Vento dominante de verão — NW, captar; E/W, fechar

- EPW `.stat` direção %: NW Jun 44%, Jul 46%, Ago 45%, Set 43%, Abr 51%, Mai 36%; secundário W 20% em Jun-Jul; N puro só domina em Mar 41%
- EPW `.stat` horário: reforço 19–23h — Jul 5.5–5.9 m/s, Ago 5.9–6.3 m/s vs 3.3 m/s ao meio-dia (nortada + brisa de fim de tarde)
- **Massa:** eixo de ventilação transversal NW↔SE; aberturas altas a NW/SE para flushing 20–24h; nada de pátio fechado a NW.

## 4. Meses de precipitação — inverno concentra, verão zero

- IPMA Prec total 596.1 mm: Nov 86.0, Dez 85.1, Out 81.5, Jan 68.6, Abr 62.1, Mar 60.8 vs Jun 10.6, Ago 6.0, Jul 2.7
- Dias P ≥ 1 mm: Nov 8.8, Dez 8.7, Jan 8.6 vs Jul 0.6, Ago 0.7
- Extremo diário: 92.6 mm em 21/10/2020
- **Massa:** beirado/caleira para Out–Dez, pódio com salpico + drenagem perimetral; pátio com escoamento rápido para tromba de Out. Jul–Ago irrelevantes para água.

## 5. Noites frias — amplitude que salva o verão e penaliza o inverno

- IPMA TN: Jan 4.5, Fev 5.0, Dez 5.3; geada TN < 0: 5.9 dias/ano (Jan 2.2, Fev 1.8, Dez 1.4); mínima absoluta -4.2 °C
- Noites tropicais TN ≥ 20: só 4.2 dias/ano
- EPW `.stat`: range diário Jul 13.0, Ago 12.6, Jun 11.2, Set 10.6 vs Jan 5.9, Dez 5.2; 06h Jul 17.0 °C / Ago 17.0 °C quando 15h está a 29.4–29.5 °C
- **Massa:** queda 11–13 K = motor do arrefecimento passivo. Inverno: captar sol de manhã E/SE (mínima às 06h), proteger vão N.

## 6. Período de necessidade de sombreamento — Mai a início Out, crítico 15 Jun > 15 Set

- IPMA TX ≥ 25: 146.8 dias (Mai 15.2 a Out 12.2); CDD18.3: Jun 68, Jul 157, Ago 157, Set 129
- EPW `.stat`: CDH23 Jul 1724, Ago 1780, Set 1331, Jun 760; Global Avg Jul 7452, Jun 7077, Ago 6720 Wh/m².dia; pico 13h Jul 922, Ago 873 Wh/m²
- **Massa:** sombrear S/W/E de ~meados-Mai a início-Out. Vidro S só com pala/lamelar a 38.6°N; W quase cego.

---

## Convergências e divergências EPW / IPMA

**Convergem:** hierarquia Ago > Jul > Jun ≈ Set; verão seco; NW de verão; grande amplitude estival; inverno ameno com geada escassa.

**Divergem:**
1. EPW 1–2 K mais frio no verão: Jul 22.7 vs TT 24.5, Jun 19.8 vs 22.0. Causa: +70 m altitude + período IWEC mais antigo/frio que 1991-2020 + ano-tipo suavizado.
2. EPW classifica algoritmicamente Cfa — errado normativamente. Vale Csa IPMA/Köppen; o próprio `.stat` avisa que pode não refletir o longo prazo.
3. Chuva: EPW só dá indicador humidade kPa, sem totais. Usar só IPMA para água.

---

## 2 regras de volumetria

**R1 — Barra E-W compacta + vazio de descarga a NW:** corpo principal de eixo maior E-W, fachada S curta-protegida e N quase cega; pátio/loggia passante NW-SE alinhada ao vento 300–320° para ventilação cruzada noturna. W/E sem vidro corrente, só frestas profundas.

**R2 — Massa pesada + cobertura sombreante:** inércia interior para absorver pico 29–34 °C e largar à noite com ar NW; cobertura ventilada/pala S para cortar sol 15 Jun–15 Set e admitir sol Dez–Jan; vãos de inverno a E/SE para aquecimento matinal após mínima das 06h.

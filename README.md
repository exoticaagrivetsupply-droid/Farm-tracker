# 🌱 Farm Tracker

App para sa records sa uma: gikan sa land prep hangtod harvest, ang capital, kita, ug ganansya o lugi sa matag tanom. Karon naa nay **TRABAHO KARONG ADLAWA** para sa trabahante.

## Mga file (i-upload TANAN sa GitHub repo nga Farm-tracker)
`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`

## ✅ TRABAHO KARONG ADLAWA (para sa trabahante)
Ablihi ang app ug sundon lang ang makita:
- **🔴 KARON**: ang tanang buhaton karong adlawa. Ang 🟡 nagpasabot nga naghulat o wala pa nahuman.
- **📅 SUNOD**: ang trabaho sa sunod nga 7 ka adlaw.
- **🟢 NAHUMAN NA**: ang mga nahuman na, uban ang petsa ug oras.

| Trabaho | Buttons |
|---|---|
| 💧 PATUBIG | NAPATUBIGAN NA · BASA PA ANG YUTA · WALA MAPATUBIGI (rason: walay tubig, naulan, basa pa, wala nahuman, uban pa) |
| 🌱 PAG-ABONO | DONE. Makita ang abono ug pila ka kilo para sa area. |
| 🐛 CHECK SA PESTE | WALAY PESTE · NAAY PESTE (pilia ang peste, pila ka tanom, litrato) · KINAHANGLANG TABANG |
| 🧴 PAG-SPRAY | Mogawas lang kon naghimo ang admin og **Spray Order**. |

**Selector sa ibabaw sa TRABAHO:** "👤 Kinsa nga taho?" (admin ra) ug "🌱 Unsa nga tanom?". Ang listahan sa tanom mosunod sa napili nga taho, ug kon daghan ang batch (pananglitan 2 ka Sweet Corn), mapili ang matag usa. Makita usab pila ang buhaton sa matag pilianan.

## 🐛 Pest monitoring: buntag ug hapon, uban ang litrato
- Matag adlaw, sa matag tanom (human sa Day 7): **🌅 BUNTAG** (6–9 AM) ug **🌇 HAPON** (3–6 PM, mogawas human sa 12:00).
- **Sample nga tanom**: 10 ka parehas nga tanom matag adlaw (markahi og lipak o plastic 1–10). Usba ang gidaghanon sa Crop Schedule → "Pila ka sample nga tanom".
- **Trabahante**: ✅ WALAY MANANAP, o 🐛 NAAY MANANAP — PICTURAN → pindota ang numero sa tanom → 📷 litrato, unsa nga mananap, ug pila → I-SAVE. Ang app mo-compute sa **% sa sample** (pananglitan 2 sa 10 = 20%).
- **Admin, sa tanom → 🐛 Peste**: stage sa tanom karon, talaan sa buntag ug hapon (14 ka adlaw), mga mananap nga nakita, gallery sa litrato, mga spray nga nagamit na (uban ang pahimangno kon parehas ang active ingredient), ug button nga **🧴 Himo og Spray Order** (nakabutang na ang peste).
- Ang hilo: ang manager ra (uban ang technician) ang modesisyon, gamit ang produkto nga **rehistrado sa FPA**. Walay automatic nga spray.
- Kon gusto nga dili kada adlaw: Crop Schedule → Pest check → "Kada pila ka adlaw".

## 🔔 Notification (5:00 AM ug 2:00 PM)
Ang **GitHub Actions** (libre) sa imong private nga `farm-data` repo maoy mopadala sa listahan sa trabaho ngadto sa cellphone. Ang admin makakita usab sa mga alert (sakit, peste). Ang matag taho, iyang trabaho ra ang makita.

**Setup (kausa ra, sa imong cellphone):**
1. ⚙️ Settings → 🔔 Notification → **🔔 I-ON** → **Allow**. Mogawas dayon ang test nga notification.
2. **⚙️ I-setup sa GitHub**. Kon mogawas ang "Kinahanglan og dugang permiso": github.com → Settings → Developer settings → Fine-grained tokens → ang imong token → **Workflows: Read and write** ug **Actions: Read and write** → Update. Dayon balika ang ⚙️ I-setup sa GitHub.
3. **🚀 Sulayi karon** aron masulayan nga moabot gikan sa GitHub (1–2 minutos).

**Sa cellphone sa matag taho:** ablihi ang app → **🔔 I-ON ANG NOTIFICATION** sa Trabaho page → Allow.
- Android: gamita ang Chrome ug i-install ang app.
- iPhone: i-Add to Home Screen una (iOS 16.4 pataas).
- Usba ang oras: Settings → 🔔 → "Usba ang oras" → ⚙️ I-update.
- Ang GitHub usahay malangan og 5–30 minutos.

## 📷 Picturan ang uma (bisan kanus-a)
- Dako nga button nga **📷 PICTURAN ANG UMA** sa ibabaw sa ✅ Trabaho (para sa admin ug sa taho), sa ➕ menu, ug sa 🐛 Peste tab sa tanom.
- Pilia ang tanom → **📷 CAMERA** o **🖼️ GALLERY** (pwede daghan) → unsa ni: 🐛 Mananap / 🍂 Sakit (uban ang sintomas) / 🌱 Kahimtang sa tanom / 💧 Tubig-yuta / 📌 Uban → nota → **I-SAVE**.
- Makita sa **🐛 Peste report** (gallery) ug sa 🟢 NAHUMAN NA. Kon mananap o sakit, naay **alert** sa Dashboard.
- Bulag kini sa sample check sa buntag ug hapon. Kini para sa bisan unsa nga makita sa uma.

## ⚠️ Kritikal nga stage ug 🍂 sakit
- Ang matag crop naay **kritikal nga stage** (pananglitan sa mais: Pagtubo, Whorl, **Tasseling/Silking**, Pagpuno sa dalumpit), uban ang **mananap ug sakit nga bantayan** ug unsay tan-awon.
- Sa pest check sa trabahante: dalag nga kahon nga **⚠️ KRITIKAL NGA STAGE**, ug "Unsaon pag-ila sa sakit?" (mga sintomas).
- **🍂 Sakit sa sample**: matag sample nga tanom, mapili ang mananap ug/o sakit (uban ang sintomas), ug naay litrato. Bulag ang % sa mananap ug % sa sakit.
- **Balantaya (alerts)**: naay sakit nakit-an (pula), kritikal nga stage karon o sa sulod sa 3 ka adlaw, ug kon **naulan ≥10 mm** (taas ang risgo sa sakit; kinahanglan ang location sa uma).
- **🐛 Peste report**: timeline sa kritikal nga stage, ang % sa mananap 🐛 ug sakit 🍂 sa buntag ug hapon, ug mga litrato.
- Kinatibuk-ang giya ra kini. Pangutana sa technician o DA para sa inyong lugar.

**Bag-ong crop:** Talong (naa nay schedule), Pipino, Chinese Cabbage (Pechay Baguio / Wombok), ug Carrot. Ang matag usa naay schedule, guide, spacing, target, mananap, sakit, ug kritikal nga stage.

## 👷 I-set ang cellphone sa trabahante
1. I-setup una ang **GitHub Sync** sa iyang cellphone (Settings).
2. Settings → **👷 Himoa kini nga cellphone para sa trabahante** → ibutang ang Admin PIN.
3. Ang TRABAHO ra ang makita. Para makabalik sa admin, pindota ang **🔒 Admin** sa ubos ug ibutang ang PIN.

## ⚙️ Para sa admin
- **Settings → Crop Schedule ug Abono**: usba ang trabaho, adlaw, instruksyon, kada pila ka adlaw ang patubig ug pest check, ug ang **abono + dosage** (kg/ha, sako/ha, o gramo/tanom). Ang app mo-compute sa total kilo base sa area sa matag tanom (pananglitan: 100 kg/ha × 0.5 ha = 50 kg). **Walay default nga dosage.** Ibutang base sa soil test o rekomendasyon sa DA o technician.
- **Settings → Manager ug location**: numero sa manager (para sa button nga KINAHANGLANG TABANG) ug location sa uma (para makita ang ulan gikan sa Open-Meteo).
- **Spray Order** (sa page sa tanom o sa ➕): produkto, active ingredient, FPA reg. no., dosage, PHI ug REI. Kopyaha ang tanan gikan sa label. Ang app dili mohatag og brand o dosage, ug dili mo-schedule og spray nga awtomatiko.
- **Dashboard alerts**: makita kon naay peste nga nakit-an o nangayo og tabang ang trabahante.

## 💰 Partehanay (Sinaligan ug Agente)
**Pormula sa matag tanom:**
1. **Benta (gross)** − **Agente 10%** sa gross
2. − **Tanang gasto** sa tanom (binhi, abono, spray, bayad sa trabahante, ug uban pa)
3. − **Parte sa general farm expenses** (walay tanom), nga gibahin base sa area sa mga tanom nga aktibo niadtong petsaha
4. = **NET**
5. **Sinaligan: 10% sa NET sa iyang kaugalingong area.** Kon lugi, ₱0 ang iyang parte. Ang nahabilin, **imo**.

Pananglitan: Benta ₱100,000 − Agente ₱10,000 − Gasto ₱20,000 − General ₱5,000 = NET ₱65,000. Si Juan: ₱6,500. Imo: ₱58,500.

**Setup (isa ra ka higayon):**
1. **💰 Partehanay → ⚙️ Sinaligan, agente %, sweldo**: idugang ang 2 ka sinaligan (ngalan, numero, 10%), ang agente 10%, ug ang sweldo sa bayaran nga trabahante kada adlaw.
2. **Edit Tanom → 👤 Sinaligan**: pilia kinsa ang nagdala sa matag area.
3. Sa cellphone sa matag sinaligan: **Settings → 👷 Himoa kini nga cellphone para sa trabahante** → pilia ang iyang ngalan. Iyang mga tanom ra ang makita, ug naa siyay **💰 PARTE** tab.

**Kinsa ang mobuhat (makita sa matag trabaho):**
- **👤 IMONG TRABAHO** (sinaligan, walay dugang bayad): taho-taho, patubig, pest check, spray
- **💰 BAYAD SA TAG-IYA**: abono, gabot sa sagbot, land prep, pagtanom, harvest. Sa DONE, pangutan-on ang trabahante kung **pila ka trabahante** ang gibayran. Ang app mo-compute dayon: tawo × sweldo = gasto.
- Ang admin makausab niini sa matag trabaho: Settings → Crop Schedule → "Kinsa ang mobuhat".

**Harvest:** sa matag benta, naka-check ang "Gibaligya pinaagi sa agente". I-uncheck kon diretso nga baligya (walay komisyon).
**Pagtan-aw:** sa ibabaw sa 💰 Partehanay naay **"Kinsa ang lantawon?"**: Tanan (summary), matag sinaligan, Walay sinaligan, o Agente. Sa matag sinaligan naay filter nga Aktibo / Tapos na, ug makita ang "Kulang pa bayran".
**Pagbayad sa sinaligan:** 💰 Partehanay → "💵 Markahi nga nabayran na". Kon mausab ang records human sa pagbayad, ipakita sa app ang kulang o sobra.

## 💵 BUDGET (plano sa trabahante ug gasto)
Sa **✅ Trabaho → 💵 BUDGET** (admin ra). Mosunod kini sa selector sa taho ug tanom. Pilia ang **7 / 14 / 30 ka adlaw o hangtod harvest**.
- **👷 Pila ka trabahante** sa matag trabaho = man-days kada hectare × area. Pananglitan: gabot sa sagbot 15 × 0.5 ha = 8 ka tawo.
- **Bayad** = tawo × sweldo kada adlaw (💰 Partehanay → ⚙️ Sinaligan → sweldo).
- **Materyales**: abono (kg ug sako gikan sa dosage × area × presyo kada sako), spray (produkto ug banabana nga gasto sa Spray Order), binhi para sa plano nga tanom (gikan sa calculator, kanus-a paliton).
- **Total nga budget**, ang **adlaw nga pinakadaghan og tawo**, listahan sa **materyales nga andamon**, ug matag adlaw.
- Ang trabaho sa sinaligan (patubig, pest check, spray) walay bayad sa trabahante.

**Usba ang banabana**: ⚙️ Settings → Crop Schedule → matag trabaho: "Trabahante kada hectare", "Ubang gasto kada hectare" (tractor, krudo), ug "Presyo kada sako" sa abono. Human sa mga DONE nga naay "Pila ka trabahante", makita ang **aktwal kaniadto** aron mas sakto ang sunod nga plano.

Sa **Edit Tanom → 🎯 Target sa Produksyon**:
- **Tanom nga mabuhi**: gikan sa calculator (binhi × germination).
- **Ani kada tanom** × **% nga mabaligya** = **target nga ani**. Default nga banabana: mais 1 ka dalumpit, kalabasa 4 kg, broccoli 0.3 kg, repolyo 1 kg, sibuyas dahon 0.1 kg, kamatis 2 kg kada tanom. Usba base sa inyong experience.
- **Gidahom nga presyo** (kamo ang mobutang) × target = **target nga benta**, minus agente.
- Sa page sa tanom: progress bar (na-harvest vs target), **gidahom nga NET**, gidahom nga parte sa sinaligan, **break-even nga ani** ug **break-even nga presyo**.

Pananglitan: 10 ka pack × 1,000 ka binhi × 85% = 8,500 ka tanom × 1 × 85% = **7,225 ka dalumpit**. Sa ₱15 kada buok = ₱108,375 − agente ₱10,837.50 = ₱97,537.50.

- I-check ang **Auto-sync** sa TANANG cellphone ug computer (Settings → GitHub Sync).
- Kon naay bag-o, mo-sync dayon human sa 1.5 segundos. Mokuha usab og bag-o gikan sa laing device **kada 30 segundos**, ug kada ablihan o balikan ang app.
- Kon walay nausab, gamay ra kaayo nga check (walay upload, walay commit), busa paspas.
- Sa ibabaw makita ang "☁ Synced 1:32 PM" (oras sa katapusang sync).

- Ang mga daan nga record wala nausab. Mga bag-ong listahan sa data: `orders`, `templates`, `settings`.
- Ang litrato sa peste ma-save sa cellphone, ug sa sync ma-upload sa `farm-data` repo sa folder nga `photos/`.

# Medições — Cartucho Patola Atari I
# Measurements — Patola Atari I Cartridge

> Todas as medições foram realizadas com paquímetro digital.
> All measurements taken with digital caliper.
> Última atualização / Last updated: 2026-04-21

---

## 🇧🇷 PORTUGUÊS

### Caixa — Dimensões Internas

| Dimensão | Valor | Status |
|----------|-------|--------|
| Largura interna (geral) | 78,0mm | ✅ confirmado |
| Largura interna (região do slot) | 78,2mm | ✅ confirmado |
| Profundidade útil (Y) | 53,1mm | ✅ confirmado 2× |
| Altura interna | 16,0mm | ✅ confirmado |
| Espessura da parede | 2,0mm | ✅ confirmado |
| Altura da parede | 7,9–8,16mm | ✅ confirmado |
| Diagonal interna | 121,4–121,6mm | ✅ confirmado 2× |

### PCB — Dimensões Finais

| Parâmetro | Valor |
|-----------|-------|
| Largura × Altura | 74 × 52mm |
| Espessura | 1,6mm |
| Acabamento | Verde + ENIG |
| Versão | v1.0 A |
| Folga lateral na caixa | 2,1mm cada lado ✅ |

### Pinos de Fixação ①②

| Parâmetro | Valor | Observação |
|-----------|-------|------------|
| Altura do pino | 7,4mm | inclui batente |
| Diâmetro do pino | Ø2,0mm | |
| Diâmetro da base | Ø4,3mm | |
| Distância entre eixos (centro-a-centro) | 43,2mm | calculado de 41,2mm fora-a-fora |
| Distância fora-a-fora | 41,2mm | medido diretamente |
| Distância entre furos da tampa | 41,5mm | medido com ferramenta nos furos |
| X interno (da parede lateral ao centro) | 18,25mm | calculado |
| X no PCB (esquerdo) | 16mm | H1 |
| X no PCB (direito) | 58mm | H2 |
| Y do topo interno ao centro do pino | 53,5mm | medido |
| Y no PCB | 50mm | calculado (offset 1,5mm) |
| Pinos atravessam o PCB? | SIM | furos H1/H2 necessários |

### Torres de Parafuso ③

| Parâmetro | Valor | Observação |
|-----------|-------|------------|
| Y do topo interno ao centro da torre | 59,7mm | medido |
| Distância lateral pino→torre | 12,7mm | medido |
| X interno (da parede lateral) | 5,8mm | calculado |
| Torres atravessam o PCB? | NÃO | Y=59,7mm > 53,1mm (fora da área do PCB) |
| Furos no PCB para torres? | NÃO | torres ficam na região da peça 3 |

### Edge Cuts — KiCad v11 (FINAL)

Retângulo base: (0,0) → (74,52)mm H1 pino ①: centro (16, 50)mm Ø2,5mm NPTH H2 pino ②: centro (58, 50)mm Ø2,5mm NPTH Notch esquerdo: (0,8) → (5,14)mm [recorte] Notch direito: (69,8) → (74,14)mm [recorte] Edge connector: X=6,52 → 67,48mm, Y=52mm Chamfer: 45°×1mm nos cantos inferiores Torres parafuso: SEM FURO no PCB


### Sistema de Fixação do PCB

O PCB é fixado na caixa Patola pelo seguinte sistema:

1. **Pinos ①②** — atravessam o PCB pelos furos H1/H2 (Ø2,5mm)
2. **Batente dos pinos** — o PCB apoia no degrau do pino, ficando na altura correta
3. **Pressão lateral** — folga de 2,1mm cada lado (74mm PCB em 78mm interno)
4. **Tampa superior** — fecha e trava o conjunto
5. **Torres de parafuso** — fixam a peça 3 (guia do conector), não o PCB diretamente

> **Nota:** O adaptador Thingiverse [thing:5922377](https://www.thingiverse.com/thing:5922377)
> confirma que os pinos da Patola interferem com PCBs padrão Atari.
> Para PCBs customizados como este, basta fazer os furos H1/H2.

### Espaço Disponível Acima do PCB

| Parâmetro | Valor |
|-----------|-------|
| Altura interna total | 16,0mm |
| Espessura do PCB | 1,6mm |
| Altura do batente dos pinos | 7,4mm |
| Espaço acima do PCB | ~8,1mm |
| Componente mais alto (WeAct Pico2 B) | ~4,0mm |
| Margem disponível | ~4,1mm ✅ |

---

## 🇺🇸 ENGLISH

### Enclosure — Internal Dimensions

| Dimension | Value | Status |
|-----------|-------|--------|
| Internal width (general) | 78.0mm | ✅ confirmed |
| Internal width (slot area) | 78.2mm | ✅ confirmed |
| Useful depth (Y) | 53.1mm | ✅ confirmed 2× |
| Internal height | 16.0mm | ✅ confirmed |
| Wall thickness | 2.0mm | ✅ confirmed |
| Wall height | 7.9–8.16mm | ✅ confirmed |
| Internal diagonal | 121.4–121.6mm | ✅ confirmed 2× |

### PCB — Final Dimensions

| Parameter | Value |
|-----------|-------|
| Width × Height | 74 × 52mm |
| Thickness | 1.6mm |
| Finish | Green + ENIG |
| Version | v1.0 A |
| Lateral clearance in enclosure | 2.1mm each side ✅ |

### Mounting Pins ①②

| Parameter | Value | Notes |
|-----------|-------|-------|
| Pin height | 7.4mm | includes step/batente |
| Pin diameter | Ø2.0mm | |
| Base diameter | Ø4.3mm | |
| Center-to-center distance | 43.2mm | calculated from 41.2mm OD |
| Outside-to-outside distance | 41.2mm | directly measured |
| Top cover hole-to-hole | 41.5mm | measured with tool in holes |
| X internal (wall to pin center) | 18.25mm | calculated |
| X on PCB (left) | 16mm | H1 |
| X on PCB (right) | 58mm | H2 |
| Y from internal top to pin center | 53.5mm | measured |
| Y on PCB | 50mm | calculated (1.5mm offset) |
| Pins traverse PCB? | YES | H1/H2 holes required |

### Screw Towers ③

| Parameter | Value | Notes |
|-----------|-------|-------|
| Y from internal top to tower center | 59.7mm | measured |
| Lateral distance pin→tower | 12.7mm | measured |
| X internal (from lateral wall) | 5.8mm | calculated |
| Towers traverse PCB? | NO | Y=59.7mm > 53.1mm (outside PCB area) |
| PCB holes for towers? | NO | towers are in piece 3 region |

### Edge Cuts — KiCad v11 (FINAL)

Base rectangle: (0,0) → (74,52)mm H1 pin ①: center (16, 50)mm Ø2.5mm NPTH H2 pin ②: center (58, 50)mm Ø2.5mm NPTH Left notch: (0,8) → (5,14)mm [cutout] Right notch: (69,8) → (74,14)mm [cutout] Edge connector: X=6.52 → 67.48mm, Y=52mm Chamfer: 45°×1mm on lower corners Screw towers: NO HOLE in PCB


### PCB Fixation System

The PCB is held in the Patola enclosure by:

1. **Pins ①②** — traverse the PCB through holes H1/H2 (Ø2.5mm)
2. **Pin step (batente)** — PCB rests on the pin shoulder at the correct height
3. **Lateral pressure** — 2.1mm clearance each side (74mm PCB in 78mm internal)
4. **Top shell** — closes and locks the assembly
5. **Screw towers** — fix piece 3 (connector guide), not the PCB directly

> **Note:** The Thingiverse adapter [thing:5922377](https://www.thingiverse.com/thing:5922377)
> confirms that Patola pins interfere with standard Atari PCBs.
> For custom PCBs like this one, simply add holes H1/H2.

### Available Space Above PCB

| Parameter | Value |
|-----------|-------|
| Total internal height | 16.0mm |
| PCB thickness | 1.6mm |
| Pin step height | 7.4mm |
| Space above PCB | ~8.1mm |
| Tallest component (WeAct Pico2 B) | ~4.0mm |
| Available margin | ~4.1mm ✅ |

---

*Measurements by: marushio-rima*
*Method: digital caliper*
*Date: 2026-04-21*

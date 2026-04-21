# Atari VCS 2600 Pico2 Cart — Ultimate Edition

> **English version below / Versão em português abaixo**

---

## 🇺🇸 ENGLISH

### Overview

The **Atari VCS 2600 Pico2 Cart — Ultimate Edition** is an open-source
multi-cart for the Atari 2600, built around the **WeAct Pico2 B (RP2350B)**
microcontroller running at 200MHz.

This project does not aim to be "the best" multicart — it aims to explore
directions that have not yet been taken, filling real gaps that the Atari 2600
community still needs today.

Use the joystick or SELECT/RESET keys to navigate the SD card menu and select
a title to play. The SD card must be formatted as FAT or FAT32.

---

### Key Features

- **Universal physical compatibility** — fits both original Atari-standard
  shells and Brazilian-made **Patola** shells (still manufactured today)
- **Full Atari 2600 slot usage** — all available signals used, no hardware
  mods required on the console
- **Independent stereo audio output** — 3.5mm stereo jack (P2), completely
  independent from the console's internal audio path
- **New audio system** — custom stereo sound engine running on Core 1 of the
  RP2350B (~26.6% Core 1 usage), supporting NTSC, PAL-M and PAL
- **Exclusive custom mapper** — new mapper design with features not available
  in any existing multicart (details below)
- **~55 mapper emulations** — covers all relevant Atari 2600 banking schemes
  (internet-dependent mappers excluded by design)
- **SD auto-bootloader** — automatic ROM selection and boot from SD card
- **WS2812B RGB LED** — visual status indicator via PIO
- **MicroSD slot** — dual footprint (SMD top + THT bottom) for flexibility
- **Debug UART** — GP17 exposed as test point TP1
- **Open source** — MIT + CC-BY-SA license

---

### Custom Mapper — Ultimate

> *(Full specification to be published with firmware release)*

The Ultimate mapper introduces features specifically designed for the modern
Atari 2600 community, including capabilities not explored by any existing
multicart solution. Details will be documented alongside the firmware source
code release.

---

### Hardware

**MCU:** WeAct Pico2 B — RP2350B A4 — dual-core ARM Cortex-M33 @ 200MHz

**GPIO Mapping (final):**

| GPIO | Function |
|------|----------|
| GP0–GP12 | A0–A12 (Address bus) |
| GP13 | SD_CLK |
| GP14 | SD_MOSI |
| GP15 | SD_MISO |
| GP16 | SD_CS |
| GP17 | UART_TX debug (TP1) |
| GP18 | WS2812B (PIO0 SM0) |
| GP19 | PIO_CLK (PIO0 SM1) |
| GP20 | PWM_L (PWM2A) |
| GP21 | PWM_R (PWM2B) |
| GP22–GP27 | SPARE |
| GP28–GP35 | D0–D7 (Data bus) |
| GP36–GP39 | SPARE |
| GP40–GP47 | ADC (unused) |

---

### Custom PCB

- **Dimensions:** 74 × 52 × 1.6mm — universal fit
- **Finish:** Green solder mask + ENIG
- **Hardware version:** v1.0 A
- **Edge connector:** 24-pin × 2.54mm, chamfered 45°×1mm
- **Mounting:** Compatible with Patola pin system (H1/H2 Ø2.5mm)
- **Components:** 44 components + 3 test points
- **Passives:** 0603 (except C1a/C1b 0805 — 2× 47µF X5R in parallel)
- **Routing:** ≥1mm component spacing; 0.5mm (+5V/GND), 0.3mm (3V3),
  0.2mm (signals); bottom GND pour; star ground topology

---

### Firmware

- **Platform:** RP2350B (Raspberry Pi Pico 2 — WeAct B variant)
- **Clock:** 200MHz (overclocked)
- **~55 mapper emulations** (all major banking schemes)
- **SD auto-bootloader** with FAT/FAT32 support
- **Video standards:** NTSC, PAL-M, PAL
- **Stereo audio:** ~26.6% Core 1 usage
- **Source:** To be published (C / RP2350B SDK)

> This project is a fork/evolution of the
> [UnoCart-2600](https://github.com/robinhedwards/UnoCart-2600)
> by Robin Edwards, ported and extended for the RP2350B platform.

---

### Building

> Detailed build instructions coming soon.

**Requirements:**
- WeAct Pico2 B module (RP2350B A4)
- Custom PCB (Gerbers in `/pcbs/`)
- MicroSD card (FAT/FAT32)
- 3.5mm stereo jack
- WS2812B LED
- See BOM for full component list

---

### Repository Structure

├── KiCad/ # KiCad 10 project files (schematic + PCB) ├── firmware/ # Compiled firmware + source (coming soon) ├── pcbs/ # Gerber files and PCB references ├── source/ # Firmware source code (coming soon) ├── images/ # Project photos and renders └── docs/ # Measurements, specs, datasheets


---

### License

- Hardware: **CC-BY-SA 4.0**
- Firmware: **MIT**
- Based on UnoCart-2600 by Robin Edwards (GPL)

---

### Credits

- **Hardware & PCB design:** marushio-rima
- **Original UnoCart-2600:** Robin Edwards (electrotrains @ AtariAge)
- **UnoCart firmware extensions:** Christian Speckner (DirtyHairy @ AtariAge)
- **Community:** AtariAge forums

---

## 🇧🇷 PORTUGUÊS

### Visão Geral

O **Atari VCS 2600 Pico2 Cart — Ultimate Edition** é um multi-cartucho
open-source para o Atari 2600, construído em torno do microcontrolador
**WeAct Pico2 B (RP2350B)** rodando a 200MHz.

Este projeto não tem a pretensão de ser "o melhor" multi-cartucho — ele
explora direções ainda não tomadas, preenchendo lacunas reais que a
comunidade Atari 2600 ainda precisa nos dias de hoje.

Use o joystick ou as teclas SELECT/RESET para navegar pelo menu do cartão SD
e selecionar um título para jogar. O cartão SD deve ser formatado em FAT ou
FAT32.

---

### Principais Funcionalidades

- **Compatibilidade física universal** — encaixa tanto nos shells padrão
  Atari originais quanto nos shells **Patola** fabricados no Brasil
  (produzidos até hoje)
- **Uso completo do slot do Atari 2600** — todos os sinais disponíveis
  utilizados, sem necessidade de modificações no console
- **Saída de áudio estéreo independente** — jack P2 3.5mm estéreo,
  completamente independente do caminho de áudio interno do console
- **Novo sistema de som** — engine de áudio estéreo customizado rodando no
  Core 1 do RP2350B (~26.6% de uso do Core 1), com suporte a NTSC, PAL-M
  e PAL
- **Mapper exclusivo customizado** — novo design de mapper com funcionalidades
  não disponíveis em nenhum multi-cartucho existente (detalhes abaixo)
- **~55 emulações de mapper** — cobre todos os esquemas de banking relevantes
  do Atari 2600 (mappers dependentes de internet excluídos por design)
- **SD auto-bootloader** — seleção e boot automático de ROM pelo cartão SD
- **LED RGB WS2812B** — indicador visual de status via PIO
- **Slot MicroSD** — footprint duplo (SMD topo + THT fundo) para flexibilidade
- **UART de debug** — GP17 exposto como ponto de teste TP1
- **Open source** — licença MIT + CC-BY-SA

---

### Mapper Customizado — Ultimate

> *(Especificação completa será publicada junto com o firmware)*

O mapper Ultimate introduz funcionalidades projetadas especificamente para a
comunidade moderna do Atari 2600, incluindo capacidades não exploradas por
nenhuma solução de multi-cartucho existente. Os detalhes serão documentados
junto com o lançamento do código-fonte do firmware.

---

### Hardware

**MCU:** WeAct Pico2 B — RP2350B A4 — dual-core ARM Cortex-M33 @ 200MHz

**Mapeamento GPIO (final):**

| GPIO | Função |
|------|--------|
| GP0–GP12 | A0–A12 (Barramento de endereços) |
| GP13 | SD_CLK |
| GP14 | SD_MOSI |
| GP15 | SD_MISO |
| GP16 | SD_CS |
| GP17 | UART_TX debug (TP1) |
| GP18 | WS2812B (PIO0 SM0) |
| GP19 | PIO_CLK (PIO0 SM1) |
| GP20 | PWM_L (PWM2A) |
| GP21 | PWM_R (PWM2B) |
| GP22–GP27 | SPARE |
| GP28–GP35 | D0–D7 (Barramento de dados) |
| GP36–GP39 | SPARE |
| GP40–GP47 | ADC (não utilizado) |

---

### PCB Customizado

- **Dimensões:** 74 × 52 × 1,6mm — encaixe universal
- **Acabamento:** Máscara verde + ENIG
- **Versão de hardware:** v1.0 A
- **Conector de borda:** 24 pinos × 2,54mm, chanfro 45°×1mm
- **Montagem:** Compatível com o sistema de pinos da Patola (H1/H2 Ø2,5mm)
- **Componentes:** 44 componentes + 3 pontos de teste
- **Passivos:** 0603 (exceto C1a/C1b 0805 — 2× 47µF X5R em paralelo)
- **Roteamento:** ≥1mm entre componentes; 0,5mm (+5V/GND), 0,3mm (3V3),
  0,2mm (sinais); plano GND na face inferior; topologia star ground

---

### Firmware

- **Plataforma:** RP2350B (Raspberry Pi Pico 2 — variante WeAct B)
- **Clock:** 200MHz (overclock)
- **~55 emulações de mapper** (todos os principais esquemas de banking)
- **SD auto-bootloader** com suporte FAT/FAT32
- **Padrões de vídeo:** NTSC, PAL-M, PAL
- **Áudio estéreo:** ~26,6% de uso do Core 1
- **Fonte:** A ser publicado (C / RP2350B SDK)

> Este projeto é um fork/evolução do
> [UnoCart-2600](https://github.com/robinhedwards/UnoCart-2600)
> de Robin Edwards, portado e estendido para a plataforma RP2350B.

---

### Como Construir

> Instruções detalhadas de montagem em breve.

**Requisitos:**
- Módulo WeAct Pico2 B (RP2350B A4)
- PCB customizado (Gerbers em `/pcbs/`)
- Cartão MicroSD (FAT/FAT32)
- Jack estéreo 3,5mm
- LED WS2812B
- Consulte o BOM para a lista completa de componentes

---

### Estrutura do Repositório

├── KiCad/ # Arquivos do projeto KiCad 10 (esquemático + PCB) ├── firmware/ # Firmware compilado + fonte (em breve) ├── pcbs/ # Arquivos Gerber e referências de PCB ├── source/ # Código-fonte do firmware (em breve) ├── images/ # Fotos e renders do projeto └── docs/ # Medições, especificações, datasheets


---

### Licença

- Hardware: **CC-BY-SA 4.0**
- Firmware: **MIT**
- Baseado no UnoCart-2600 de Robin Edwards (GPL)

---

### Créditos

- **Hardware & design de PCB:** marushio-rima
- **UnoCart-2600 original:** Robin Edwards (electrotrains @ AtariAge)
- **Extensões do firmware UnoCart:** Christian Speckner (DirtyHairy @ AtariAge)
- **Comunidade:** Fóruns AtariAge
-------
* Design, hardware and firmware by Robin Edwards (electrotrains at atariage)
* Additional work on firmware by Christian Speckner (DirtyHairy at atariage)

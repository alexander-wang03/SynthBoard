<h1 align="center">SynthBoard: Open-Source Audio Synthesizer 🎶</h1>

<p align="center">
    <a href="https://www.youtube.com/watch?v=wo0ibzK1-dg">
        <img src="https://img.shields.io/badge/YouTube-red?style=flat-square&logo=youtube&logoColor=white" alt="YouTube" align="center" />
    </a>
</p>

<p align="center"><img width=50% alt="" src="/synthboard.jpg" /></p>
SynthBoard is a compact, open-source audio synthesizer designed to provide aspiring musicians with professional-grade sound generation capabilities. The project combines the flexibility of traditional synthesizers with the accessibility and modern design of illuminated grid-based controllers.

---

## 🎯 **Project Overview**

### Key Features:
- **4x4 Button Matrix:** Allows real-time audio triggering with tactile feedback.
- **RGB LED Integration:** Individually addressable LEDs provide interactive lighting effects for enhanced user experience.
- **Waveform Generation & Manipulation:** Supports sine, square, triangle, and sawtooth waveforms with adjustable parameters.
- **8 Potentiometers:** Provide precise control over volume, harmonic content, and ADSR envelope (Attack, Decay, Sustain, Release) settings.
- **Audio Output:** High-quality sound delivered through the STM32's integrated DAC and audio amplifier.
- **Compact Design:** A 3D-printed enclosure optimized for durability and functionality.

## ⚙️ **Hardware Specifications**

### Components:
1. **Microcontroller:** STM32F407G-DISC1, chosen for its:
   - Built-in audio DAC for high-quality sound output.
   - Sufficient GPIO and ADC channels for matrix buttons and potentiometers.
   - SPI support for controlling WS2812B LEDs.
2. **Buttons:** A 4x4 tactile grid optimized with diodes to prevent ghosting.
3. **LEDs:** WS2812B LEDs in a daisy-chain configuration for efficient lighting control.
4. **Potentiometers:** 8 knobs for analog control of audio parameters, connected to ADC channels.
5. **Enclosure:** Designed and validated in Fusion360, featuring modular components and precise cutouts.

## 🛠️ **Software Features**

- **Programming Environment:** STM32CubeIDE using C++ for object-oriented implementation.
- **Real-Time Control:**
  - Audio synthesis based on additive principles and lookup tables for efficiency.
  - Adjustable parameters for harmonic generation and low-pass filtering.
- **LED Control:** RGB animations synchronized with button presses.
- **Audio Buffering:** Continuous playback via I2S protocol with interrupt-driven updates.

### Code Structure:
- **Oscillator Class:** Handles waveform generation and harmonic synthesis.
- **ADSR Envelope Class:** Controls sound amplitude dynamics across Attack, Decay, Sustain, and Release phases.
- **InputHandler:** Manages button presses and potentiometer inputs for seamless interaction.
- **Low-Pass Filter:** Shapes sound frequency for smoother audio output.

## 📚 **Documentation and Resources**

- **Project Report:** [Report (PDF)](./report.pdf)
- **Demo Video:** [YouTube Link](https://www.youtube.com/watch?v=wo0ibzK1-dg)

## 📜 **License**

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

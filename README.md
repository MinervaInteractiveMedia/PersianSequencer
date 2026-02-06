# Persian Chords Sequencer

A Max/MSP MIDI sequencer designed for exploring Persian modal harmony and Middle Eastern musical traditions.

## Overview

This Max/MSP patch is a specialized chord sequencer built around Persian musical intervals and harmonic progressions. It provides an intuitive interface for generating MIDI sequences based on traditional Persian modes (dastgāh) while offering modern sequencing capabilities.

**Current Status:** Phase 1 - Persian Chord Sequencer  
**Planned:** Phase 2 - Euclidean-based percussion sequencer with classical Turkish, Persian, and Arab rhythm patterns

## Features

### Current Implementation (Phase 1)

- **5 Chord Progression Banks**: Pre-programmed chord sequences representing different Persian modal progressions
- **Arpeggiation System**: Each chord is broken down into individual notes with randomized velocity and probabilistic note triggering
- **Multi-Channel MIDI Output**: Support for up to 4 additional MIDI channels for layered instrumentation
- **Adjustable Parameters**:
  - Note length control
  - Interval timing between chord changes
  - Chord progression selection (0-5)
  - Per-channel MIDI routing and enable/disable

### Technical Features

- 4-step counter system for each chord progression
- Randomized velocity (0-127) for organic feel
- Probability-based note triggering (50% gate threshold)
- Real-time MIDI output via `noteout` objects
- Presentation mode UI for live performance

## Chord Progressions

The sequencer includes carefully crafted chord voicings that reflect Persian modal intervals:

**Example progressions include:**
- G-B-D (57 60 64) - Major-like structures
- F-A-C (53 57 60) - Minor-like structures  
- G-Bb-D (55 59 62) - Modal variations
- C-E-G (48 52 55) - Root position triads
- F#-A-D (46 50 53) - Unique Persian intervals

These voicings are designed to work within various Persian dastgāh systems including Shur, Segah, Chahargah, and others.

## Installation

1. Ensure you have [Max/MSP](https://cycling74.com/products/max) installed (version 8.5+ recommended)
2. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/persian-chords-sequencer.git
   ```
3. Open the `.maxpat` file in Max/MSP
4. Configure your MIDI output device in Max/MSP preferences

## Usage

### Basic Operation

1. **Start/Stop**: Toggle the main start button to begin/stop the sequence
2. **Set Note Length**: Adjust the note length parameter (default: 1000ms)
3. **Set Interval**: Control the time between chord changes (default: 1000ms)
4. **Choose Progression**: Select chord index (0-5) to switch between different progressions
5. **Enable Channels**: Activate additional MIDI channels for layered output

### Performance Tips

- Start with a single progression and gradually introduce additional MIDI channels
- Experiment with different note lengths and intervals to create rhythmic variations
- Use the probability gates to create evolving, non-repetitive patterns
- Map to different synthesizers or samplers on each MIDI channel for rich timbral variety

## MIDI Routing

The patch outputs MIDI on multiple channels:
- **Primary Channel**: Main chord progression output
- **Channels 1-3**: Additional programmable channels with individual enable toggles

Each channel can be independently controlled and routed to different MIDI channel numbers.

## Roadmap

### Phase 2: Euclidean Rhythm Engine

The next phase will introduce:

- **Euclidean rhythm generator** for creating complex polyrhythmic patterns
- **Classical rhythm patterns** from:
  - Persian traditions (Reng, Zarbi, Mokhālef)
  - Turkish usul patterns (Aksak, Sofyan, Devr-i Hindi)
  - Arabic iqā'āt (Maqsum, Samai Thaqil, Wahda)
- **Integration** between harmonic and rhythmic layers
- **Pattern banks** for traditional time signatures (5/8, 7/8, 9/8, 10/8, etc.)
- **Probability controls** for each rhythm layer

## Musical Background

### Persian Modal System

Persian classical music is based on the radif system, which organizes melodies into modal families called dastgāh. Unlike Western major/minor tonality, Persian modes feature:

- Microtonal intervals (koron and sori)
- Flexible intonation
- Modal modulation (gushe)
- Specific melodic contours and phrases

This sequencer approximates these intervals using standard MIDI pitches while maintaining the characteristic voice leading and harmonic movement of Persian music.

### Applications

- **Composition**: Explore Persian harmonic progressions as foundation for new works
- **Live Performance**: Use as backing harmony for improvisation
- **Education**: Learn Persian modal relationships and chord structures
- **Sound Design**: Generate MIDI for synthesis and sampling
- **Film Scoring**: Create authentic Middle Eastern harmonic atmospheres

## Technical Requirements

- Max/MSP 8.0 or higher
- MIDI-capable synthesizer or DAW
- Basic understanding of Max/MSP patching (for modifications)

## Contributing

Contributions are welcome! Areas of interest:

- Additional Persian dastgāh progressions
- Turkish makam harmonic patterns
- Arabic maqam sequences
- UI/UX improvements
- Documentation and tutorials

Please open an issue or submit a pull request.

## Acknowledgments

This project draws inspiration from:
- Traditional Persian radif and dastgāh systems
- Turkish makam theory
- Arabic maqam traditions
- Contemporary Middle Eastern composers and improvisers


## References

- *The Radif of Persian Music* - Various editions
- *The Dastgah Concept in Persian Music* - Hormoz Farhat
- *Turkish makam Guide* - Karl Signell
- *Inside Arabic Music* - Johnny Farraj & Sami Abu Shumays

---

**Note**: This is an experimental tool for musical exploration. The MIDI note mappings approximate Persian intervals using equal temperament and may not reflect the subtle microtonal nuances of authentic Persian performance practice.

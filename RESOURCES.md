# Muse 2 EEG Development Resources

Comprehensive guide to tools, libraries, and communities for developing with the Muse 2 EEG headband.

> **Source**: Based on [Muse 101 guide by Anush Mutyala](https://anushmutyala.medium.com/muse-101-how-to-start-developing-with-the-muse-2-right-now-a1b87119be5c)

## Table of Contents
- [Signal Acquisition & Streaming](#signal-acquisition--streaming)
- [Signal Processing](#signal-processing)
- [Visualization](#visualization)
- [Communities & Support](#communities--support)
- [Key Learning Resources](#key-learning-resources)

---

## Signal Acquisition & Streaming

### LSL Outlet Applications
These applications create Lab Streaming Layer (LSL) outlets for the Muse 2:

- **[BlueMuse](https://github.com/kowalej/BlueMuse)** - Windows app for LSL streaming from Muse 2
  - Minimalistic and intuitive GUI
  - Streams EEG and all other sensor data
  - Requires Windows 10

- **[uvicMuse](https://github.com/Venryx/uvicMuse)** - Cross-platform (Mac/Win/Linux) with UDP streaming
  - Streams all Muse 2 data types
  - Can apply filters (Highpass, Lowpass, Notch)
  - UDP streaming support for MATLAB

- **[Petal Metrics](https://petal.tech/)** - ⭐ Recommended for LSL/OSC streaming
  - Streams via both LSL and OSC
  - Automatic CSV logging of sessions
  - Support for extra auxiliary electrodes
  - Frequently updated with new features

### Python LSL Libraries

- **[PyLSL](https://github.com/chkothe/pylsl)** - Python wrapper for Lab Streaming Layer
  - Core library for LSL in Python
  - Simple API for creating inlets/outlets

- **[MuseLSL](https://github.com/alexandrebarachant/muse-lsl)** - Python package for streaming, visualizing, recording
  - Built on top of PyLSL
  - Real-time visualization capabilities
  - Easy recording functionality

- **[Lab Recorder](https://github.com/labstreaminglayer/App-LabRecorder)** - Application for recording LSL streams
  - Save streams for later processing
  - Supports multiple concurrent streams

### Alternative Streaming Methods

- **[Brainflow](https://brainflow.readthedocs.io/)** - Unified SDK for EEG streaming
  - Everything in one SDK (no separate outlet apps needed)
  - Requires BLED112 dongle
  - Pre-trained models for relaxation/concentration

### Web Development Tools

- **[Node-LSL](https://github.com/urish/node-lsl)** - LSL bindings for Node.js web development
  - Use LSL streams in JavaScript
  - Requires users to create LSL outlet

- **[TimeFlux](https://timeflux.io/)** - Graph-based framework for BCI applications
  - No-code approach via YAML configuration
  - Plugin system for signal processing
  - Supports LSL streams

- **[Brains@play](https://brainsatplay.com/)** - ⭐ Framework for brain-responsive web apps
  - Handles Web Bluetooth connection
  - Graph-based architecture
  - Multiplayer/brain-to-brain capabilities
  - Active community

### Mobile Development

- **[Mind Monitor](https://mind-monitor.com/)** - Mobile app for no-code signal acquisition
  - Real-time EEG plotting
  - Data recording
  - OSC streaming to other devices
  - Popular in research community

---

## Signal Processing

### Real-Time Processing

- **[Brainflow](https://brainflow.readthedocs.io/)** - Beginner-friendly filters & real-time analysis
  - Optimized for real-time BCI applications
  - Pre-defined filter parameters
  - Works with single epochs
  - Pre-trained ML models included

- **[Wyrm](https://github.com/bbci/wyrm)** - Real-time optimized BCI toolbox
  - Similar to MNE but for real-time
  - Wyrm Data objects
  - Wide variety of filters and transforms

### Research & Analysis

- **[MNE](https://mne.tools/stable/index.html)** - ⭐ Industry standard for neurophysiological data processing
  - End-to-end EEG analysis pipeline
  - Time-frequency analysis
  - Source localization
  - Extensive documentation
  - Large community

- **[Scipy.signal](https://docs.scipy.org/doc/scipy/reference/signal.html) & [Scipy.fft](https://docs.scipy.org/doc/scipy/reference/tutorial/fft.html)** - Foundational signal processing
  - Custom filter design
  - Spectrograms and wavelets
  - FFT transforms
  - Requires more technical knowledge

### Feature Extraction

- **[Antropy](https://github.com/raphaelvallat/antropy)** - Entropy calculations for EEG features
  - Spectral entropy
  - Shannon entropy
  - Sample entropy
  - Important for emotion detection and classification

- **[PyWavelets](https://pywavelets.readthedocs.io/)** - Wavelet transform implementation
  - All major wavelet families
  - Continuous and discrete wavelets
  - Decomposition and recomposition

---

## Visualization

- **[MNE](https://mne.tools/stable/index.html)** - Comprehensive EEG plotting
  - Event-related potentials (ERPs)
  - Topographic maps
  - Time-frequency representations
  - Real-time plotting support

- **[Wyrm](http://bbci.github.io/wyrm/api/wyrm.html#module-wyrm.plot)** - Real-time plotting for BCI
  - Spectrograms
  - Topographic maps
  - Time-course plots
  - Works with MatPlotLib animation

- **[Visbrain](http://visbrain.org/)** - Multi-dimensional dataset visualization
  - Works with NumPy arrays directly
  - Brain module (MNI space)
  - Sleep module (polysomnography)
  - Signal module (multi-dimensional data)

- **[MuseLSL](https://github.com/alexandrebarachant/muse-lsl)** - ⭐ Quick real-time EEG plotting
  - Fastest option for live visualization
  - One command: `muselsl view`
  - Great for checking electrode contact quality

---

## Communities & Support

### Slack Communities

- **[Brainflow Slack](https://c6ber255cc.execute-api.eu-west-1.amazonaws.com/Express/)** - EEG data filtering & analysis help
  - Support for Brainflow library
  - Signal processing discussions

- **[LabStreamingLayer Slack](https://labstreaminglayer.slack.com/)** - LSL-specific support
  - Troubleshooting LSL streams
  - Multi-device synchronization help

### Active Communities

- **[NeurotechX](https://neurotechx.com/)** - 23k+ neurotech enthusiasts community
  - International presence (30 cities)
  - Muse 2 troubleshooting
  - Project collaboration
  - Educational resources

- **[Brains@play Discord](https://discord.com/invite/sPV7Ekpy)** - Brain-responsive web app development
  - Active development community
  - Innovative BCI web app ideas
  - Framework support

---

## Key Learning Resources

### Tutorials & Guides

- **[EEG-Notebooks](https://github.com/NeuroTechX/eeg-notebooks)** - Classic EEG experiments in Python/Jupyter
  - Out-of-the-box experiments
  - LSL connection examples
  - Stimulus presentation code
  - Signal processing pipelines
  - ML analysis examples

- **[Muse 101 Article](https://anushmutyala.medium.com/muse-101-how-to-start-developing-with-the-muse-2-right-now-a1b87119be5c)** - Comprehensive development guide
  - Complete overview of Muse 2 development
  - Tool comparisons and recommendations
  - Best practices and common pitfalls

### Key Concepts to Learn

1. **Power Spectral Density (PSD)** - Frequency domain analysis
2. **Wavelets** - Time-frequency decomposition
3. **Event-Related Potentials (ERP)** - Time-locked responses
4. **Filtering** - Noise reduction (highpass, lowpass, notch)
5. **Artifacts** - Eye blinks, muscle activity, electrode noise

---

## Development Workflow

Typical pipeline for Muse 2 development:

1. **Signal Acquisition** - Get raw EEG stream
2. **Preprocessing** - Apply filters to clean signal
3. **Feature Extraction** - Transform data (PSD, wavelets, etc.)
4. **Analysis/Classification** - Extract meaningful patterns
5. **Action Mapping** - Trigger events based on brain state

---

## Quick Start Recommendations

### For Beginners
1. Start with **MuseLSL** for visualization
2. Use **MNE** for learning signal processing concepts
3. Join **NeurotechX** community for support
4. Follow **EEG-Notebooks** tutorials

### For Web Developers
1. Use **Brains@play** framework
2. Explore **Mind Monitor** for mobile
3. Study **Web Bluetooth API** basics

### For Real-Time Applications
1. Use **Brainflow** or **Wyrm** for processing
2. **Petal Metrics** for streaming
3. **MuseLSL** for quick visualization checks

---

## Hardware Notes

### Muse 2 Electrode Positions
- **AF7, AF8** - Forehead (frontal lobe)
- **TP9, TP10** - Above ears (temporal lobe)

### Considerations
- Not ideal for visual evoked potentials (no occipital electrodes)
- Great for frontal lobe studies (attention, meditation, working memory)
- Good for temporal lobe (auditory processing, some emotion)

---

## Contributing

This resource list is maintained as part of the MuseEEGProject. Contributions and updates are welcome!

## License

This documentation is provided as-is for educational and research purposes.

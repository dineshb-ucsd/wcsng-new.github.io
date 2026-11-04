---
layout: publication
title: "RadioStream: A Wideband Multi-Antenna SDR Platform"
short_title: "RadioStream"
tags: Communications
cover: /assets/images/radiostream/architecture.png
disp_cover: "False" # architecture figure is wide; shown in the description below instead of the fixed 16:9 cover slot
authors: "Adel Heidari, Jeeva Keshav Sattianarayanin, Rohith Reddy Vennam, Aaron Tartz, Agrim Gupta, Kishore Rajendran, Raviteja Devara, Lakshman Bhaskaran, Radha Krishna Ganti, Dinesh Bharadia" # needed for publications/
author_list:
    - name: Adel Heidari*
      url: https://www.linkedin.com/in/adel-heidari-85490321a/
      email: adheidari@ucsd.edu
    - name: Jeeva Keshav Sattianarayanin*
      email: jeevakeshavs@smail.iitm.ac.in
    - name: Rohith Reddy Vennam
      url: https://acsweb.ucsd.edu/~rvennam/
      email: rvennam@ucsd.edu
    - name: Aaron Tartz
      email: atartz@ucsd.edu
    - name: Agrim Gupta
      url: https://agrim9.github.io/
      email: agg003@ucsd.edu
    - name: Kishore Rajendran
      email: kirajendran@ucsd.edu
    - name: Raviteja Devara
      email: raviteja@wiseriitm.in
    - name: Lakshman Bhaskaran
      email: lakshman@wiseriitm.in
    - name: Radha Krishna Ganti
      email: rganti@ee.iitm.ac.in
    - name: Dinesh Bharadia
      url: https://dineshb-ucsd.github.io/
      email: dineshb@ucsd.edu
eqcon: true #Put true if you want equal contrribution on pub page
conference: "ACM MobiCom 2026"
conference_site: https://www.sigmobile.org/mobicom/2026/
paper: /files/radiostream.pdf
slides: /files/radiostream_mobicom_slides.pdf
slides_label: "MobiCom Slides"
slides2: /files/radiostream_grcon_slides.pdf
slides2_label: "GNURadio Slides"
# video: teaser to be added once hosted (e.g. YouTube embed URL)
miscs:
    - content_type: Poster
      content_url: /files/radiostream_poster.pdf
    - content_type: GNU Radio Conference Talk
      content_url: https://events.gnuradio.org/event/28/contributions/896/
description:
    - title: "Why Host-Centric SDRs Break at Wideband"
      text: "Software-defined radios underpin many deployed wireless systems, but host-centric streaming becomes unreliable at high bandwidths, with many antennas, and when time-granular control is required. The root difficulty is a <b>timing-domain mismatch</b>: the FPGA and RF front-end run on a deterministic, clock-driven timeline locked to the RF sampling clock, while the host runs asynchronously under OS scheduling, interrupts, and queueing delay. Traditional stacks resolve this by forcing the host to keep pace with the radio, so an ordinary context switch can leave the buffer running dry. At wideband rates this produces underflows, overflows, and late commands. Modern applications need all four of continuous wideband streaming, RF synchronization across channels, slot-level control, and easy programmability — and existing platforms support only one or two."
      image: /assets/images/radiostream/requirements.png
      image_width: 600 # px

    - title: "A Slot-Synchronous Host–Radio Contract"
      text: "We present <b>RadioStream</b>, a radio-centric, slot-synchronous SDR architecture in which the host and radio coordinate using <i>slots</i> (a pre-defined unit of time) rather than individual sample transfers. The FPGA owns slot timing and all time-critical radio actions, and exports slot boundaries as 64-byte slot-tick Ethernet packets. The host programs future slots against that timeline, and the FPGA applies every radio-visible update only at slot boundaries, with control and data both tagged by slot number. Slot-aligned buffering and a two-slot look-ahead absorb transport delay and host jitter, so the host can stay fully asynchronous while radio behavior remains deterministic. A lightweight three-packet fronthaul (slot ticks, jumbo-frame data, fixed-size control) runs over 100 GbE, and a DPDK-based host path hands samples to applications such as GNU Radio, Python, and MATLAB through shared memory, with no kernel in the way."
      image: /assets/images/radiostream/architecture.png
      image_width: 900 # px

    - title: "Built on RFSoC, Up to 8T8R"
      text: "We implement RadioStream on the Xilinx XCZU48DR RFSoC, prototyping on both the commercially available RFSoC 4x2 board and a custom 8T8R platform: an RFSoC system-on-module paired with an RF board carrying dual QSFP28 cages, SMA connectors for all eight TX and eight RX chains, PL-side DDR4 for slot-indexed IQ buffering, and a zero-delay-multiplier clock circuit that drives all ADC and DAC tiles to eliminate inter-tile skew. The design stays lightweight on the FPGA, leaving over 84% of LUTs and 99% of DSPs free for additional processing blocks."
      image: /assets/images/radiostream/hardware.jpg
      image_width: 700 # px

    - title: "Deterministic Timing at 90 Gbps"
      text: "On a 100 Gbps interface, RadioStream sustains <b>90 Gbps</b> concurrently on uplink and downlink with no packet drops across a 5-hour experiment, and streams <b>2 GHz</b> of aggregated RF bandwidth. Slot-tick jitter measured at the host stays near 113 ns at the median and under <b>600 ns at the 99th percentile</b>, confirming that the FPGA remains the timing master while the host simply follows that timeline. Per-slot control reaches the RF output in under <b>500 ns</b>, measured on an NCO frequency update. Against a commercial USRP X410 baseline given more CPU cores, RadioStream is lossless where the X410 drops 99% of samples at 1966.08 Msps, using only three cores."
      image: /assets/images/radiostream/jitter.png
      image_width: 600 # px

    - title: "Applications: Beam Sweeping and Coherent Sensing"
      text: "We demonstrate these capabilities on three workloads sharing the same timing, transport, and control substrate. A point-to-point 28 GHz link carries a continuous 5G NR OFDM waveform with stable 4–6% EVM, and a 491.52 MHz WiFi waveform yields clean 64-QAM and 256-QAM constellations. A mmWave beam-sweeping experiment sweeps the receiver across azimuth and selects the correct beam to within 2.5°, with only 0.5 dB SNR loss. Finally, a sub-6 GHz multi-antenna capture resolves two sources in joint angle and range: moving from 2 antennas to 4 sharpens the angular profile, and raising bandwidth to 491.52 MHz improves distance resolution from 2.4 m to 0.6 m."
      image: /assets/images/radiostream/beam_sweep.jpg
      image_width: 800 # px

    - image: /assets/images/radiostream/aoa_range.png
      image_width: 900 # px
citation:
    - text: 'Adel Heidari, Jeeva Keshav Sattianarayanin, Rohith Reddy Vennam, Aaron Tartz, Agrim Gupta, Kishore Rajendran, Raviteja Devara, Lakshman Bhaskaran, Radha Krishna Ganti, Dinesh Bharadia. "RadioStream: A Wideband Multi-Antenna SDR Platform." In Proceedings of the 32nd Annual International Conference on Mobile Computing and Networking (MobiCom ''26), Austin, TX, USA, 2026.'
      bib: "https://doi.org/10.1145/3795866.3844452"
      bibtex: "
      @inproceedings{heidari2026radiostream,
  title={RadioStream: A Wideband Multi-Antenna SDR Platform},
  author={Heidari, Adel and Sattianarayanin, Jeeva Keshav and Vennam, Rohith Reddy and Tartz, Aaron and Gupta, Agrim and Rajendran, Kishore and Devara, Raviteja and Bhaskaran, Lakshman and Ganti, Radha Krishna and Bharadia, Dinesh},
  booktitle={Proceedings of the 32nd Annual International Conference on Mobile Computing and Networking (MobiCom '26)},
  year={2026},
  doi={10.1145/3795866.3844452}
}
"
---

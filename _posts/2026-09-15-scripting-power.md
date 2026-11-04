---
layout: publication
title: "Scripting Traffic, Aligning Power: A 5G Testbed Integrating gNB Activity and Commercial UE Power"
short_title: "Scripting Power"
tags: Communications
cover: /assets/images/scripting-power/overview.png
disp_cover: "False" # overview figure is wide; shown in the description below instead of the fixed 16:9 cover slot
authors: "Haochen Wang, Aaron Tartz, Adel Heidari, Kotturi Sai Prasanth, Agrim Gupta, Radha Krishna Ganti, Dinesh Bharadia" # needed for publications/
author_list:
    - name: Haochen Wang
      email: haw057@ucsd.edu
    - name: Aaron Tartz
      email: atartz@ucsd.edu
    - name: Adel Heidari
      url: https://www.linkedin.com/in/adel-heidari-85490321a/
      email: adheidari@ucsd.edu
    - name: Kotturi Sai Prasanth
      email: ksaiprasanth7@smail.iitm.ac.in
    - name: Agrim Gupta
      url: https://agrim9.github.io/
      email: agg003@ucsd.edu
    - name: Radha Krishna Ganti
      email: rganti@ee.iitm.ac.in
    - name: Dinesh Bharadia
      url: https://dineshb-ucsd.github.io/
      email: dineshb@ucsd.edu
eqcon: false #Put true if you want equal contrribution on pub page
conference: "ACM WiNTECH 2026"
conference_site: https://acm-wintech.github.io/2026/
paper: /files/scripting_power.pdf
github: https://github.com/ucsdwcsng-iitm/scripting_traffic
slides: /files/scripting_power_slides.pdf
description:
    - title: "Why UE Power Is Hard to Study"
      text: "On a modern smartphone, the cellular subsystem is one of the largest energy consumers: on a Google Pixel 9, cellular communication accounts for roughly 46% of total device energy during both normal usage and standby, more than compute, memory, or display. That power is jointly determined by application-layer IP traffic and by the gNB's configuration and scheduling decisions. Studying this relationship on real hardware is challenging because the application server, radio activity, and UE are distributed across separate systems, making them difficult to instrument and control within a single experimental environment. As a result, most studies rely on analytical models such as 3GPP TR 38.840, which assigns relative power units to slot-level activities but is not a calibrated replica of any commercial modem."
      image: /assets/images/scripting-power/pixel9_energy.jpg
      image_width: 600 # px

    - title: "A Slot-Aligned 5G Measurement Platform"
      text: "We present a configurable 5G testbed that integrates these components into a unified experimental platform. A Linux host runs an Open5GS core and an srsRAN gNB serving a private 5G standalone cell over a USRP B210 (band n41, 20 MHz, 30 kHz SCS). The UE is a commercial Telit FN990A28 data card built around Qualcomm's Snapdragon X65 modem, mounted on a PCIe-to-M.2 HAT on a Raspberry Pi 5, with an INA219 current sensor measuring the modem supply. The platform drives either <b>real Internet applications</b> or <b>arbitrary scripted traffic</b> over the same radio path, and links per-slot gNB PHY/FAPI/scheduler activity to hardware-measured UE power using an efficient TR 38.840-based timing-alignment method."
      image: /assets/images/scripting-power/overview.png
      image_width: 900 # px

    - image: /assets/images/scripting-power/hardware.jpg
      image_width: 700 # px

    - title: "Same Throughput, Different Energy"
      text: "A programmable bidirectional traffic generator lets us script downlink and uplink rate schedules down to 1 ms resolution. Even simple probes reveal that UE energy is not determined by average traffic volume alone: for example, an uplink burst train and an uplink triangle deliver the same aggregate throughput over 60 s but consume substantially different energy, because distinct traffic patterns activate different combinations of uplink transmission, downlink reception, control monitoring, retransmissions, and modem state transitions."
      image: /assets/images/scripting-power/traffic_probes.png
      image_width: 900 # px

    - title: "Case Study: gNB-Power"
      text: "As one demonstration of what the resulting dataset enables, we build <b>gNB-Power</b>, an XGBoost estimator that predicts commercial UE power from causal gNB-observable features alone. Across five real applications (YouTube, Instagram, slither.io, X, and Zoom), gNB-Power predicts instantaneous UE power to 86–133 mW MAE, roughly halving the error of the standardized TR 38.840 baseline, with a mean interval-energy error of 1.1% compared with 16.0% for raw TR 38.840. Trained <i>only</i> on scripted synthetic traffic, it still transfers to unseen real applications (150 mW MAE, 4.3% energy error), outperforming even a TR 38.840 calibration fit directly on the target power. The platform offers a flexible measurement primitive for UE power-saving studies, enabling controlled investigation of how both application-layer and network-side decisions affect UE energy consumption."
      image: /assets/images/scripting-power/estimation.png
      image_width: 900 # px
citation:
    - text: 'Haochen Wang, Aaron Tartz, Adel Heidari, Kotturi Sai Prasanth, Agrim Gupta, Radha Krishna Ganti, Dinesh Bharadia. "Scripting Traffic, Aligning Power: A 5G Testbed Integrating gNB Activity and Commercial UE Power." In Proceedings of the ACM Workshop on Wireless Network Testbeds, Experimental Evaluation & Characterization (WiNTECH ''26), Austin, TX, USA, 2026.'
      bib: "https://doi.org/10.1145/3831662.3844174"
      bibtex: "
      @inproceedings{wang2026scripting,
  title={Scripting Traffic, Aligning Power: A 5G Testbed Integrating gNB Activity and Commercial UE Power},
  author={Wang, Haochen and Tartz, Aaron and Heidari, Adel and Prasanth, Kotturi Sai and Gupta, Agrim and Ganti, Radha Krishna and Bharadia, Dinesh},
  booktitle={Proceedings of the ACM Workshop on Wireless Network Testbeds, Experimental Evaluation \\& Characterization (WiNTECH '26)},
  year={2026},
  doi={10.1145/3831662.3844174}
}
"
---

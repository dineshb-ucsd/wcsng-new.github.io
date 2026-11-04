---
layout: publication
title: "AgriSense: Battery-Free Soil Sensing for Next-Gen Connected Agriculture"
short_title: "AgriSense"
tags: Backscatter
cover: /assets/images/agrisense/agrisense-overview.png
authors: "Ishan Bansal, Nagarjun Bhat, Agrim Gupta, Harine Govindarajan, Dinesh Bharadia" # needed for publications/
author_list:
    - name: Ishan Bansal
      url: https://b-ishan.github.io/
      email: isbansal@ucsd.edu
    - name: Nagarjun Bhat
      email:  nbhat@ucsd.edu
    - name: Agrim Gupta
      url: https://agrim9.github.io/
      email: agg003@ucsd.edu
    - name: Harine Govindarajan
      email: hgovindarajan@ucsd.edu
    - name: Dinesh Bharadia
      url: https://dineshb-ucsd.github.io/
      email: dineshb@ucsd.edu
eqcon: false #Put true if you want equal contrribution on pub page
conference: "AgWireless 2026"
conference_site: https://arawireless.org/agwireless26/
video: https://www.youtube.com/embed/7eiO4BO_wTQ
video_str: Demonstration of AgriSense
miscs:
    - content_type: Poster
      content_url: /files/agrisense_poster.pdf
description: # all combinations are possible: (title+text+image, title+image, text+image etc), things will be populated in orders
    - title: "The Data Problem Holding AI Agriculture Back"
      text: "AI promises to transform farming — precision irrigation, predictive disease control, autonomous fertigation. But AI is only as smart as the data feeding it. Today's sensor networks are sparse by design: at $100+ per node, farmers can afford only a handful of sensors per field, leaving vast swaths of land entirely unmeasured. AI models interpolate across these blind regions and routinely get it wrong — one study found that missing data streams alone cause 35% water waste. The missing ingredient isn't better AI models. It's dense, continuous, ground-truth data from the soil itself. Without it, AI for agriculture remains a distant promise."
      image: /assets/images/agrisense/agrisense-ai-data-gap.jpg
      image_width: 600 # px
    - title: "The Sensing Bottleneck — and How We Break It"
      text: "Two forces conspire to keep field sensing sparse. First, <b>prohibitive node cost</b>: at $100+ per sensor, deploying the thousands of nodes needed for true spatial coverage would bankrupt any farm operation. Second, <b>the battery trap</b>: even if you could afford the upfront cost, replacing thousands of buried batteries every few years across a large field is operationally impossible at scale. AgriSense breaks both barriers at once. By decoupling sensing from power using RFID — pairing a standard soil sensor directly with an ultra-low-cost passive RFID tag — we produce a sensor node that costs about <b>$1, needs zero batteries, and operates indefinitely</b>. This is the ZenseTag platform: sticker-like, flexible, and built entirely from commercial off-the-shelf components. No batteries to replace. No complex electronics. Just perpetual soil intelligence."
      image: /assets/images/agrisense/agrisense-zensetag-platform.jpg
      image_width: 600 # px
    - title: "Field-Scale Data Harvesting: 70x Cheaper, Zero Infrastructure"
      text: "Cheap sensors alone don't solve the problem — you still need to read them across a large field. Conventional battery-free networks address this with fixed RFID readers, but 200 fixed readers for a 5-hectare field costs $200,000 in infrastructure alone. AgriSense takes a radically different approach: a single RFID reader mounted on a drone reads every node en-route as it flies a pre-planned path. A 10km drone flight at 3m/s covers a 5-hectare field with 2,000 sensor nodes in 60 minutes — with no fixed infrastructure at all. The total system cost, including a decade of maintenance, comes to roughly $5,000. That's 70x cheaper than conventional active sensor networks and more than 40x cheaper than fixed battery-free infrastructure."
      image: /assets/images/agrisense/agrisense-drone-harvesting.png
      image_width: 600 # px
    - text: "
        <center><table style=\"border-collapse: collapse; width: 90%; max-width: 900px; text-align: center; font-size: 15px; margin: 0 auto;\">
          <thead>
            <tr>
              <th style=\"border: 1px solid #999; padding: 10px; background-color: #4a4a4a; color: #fff;\">Cost Category</th>
              <th style=\"border: 1px solid #999; padding: 10px; background-color: #8b1a1a; color: #fff;\">Active Sensor Networks</th>
              <th style=\"border: 1px solid #999; padding: 10px; background-color: #8b1a1a; color: #fff;\">Battery-free Networks</th>
              <th style=\"border: 1px solid #999; padding: 10px; background-color: #2e6b2e; color: #fff;\">Our Approach</th>
            </tr>
          </thead>
          <tbody>
            <tr style=\"background-color: #fdf0f0;\">
              <td style=\"border: 1px solid #999; padding: 9px; font-weight: bold;\">Nodes</td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #8b1a1a; font-weight: bold;\">$200,000<br><span style=\"font-weight:normal;\">($100/node)</span></td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #8b1a1a; font-weight: bold;\">$2,000<br><span style=\"font-weight:normal;\">($1/node)</span></td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #2e6b2e; font-weight: bold;\">$2,000<br><span style=\"font-weight:normal;\">($1/node)</span></td>
            </tr>
            <tr style=\"background-color: #fff8f8;\">
              <td style=\"border: 1px solid #999; padding: 9px; font-weight: bold;\">Gateways / Equipment</td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #8b1a1a; font-weight: bold;\">$10,000<br><span style=\"font-weight:normal;\">(4-5 LoRa-WANs)</span></td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #8b1a1a; font-weight: bold;\">$200,000<br><span style=\"font-weight:normal;\">(200 fixed readers)</span></td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #2e6b2e; font-weight: bold;\">$2,000<br><span style=\"font-weight:normal;\">(drone + reader)</span></td>
            </tr>
            <tr style=\"background-color: #fdf0f0;\">
              <td style=\"border: 1px solid #999; padding: 9px; font-weight: bold;\">Long Term (10yr) Maintenance</td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #8b1a1a; font-weight: bold;\">$150,000<br><span style=\"font-weight:normal;\">(batteries + labor)</span></td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #8b1a1a; font-weight: bold;\">~$20,000<br><span style=\"font-weight:normal;\">(readers + labor)</span></td>
              <td style=\"border: 1px solid #999; padding: 9px; color: #2e6b2e; font-weight: bold;\">~$1,000<br><span style=\"font-weight:normal;\">(basic servicing)</span></td>
            </tr>
            <tr style=\"background-color: #fff;\">
              <td style=\"border: 1px solid #999; padding: 9px; font-weight: bold;\">Total Gross</td>
              <td style=\"border: 1px solid #999; padding: 9px; background-color: #8b1a1a; color: #fff; font-weight: bold; font-size: 16px;\">~$350,000</td>
              <td style=\"border: 1px solid #999; padding: 9px; background-color: #8b1a1a; color: #fff; font-weight: bold; font-size: 16px;\">~$225,000</td>
              <td style=\"border: 1px solid #999; padding: 9px; background-color: #2e6b2e; color: #fff; font-weight: bold; font-size: 16px;\">~$5,000</td>
            </tr>
          </tbody>
        </table></center>
        <p style=\"text-align:center; font-weight: bold; margin-top: 8px; color: #2e6b2e;\">Field: 5ha @ 250m x 200m &nbsp;|&nbsp; 2000 nodes @ 50x40 grid &nbsp;|&nbsp; Drone path: 10km @ 3m/s &nbsp;|&nbsp; Duration: 60 min</p>
        <div style=\"display:flex; flex-wrap:wrap; justify-content:center; gap:10px; margin: 16px 0 8px 0;\">
          <div style=\"background:#2e6b2e; color:#fff; border-radius:8px; padding:8px 12px; text-align:center; width:110px; box-sizing:border-box;\">
            <div style=\"font-size:26px; font-weight:bold; line-height:1.1;\">$1</div>
            <div style=\"font-size:12px; margin-top:3px;\">per sensor node</div>
          </div>
          <div style=\"background:#2e6b2e; color:#fff; border-radius:8px; padding:8px 12px; text-align:center; width:110px; box-sizing:border-box;\">
            <div style=\"font-size:26px; font-weight:bold; line-height:1.1;\">70x</div>
            <div style=\"font-size:12px; margin-top:3px;\">cost reduction</div>
          </div>
          <div style=\"background:#2e6b2e; color:#fff; border-radius:8px; padding:8px 12px; text-align:center; width:110px; box-sizing:border-box;\">
            <div style=\"font-size:26px; font-weight:bold; line-height:1.1;\">2,000</div>
            <div style=\"font-size:12px; margin-top:3px;\">nodes in 60 min</div>
          </div>
          <div style=\"background:#2e6b2e; color:#fff; border-radius:8px; padding:8px 12px; text-align:center; width:110px; box-sizing:border-box;\">
            <div style=\"font-size:26px; font-weight:bold; line-height:1.1;\">0</div>
            <div style=\"font-size:12px; margin-top:3px;\">batteries</div>
          </div>
        </div>
        "
    - title: "From Lab to Landscape: End-to-End Field Validation"
      text: "We validated every layer of the pipeline in real field conditions — not simulated or lab-only. The soil sensing physics checks out: IDC capacitance tracks volumetric water content linearly across the full soil moisture range, matching the Topp model at 915 MHz. Soil property changes directly shift the backscattered wireless signal detected by the drone-equipped RFID reader, giving a clear, reliable measurement channel. In the field, dense ZenseTag deployments were read by a drone-mounted RFID reader flying overhead, and sensor data was surfaced in real time through an AR application — letting growers see a live soil map overlaid on the physical field just by pointing a phone at it.
        <br><br>
        <center><iframe width=\"768\" height=\"432\" max-width=\"100%\" src=\"https://www.youtube.com/embed/CDn5hxnWvCo\" frameborder=\"1\" allowfullscreen></iframe></center>"
      image: /assets/images/agrisense/agrisense-field-validation.jpg
      image_width: 600 # px
    - title: "Closing the Loop: Sensor Foundation Models for Autonomous Farm Orchestration"
      text: "Dense, continuous soil data is the missing foundation for physical AI in agriculture. With that foundation in place, AgriSense points toward a fully autonomous precision farming pipeline. <b>Stage 1</b> uses drone-harvested sensor data to generate on-demand, high-resolution soil maps across the entire field. <b>Stage 2</b> feeds these maps into Sensor Language Foundation Models and spatial AI agents that learn the dynamics of root-zone moisture, predict stress before it becomes visible, and act as an always-on agronomy advisor. <b>Stage 3</b> closes the loop: AI decisions drive automated precision actuation systems that deliver exactly the right amount of water and nutrients to exactly the right locations — with the grower kept in the loop through an AR interface that requires zero manual data entry. The result is a farm that senses, thinks, and acts — continuously, autonomously, and at scale."
      image: /assets/images/agrisense/agrisense-overview.png
      image_width: 800 # px
    - title: "Deployment at ARA: A Living Laboratory for Precision Agriculture"
      text: "AgriSense is being deployed at the <a href=\"https://arawireless.org/\"><b>NSF ARA Wireless Living Lab</b></a> — a large-scale outdoor research testbed spanning hundreds of acres of real agricultural land in Ames, Iowa. ARA provides the wireless backbone infrastructure (towers, backhaul, edge compute) that complements AgriSense's dense ground-sensing layer: our battery-free nodes feed soil data into ARA's connected infrastructure, creating a vertically integrated stack from physical soil to AI-driven actuation. This is not a controlled greenhouse or parking-lot pilot — it is a working farm environment with real crops, real weather, and real agronomic stakes. Deploying at ARA lets us stress-test drone-based data harvesting at field scale, validate sensing accuracy across heterogeneous soil conditions, and build the ground-truth datasets that will train the next generation of Sensor Language Foundation Models for agriculture."
      # image: /assets/images/agrisense/agrisense-ara-testbed.jpg # TODO: add ARA testbed aerial/field photo
      # image_width: 800 # px
    - title: "Awards & Recognition"
      text: "
        <div style=\"display:flex; flex-wrap:wrap; justify-content:center; gap:16px; margin: 12px 0;\">
          <div style=\"border:2px solid #c9a227; border-radius:8px; padding:10px 12px; width:190px; text-align:center; background:#fffdf0; box-sizing:border-box;\">
            <div style=\"font-size:28px; margin-bottom:4px;\">&#127942;</div>
            <div style=\"font-weight:bold; font-size:14px; color:#7a5c00;\">Best Paper Award</div>
            <div style=\"font-size:13px; margin-top:3px;\">IEEE RFID 2025</div>
            <div style=\"font-size:13px; color:#555;\"><a href=\"https://wcsng.ucsd.edu/sensync/\">SenSync</a>: Real-Time and Accurate Passive Sensing</div>
          </div>
          <div style=\"border:2px solid #aaa; border-radius:8px; padding:10px 12px; width:190px; text-align:center; background:#f8f8f8; box-sizing:border-box;\">
            <div style=\"font-size:28px; margin-bottom:4px;\">&#129352;</div>
            <div style=\"font-weight:bold; font-size:14px; color:#444;\">Best Demo — Runner-up</div>
            <div style=\"font-size:13px; margin-top:3px;\">ACM MobiCom 2024</div>
            <div style=\"font-size:13px; color:#555;\"><a href=\"https://wcsng.ucsd.edu/zensetag_demo/\">ZenseTag Demo</a>: Real-Time Passive RFID Sensing</div>
          </div>
          <div style=\"border:2px solid #aaa; border-radius:8px; padding:10px 12px; width:190px; text-align:center; background:#f8f8f8; box-sizing:border-box;\">
            <div style=\"font-size:28px; margin-bottom:4px;\">&#129352;</div>
            <div style=\"font-weight:bold; font-size:14px; color:#444;\">Best Demo — Runner-up</div>
            <div style=\"font-size:13px; margin-top:3px;\">ACM/IEEE SenSys 2025</div>
            <div style=\"font-size:13px; color:#555;\"><a href=\"https://wcsng.ucsd.edu/sigar_demo/\">SIGAR</a>: Sensor Integration Gateway using AR</div>
          </div>
        </div>
        "
    - title: Related Publications
      text: "AgriSense builds on our growing line of award-winning work in battery-free RFID sensing:
        <ul style=\"line-height:2;\">
          <li><a href=\"https://wcsng.ucsd.edu/zensetag/\"><b>ZenseTag</b></a> — RFID-assisted twin-tag single antenna COTS sensor interface. ACM SenSys 2024.</li>
          <li><a href=\"https://wcsng.ucsd.edu/zensetag_demo/\"><b>ZenseTag Demo</b></a> — Real-time passive RFID sensing. ACM MobiCom 2024. &nbsp;<span style=\"background:#f0f0f0; border:1px solid #aaa; border-radius:4px; padding:2px 7px; font-size:12px;\">&#129352; Best Demo Runner-up</span></li>
          <li><a href=\"https://wcsng.ucsd.edu/sensync/\"><b>SenSync</b></a> — Real-time and accurate passive sensing. IEEE RFID 2025. &nbsp;<span style=\"background:#fffdf0; border:1px solid #c9a227; border-radius:4px; padding:2px 7px; font-size:12px;\">&#127942; Best Paper Award</span></li>
          <li><a href=\"https://wcsng.ucsd.edu/sigar_demo/\"><b>SIGAR</b></a> — Sensor integration gateway using augmented reality. ACM/IEEE SenSys 2025. &nbsp;<span style=\"background:#f0f0f0; border:1px solid #aaa; border-radius:4px; padding:2px 7px; font-size:12px;\">&#129352; Best Demo Runner-up</span></li>
          <li><a href=\"https://wcsng.ucsd.edu/tunetag/\"><b>TuneTag</b></a> — Long-range reliable battery-free sensing. IEEE Journal of RFID 2025.</li>
        </ul>"
---

---
title: "Dempster–Shafer Theory for Condition Diagnosis"
image: "/assets/dsp1.png"
excerpt: "Utilizing the Dempster–Shafer Theory for Condition Diagnosis of a Continuous Casting Machines."
---
*_URL pdf (RUS): https://vestnikvivt.ru/ru/journal/pdf?id=1410_
*_URL to test model: https://damshaf.onrender.com/_


The paper aims to apply the Dempster–Shafer Theory (DST) to improve diagnostics of industrial equipment, focusing on continuous casting machines (CCM) in metallurgy.
The main goal was to create a mathematical and software framework that aggregates uncertain, noisy sensor data — temperature, vibration, and acoustic signals — to assess equipment condition more reliably.

Key results include:

A multi-level DST-based diagnostic model for data fusion under uncertainty.
Implementation of adaptive evidence combination, switching between Dempster’s and Yager’s rules depending on the conflict coefficient.
Experimental validation showing a 5–6% accuracy improvement and reduced false confidence in high-conflict scenarios.
A comparison with the open-source pyds library confirmed better speed and robustness of the proposed approach.
The developed system provides a foundation for intelligent maintenance, IoT-based monitoring, and future multi-agent diagnostic architectures in industrial automation.


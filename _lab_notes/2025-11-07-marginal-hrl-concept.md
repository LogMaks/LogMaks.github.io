---
title: "Marginal HRL for Asymmetric Multi-Agent Systems"
date: 2025-11-07
excerpt: "Early concept note on treating computation as a scarce, allocatable resource in hierarchical MARL."
status: concept note
---

## Problem

Classical MARL assumes homogeneous agents with fixed computational and communication capacity. Real systems (drones, robots, vehicles) differ in resources, observation limits, and safety requirements.

## Hypothesis

**Marginal Hierarchical Reinforcement Learning (M-HRL)** can improve coordination by treating computation as a scarce resource and allocating a leader-controlled budget between safety and task layers across a coalition.

## Possible Formalization

Lexicographic hierarchy: safety layer dominates reward pursuit; leader agent migrates computational priority based on marginal utility of control.

## Possible Experiment

Small-scale asymmetric MARL simulation with variable agent compute budgets and safety-critical constraints.

## Status

Concept note — early-stage.

{% assign marginal_post = site.posts | where_exp: "p", "p.title contains 'Marginal Hierarchical'" | first %}
{% if marginal_post %}
See also the [full concept post]({{ marginal_post.url | relative_url }}).
{% endif %}

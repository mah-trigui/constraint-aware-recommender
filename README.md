# Constraint-Aware Recommender

A geography-first recommendation project showing how hard delivery constraints can shape recommender architecture before ranking begins.

## Project Website

[View Project Site](https://mah-trigui.github.io/constraint-aware-recommender/)

## Overview

This project predicts which restaurant vendors customers are likely to order from in a marketplace with:
- a small vendor catalog
- sparse customer history
- strong location and delivery constraints

Instead of defaulting to collaborative filtering, the recommender was built around geography first.

## Core Idea

A hard constraint should not be treated as just another feature.

In this problem, geography defines the feasible vendor set. Recommendations are therefore generated inside a geographic boundary first, then ranked using behavioral and proximity signals.

## Architecture

![Architecture](images/architecture.jpg)

## Main Design Components

- vendor geographic zones from K-means clustering
- customer assignment to nearest vendor zone
- customer segmentation using gender, location count, and account tenure
- within each segment × zone pair, vendor ranking by historical frequency and inverse distance

## Selected Implementation Elements

- customer × location profiles
- vendor tag grouping into broader cuisine families
- coordinate cleaning and zone assignment
- segment × zone recommendation engine
- customer × vendor submission frame generation

## Key Takeaway

**Hard constraints belong in the architecture, not just the feature list.**

## Public Scope

This repository shares the recommender design logic, selected code structure, and project presentation only.

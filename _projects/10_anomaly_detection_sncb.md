---
layout: page
title: Anomaly Detection in Diesel Train Cooling Systems
description: Developed unsupervised models to detect anomalies in train cooling systems for the Belgian National Railway Company (SNCB), helping prevent train delays and reduce maintenance costs.
img: assets/img/sncb_dashboard.png
importance: 3
year: 2023
semester: Fall 2023
github: https://github.com/kamrulkonok/Anomaly-Detection-in-Diesel-Train-Cooling-Systems
technologies: Python, SQL, Scikit-learn, Pandas, NumPy, Matplotlib, Tableau
---

## Overview

Collaborated with the National Railway Company of Belgium (SNCB) on a data-driven anomaly detection system for diesel train cooling systems. Part of the INFOH423 Data Mining Project for 2023/24, this initiative focused on analyzing and improving the cooling systems of SNCB's Belgian Railways Class 41 (two-vehicle AR41 trains) to detect potential failures in engine or transmission operations.

## Challenge

The two-vehicle AR41 diesel trains are equipped with intricate dual cooling systems. Anomalies in these systems can lead to significant operational disruptions and train delays. The project aimed to develop methods to effectively detect and categorize anomalies, distinguishing between sensor noise, individual cooling system deviations, and systemic issues.

## Approach

Processed a **2GB time-series dataset** (January-September 2023) containing operational parameters including temperatures, pressures, engine RPMs, and GPS locations. Conducted comprehensive data preprocessing and integrated external weather data from the OpenWeatherMap API to add environmental context.

Implemented **K-means clustering** and **Isolation Forest** algorithms using Scikit-Learn to differentiate between noise and genuine deviations in cooling systems. Developed a real-time Tableau dashboard for anomaly visualization, enabling SNCB's rolling stock team to make data-driven maintenance decisions.

## Key Results

Successfully identified anomalies in cooling systems that could indicate potential failures before they escalate, helping SNCB avoid train delays, ensure operational efficiency, and reduce maintenance costs through proactive scheduling.

## Technologies

Python, SQL, Scikit-learn, Pandas, NumPy, Matplotlib, Tableau


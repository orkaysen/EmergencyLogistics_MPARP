# Benchmark Test Data for the Joint Optimization of Multi-period Allocation and Delivery Routing of Emergency Supplies


## Overview

This repository provides the benchmark datasets used to evaluate the proposed algorithm in our study.  
The dataset is designed for a multi-period emergency logistics / distribution optimization problem involving multiple distribution centers, demand areas, vehicle fleet constraints, and different emergency supply types.

All benchmark instances are provided in Excel format (`.xlsx`) and can be used for algorithm validation, comparative experiments, and reproducibility purposes.

## Dataset Contents

The repository contains **12 benchmark instances**:

- `E1-2-5-2-2.xlsx`
- `E2-2-5-3-3.xlsx`
- `E3-2-10-2-2.xlsx`
- `E4-2-10-3-3.xlsx`
- `E5-3-15-2-2.xlsx`
- `E6-3-20-2-2.xlsx`
- `E7-4-25-2-2.xlsx`
- `E8-3-15-3-3.xlsx`
- `E9-4-30-2-2.xlsx`
- `E10-3-20-3-3.xlsx`
- `E11-4-25-3-3.xlsx`
- `E12-4-30-3-3.xlsx`

## File Naming Convention

Each file name follows the format:

`E{instance_id}-{number_of_distribution_centers}-{number_of_demand_areas}-{number_of_periods}-{number_of_emergency_supply_types}.xlsx`

For example:

- `E1-2-5-2-2.xlsx` means:
  - Instance ID = 1
  - Number of distribution centers = 2
  - Number of demand areas = 5
  - Number of periods = 2
  - Number of emergency supply types = 2

## Instance Summary

| Instance | Distribution Centers | Demand Areas | Periods | Emergency Supply Types |
|----------|----------------------|--------------|---------|------------------------|
| E1       | 2                    | 5            | 2       | 2                      |
| E2       | 2                    | 5            | 3       | 3                      |
| E3       | 2                    | 10           | 2       | 2                      |
| E4       | 2                    | 10           | 3       | 3                      |
| E5       | 3                    | 15           | 2       | 2                      |
| E6       | 3                    | 20           | 2       | 2                      |
| E7       | 4                    | 25           | 2       | 2                      |
| E8       | 3                    | 15           | 3       | 3                      |
| E9       | 4                    | 30           | 2       | 2                      |
| E10      | 3                    | 20           | 3       | 3                      |
| E11      | 4                    | 25           | 3       | 3                      |
| E12      | 4                    | 30           | 3       | 3                      |

## Data Format

Each Excel instance file contains the following worksheets:

### 1. `Node coordinates`
This sheet provides the coordinates of all nodes in the instance.

**Columns:**
- `NodeId`: node identifier
- `Type`: node type (`DC` for distribution center, `DA` for demand area)
- `X-coordinate`
- `Y-coordinate`

### 2. `Demand`
This sheet records the demand of each demand area in different periods for different emergency supply types.

The data are organized by:
- `T`: period
- `DA`: demand area
- `K1`, `K2`, `K3`, ...: emergency supply types

### 3. `Supply`
This sheet records the available supply at each distribution center in different periods for different emergency supply types.

The data are organized by:
- `T`: period
- `DC`: distribution center
- `K1`, `K2`, `K3`, ...: emergency supply types

### 4. `Distance matrix`
This sheet provides the pairwise distance matrix among all nodes, including distribution centers and demand areas.

### 5. `Speed adjustment factor matrix`
This sheet provides the pairwise speed adjustment factors between nodes.  
These factors can be used together with the standard vehicle speed to estimate travel time under different transportation conditions.

### 6. `Demand urgency`
This sheet provides urgency coefficients for each demand area and each emergency supply type.

### 7. `Vehicle fleet configuration`
This sheet describes the available vehicles used in the experiments.

**Columns:**
- `VehicleId`
- `MaximumPayload`
- `MaximumVolume`
- `StandardSpeed`
- `AssignedDepot`
- `MaximumEndurance`

## Usage

These benchmark instances can be used for:

- testing and validating optimization algorithms
- comparing solution quality and computational performance
- reproducing the numerical experiments reported in the paper
- conducting further research on emergency logistics and humanitarian distribution problems

## Notes

- All instance files follow the same worksheet structure.
- The data are provided in Excel format for readability and convenience.
- Users may convert the files into CSV or other machine-readable formats as needed.

## Reproducibility

This dataset is publicly released to improve the transparency and reproducibility of the research results reported in the associated paper.  
It may also serve as a benchmark set for future comparative studies on emergency supply distribution and routing problems.

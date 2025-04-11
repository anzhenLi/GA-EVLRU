<div align="center">
<h1>Genetic Algorithm - EV Least Recently Used</h1>

<a href="https://arxiv.org/abs/2504.07453"><img src='https://img.shields.io/badge/Paper-%20GA_EVLRU%20-red' alt='Paper PDF'></a>
<a ><img alt="PRs-Welcome" src="https://img.shields.io/badge/PRs-Welcome-white" /></a>[![GitHub Stars](https://img.shields.io/github/stars/anzhenLi/GA-EVLRU.svg)](https://github.com/anzhenLi/GA-EVLRU/stargazers)<a href="https://github.com/anzhenLi/GA-EVLRU/network/members">
<img alt="FORK" src="https://img.shields.io/github/forks/anzhenLi/GA-EVLRU?color=white" />
</a> [![GitHub Issues](https://img.shields.io/github/issues/anzhenLi/GA-EVLRU.svg)](https://github.com/anzhenLi/GA-EVLRU/issues)[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://opensource.org/licenses/gpl-3-0)

![overview](assets/exr.png)

This study proposes a probability estimation model based on charging pile data and constructs nine scenario-specific battery swap demand datasets. An innovative approach by combining the Least Recently Used (LRU) strategy with genetic algorithms and incorporating a guided search mechanism, which effectively enhances the global optimization capability.
</div>

## News
- **2025-04-08:** Paper and code are all released.

## Our BSS datasets
The description for our bss datasets is as follow: 

| Name       	 | E-Price 	| Our Estimated Data 		   | Orginal Data									   					   |
| :------------- | :------: | :--------------------------- | :------------------------------------------------ 					   |
| acn            | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| boulder_2021   | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| dundee         | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| palo_alto      | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| paris          | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| perth          | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| sap            | ×        | `demand.csv`, `bss.csv`      | [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) |
| st-evcdp       | √        | `demand.csv`, `bss.csv`      | [ST-EVCDP](https://github.com/IntelligentSystemsLab/ST-EVCDP) 		   |
| urbanev        | √        | `demand.csv`, `bss.csv`      | [UrbanEV](https://github.com/IntelligentSystemsLab/UrbanEV) 		   |

We provide a battery swapping demand dataset generated by the conversion of the [ST-EVCDP](https://github.com/IntelligentSystemsLab/ST-EVCDP), [UrbanEV](https://github.com/IntelligentSystemsLab/UrbanEV), and [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data), consisting of a total of 9 folders, each folder containing unstructured demand data demand.csv and data normalized to 1 hour bss.csv. You can download the raw data from [Google Drive Link](https://drive.google.com/drive/folders/1rz6EGdvIIXo9fobnQkJlD2SdbtNeZ_BH?usp=sharing). Or download the original dataset and run our algorithm.

## Getting Started

We recommend setting up a conda environment:

```shell
conda create -n GA_EVLRU python=3.9 -y
conda activate GA_EVLRU
```
Installing the required packages:

```shell
pip install -r requirements.txt
```

## Running GA-EVLRU

### Linux
```shell
git clone https://github.com/anzhenLi/GA-EVLRU.git
cd ga-evlru
./run.sh
```

### Windows
```shell
git clone https://github.com/anzhenLi/GA-EVLRU.git
cd ga-evlru
./run.bat
```

This script is designed to run GA-EVLRU quickly. 
Firstly, from the [ST-EVCDP](https://github.com/IntelligentSystemsLab/ST-EVCDP), [UrbanEV](https://github.com/IntelligentSystemsLab/UrbanEV), and [EV-Load-Open-Data](https://github.com/yvenn-amara/ev-load-open-data) project download raw dataset.
Secondly, run the estimation algorithm to generate an estimation dataset, run the GA-EVLRU algorithm to generate comparison results.
Finally, run multiple scripts to generate evaluation metrics results.

## LICENSE

The ST-EVCDP dataset is under the MIT license. The UrbanEV dataset is under the CC0 1.0 Universal License.  The EV Load Open Data dataset is under the GPL-3.0 license. And Our GA-EVLRU are under the GPL-3.0 license.

## Citation

If you find this project useful, please consider citing:
```bibtex
@inproceedings{li2025gaevlru,
      title={Probability Estimation and Scheduling Optimization for Battery Swap Stations via LRU-Enhanced Genetic Algorithm and Dual-Factor Decision System}, 
      author={Anzhen Li and Shufan Qing and Xiaochang Li and Rui Mao and Mingchen Feng},
      journal={arXiv preprint arXiv:2504.07453},
      year={2025}
}
```
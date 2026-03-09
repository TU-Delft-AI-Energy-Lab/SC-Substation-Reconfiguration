🚧 Code release in progress
# Security-Constrained Substation Reconfiguration

**Author:** Ali Rajaei  
**Affiliation:** Delft-AI Energy Lab, Department of Electrical Sustainable Energy, Delft University of Technology, the Netherlands  
**Contact:** a.rajaei@tudelft.nl  
**Date:** April 2025  

This repository accompanies the research paper:

> Rajaei, Ali, Olayiwola Arowolo, and Jochen L. Cremer.  
> ["Security-Constrained Substation Reconfiguration Considering Busbar and Coupler Contingencies."](https://arxiv.org/abs/2603.04203)  
> *IEEE Transactions on Power Systems*, 2026.

---

## Motivation

On **January 8, 2021**, the European power system experienced a major disturbance that split the continental grid into two areas.  
The event was triggered by the **tripping of a highly loaded busbar coupler**, which led to cascading failures across the network.

The post-event analysis showed that the **substation topology had not been adjusted after a transmission line outage**, and the **coupler contingency had not been included in the N-1 security analysis**.

This incident highlights the importance of explicitly considering **substation elements such as busbars and couplers** when determining secure grid configurations.

<p align="center">
<img src="figures/europe_grid_split.jpg" width="650">
</p>

*European system split on January 8, 2021 (adapted from ENTSO-E report).*

<p align="center">
<img src="figures/substation_topology.jpg" width="500">
</p>

*Illustration of the substation topology involved in the event.*

To address this challenge, our work proposes a **security-constrained substation reconfiguration framework** that considers **line, coupler, and busbar contingencies**, while remaining computationally scalable for large power systems.

---

## 📄 Abstract

Substation reconfiguration via busbar splitting can mitigate transmission grid congestion and reduce operational costs. However, existing approaches neglect the security of substation topology, particularly for substations without busbar splitting (i.e., closed couplers), which can lead to severe consequences. Additionally, the computational complexity of optimizing substation topology remains a challenge. 

This paper introduces a MILP formulation for security-constrained substation reconfiguration (SC-SR), considering N-1 line, coupler and busbar contingencies to ensure secure substation topology. To efficiently solve this problem, we propose a heuristic approach with multiple master problems (HMMP). A central master problem optimizes dispatch, while independent substation master problems determine individual substation topologies in parallel. Linear AC power flow equations ensure PF accuracy, while feasibility and optimality sub-problems evaluate contingency cases. 

The proposed HMMP significantly reduces computational complexity and enables scalability to large-scale power systems. Case studies on the IEEE 14-bus, 118-bus, and PEGASE 1354-bus system show the effectiveness of the approach in mitigating the impact of coupler and busbar tripping, balancing system security and cost, and computational efficiency.

---

## Repository Status

🚧 **Code under preparation**

The implementation used in the paper is currently being prepared for public release.  
The repository will be updated soon with:

- The proposed **SC-SR formulation** implemented in Python
- The **heuristic multi-master problem** solution approach
- Baseline solution approaches, including Bender decomposition variants, and heuristic methods
- Case study scripts for the IEEE benchmark systems

---

## Citation

If you use this work in your research, please cite:
```bibtex
@article{rajaei2026security,
  title={Security-Constrained Substation Reconfiguration Considering Busbar and Coupler Contingencies},
  author={Rajaei, Ali and Cremer, Jochen L},
  journal={IEEE Transactions on Power Systems},
  year={2026}
}
```

## License

This project will be released under the MIT License.

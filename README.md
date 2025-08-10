## Wireless Internet project: encrypted traffic classification (M.Sc. Computer Science and Engineering, A.Y. 2023/24) - Politecnico di Milano (PoliMi)

Evaluated positively: 4/4

### License and publishing notes

See [license file](LICENSE)

### Specifications

Wi-Fi encrypted traffic classification: implement a machine-learning classifier able to distinguish what kind of activity a user is performing with his/her smartphone/laptop by sniffing traffic in monitor mode.

The system should perform the following operations:

a. Sniff traffic in monitor mode from a known MAC address

b. Extract statistical features from the traffic every W seconds. The following traffic features can be extracted: number of packets up/down, average and variance of the packet size, average and variance of the inter-arrival packet times etc.

c. Use a pre-trained machine-learning classifier of your choice to recognize the user activity among at least the following: idle, web browsing, YouTube streaming.

d. Report the accuracy of the approach through a confusion matrix

Reference: https://ieeexplore.ieee.org/abstract/document/8543584

### Extra

See [the development container](.devcontainer) tailored to the project requirements, for local execution, as an alternative to the on-line _Google Colab_'s environment.

Note that in the use of the _development container_ all requirements are already satisfied (therefore, there is no need for initial package provisioning, as instead needed in _Google Colab_).
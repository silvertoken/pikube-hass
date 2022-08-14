<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<p align="center">
	<a href="https://github.com/silvertoken/pikube-mqtt/graphs/contributors">
    	<img src="https://shields.io/github/contributors/silvertoken/pikube-mqtt.svg?style=plastic" alt="Contributors">
	</a>
	<a href="https://github.com/silvertoken/pikube-mqtt/network/members">
    	<img src="https://shields.io/github/forks/silvertoken/pikube-mqtt.svg?style=plastic" alt="Forks">
	</a>
	<a href="https://github.com/silvertoken/pikube-mqtt/stargazers">
    	<img src="https://shields.io/github/stars/silvertoken/pikube-mqtt.svg?style=plastic" alt="Stars">
	</a>
	<a href="https://github.com/silvertoken/pikube-mqtt/pulse">
    	<img src="https://shields.io/github/commit-activity/m/silvertoken/pikube-mqtt.svg?style=plastic" alt="Commits">
	</a>
	<a href="https://github.com/silvertoken/pikube-mqtt/issues">
    	<img src="https://shields.io/github/issues/silvertoken/pikube-mqtt.svg?style=plastic" alt="Issues">
	</a>
	<a href="https://github.com/silvertoken/pikube-mqtt/blob/master/LICENSE">
    	<img src="https://shields.io/github/license/silvertoken/pikube-mqtt.svg?style=plastic" alt="License">
	</a>
</p>

<!-- PROJECT LOGO -->
<br />
<div align="center">

  <h3 align="center">pikube-mqtt</h3>

  <p align="center">
    pikube-mqtt is my operator for dns on piKube. A kubernetes MicroK8s cluster running on a Raspberry Pi that I use for my home.
    <br />
    <br />
	<a href="https://github.com/silvertoken/pikube-mqtt/wiki"><strong>Read the Wiki</strong></a>
	·
    <a href="https://github.com/silvertoken/pikube-mqtt/issues">Report Bugs</a>
    ·
    <a href="https://github.com/silvertoken/pikube-mqtt/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#About-pikube-mqtt">About pikube-mqtt</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

<!-- ABOUT pikube-mqtt -->
## About pikube-mqtt

I built a Raspberry Pi cluster to run all my security camera's and home automation services on 5 devices.  It started to become a little tedious to update and deploy new versions as needed.  I decided it would be best to automate the build since we all know our time is precious.  pikube-mqtt will manage the day 2 day operation and setup of the DNS services on my MikroTik router.

My Setup:
* 4 Raspberry Pi 4's running MicroK8s
* 1 Raspberry Pi 4 running vault and a local registry
* Mikrotik RouterBOARD 3011UiAS
* Private IP space 10.0.0.0/8
* 10.10.10.0/23 assigned to infrastructure and Metal LB
* Synology DS418j for NFS
* 2 Ubiquiti UAP-AC-PRO hotspots

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

* [Kopf](https://kopf.readthedocs.io/en/stable/)
* [Python](https://www.python.org/)
* [MikroK8s](https://microk8s.io/)
* [RaspberrPi](https://www.raspberrypi.org/)
* [Ubuntu](https://ubuntu.com/download/raspberry-pi)
* [MikroTik] (https://mikrotik.com/)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

Setup a MicroK8s cluster or use my ansible playbooks from the piKube project to set one up

* [piKube] (https://github.com/silvertoken/piKube)
* [MicroK8s Raspberry Pi Tutorial](https://ubuntu.com/tutorials/how-to-kubernetes-cluster-on-raspberry-pi#1-overview)

### Prerequisites

* MicroK8s cluster to run the operator on

### Installation

1. Setup Kopf peering in the cluster
	```sh
	kubectl apply -f https://github.com/nolar/kopf/raw/main/peering.yaml
	```

2. Clone the repo
   ```sh
   git clone https://github.com/silvertoken/pikube-mqtt.git
   ```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://github.com/silvertoken/pikube-mqtt/wiki)_

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

silvertoken - [@silvertoken](https://github.com/silvertoken)

Project Link: [https://github.com/silvertoken/pikube-mqtt](https://github.com/silvertoken/pikube-mqtt)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://shields.io/github/contributors/silvertoken/pikube-mqtt.svg?style=plastic
[contributors-url]: https://github.com/silvertoken/pikube-mqtt/graphs/contributors
[forks-shield]: https://shields.io/github/forks/silvertoken/pikube-mqtt.svg?style=plastic
[forks-url]: https://github.com/silvertoken/pikube-mqtt/network/members
[stars-shield]: https://shields.io/github/stars/silvertoken/pikube-mqtt.svg?style=plastic
[stars-url]: https://github.com/silvertoken/pikube-mqtt/stargazers
[issues-shield]: https://shields.io/github/issues/silvertoken/pikube-mqtt.svg?style=plastic
[issues-url]: https://github.com/silvertoken/pikube-mqtt/issues
[license-shield]: https://shields.io/github/license/silvertoken/pikube-mqtt.svg?style=plastic
[license-url]: https://github.com/silvertoken/pikube-mqtt/blob/master/LICENSE.txt
[commits-shield]: https://shields.io/github/commit-activity/m/silvertoken/pikube-mqtt.svg?style=plastic
[commits-url]: hhttps://github.com/silvertoken/pikube-mqtt/pulse
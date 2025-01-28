# DDOS-mitigation
DDoS Attack Detection and Mitigation using Machine Learning.
# Introduction
  A distributed denial-of-service (DDoS) attack is a malicious attempt to disrupt the normal traffic of a targeted server, service, or network by overwhelming the target or its surrounding infrastructure with a flood of internet traffic. DDoS attacks achieve effectiveness by utilizing multiple compromised computer systems as sources of attack traffic. Exploited machines can include computers and other networked resources such as IoT devices. From a high level, a DDoS attack is like an unexpected traffic jam clogging up the highway, preventing regular traffic from arriving at its destination. It's critical to act soon after discovering a DDoS attack since it provides you the chance to avert significant disruption. The server can start to crash on waiting too long, and a full recovery might take hours. The hardest part about mitigating a DDoS attack is that often it’s virtually impossible to do so without impacting legitimate traffic. This is because attackers go to great lengths to masquerade fake traffic as real.

# Motivation
  For enterprises operating at the edge with mission-critical activities that cannot afford downtime, DDoS mitigation as a protective layer is crucial. DDoS mitigation contributes to maintaining such activities' and services' ongoing availability. SDN allows for network design, construction, and operation. Attacks via distributed denial-of-service (DDoS) represent a serious risk to data centers. New security concerns and assaults, particularly Distributed Denial of Service (DDoS) attacks, are frequently launched against SDN networks.

# Objectives:-
* To implement a network using mininet and Ryu controller.
* To generate the dataset.
* To apply Random Forest Machine learning algorithm to detect DDoS attack.
* To add mitigation module.
# Installation
-  install [Virtual box](https://www.virtualbox.org/wiki/Downloads) or VM-ware workstation.

- install [Mininet-VM](https://github.com/mininet/mininet/releases/).

- install [Ubuntu](https://ubuntu.com/download/desktop) in virtual box.

- install [ryu-controller](https://ryu.readthedocs.io/en/latest/getting_started.html) in ubuntu vm.

# Go to Ubuntu/ryu controller vm
    #check your IP address
    ifcongif
   
    # it should be something 198.162.XX.XX copy it
    # change working directory to controller folder
    cd controller

    # switch on the ryu-controller
    ryu-manager controller.py

# Go to Mininet-vm

    # change working directory to mininet folder
      cd mininet

    # change controller ip address that you copied from ryu controller ip
      nano topology.py

    # run topology
      sudo python topology.py

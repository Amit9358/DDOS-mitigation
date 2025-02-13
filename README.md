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
# hping commands
    # icmp flood
      hping3 -1 -V -d 120 -w 64 -p 80 --rand-source --flood
    
    # syn flood
      hping3 -S -V -d 120 -w 64 -p 80 --rand-source --flood

    # udp flood
      hping3 -2 -V -d 120 -w 64 -p 80 --rand-source --flood

# Literature Survey

   [1]  This paper proposed a model which is able to detect and mitigate DDoS attacks automatically in SDN networks using ML.All of the switches' traffic flow entries are periodically collected by the model, which then extracts the native flow features and expands them by incorporating new features. A detection module uses five features to categorize each flow as normal or anomalous. When an attack is discovered, its source is prevented. Six ML algorithms were assessed with regard to the classification ML method utilized in the detection module, including LR, NB, KNN, SVM, DT, and RF. The outcomes of the experiment demonstrated that RF is the best classifier for the generated network. Without losing typical performance, the model was able to swiftly and effectively identify and block attacks.

[2] This work proposes a method of DDoS attack detection based on deep belief network feature extraction and LSTM model. This technique uses deep learning to extract IP packet attributes, builds an LSTM traffic prediction model, and then recognises DDoS attacks using the built-in LSTM model. Technology for detecting DDoS attacks is appropriate for this system. The model can effectively forecast the pattern of typical network traffic, spot irregularities brought on by DDoS attacks, and be used to develop more DDoS attack detection techniques in the future.

[3] In this work, the authors proposed a model which analyzes the correlation information of flows in data centers. It offers a reliable method of detecting DDoS attacks based on CKNN (K-nearest neighbors traffic categorization with correlation analysis).

[4] This paper proposes a new model to detect DDoS attacks in SDN based on SVM . Firstly a trained Support Vector Machine (SVM) approach is used by the model to extract numerous important features from the packet-in messages and measure the distribution of each feature using entropy. Studies reveal that this technique is highly effective at both real-time DDoS mitigation and security event detection.

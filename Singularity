Bootstrap: docker
From: ubuntu:bionic

%labels
Author "Randall Cab White - rcwhite@stanford.edu"


#########
#%setup
#########

#Downlaod packages
%post

  apt-get -ymq update
    ln -fs /usr/share/zoneinfo/America/Los_Angeles /etc/localtime
    apt-get install -y tzdata  rsh-client rsh-server xinetd 
    dpkg-reconfigure --frontend noninteractive tzdata
  apt-get -ymq  install software-properties-common
  add-apt-repository -y ppa:fenics-packages/fenics
  apt-get -ymq update
  apt-get -ymq  install fenics
  apt-get -ymq  install python3-matplotlib python3-pip

 pip3 install numpy matplotlib


%environment
  export IMAGE_NAME="fenics_ppa"
%runscript

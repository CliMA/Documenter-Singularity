Bootstrap: docker
From: julia:1.5.2-buster

%environment
  export LANG=C.UTF-8
  export LC_ALL=C.UTF-8

  export GKSwstype="100"

  export CLIMATEMACHINE_DOCS_GENERATE_TUTORIALS="true"
  export ClIMATEMACHINE_SETTINGS_DISABLE_GPU="true"
  export CLIMATEMACHINE_SETTINGS_DISABLE_CUSTOM_LOGGER="true"
  export CLIMATEMACHINE_SETTINGS_FIX_RNG_SEED="true"

%post
  apt-get update
  apt-get -qq install libxt6 libxrender1 libxext6 libgl1-mesa-glx libqt5widgets5 xvfb

%runscript
  xvfb-run -- julia -e 'versioninfo()'
Bootstrap: docker
From: julia:1.5.2-buster

%environment
  export LANG=C.UTF-8
  export LC_ALL=C.UTF-8

  export JULIA_DEPOT_PATH="/data"
  export JULIA_HISTORY="/data/logs/repl_history.jl"

  export CLIMATEMACHINE_DOCS_GENERATE_TUTORIALS="true"
  export ClIMATEMACHINE_SETTINGS_DISABLE_GPU="true"
  export CLIMATEMACHINE_SETTINGS_DISABLE_CUSTOM_LOGGER="true"
  export CLIMATEMACHINE_SETTINGS_FIX_RNG_SEED="true"

  export GKSwstype="100"

%post
  apt-get update
  apt-get -qq install libxrender1 libxext6 libgl1-mesa-glx libqt5widgets5 xvfb
  apt-get clean && rm -rf /var/lib/apt/lists/*

  mkdir -m 0777 /data

%runscript
  xvfb-run -- "@"

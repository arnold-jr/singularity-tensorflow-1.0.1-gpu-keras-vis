BootStrap:docker
From:tensorflow/tensorflow:latest-gpu

%runscript
  exec python "$@" 

%post
  # Enables access to ACCRE storage
  mkdir /scratch /data /gpfs22 /gpfs23 /dors
  
  pip install dill h5py hyperopt keras pandas \
    protobuf pymongo scikit-learn seaborn keras-vis

%test
  python -c "import tensorflow; import keras; import vis"

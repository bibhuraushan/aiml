Add .condarc

channels:
  - apple
  - conda-forge
  - defaults
subdirs:
  - osx-arm64
  - osx-64
  - noarch

conda env create -f aiml.yml --subdir os-arm64

pip install --pre torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/nightly/cpu
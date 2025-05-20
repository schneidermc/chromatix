### Installation instructions

Run the following to create and install the environment with jax and NVIDIA GPU support:

```bash
conda create -n chromatix python=3.11
conda activate chromatix
```
Check if `pip` is installed by `pip --version`. If not, install it with:
```bash
conda install pip
pip install --upgrade pip
```

Next, install `jax` with the appropriate GPU support:
```bash
pip install -U "jax[cuda12]"
```
Check with `conda env list` if `jax` is installed correctly. Otherwise, run `pip install --upgrade jax`.

Continue with the installation of `chromatix`:
```bash
pip install -e .
pip install pytest ruff pre-commit
pre-commit install
```

Install a few additional dependencies:
```bash
conda install matplotlib notebook
```

For some reason, you need to run the following in your terminal to make sure there is no segfault errors:
```bash
unset LD_LIBRARY_PATH
```
Note that you will need to run this command every time you start a new session.

Finally, run `pytest` to check that everything is working correctly.

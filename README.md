# Question 1 install instructions

Add conda-forge to the list of channels.

```
conda config --append channels conda-forge
```

Install all requirements to a new environment.

```
conda create --name 375a2q1 --file requirements_q1.txt
```

Activate the new environment before running code.

```
conda activate 375a2q1
```

Then you can run your code and view results in `plots/`.

```
python P1_differential_flatness.py
```

# Question 2 install instructions

Follow instructions from pdf to install MuJoCo.

The following command will install MuJoCo pre-reqs under Ubuntu.

```
sudo apt install libosmesa6-dev libgl1-mesa-glx libglfw3 build-essential libglfw3-dev libglib2.0-0
```

 If you see an error that `-lGL` cannot be found, you may need to create a symbolic link directly.

```
sudo ln -s /usr/lib/x86_64-linux-gnu/libGL.so.1 /usr/lib/x86_64-linux-gnu/libGL.so
```

Install all requirements to a new environment.

```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/ubuntu/.mujoco/mujoco200/bin
conda env create -f environment_q2.yml
```

Activate the new environment before running code.

```
conda activate 375a2q2
```

Start jupyter and run notebooks.

```
jupyter notebook
```

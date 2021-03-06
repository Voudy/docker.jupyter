# Docker container with JupyterLab

This dockerfile contains instruction to build container with Jupyter from Anaconda.  
Also, there is GPU support for `TensorFlow`, `PyTorch`, `XGBoost`, `LGBM`.  
Additional packages: `OpenCV`, `CatBoost`

## Build
Use this command for build:
```
sudo docker build -t name:tag <path/to/Dockerfile>
```
(this may take a lot of time)  
Or just download it from docker hub (~12 GB):
```
sudo docker pull voudy/jupyter
```
## Run
If you want to run with GPU support use:
```
sudo nvidia-docker run --rm -it -v <local/dir/for/notebooks>:/working_dir -p <local port>:8888 name:tag
```
But you can run it only on CPU:
```
sudo docker run --rm -it -v <local/dir/for/notebooks>:/working_dir -p <local port>:8888 name:tag
```
After that go to `localhost:port` or other ip you would like to use.

For downloaded version use `voudy/jupyter` instead of `name:tag`

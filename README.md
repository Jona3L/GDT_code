# GDT_code
Please modify the original code at where it is listed as your path to current working folder
Also modify the dataset path to the relative path to load it properly


### Setting up the project environments
- Install the project environment:
  ```
  conda env create --file=conda_env.yml
  ```
- Activate the environment:
  ```
  conda activate cbet
  ```

  ### Getting the training datasets
Datasets used for training will be uploaded to [this OSF link](https://osf.io/q3dx2).
- Download and unzip the datasets.
- In `./config/env_vars/env_vars.yaml`, set the dataset paths to the unzipped directories.
  - `carla_multipath_town04_merge`: CARLA environment
  - `relay_kitchen`: Franka kitchen environment
  - `multimodal_push_fixed_target`: Block push environment

### experiments
- Train :
  ```
  python3 train.py --config-name=train_carla_future_cond
  ```

- Evaluation:
  ```
  python3 run_on_env.py --config-name=eval_carla_future_cond
  ```
Also needed to modify the task to needed task such as CARLA, Franka kitchen and Block Push

Citation

Cui, Zichen Jeff, et al. "From play to policy: Conditional behavior generation from uncurated robot data." arXiv preprint arXiv:2210.10047 (2022).

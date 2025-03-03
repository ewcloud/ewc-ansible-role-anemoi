EWC Ansible Role Anemoi
=======================

Create a conda environment with the Anemoi framework  for weather forecasting based on machine learning and associated software stack.

Requirements
------------

This ansible role depends on ewc-ansible-role-conda and needs to be applied on a GPU-powered instance if training or inference are used.

Role Variables
--------------

 - `anemoi_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
 - `anemoi_env_name`: Name of the environment containing the software stack. Default: aifs-single-mse
 - `anemoi_env_path`: Installation path for the environment. Default: "{{ conda_prefix }}/envs/{{ anemoi_env_name }}"
 - `anemoi_create_ipykernel`: Create the jupyter kernel for this environment. Default: yes
 - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
 - `conda_user`: User owning the conda installation. Default: `root`

Example Playbook
----------------

    - hosts: all
      roles:
         -  ewc-ansible-role-anemoi

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud
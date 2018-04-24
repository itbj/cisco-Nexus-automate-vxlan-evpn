# VxLAN Python Package
# forked from momobade/cisco-Nexus-automate-vxlan-evpn
# 感谢 momobade.
The project's purpose is to build a python package that can store VxLAN parameters for underlay and overlay configuration and output the parameters into any device that supports VxLAN. Currently the deployment is tested on Nexus 9000 switches which are widely deployed in the data center as VxLAN capable switches. The pacakge includes an input script that reads from an excel file in order to populate the VxLAN parameters.

## Getting Started/开始

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Dependencies-依赖

* Python 3.5
* Packages:  预先要安装的模块
  - pandas 
  - xlrd


## Running the package/运行这个程序

The code is provided with a sample excel file which contains configuration parameters for the devices in VxLAN network. Each sheet from the excel file represent the protocol used to form the VxLAN fabric.

The program then generates text files containing the device complete configuration. The number of text files is linked to the number of devices provided in the excel file (in this example, we have four devices 'Spine1', 'Spine2', 'Leaf1, and 'Leaf2')

Run the following command in order to generate the text file samples

```
python generate_config.py -s ip_information.xlsx
```

The above command will generate four txt files which contains all the parameters of the ip_information.xlsx file.

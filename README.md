## How to Use
1. Download/Install [packer](https://releases.hashicorp.com/packer/1.1.0/packer_1.1.0_linux_amd64.zip?_ga=2.29786044.20708002.1505763097-2022437500.1505763097)
2. Download CentOS7 Minimal ISO to the iso/ directory in this project
3. Run `packer build packer/centos7-disa-stig.json`
4. After packer image is built we can import into Vagrant with `vagrant box add <path to box> --name <name of box>`

### Building the base image
1. Download the CentOS7 Minimal ISO to the iso directory
2. Generate a sha1sum for the iso using `sha1sum`
3. Open the packer file in `packer/<desired packer file>` and change the iso_hash
4. Run packer to build the desired packer image `packer build packer/centos7-disa-stig.json
5. Import the packer box into Vagrant with `vagrant box add <path to box> --name <name of box>`

### Building the Workstation Image
1. Download the CentOS7 NetInstall ISO to the iso directory
2. Generate the sha1sum for the iso usin `sha1sum`
3. open the packer file in `packer/centos7-disa-stig-workstation.json` and change the iso_hash
4. Run packer to build the desired packer iamge `packer build packer/centos7-disa-stig-workstation.json`
5. Import the packer box into Vagrant with `vagrant box add centos7-disa-stig-workstation_libvirt.box --name centos7-disa-stig-workstation`

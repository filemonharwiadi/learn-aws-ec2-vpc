# learn-aws-ec2-vpc
Deploy EC2 Manual di AWS

Dari topologi yang saya buat, menjelaskan tentang gimana sih sederhana deploy ec2 di dalam VPC sampai dapat akses ke internet?

Pertama-tama saya tentukan :
1. IPv4 CIDR Block for VPC: xxx.xxx.xx.xx/xx
2. Public subnet : xxx.xxx.xx.xx/xx

Nah, komponen apa aja sih yang kita pakai untuk create VPC?
1. VPC : create VPC dengan IPv4 CIDR Block yang sudah kita tentukan
2. Internet Gateway (IGW) : create IGW dan attach ke VPC
3. Public Subnet : create subnet dengan subnet IPv4 Block yang sudah kita tentukan
4. Route Tables : Edit routes, Add route. Pasang Internet gateway, destination 0.0.0.0/0. Edit subnet associations dan pilih subnet publicnya, Save associations
5. Security Groups : Setting Inbound dan Outbond
6. Elastic IPs : create Elastic IPs. Associate Elastic IP address.

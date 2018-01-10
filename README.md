# To build

docker build -t chriscohoat/raiblocks-docker .

# To run node

docker run --runtime=nvidia -it -p 7075:7075/udp -p 7075:7075 -p 127.0.0.1:7076:7076 -v ~/workspaces/chriscohoat/raiblocks-node-data/:/root/data chriscohoat/raiblocks-docker

# Diagnostics

docker run --runtime=nvidia -it chriscohoat/raiblocks-docker ./rai_node --debug_opencl --platform=0 --device=0 --threads=1048576
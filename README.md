### Docker-hobbit

This is a recipe to put Xymon (Hobbit) monitoring software in a docker container using Linux, Apache + Xymon + Python setup tools.

Enjoy.

The only thing you have to supply is the static file for Hobbit named bb-hosts, I have supplied a test file with some random servers.

If you want to clone this repository:

	git clone https://github.com/sillkongen/docker-hobbit

This repo contains a recipe for making a Docker container for Hobbit, using Linux, Apache and Hobbit.

If you ahve installed Docker and cloned the repository it is just a matter of:

	docker build -rm -t <yourname>/hobbit .

You could also build it directly from the github repository:

docker build -rm -t <yourname/hobbit> https://github.com/sillkongen/docker-hobbit.git

Then run it:

	docker run -d -p 80 <yourname>/hobbit

Then find the external port exposed from the container:

	docker port <container-id> 80

Visit in a web browser:
	http://<yourhost>:<exposed_port_number>/hobbit/

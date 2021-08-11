# GTT - 2021 TSMC IT Hackathon Group K

GTT is a newbie-friendly forum. It is powered by Node.js and mongoDB Atlas service. It is based on [**NodeBB Forum Software**](https://nodebb.org). NodeBB has many modern features out of the box such as social network integration and streaming discussions, while still making sure to be compatible with older browsers.

## Requirements

GTT requires the following software to be installed:

* A version of Node.js at least 12 or greater

## Installation

To run GTT, please follow the following steps

1. Install Requirements and clone this repo, or simply go to [https://www.gitpod.io/#https://github.com/darker66678/NodeBB](https://www.gitpod.io/#https://github.com/darker66678/NodeBB)
2. run `npm install` to install dependencies
3. run `./nodebb setup` to build
4. run `./nodebb start` to start the service
5. the service should be available at [http://localhost:4567/](http://localhost:4567/) or `http://4567-*****.gitpod.io`

For more details, please refer to [NodeBB installation documentation](https://docs.nodebb.org/installing/os)
## buliding Search engine
We use Apache Solr as our Search engine

1. run `docker pull solr` to get solr image
2. run `docker run --restart always --name solr -d -p 8983:8983 -t solr` to bulid solr
3. run `docker exec -it --user=solr solr bin/solr create_core -c nodebb` to bulid a nodebb core

## License

GTT is based on NodeBB and NodeBB is licensed under the [**GNU General Public License v3 (GPL-3)**](http://www.gnu.org/copyleft/gpl.html).
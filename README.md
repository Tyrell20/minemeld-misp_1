# ThreatIntelPFExtensions
Forked version of [minemeld-misp](https://github.com/PaloAltoNetworks/minemeld-misp)

Contains extensions for [Minemeld](https://www.paloaltonetworks.com/products/secure-the-network/subscriptions/minemeld) used for the project Threat Intel Platform:
* Dedicated miner nodes to fetch IoCs over the [MISP](http://www.misp-project.org/) API.
* Additional processor nodes that allow for filtering of tlp-tags.
* Output nodes providing the IoCs in form of a feed, either as a list or in the STIX/TAXII format.
* Support for additional types of IoCs

## Code structure
``minemeld.json`` - Metadata including information about the setup of the extension

``/mmmisp/prototypes`` - Configuration files defining prototypes

``/mmmisp/taxiiserver`` - Implementation of TAXII-server including its API

``/mmmisp/taxiiwebui`` - Implementation of Web-UI for prototypes of class "mmmisp.taxii.DataFeed"

``/mmmisp/webui`` - Implementation of Web-UI for prototypes of class "mmmisp.Miner"

``/mmmisp/node.py`` - Implementation of miner base class "mmmisp.Miner"

``/mmmisp/taxii.py`` - Implementation of output base class "mmmisp.taxi.DataFeed"

## Requirements
Written in python 2.7 since core system does not support python 3

minemeld-core>=0.9.37b1\
pymisp==2.4.96\
pytz==2015.4\
lz4==2.2.1\
lxml==4.1.0\
PyYAML==3.11\
redis==2.10.5\
gevent==1.0.2\
netaddr==0.7.18\
Werkzeug==0.12.2\
six==1.11.0\
libtaxii==1.1.107\
stix==1.1.1.8\
stix-edh==1.0.0\
cybox==2.1.0.17\


## Documentation

Upload the provided wheel (misp_taxii-1.0-py2-none-any.whl) in Minemeld as an extension and then install it.

For further documentation and setup instruction refer to the code or the [internal documentation](https://infoboard.ig.loc/display/SSD/TIP+-+Documentation)


Usage with ODL and Postman:

make dir cache/junos142 under ODL root and copy all files to it.

In Postman do:
PUT http://osboxes:8181/restconf/config/network-topology:network-topology/topology/topology-netconf/node/PE-1

<node xmlns="urn:TBD:params:xml:ns:yang:network-topology">
   <node-id>PE-1</node-id>
   <host xmlns="urn:opendaylight:netconf-node-topology">172.16.16.1</host>
   <port xmlns="urn:opendaylight:netconf-node-topology">830</port>
   <username xmlns="urn:opendaylight:netconf-node-topology">root</username>
   <password xmlns="urn:opendaylight:netconf-node-topology">passw0rd</password>
   <schema-cache-directory xmlns="urn:opendaylight:netconf-node-topology">junos142</schema-cache-directory>
   <tcp-only xmlns="urn:opendaylight:netconf-node-topology">false</tcp-only>
   <keepalive-delay xmlns="urn:opendaylight:netconf-node-topology">0</keepalive-delay>
   <yang-module-capabilities xmlns="urn:opendaylight:netconf-node-topology">
   	<capability>http://xml.juniper.net/xnm/1.1/xnm?module=configuration&amp;revision=2015-09-11</capability>
    <capability>urn:ietf:params:xml:ns:netconf:base:1.0?module=ietf-netconf&amp;revision=2011-06-01</capability>
    <capability>urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&amp;revision=2013-07-15</capability>
    <capability>urn:ietf:params:xml:ns:netconf:base:1.0?module=database-status-information&amp;revision=2017-03-07</capability>
   </yang-module-capabilities>
</node>

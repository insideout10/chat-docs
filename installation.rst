Installation
============

Create a database
-----------------

Create a database and assign access privileges:

    create database chat_server default charset utf8 default collate utf8_bin;
    grant all privileges on chat_server.* to <username>@<server-ip> identified by <password>;



Initial configuration
---------------------

Manually insert the configuration for the first app:

    INSERT INTO apps( `key`, name, secret, title ) values( <key>, <name>, <secret>, <title> );


Start-up
--------

Start the Chat Server:

    java -jar lib/chat-server-1.0.0-SNAPSHOT.jar
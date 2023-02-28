# Notes for ITEC 325

This repository contains notes associated with running and managing services in Linux.

## Preprequisites

The example reported in this repository runs on Linux. Make sure you have the following applications installed:

- zip
- unzip
- nodejs
- npm

As the server example uses code that is compatible with an older version of Node.JS, you do not need to have the latest version.

For Debian users, you can run the following command: `sudo apt install zip unzip nodejs npm`

If you wish to utilize the Postman file, you will also have to install this application

For Debian users, you can install it in two steps:

- Install the snap package: `sudo apt install snap`
- Install snap's core: `sudo snap install core`
- Install Postman: `sudo snap install postman`

## To use the demo files

Using Postman, import the file ITEC 325.postman_collection.json.

Save the files itec325.zip and simpleapi.service to a directory of your choice.

Create the directory 'demo' and expand the file itec325.zip in it.

Using a terminal window, navigate to /path/to/demo and then run `npm install`, which will install the necessary packages.

To run the application, you can either call `node index.js`, `npm start`, or `npm run dev`.

Use the Postman collection to test that the application is running as expected.

## systemd commands

The following commands are frequently used to manage systemd:

- `systemctl start <service>` to start a service
- `systemctl status <service>` to get the status of a service
- `systemctl stop <service>` to stop a service
- `systemctl enable <service>` to enable a service at startup
- `systemctl disable <service>` to remove a service from startup
- `journalctl` to access the logs associated with systemd

## Commands for this example

systemd commands that we will use for this example:

- Move the simpleapi.service file into position: `sudo mv /path/to/file/simpleapi.service /etc/systemd/system/`
- Enable the service: `sudo systemctl enable simpleapi`
- Start the service: `sudo systemctl start simpleapi`
- Check the status of the service: `sudo systemctl status simpleapi`
- Stop the service: `sudo systemctl stop simpleapi`
- Disable the service: `sudo systemctl disable simpleapi`
- Remove the file from the directory: `sudo rm /etc/systemd/system/simpleapi.service`

# socketio-gcmvm

A quick demo for node.js and socket.io on Google App Engine Managed VMs using Custom Runtimes. You can see a working demo of it here: http://104.197.126.175:3000/

## Usage

Start by cloning this repository.

To run the app locally:

~~~~
npm install
npm start
~~~~

The demo chat app is then available at:  http://localhost:3000

Docker is no longer required.

To deploy the app to Google Cloud:

~~~~
gcloud preview app deploy app.yaml
~~~~

Since this app is using port 3000, you will need to go into the Managed VM console and edit the Network firewall to allow access to this port.  The app will then be available from the VM's external IP address on socket 3000.  Example:  http://[VM-EXTERNAL-IP]:3000

You cannot access the app through the *.appspot.com host.  You have to look up the external IP of your VM and use that.  Another option is to assign the Managed VM a static external ip address and allow your front-end code to use that to access the app.
=======
# socketio-mvm
Forked from https://github.com/jdeskins/socketio-gcmvm.git

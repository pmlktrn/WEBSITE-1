quantum-dxi-series
This is a plugin used to monitor quantum dxi series devices in icinga via sshpass.

Download check_dxi.sh script from this link: https://exchange.nagios.org/directory/Plugins/Hardware/Storage-Systems/Tape-Drives-and-Libraries/Check-Quantum-DXi-Series/details
Edit the script: remove all the -x and check if the code in a "MEMORY" part are properly written.
Install the script in the /usr/lib64/nagios/plugins directory in icinga. Make sure that the script is run via unix.
The plugin can be accessed via sshpass. Make sure the remote server to monitor has sshpass configured.
create keys for authorization in icinga user. sudo -u icinga -s /bin/bash -i >> ssh -x user@ >> execute to test the connection: sshpass -p ${PASSWORD} ssh -x ${USER}@${HOST} >> syscli --getstatus compaction
you can configure the plugin in icingaweb2 once you can successfully execute the syscli --getstatus compaction in icinga user.

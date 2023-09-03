# Create a script that switches the current user to the user betty.

#!/bin/bash

su betty

# Write a script that prints the effective username of the current user.

#!/bin/bash

whoami

# Write a script that prints all the groups the current user is part of.

#!/bin/bash

groups

# Write a script that changes the owner of the file hello to the user betty.

#!/bin/bash

#Create the file

touch hello

#Change the owner of the file to "betty"

sudo chown betty hello

# Write a script that adds execute permission to the owner of the file hello.

#!/bin/bash

chmod +x hello

# Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

#!/bin/bash

chmod ug+x,o+r hello

# Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

#!/bin/bash

chmod +x hello

# Write a script that sets the permission to the file hello as follows:

Owner: no permission at all
Group: no permission at all
Other users: all the permissions

#!/bin/bash

chmod 007 hello

# Write a script that sets the mode of the file hello to this:
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

#!/bin/bash

chmod 753 hello

# Write a script that sets the mode of the file hello the same as olleh’s mode.

touch olleh

#!/bin/bash

chmod --reference=olleh hello

# Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.
Regular files should not be changed.


#!/bin/bash

find . -type d -exec chmod 711 {} +

# Create a script that creates a directory called my_dir with permissions 751 in the working directory.

#!/bin/bash

mkdir -m 751 my_dir

# Write a script that changes the group owner to school for the file hello

#!/bin/bash

chgrp school hello

# Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.

sudo groupadd staff
sudo useradd vincent

#!/bin/bash

chown -R vincent:staff *

# Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.

#!/bin/bash

chown -h vincent:staff _hello

# Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume.

#!/bin/bash

chown --from=guillaume betty hello

# Write a script that will play the StarWars IV episode in the terminal. 


#!/bin/bash

telnet towel.blinkenlights.nl

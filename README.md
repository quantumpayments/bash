# bash
trigger payments from bash

# pre requisites

setup `basic` ledger workflow

    export WEBID=<webid>

In your .bashrc

# driver to bash

    export PROMPT_COMMAND='bash_points.sh 2>/dev/null 1>&2'
    
# advanced

In order to get bash history updating every time add

    export PROMPT_COMMAND="history -a;$PROMPT_COMMAND"


# command to run (bash)


where `bash_points.sh` looks like

    credit insert https://workbot.databox.me/card/profile#me 5 '' $WEBID -d small -w https://localhost/wallet/small/wallet#this bash

5 bits are selected here with a message of `bash` 

It is also possible to run the same script in node

# testing

    credit balance $WEBID [-d database] [-w wallet]

    5

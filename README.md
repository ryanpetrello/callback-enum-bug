To reproduce the error, make a clean virtualenv, and run:

    $ pip install -r ./requirements.txt
    $ ANSIBLE_LOAD_CALLBACK_PLUGINS=1 ANSIBLE_CALLBACK_PLUGINS=`pwd`/stdout ANSIBLE_STDOUT_CALLBACK=stdout ansible -i 'localhost,' -m shell -a hostname -e 'ansible_connection: local' all -v

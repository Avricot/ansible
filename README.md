# ansible

    sudo apt-get install ansible
    sudo apt-get install git
    cd /home/admin
    git clone https://github.com/Avricot/ansible


    cd .ssh
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    cat id_rsa.pub >> authorized_keys
    chmod 700 ~/.ssh && chmod 600 ~/.ssh/*

Make sure you can ssh to localhost and add it to known_host :

    ssh -i ~/.ssh/id_rsa admin@localhost

    cd ansible
    #make sure everything is ok:
    ansible all -i "localhost," -c local -m shell -a 'echo hello world'
    ansible-playbook -i hosts site.yml -kK -vvvv

Instructions to setup a base django install:

1.  Install Vagrant and Virtualbox on your machine
2.  Put this Vagrantfile in a directory
3.  Make a 'cookbooks' directory and git clone the following cookbooks:
        git clone git://github.com/opscode-cookbooks/apache2.git
        git clone git://github.com/opscode-cookbooks/apt.git
        git clone git://github.com/opscode-cookbooks/build-essential.git
        git clone git://github.com/opscode-cookbooks/git.git
        git clone git://github.com/opscode-cookbooks/vim.git
4.  'vagrant up' to start the VM
5.  'vagrant ssh' into the VM
6.  In the VM, run: 'sudo apt-get install python-pip', then run:
    'sudo pip install django'
8.  Run: 'django-admin.py startproject django-project'
9.  Change into the directory and run: 'python manage.py runserver [::]:8000'
10. In a web browser on the host machine, load 'localhost:8001' and you should
    access the starter page.

Instructions to setup a base django install:

1.  Install Vagrant and Virtualbox on your machine
2.  Put this Vagrantfile in a directory
3.  Make a 'cookbooks' directory and git clone the following cookbooks:
        git clone git://github.com/opscode-cookbooks/apache2.git
        git clone git://github.com/opscode-cookbooks/apt.git
        git clone git://github.com/opscode-cookbooks/build-essential.git
        git clone git://github.com/opscode-cookbooks/git.git
        git clone git://github.com/opscode-cookbooks/vim.git
        git clone git://github.com/opscode-cookbooks/mysql.git
4.  'vagrant up' to start the VM
5.  'vagrant ssh' into the VM
6.  Run: 'django-admin.py startproject django_project'
7.  Change into the directory and run: 'python manage.py runserver [::]:8000'
8.  In a web browser on the host machine, load 'localhost:8001' and you should
    access the starter page.

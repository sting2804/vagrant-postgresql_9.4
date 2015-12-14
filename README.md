
# Clone it locally:
    $ git clone https://github.com/sting2804/vagrant-postgresql_9.4.git testapp

    # Enter the cloned directory:
    $ cd testapp

### Usage

    # Start up the virtual machine:
    $ vagrant up

    # Stop the virtual machine:
    $ vagrant halt


    Your PostgreSQL database has been setup and can be accessed on your local machine on the forwarded port (default: 15432)
      Host: localhost
      Port: 15432
      Database: admin
      Username: admin
      Password: adminpass

    Admin access to postgres user via VM:
      vagrant ssh
      sudo su - postgres

    psql access to app database user via VM:
      vagrant ssh
      sudo su - postgres
      PGUSER=admin PGPASSWORD=adminoass psql -h localhost admin

    Env variable for application development:
      DATABASE_URL=postgresql://myapp:dbpass@localhost:15432/admin

    Local command to access the database via psql:
      PGUSER=admin PGPASSWORD=adminpass psql -h localhost -p 15432 admin

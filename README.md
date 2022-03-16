# ami

Steps for demo:

Run terraform
Run using the packer build command

scp -i ami.pem -r webapp/ ubuntu@DNS:/home/ubuntu/
ssh -i ami.pem ubuntu@IP -p 22

pip install -r requirements.txt

sudo su - postgres

CREATE DATABASE 
	djangodb;
CREATE USER 
	djangouser 
	WITH PASSWORD 'password';


ALTER ROLE djangouser 
	SET client_encoding 
	TO 'utf8';
ALTER ROLE djangouser 
	SET default_transaction_isolation 
	TO 'read committed';
ALTER ROLE djangouser 
	SET timezone 
	TO 'UTC';
GRANT ALL PRIVILEGES 
	ON DATABASE djangodb 
	TO djangouser;


python3 manage.py migrate

python3 manage.py runserver 0.0.0.0:8000

Create A record and expose IP
Run API on postman
Cool

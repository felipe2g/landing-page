# Strapi application

A quick description of your strapi application


# Criando usuário para o banco de dados

ALTER USER strapi WITH ENCRYPTED PASSWORD 'strapi';

GRANT ALL PRIVILEGES ON DATABASE strapi TO strapi;

\l
# Criando banco de dados para o strapi

sudo -u postgres psql

\l

DROP DATABASE strapi;

grant all privileges on database strapi to strapi;

# Criando dump file do banco de dados

pg_dump -c --if-exists --exclude-table=strapi_administrator -h 127.0.0.1 -U strapi -d strapi -W > strapi.sql

FROM mariadb:lts

ADD Server/utils/sql/database_full/alkabor_2025-05-07-08_02.tar.gz /docker-entrypoint-initdb.d
ADD Server/loginserver/login_util/tblloginserversettings.sql /docker-entrypoint-initdb.d
RUN rm /docker-entrypoint-initdb.d/drop_system.sql

ADD containers/database/auto_create.sql /docker-entrypoint-initdb.d/z_auto_create.sql
ADD containers/database/launcher_boats.sql /docker-entrypoint-initdb.d/z_launcher_boats.sql

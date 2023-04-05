FROM --platform=linux/amd64 odoo:15.0

# Copy entrypoint script and Odoo configuration file
COPY ./entrypoint.sh /
COPY ./odoo.conf /etc/odoo/
COPY ./wait-for-psql.py /usr/local/bin/wait-for-psql.py
COPY ./cli_server.py /usr/lib/python3/dist-packages/odoo/cli/server.py
COPY ./service_server.py /usr/lib/python3/dist-packages/odoo/service/server.py

#ENTRYPOINT ["/entrypoint.sh"]
#CMD ["odoo"]
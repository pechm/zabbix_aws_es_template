Zabbix AWS ElasticSearch simple template
========================================

###AWS ElasticSearch Template for Zabbix

1. place the script "es_stats.py" at zabbix-server externalscripts folder (https://www.zabbix.com/documentation/2.0/manual/config/items/itemtypes/external), make sure it has execute permissio. 
2. Import the template "zbx_export_templates.xml".
3. enter you aws credentials in the template's macro section ({$AWS_ACCESS_KEY}, {$AWS_SECRET_KEY}) or leave it blank to use IAM roles 
4. set you default AWS region in the template's macro section {$REGION}
5. set you default AWS ES DomainName and ClientID in the template's macro section {$DOMAIN} and {$CLIENT}
6. Attach the above template to the relevant hosts.
7. note that you can override the AWS region for specific hosts by adding the {$REGION} macro to the host
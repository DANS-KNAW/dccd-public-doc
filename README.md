# dccd-public-doc

Documentation about the DCCD services published on the DCCD server. 

The DCCD web application (dccd-webui) links to these documents and expect them to be available from a 'docs' location on the server, like `https://dendro.dans.knaw.nl/docs`.  
Therefore the docs folder needs to be placed in the web server document root, for instance in `/var/www/html`. 

Also make sure that this docs is reachable and check the apache config. 
If you have ajp, you probably have to exclude the docs from being forwarded. 
Just before the ajp RewriteRule place the following: 
`RewriteCond %{REQUEST_URI} !/docs`

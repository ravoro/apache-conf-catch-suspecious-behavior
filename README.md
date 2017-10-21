# Apache Conf - Catch Suspecious Behavior

Apache server config for catching suspecious behavior.

Analyzes incoming request data (Request URI, User Agent, etc.) for pre-defined patterns of suspecious activity.

Requests deemed suspecious are stopped from being processed and a standard response is given (by default, a plain 404).

## Requirements
- Apache server
- Apache `mod_rewrite` module enabled

## Installation

- Method 1: Global Installation
    - *Note: this method may not work with individual VirtualHosts. To use with VirtualHosts see Method 2 below.*
    - Place the `catch-suspecious-behavior.conf` file inside your Apache's conf directory - `/etc/apache2/conf-available/`.
    - Enable the new conf with `a2enconf catch-suspecious-behavior` and reload Apache with `service apache2 restart`.
- Method 2: VirtualHost Installation
    - Place the `catch-suspecious-behavior.conf` file inside your Apache's conf directory - `/etc/apache2/conf-available/`.
    - Include the new conf inside your VirtualHost by adding the line `Include conf-available/catch-suspecious-behavior.conf`.
    - Enable the new conf by reloading Apache with `service apache2 reload`.    


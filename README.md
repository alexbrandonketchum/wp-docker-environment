## WordPress environment with Docker

## Dependencies
* Docker
* Docker Compose

## Development Setup
1. Update local-config.php and docker-compose.yml to match new projects (make sure database name matches in all files).
2. Plugins go in the `wp-content/plugins` directory.
3. Assets go in the `wp-content/uploads` directory.
4. Run `docker-compose up -d`.
5. Run `docker exec wp_app cp /wp-config.php .` to ensure config is copied over (Change the wp in wp_app first!).
6. Run `docker exec wp_mysql bash` to enter a bash shell in the MySQL database container (Change the wp in wp_mysql first!).
7. Run `mysql -uroot -pdevsu -e 'create database database_name;'`. Change database_name to actual database name (duh!).
8. That's it!
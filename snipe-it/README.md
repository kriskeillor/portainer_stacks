# Snipe-IT on Portainer 
## Stack Configuration
v1.2.1 - corrected database address alias thanks to @screwyluie  
v1.2 - improved networking thanks to @growlf  
v1.1 - improved volumes thanks to @joshbuker  
v1.0 - roughly assembled from [source 1](https://dannyda.com/2022/09/04/working-snipe-it-docker-stack-configuration-yaml-yml-docker-compose-file-snipe-it-and-mysql-mariadb-docker-container/) and [source 2](https://github.com/Sthopeless/portainer-stacks/blob/master/Snipe-It.yml)

### Changelog
#### v1.2.1 - Database Error
Commit b6d5150ca595ddd0f91c01d4812d58a1b662ceb9  
The following error:
| Setting  | Valid | Notes |
| :------- | :---- | :---- |
| Database | X     | D'oh! Looks like we can't connect to your database. Please update your database settings in your .env file. Your database says: SQLSTATE[HY000] [2002] php_network_getaddresses: getaddrinfo for mysql failed: Name does not resolve (SQL: select 2 + 2) |

Was corrected by changing the aliased address from "mysql" to "db", as the database service had been named prior in the config file.

#### v1.2 - Streamlined and Secured Networking
Commit c03ccaeeeae504c3996c09d85f1213e0768ad588

#### v1.1 - Improved Volume Mapping
Commit b01e67c098566b3f5191c15c8fa8b7ce9b476c4b

#### v1.0 - Initial Commit
Commit 5390603eebdad19a0340b901d382f9833e5d8fe1
# APSIM Docs Files

To help with the updating of documentation files for the website hosted at [https://docs.apsim.info](https://docs.apsim.info).

# How to update the version on the production server

1. compress the two folders
2. scp each folder over to the server the command should look something like:
    ```bash
    scp webmaster@dev.apsim.info:/data apsim-docs-html.tar
    ```
3. uncompress the folders on the production server 
4. replace the folders and their contents on the server with the new ones
5. login to the server
6. navigate to the apsim-web directory:
    ```bash
    cd ~/sources/apsim-web
    ```
7. redeploy the apsim-docs service:
    ```bash
    docker compose restart --profile apsim-docs 
    ```
8. check your changes
9. done 


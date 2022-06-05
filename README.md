# Local Docker Proxy Gateway
Docker Proxy Environment for Web services with LetsEnrypt Certificate implementation.  
Helps to run HTTPS Web services on local development environment.  
Also creates a network to orchestrate different dockerized services (e.g.mailhog, mysql etc.)

## Installation/Usage
- Prerequisite is docker/docker-compose installed on local machine
- Optionally adjust `docker-compose.yml` to your liking
- Spin up proxy with `proxy_up.sh` to serce on ports 80 and 443 (localhost)
- Take down with `proxy_down.sh` after use
- Run other containers behind proxy with `VIRTUAL_HOST` and `LETSENCRYPT_*` ENV-Vars

## Notes
- Set up other containers to be automatically started in `docker-compose.yml` file  
according to sample syntax `sample.yml`
- Alternatively run containers directly from command line like in   
`docker run --rm -d --network=dockerland -e LETSENCRYPT_HOST=myurl.com  
-e LETSENCRYPT_EMAIL=info@myurl.com -e VIRTUAL_HOST=myurl.com --name myurl  
-p 80:80 docker/dockerimage`  

<br><hr>
// ITEOTWAWKI  
// It's the end of the World as we know it 🤔  
// But I feel fine!
        

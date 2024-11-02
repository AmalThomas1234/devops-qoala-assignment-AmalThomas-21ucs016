# devops-qoala-assignment-AmalThomas-21ucs016

This repository is submission for the devops assignment at qoala This readme contains all the setup instructions and errors which are solved while doing the assignment 

## Issues 

The main issues were in the docker-compose and the dockerfile

### In docker-compose.yaml 
1. Incorrectly used `eighty` instead of `80` for the `Nginx service`.
2. Incorrectly used "eight thousand" instead of `8000` for the `python-app` service.
3. Typo in the volume path: nginx.confi should be `nginx.conf`.
4. Typo in the network driver: bridg should be `bridge`.
5. Typo in the network option key: `compelex_option` should be `complex_option`.

### In python directory 
1. `WORKDIR /appp` should be `WORKDIR /app`
2. `COPY appy.py /app` should be `COPY app.py /app`, assuming the file is actually named `app.py`
3. RUN pip install flask netiface should be `RUN pip install flask netifaces` (the correct package name is netifaces).
4. EXPOSE "eight thousand" should be `EXPOSE 8000` (ports should be numeric).
5. CMD ["pythn", "app.py"] should be `CMD ["python", "app.py"]` (correct spelling for python).

### In nginx directory
1. nginx:latests should be nginx:latest
2. COPY nginix.conf /etc/nginx/nginx.conf should be COPY nginx.conf /etc/nginx/nginx.conf (correct spelling of nginx.conf).
3. COPY ./html /usr/share/nginx/htmll should be COPY ./html /usr/share/nginx/html.
4. EXPOSE "eighty" should be EXPOSE 80 (ports should be numeric).
5. CMD ["nginx", "-g", "daemon of;"] should be CMD ["nginx", "-g", "daemon off;"] (correct spelling of daemon off; to keep Nginx running in the foreground).
6. In `nginx.conf` the `default_type` is written as `default_typ` .


After resolving these issues the application code can be run at `localhost` using the `docker compose up` command as shown in the screenshots 


## Checklist 
- Set up Docker and Docker Compose.
- Clone and build Docker images.
- Debug and fix issues in code, Dockerfiles, or `docker-compose.yml`.
- Start containers and verify application accessibility on port 80.
- Upload files to a new GitHub repository and grant access to `devops@qoala.id`.
- Submit screenshots and a concise report of issues and solutions.

## SCREENSHOTS:

### Python application running at localhost 

![WhatsApp Image 2024-10-30 at 1 05 57 AM](https://github.com/user-attachments/assets/20a0c54e-fb29-4275-bdf4-1e4534ac556a)

## NGINX Server logs
![WhatsApp Image 2024-11-01 at 16 10 28_4e649b94](https://github.com/user-attachments/assets/b0e73bf0-ca2c-4436-a412-a4f0f622aa85)



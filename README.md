# Introduction
## Features
- User registration and login
- Sharing YouTube videos
- Viewing a list of shared videos (no need to display up/down votes)
- Real-time notifications for new video shares: When a user shares a new video, other logged-in users should receive a real-time notification about the newly - shared video. This notification can be displayed as a pop-up or a banner in the application, and it should contain the video title and the name of the user who shared it. 
## Tech
### BE: 
- Nestjs monorepo with 3 microservices: AuthService, ShareService and AppService. 
- Using GraphQL for delivery data. 
- MongoDB to store data.
- Socket.io for realtime notify feature, with redis adapter.
### FE:
- Nextjs, bootstrap, Apollo client, socketIO.
# Run
1. Clone project: https://github.com/phaobinh868/renec-youtube-sharing-app.git
2. Create .env file: using .env.example ffor docker.
- renec-fe/.env
- renec-be/apps/app/.env
- renec-be/apps/auth/.env
- renec-be/apps/share/.env
3. install dependencies
- cd renec-be & yarn install
- cd renec-fe & yarn install
4. test
- cd renec-be & yarn test
5. Start docker
- docker compose up
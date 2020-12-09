## Spotify API Automation

This repository was created to API test automation of [spotify APIs](https://developer.spotify.com/documentation/web-api/).

Technologies used:
- [Mocha](https://mochajs.org)
- [Chai](https://www.chaijs.com)
- [Nodejs](https://nodejs.org/)
- [Docker](https://docker.com)
- [Redis](https://redis.io)

### Setup

The guide goes throught steps required to setup test automation project in order to work with Docker and Redis.

1. Keep sensitive data separatedly. It is recommended to keep sensitive data in secret, so we are not going to commit any of this. Let's use `dotenv` to conveniently provide and access such data in the project. Ducplicate and rename `.env-sample` file in the project root and set values for these variables:
- SPOTIFY_ID: Your ID on spotify developers zone.
- SPOTIFY_SECRET: Your secret key.
- KEY_AUTH_TOKEN: Key for storage our acess token on Redis.
- AUTH_INVALID_TOKEN: An invalid token generated by Authentication Spotify endpoint.
2. Install the dependencies of this project with `npm install`.
3. Create a container to run the Redis. Run: `npm run create-redis`.

### Running test suit

To run our test suit:
- Open terminal.
- Navigate to the path the project was cloned in.
- Run `npm test`
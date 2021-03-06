# server-planner-with-docker

## How to use
### Docker - Docker Compose - Localhost
- clone
- On the project directory run: 
  - In development mode: `docker-compose up --build dev`
  - If error occurs for what ever reason, run:
    - `docker-compose down` to stop and remove the containers or `docker container stop <this-container_id> && docker container rm <this-container_id>` to stop and remove the(this) container
    - Then run: `docker-compose up --build dev` to start the containers

- Make a request to the server. `Hint->` use the sample request as a guide.

### Heroku - Remote Server - Online
- Use this `POST`: `https://app-server-planner.herokuapp.com/server-plans` instead of the localhost url specified on the sample request.

## Sample request:
- `POST`: `http://localhost:3001/server-plans`
- `Content-Type`: `application/json`
- `Body`: 
```json
{
	"server": {
		"CPU": 2, "RAM": 32, "HDD": 100
	},
	"vm": [
		{ "CPU": 1, "RAM": 16, "HDD": 10 },
      { "CPU": 1, "RAM": 16, "HDD": 10 },
      { "CPU": 2, "RAM": 32, "HDD": 100 }
	]
}
```

## Sample Response
```json
{
	"Result": 2
}
```




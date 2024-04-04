# booking-4WEBD

The booking project is realized by Alexis GANGNEUX, Axel CHOTEAU and Julien BOISGARD.

We have 3 databases model follow this MLD:
![Alt text](/images/archi.png "follow this model")
each models has his pod

In docker, we have this architecture
![Alt text](/images/pods.png "follow this model")

## Lauch this project

For launch use this command :

```Bash
docker-compose up

```

this command will create the correctly images and lunch all pods

The back API is ready on http://localhost:8080

The front ui is ready on http://localhost:5001

## Recreate an image

```Bash
docker-compose build "nameOfimage"
```

## Docs

### for the user , event and buy API's

it's necessary run an other pods with an exposion port because in our project the pods not exposed for security ask.

launch this command for launch the project with exposed port to display the docs

```Bash
docker-compose -f docker-compose-expose.yml up

```

once launched each API have one docs on the links:
user: http://localhost:3001/api-docs
event: http://localhost:3002/api-docs
buy: http://localhost:3003/api-docs

### for the front api

once our application is launched the docs is directly on the link : http://localhost:8080/api-docs

## Tests

For the tests, first launch the docker-compose-expose.yml :

```Bash
docker-compose -f docker-compose-expose.yml up

```

then go to the relevant folder : users , event , frontapi or buy 

```Bash
cd 'name of the folder'

```

then launch the npm run test command :

```Bash
npm install
npm run test 

```
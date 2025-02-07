
# Snake Game

this app is a blazor app who try to help how create a snake game using blazor was not just me, i had a lot of help create the app also you can run the app using docker





## Deployment

To run there are two ways using the visual studio ide just running the app or:

```bash
  dotnet restore
  dotnet publish -c Release -o out
```

after that building the docker in my case i am using this:

```bash
    docker build -t snakegame .
    docket run -d  -p 5000:5000 --name snakeGame snakegame
```

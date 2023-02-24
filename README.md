# mc-bot-server

start a minecraft bot remotely

## API

### Creating Bots

```
POST /create 
Content-Type: application/json
{
  apiKey: "valid api key",
  type: "one of the bots from lib/bots/*.js",
  port: 44959,
  host: "RQNDOM.aternos.me"
  username: "bot",
  password: "optional password",
  owner: "CandraMyName"
}
```

Returns an ID that you can pass to /destroy

### Destroying Bots

```
POST /destroy
Content-Type: application/json
{
  apiKey: "valid api key",
  id: "bot id to destroy"
}
```

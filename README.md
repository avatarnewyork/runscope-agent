# Runscope Radar Docker Agent
This is an alpine based light-weight Docker image for running the Runscope Radar on-premise agent.  

## Usage
The image includes an empty file /runscope.conf (useful if you only want to pass command line options)

### Example with command line options only
For a full list of command line options, see documentation: https://www.runscope.com/docs/api-testing/agent/

```bash
docker run -ti avatarnewyork/runscope --name=circleci --token=[MY_TOKEN] --agent-id=[MY_AGENT_ID] --team-id=[MY_TEAM_ID] -f /runscope.conf -v
```

### Example with mounted config file
This assumes you have a config file in the current directory named `runscope.conf`.  For config file options, see documentation: https://www.runscope.com/docs/api-testing/agent/

```bash
docker run -ti -v $(pwd):/mnt avatarnewyork/runscope -f /mnt/runscope.conf -v
```

## Reference
* Full documentation: https://www.runscope.com/docs/api-testing/agent/
* Source Code: https://github.com/avatarnewyork/runscope-agent
* Docker Image: avatarnewyork/runscope-agent

## Credits
This image is mostly based on:
* https://github.com/mmcc/runscope-agent-docker
* https://github.com/frol/docker-alpine-glibc


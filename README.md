# Project Maka API


## Agent Administration

### Create Agent
Useful for bulk creating new agents in deployment scripts.

Content Type: `application/x-www-form-urlencoded`

URL: `POST https://s.en0.io/api/createReporter`

Required fields: 
 - `key` - your _account_ API key
 - `hostname` - the hostname of the agent


### Delete Agent
Unavailable via API at this time, must be done from UI or directly via database.

---

## Report Endpoints

### UFW-formatted log submission
Content Type: `application/x-www-form-urlencoded`

URL: `POST https://s.en0.io/api/v2/logevent/ufw`

Required fields:
- `key` - your _agent_ API key
- `log` - the line from the `ufw.log` file, _encoded in base64_

### filterlog-formatted log submission
WIP

### fail2ban sshd log submission
Content Type: `application/x-www-form-urlencoded`

URL: `POST https://s.en0.io/api/v2/logevent/sshd`

Required fields:
- `key` - your _agent_ API key
- `log` - the line from the `fail2ban.log` file, _encoded in base64_

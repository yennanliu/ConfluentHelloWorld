# ConfluentHelloWorld


### Quick Start (docker)
```bash
# https://docs.confluent.io/current/quickstart/cos-docker-quickstart.html#cos-docker-quickstart
git clone https://github.com/confluentinc/cp-all-in-one
cd cp-all-in-one
git checkout 5.5.0-post
cd cp-all-in-one-community/
docker-compose up -d --build
```

### Quick Start (local)
```bash
# https://docs.confluent.io/current/quickstart/cos-docker-quickstart.html#cos-docker-quickstart

# STEP 1) install confluent app
# https://www.confluent.io/download/?_ga=2.178726244.1388377793.1590507730-295605477.1589554448&_gac=1.229362088.1590508119.EAIaIQobChMIotDVgu_R6QIVDNiWCh2uiwxUEAAYASAAEgITWPD_BwE

# STEP 2) install confluent-hub
brew tap confluentinc/homebrew-confluent-hub-client
brew cask install confluent-hub-client
confluent-hub

# STEP 3) install confluent CLI
curl -L --http1.1 https://cnfl.io/cli | sh -s -- -b /usr/local/bin

# STEP 4) install kafka-connect-datagen
confluent-hub install \
--no-prompt confluentinc/kafka-connect-datagen:latest

# STEP 5) set up env, path
cat ~/.bash_profile
export CONFLUENT_HOME=<path-to-confluent>
export PATH="${CONFLUENT_HOME}/bin:$PATH"

# STEP 6)
# Start Confluent Platform using the Confluent CLI 
confluent local start command
```

### Ref
- https://docs.confluent.io/current/quickstart/index.html

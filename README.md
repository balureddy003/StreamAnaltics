# Setup
git clone https://github.com/Fokko/divolte-kafka-druid-superset.git
cd divolte-kafka-druid-superset
git submodule update --init --recursive

docker-compose rm -f && docker-compose build && docker-compose up

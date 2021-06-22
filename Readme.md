# SpringBoot > Kafka > ELK stack 

This project uses springboot that pass messages to Kafka consumer and can be seen to Kibana

## Installation

Use [docker-compose](https://docs.docker.com/compose/install/) to install.
User [docker-desktop](https://www.docker.com/products/docker-desktop) to install

##Setup and Usage

```logstash 
 *  Update logstash_pipeline/logstash.conf [ifconfig:en0:inet"ip address"] to the machine ip address. for mac ifconfig > en0 > inet > 
 search for ip your ip address (format 192.x.x.x)
 * increase docker desktop resources (my settings Memory : 12GB; Swap 3GB)
 * docker-compose -f src/main/resources/selftut-elk.yml up -d  
 * docker-compose -f src/main/resources/selftut-kafka.yml up -d  
 * Refer to selftuts kafka topic (make sure its the same with the one you declare on the logstash.conf 
 * Refer to selftuts on how to create kibana index 
 * Run springboot app
 * on Terminal curl -X POST -F 'message=Bump Version Testing 123' http://localhost:8080/kafka/publish
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

I've followed the steps from this site [selftuts](http://selftuts.com/)
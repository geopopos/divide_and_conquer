# Divide and Conquer
This project is being developed as a toy project. Intend to use it for managing GPU computation across multiple machine for machine learning algorithms, but that may change ast this project grows.

The initial implementation of the ventilator, worker, and sink are from 0MQ's 'The Guide' [The Guide](http://zguide.zeromq.org/py:all#Divide-and-Conquer)

I have gone ahead and dockerized each program so that I can quickly spin up and down new workers as needed.

The ventilator and sink are static. They are single program instances which should live through the life of the program.

The workers are built to be dynamic. Being able scale them as needed.

## Getting started
### Using the requirements.txt file.
1. First install the required dependencies for this project
```
pip3 install -r requirements.txt
```

2. spin up the sink, worker(s), and ventilator in that order
```
> python3 sink/sink.py
> python3 worker/worker.py
> python3 ventilator/ventilator.py
  http://zguide.zeromq.org/py:all#Divide-and-Conquer

### Using docker-compose
#### Prerequisites
1. Have the docker version 19.03 or higher installed on your local machine
2. Have docker-compose version 1.25 for higher installed on your local machine

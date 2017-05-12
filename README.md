# Demo for Docker Monitoring Meetup

Run `docker-compose up`

After setting your hosts file (see below) the following sites will be available:

- blog.meetup.local
- drupal.meetup.local
- grafana.meetup.local
- prometheus.meetup.local
- cadvisor.meetup.local

## Setup hosts
The demo uses some local domains where you can visit your services. These must be registered as domains on your local machine; just append the content of `hosts` to your `/etc/hosts` file:

```
$ sudo sh -c 'cat ./hosts >> /etc/hosts'
```

## Setup Grafana

You can login to the Grafana dashboard with user **admin** and password **docker**. After this you will have to add your Prometheus instance as a data source. This can be done in the Menu under **Data Sources**. Set the name of the data source to **prometheus**, type to **Prometheus** and url to **http://prometheus:9090**.

Optionally you can import the demo dashboard located in this repository at `grafana/demo_dashboard.json`.

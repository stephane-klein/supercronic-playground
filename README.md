# supercronic playground

[supercronic](https://github.com/aptible/supercronic) playground:

```sh
$ docker-compose build
$ docker-compose up -d
$ docker-compose logs -f
Attaching to supercronic-playground_echo-cron_1
echo-cron_1  | time="2021-02-25T12:30:28Z" level=info msg="read crontab: /my-crontab"
echo-cron_1  | time="2021-02-25T12:30:29Z" level=info msg=starting iteration=0 job.command="echo \"hello from Supercronic\"" job.position=0 job.schedule="*/5 * * * * * *"
echo-cron_1  | time="2021-02-25T12:30:29Z" level=info msg="hello from Supercronic" channel=stdout iteration=0 job.command="echo \"hello from Supercronic\"" job.position=0 job.schedule="*/5 * * * * * *"
echo-cron_1  | time="2021-02-25T12:30:29Z" level=info msg="job succeeded" iteration=0 job.command="echo \"hello from Supercronic\"" job.position=0 job.schedule="*/5 * * * * * *"
echo-cron_1  | time="2021-02-25T12:30:35Z" level=info msg=starting iteration=1 job.command="echo \"hello from Supercronic\"" job.position=0 job.schedule="*/5 * * * * * *"
echo-cron_1  | time="2021-02-25T12:30:35Z" level=info msg="hello from Supercronic" channel=stdout iteration=1 job.command="echo \"hello from Supercronic\"" job.position=0 job.schedule="*/5 * * * * * *"
```

```sh
$ docker-compose down
```

Playground todo list:

- [ ] Connect `supercronic` to [Prometheus](https://github.com/prometheus/prometheus)
  - [ ] Setup Prometheus container in this playground
- [ ] Connect `supercronic` to [Sentry](https://github.com/getsentry)
  - [ ] Setup Sentry container in this playground
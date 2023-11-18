# This is a test project to show advantages of async email sending using Symfony messenger

## To run project execute
```
docker-compose up -d
symfony console doctrine:schema:create
symfony console doctrine:migrations:migrate
```

## To consume messages from the queue
```
symfony console messenger:consume
```

## If you want to experiment with sync delivery change routing 
`Symfony\Component\Mailer\Messenger\SendEmailMessage: async`

to 
`Symfony\Component\Mailer\Messenger\SendEmailMessage: sync`

in `config/packages/messenger.yaml`


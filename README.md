# test-google-pubsub-problem

Reproduce the problem

## Installing

1. `git clone` this repo.
1. Run `npm install`. I tested this using NodeJS v10, but it can probably work with NodeJS v8.
1. Then, run `./scripts/create-backing-pubsub-topics.js <env>`. This will create a topic and a subscription that will later
   be used by the reproduction code. The `env` is whatever string you want, and it will be prepended to the
   topic and subscription name.

## Using it

The script to run is `./scripts/run-test-google-pubsub-problem.js`. You can run it with `-h` to get help on all the options.

To listen on messages, run:

```sh
./scripts/run-test-google-pubsub-problem.js -e <env> -l -c 100000 -w 5
```

To publish 100 messages, run:

```sh
./scripts/run-test-google-pubsub-problem.js -e <env> -m message -c 100
```

Once published, you should see them in the listener

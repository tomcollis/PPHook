# Webhook Relay aka P(ush)P(ull)Hooks
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)

[![Deploy](https://button.deta.dev/1/svg)](https://go.deta.dev/deploy)

A brief description of what this project does and who it's for


## Usage/Examples

```javascript
import Component from 'my-project'

function App() {
  return <Component />
}
```


## Environment Variables

To run this code, you will need to add the following environment variables to your .env.local file

`DETA_PROJECT_KEY`

`API_KEYS` (Work in Progress - currently specified in index.js)

## Deployment to [Deta](https://www.deta.sh/)

To deploy this project on Deta, run

```bash
  npm run deploy
```


## API Reference

#### Post Webhook

```http
  POST /
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `source` | `string` | **Optional but Recommended**. Source System Key, can be anything you want or left blank .|


#### Get items for source system by id

```http
  GET /webhooks/$source
```
This will return all webhooks from the system with a matching source keey and delete all corresponding results from the database by design.

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api-key` | `string` | **Required**. Your API key |


#### Get items for source system unknown

```http
  GET /webhooks
```
This will retrieve all webhooks posted without a source key, it will also delete all corresponding results from the database by design.

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api-key` | `string` | **Required**. Your API key |


## Feedback

If you have any feedback, please reach out to us at fake@fake.com

## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.

## Acknowledgements
 - [ExpressJS Example - Simple Web API](https://github.com/expressjs/express/blob/28db2c2c5cf992c897d1fbbc6b119ee02fe32ab1/examples/web-service/index.js)

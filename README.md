#### ⚠️ **IMPORTANT** ⚠️: THIS PROJECT IS A WORK IN PROGRESS, TURN ON RELEASE NOTIFICATIONS TO GET NOTIFIED WHEN IT IS READY.
# PPHook = **P**(ush)**P**(ull)(Web)**Hook**
[![](https://img.shields.io/badge/Buy%20me%20-coffee!-orange.svg?logo=buy-me-a-coffee&color=795548)](https://paypal.me/TomCollisUK/2)
[![GitHub stars](https://img.shields.io/github/stars/tomcollis/PPHook)](https://github.com/tomcollis/PPHook/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/tomcollis/PPHook)](https://github.com/tomcollis/PPHook/issues)
[![Github All Releases download count](https://img.shields.io/github/downloads/tomcollis/PPHook/total.svg?style=flat)](https://github.com/tomcollis/PPHook/releases/latest)
[![GitHub latest release version](https://img.shields.io/github/v/release/tomcollis/PPHook.svg?style=flat)](https://github.com/tomcollis/PPHook/releases/latest)

[![Deploy](https://button.deta.dev/1/svg)](https://go.deta.dev/deploy)

A brief description of what this project does and who it's for


## Environment Variables

To run this code, you will need to add the following environment variables to your .env.local file

`DETA_PROJECT_KEY`

`API_KEY`

## Deploy to [Deta](https://www.deta.sh/)

To deploy this project on Deta, click the button below:

[![Deploy](https://button.deta.dev/1/svg)](https://go.deta.dev/deploy)

You will automatically be prompted to enter the required environment variables and all data will be private in your own account.

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

If you have any feedback, you can:

[![](https://img.shields.io/static/v1?label=Message%20on&message=Telegram&color=27A7E7&logo=telegram&style=for-the-badge)](https://t.me/tomcollis)

or

[![](https://img.shields.io/static/v1?label=Create%20New&message=Issue&color=4EC820&logo=github&style=for-the-badge)](https://github.com/tomcollis/PPHook/issues)




## Acknowledgements
 - [ExpressJS Example - Simple Web API](https://github.com/expressjs/express/blob/28db2c2c5cf992c897d1fbbc6b119ee02fe32ab1/examples/web-service/index.js)

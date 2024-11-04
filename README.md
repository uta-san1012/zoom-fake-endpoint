
## Installation

In terminal, run the following command to clone the repo:

`$ git clone git@github.com:uta-san1012/zoom-fake-endpoint.git`

## Setup

1. In terminal, `cd` into the cloned repository:

   `$ cd meetingsdk-auth-endpoint-sample`

1. Then install the dependencies:

   `$ npm install`

2. Rename `.env.example` to `.env`, edit the file contents to include your [Zoom Meeting SDK key and secret](https://developers.zoom.us/docs/meeting-sdk/developer-accounts/), save the file contents, and close the file.

3. Start the server:

   `$ npm run start`

## Usage

Make a POST request to `http://localhost:4000` (or your deployed url) with the following request body:

| Property            | Type     | Required?  | Validation Rule(s)                                                                          |
| ------------------- | -------- | ---------- | ------------------------------------------------------------------------------------------- |
| `meetingNumber`     | `string` | Yes (web)* | - Required if generating a web JWT, optional for native.                                    |
| `role`              | `number` | Yes (web)* | - Required if generating a web JWT, optional for native. <br> - Must be equal to `0` or `1` |
| `expirationSeconds` | `number` | No         | - Must be between `1800` (30 minutes) and `172800` (48 hours) seconds                       |


その他必要な情報はoffcial-doc.mdを参照

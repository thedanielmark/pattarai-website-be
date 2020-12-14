# REST API Layer - KuTumba FC

![](https://github.com/thedanielmark/kutumbafc-api/blob/main/logo-180x180.png)

This repository contains scripts written in PHP 7 to implement a REST API layer for KuTumba FC - a football club founded in Chennai, India.
This project is a partnership between [MixSpace Internet Services](https://mixspace.xyz) and [KuTumba FC](https://kutumbafc.com).

The code in this repository is closed source and it requires the explicit written permission of [Daniel Mark](https://thedanielmark.com) in order to download, modify or distribute pieces of it or entire scripts itself.

----

### APIs Built
- Login
- Register
- Verify Account
- Resend Verification Code
- Logout
- Auth Status

----

### Format of the APIs

> All APIs are called via the `GET` method and responses are sent back in `JSON` format.

The APIs [require](https://www.php.net/manual/en/function.require.php) a <b>config.php</b> file at the start. This config file contains the <b>server-address</b>, <b>username</b>, <b>password</b> & <b>database-name</b> variables and a connection instance to the database. This connection is called every time a query is to be run.

The API receives the <b>URL parameters</b> and assigns them to <b>global variables</b>.
It then proceeds to retrieve the <b>auth_token</b> of the user from the DB and compares it to the auth token it just received. If the tokens match, the assets/CRUD operations the user requested for may be performed.

In all cases when a CRUD operation is carried out, an <b>&apos;if&apos;</b> conditional is used to check whether the database operation completed successfully and an appropriate response message is sent back. All outcomes are unit tested and handled appropriately.

<!-- ![](https://img.shields.io/github/stars/pandao/editor.md.svg) ![](https://img.shields.io/github/forks/pandao/editor.md.svg) ![](https://img.shields.io/github/tag/pandao/editor.md.svg) ![](https://img.shields.io/github/release/pandao/editor.md.svg) ![](https://img.shields.io/github/issues/pandao/editor.md.svg) ![](https://img.shields.io/bower/v/editor.md.svg) -->

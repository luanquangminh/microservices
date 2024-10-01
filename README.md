<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

### `README.md` file

```markdown
# Introdcution

The **Graduation 1** project is a NestJS application using microservices to provide various APIs, including:
- Retrieve student information (name + student ID)
- Return the current date and time on the server
- Get an email address with student ID and student name
- Fetch exchange rates from Vietcombank
- Transform the text to QRCode.

## 1. Installation

### Step 1: Clone the project

Use the following command to clone the project from GitHub to your local machine:

```bash
git clone https://github.com/luanquangminh/Microservices.git
```

### Step 2: Install dependencies

Navigate to the `gr1` project directory and install the dependencies:

```bash
cd gr1
npm install
```

### Step 3: Run the application

After installing the dependencies, run the application with the following command:

```bash
npm run start
```

The application will run on `http://localhost:3000`.

## 2. Main Features

### 2.1. Retrieve student information

- **Endpoint**: `/gr1/aboutus`
- **Method**: GET
- **Function**: Return the student's name and student ID.
- **Example**:

```
GET http://localhost:3000/gr1/aboutus
```

- **Response**:

```json
{
  "name": "Nguyen Van A",
  "mssv": "20221111"
}
```

### 2.2. Get the current date and time

- **Endpoint**: `/gr1/today`
- **Method**: GET
- **Function**: Return the current date and time from the server.
- **Example**:

```
GET http://localhost:3000/gr1/today
```

- **Response**:

```json
{
  "currentDateTime": "2024-09-28T14:25:36.123Z"
}
```

### 2.3. Generate an email address from student ID and name

- **Endpoint**: `/gr1/generate-email`
- **Method**: GET
- **Parameters**:
  - `mssv`: The student ID.
  - `name`: The student's name.
- **Function**: Generate an email address following the format `<firstName>.<lastInitialAndMiddleInitial>+6digitsOfStudentID@sis.hust.edu.vn`.
- **Example**:

```
GET http://localhost:3000/gr1/generate-email?mssv=20221111&name=Nguyen%20Van%20A
```

- **Response**:

```json
{
  "email": "a.nv221111@sis.hust.edu.vn"
}
```

### 2.4. Fetch exchange rates from Vietcombank

- **Endpoint**: `/gr1/vcb-exchange-rate`
- **Method**: GET
- **Function**: Fetch exchange rates from Vietcombank's API.
- **Example**:

```
GET http://localhost:3000/gr1/vcb-exchange-rate
```

- **Response**:

```json
{
  "rates": {
    "USD": {
      "buy": "23,000",
      "sell": "23,200"
    },
    "EUR": {
      "buy": "25,500",
      "sell": "26,000"
    }
  }
}
```

### 2.5. Return a QRCode of a given text

- **Endpoint**: `/gr1/qrcode`
- **Method**: GET
- **Parameter**: `text` - The text to be encoded into a QR code.
- **Function**: Return a QR code image for the given text.
- **Example**:

```
GET http://localhost:3000/gr1/qrcode?text=HelloWorld
```

- **Response**: A PNG image of the QR code will be returned and displayed in the browser.





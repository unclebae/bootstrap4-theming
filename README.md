# Bootstrap4 Theming

## Step1.
Create a directory what you want.

```
mkdir BootTheming
cd BootTheming
```

## Step2.
Initialize npm and install bootstrap

```
npm init
npm install bootstrap
```

## Step3.
Install scss-powertools in working directory

```
npm install scss-powertools --save-dev
```

## Step4.
Create scss folder and make custom.scss file in scss

```
mkdir scss
touch scss/custom.scss
```

## Step5.
Editing custom.scss like blow.

```
cd scss
vi custom.scss
```

and Esc + w + q

```

$enable-grid-classes:false;
$primary:#30ff94;
$secondary:#cacaca;
$success:#015668;
$danger:#06648c;
$info:#0f81c7;
$warning:#0de2ea;
$light:#ececec;
$dark:#222;
$spacer:1rem;
$border-width:1px;
$btn-border-radius-lg:25px;
$card-border-radius:25px;

@import "../node_modules/bootstrap/scss/bootstrap";

```

## Step6.
Modify package.json like this.
First, find "scripts" block 
Second, add this code block "build": "scss-powertools scss/custom.scss dist/custom.css"

```
{
  "name": "bootstrap_cust",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "scss-powertools scss/custom.scss dist/custom.css"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bootstrap": "^4.2.1"
  },
  "devDependencies": {
    "scss-powertools": "^1.0.1"
  }
}
```

## Step7.
Run npm build

```
npm run build
```

## Step8.
Check created custom.css file in dist folder.
And create index.html and edit like this. (This code blocks from Bootstrap Example)

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Theming.</title>
    <base href="/">
    <meta name="description" content="BootStrap Theming." />
    <link rel="stylesheet" href="dist/custom.css" />
  </head>
  <body>
    <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white border-bottom box-shadow">
        <h5 class="my-0 mr-md-auto font-weight-normal">Company name</h5>
        <nav class="my-2 my-md-0 mr-md-3">
          <a class="p-2 text-dark" href="#">Features</a>
          <a class="p-2 text-dark" href="#">Enterprise</a>
          <a class="p-2 text-dark" href="#">Support</a>
          <a class="p-2 text-dark" href="#">Pricing</a>
        </nav>
        <a class="btn btn-outline-primary" href="#">Sign up</a>
      </div>
  
      <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
        <h1 class="display-4">Pricing</h1>
        <p class="lead">Quickly build an effective pricing table for your potential customers with this Bootstrap example. It's built with default Bootstrap components and utilities with little customization.</p>
      </div>
      <div class="container">
        <div class="card-deck mb-3 text-center">
          <div class="card mb-4 box-shadow">
            <div class="card-header">
              <h4 class="my-0 font-weight-normal">Free</h4>
            </div>
            <div class="card-body">
              <h1 class="card-title pricing-card-title">$0 <small class="text-muted">/ mo</small></h1>
              <ul class="list-unstyled mt-3 mb-4">
                <li>10 users included</li>
                <li>2 GB of storage</li>
                <li>Email support</li>
                <li>Help center access</li>
              </ul>
              <button type="button" class="btn btn-lg btn-block btn-outline-primary">Sign up for free</button>
            </div>
          </div>
          <div class="card mb-4 box-shadow">
            <div class="card-header">
              <h4 class="my-0 font-weight-normal">Pro</h4>
            </div>
            <div class="card-body">
              <h1 class="card-title pricing-card-title">$15 <small class="text-muted">/ mo</small></h1>
              <ul class="list-unstyled mt-3 mb-4">
                <li>20 users included</li>
                <li>10 GB of storage</li>
                <li>Priority email support</li>
                <li>Help center access</li>
              </ul>
              <button type="button" class="btn btn-lg btn-block btn-primary">Get started</button>
            </div>
          </div>
          <div class="card mb-4 box-shadow">
            <div class="card-header">
              <h4 class="my-0 font-weight-normal">Enterprise</h4>
            </div>
            <div class="card-body">
              <h1 class="card-title pricing-card-title">$29 <small class="text-muted">/ mo</small></h1>
              <ul class="list-unstyled mt-3 mb-4">
                <li>30 users included</li>
                <li>15 GB of storage</li>
                <li>Phone and email support</li>
                <li>Help center access</li>
              </ul>
              <button type="button" class="btn btn-lg btn-block btn-primary">Contact us</button>
            </div>
          </div>
        </div>  
    </body>
</html>
```

Then you can see like this picture.

![Picture]("./bootstrap_sample.png")





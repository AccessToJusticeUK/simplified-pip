# Simplified PiP
Digital form for agencies assisting clients with their Personal Independence Payment request to the UK Department for Work and Pensions (DWP).

## Contributing
We practise [Trunk Based Development](https://trunkbaseddevelopment.com) which means that all commits should go directly to master.
On commit, our AWS CodeBuild will kick off a build and deploy a static website in Amazon S3.

![Build badge](https://codebuild.eu-west-2.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiWVpraG8vZm1qMEJSZzJoUVk1MUo0TFd0dW5VaXRua2ZQMVFiejEwVkRMTjBGTkcwNHc5MWFzTjhTemNJNklUaFlTd1IrTDZLbENLS2hacWc2dExjL2tnPSIsIml2UGFyYW1ldGVyU3BlYyI6IkZYbnlCUTJ4a3dNS21nQUYiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)

Production URL: http://simplified-pip.s3-website.eu-west-2.amazonaws.com/.

### Project setup
`npm install`

Compile and hot-reloads for development: 
`npm run serve`

Compile and minifies for production: 
`npm run build`

Lint and fix files: 
`npm run lint`

Run your unit tests: 
`npm run test:unit`

### AWS Account
Please contact [@BAPostma](https://github.com/BAPostma) for obtaining access.

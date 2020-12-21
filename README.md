# Simplified PiP
Digital form for agencies assisting clients with their Personal Independence Payment request to the UK Department for Work and Pensions (DWP).

## Contributing
We practise [Trunk Based Development](https://trunkbaseddevelopment.com) which means that all commits should go directly to master.
On commit, our AWS CodeBuild will kick off a build and deploy a static website in Amazon S3.

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

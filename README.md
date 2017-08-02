This repo emerged out of the need to quickly set up a new .NET / React based web applicaiton inside of Visual Studio. There is currently no easy way of using Facebook's create-react-app tool together with Visual Studi0 2017 without all sorts of rewiring. ReactJS.NET exists, but it includes all sorts of magic for Razor and does not fully support create-react-app, ES2016 component exports, etc.  I wanted to make it

* easier
* as intended by the vendor
* simplier, no black magic / automagic code generation in the background

The repo incldues a basic template solution  for Visual Studio 2017 to build a React / ASP.NET Core based application in one place. The solution is largely based off https://sethreid.co.nz/delivering-single-page-apps-aspnet-core/ with some tweaks, e.g. inclusion of Bootstrap CSS, setup of a solution file, and others.

The ```client``` folder contains the client single page app, which was created using create-react-app. To run the client just run ```npm start``` from a terminal window. To push your bundled app and static HTML / CSS into production, files will need to be copied into the ```server/wwwroot``` folder. ```npm run build``` will do the job. 
(remember to run  first to ensure the appropriate tooling is installed ```npm install --save-dev rimraf ncp```). 

The ```server``` folder contains the API back-end, which was created using ```dotnet new```.

Happy hacking!

Anders
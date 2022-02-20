# bootstrap-11ty
Eleventy (11ty) tryout, a simple static website generator that is capable of mixing template languages. The base is using NODE.js and NPM.

## Install

Here you will see a quick no fuss instructions to get up a running.

For a more detailed howto guide, the resulting website here on Github Pages, should offer a resonable additional information and references. 
The idea is to kep its simple.  

Lets get started

- What prereguisite skills are necessary?
    - Some knowledge of HTML, CSS, Java/js and script/bash,   
 - What development tools?
   -  Plain text editor or advanced dev tools like [ATOM](https://atom.io/)
 - What is the Developmet Target and production target?
    - best to start using local machine for this tryour before any test deployment on github 
 - Is it virtual, local or remote hosting?
    - this depends on options. Easy to use local folder setup as all necessary tools and packages can be included in the setup.
 - Do you have 'root' access?
    - If you can write to FOLDER, then all tools and packages can be installed. However, in somecase you may need live internet access to download all packages, language tools and BOOTSTRAPS, CSS and other linked files. ALL can be downloaded to setup for local development deployment. In full deployment, most linked stylesheets, images and or scripts can be establish in cloud services. 

### Local host

Open terminal and setup environment

```bash
mkdir -p ~/webdev/11ty/01-base/
cd ~/webdev/11ty/01-base/

```
Initialise

Install Node.js (version 16) and NPM is not installed

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
nvm install 16
```
check versions

```bash
 node -v
 npm -v
 
 
```

Lets write a simple _package.json_ file in current directory.

```
npm init -y
```
Now install Eleventy basic site modules. "eleventy" here is our structure.

```bash
npm install @11ty/eleventy
```
lets test abit

```bash
echo "console.log('hello world');" > hello.js
node hello.js

```
This should give us a `hello world` back from Node.js

The instalation may return errors
 and you may need to follow instructions and update

```bash
npm install -g npm@8.5.1

npm audit fix
nvm install --lts
nvm install node
nvm use node
```

Now lets try 11ty
```bash
npx @11ty/eleventy --serve
```
this should give us
```
$ npx @11ty/eleventy --serve
Processed 0 files in 0.01 seconds
Watching…
[Browsersync] Access URLs:
 ---------------------------------------
       Local: http://localhost:8080
    External: http://[your IP address]:8080
 ---------------------------------------
          UI: http://localhost:3001
 UI External: http://localhost:3001
 ---------------------------------------
[Browsersync] Serving files from: _site
```

After starting the basic server, there is nothing to present to the browser until you add content.
To shut down type 
_ctrl C_

Close Terminal and start up new Terminal again and try again.
```bash
npx @11ty/eleventy --serve
Need to install the following packages:
  @11ty/eleventy
Ok to proceed? (y) y
# maybe some "npm WARN deprecated" warnings ...... 
[11ty] Wrote 0 files in 0.03 seconds (v1.0.0)
[11ty] Watching…
[Browsersync] Access URLs:
 ------------------------------------
    Local: http://localhost:8080
 External: http://[your IP address]:8080
 ------------------------------------
[Browsersync] Serving files from: _site

```
So far so good but still nothing presented.
now lets clean up and pull in from
bootstrap-11ty/ stage1

```bash
cd ..
rm -fr 01-base/
git clone https://github.com/DavitTec/bootstrap-11ty 01-base
cd 01-base
npx @11ty/eleventy --serve

```
Now lets pull some simple docs from git hub
using state merge.





## References

- [Building Node.js](https://github.com/nodejs/node/blob/master/BUILDING.md#building-nodejs-on-supported-platforms)

## ToDo







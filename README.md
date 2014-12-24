# uploads

a cli tools for uploads ui

[![npm version](https://badge.fury.io/js/upload-cli.svg)](http://badge.fury.io/js/upload-cli)

## Install

	sudo npm install -g upload-cli
	
## Usage 

in current dir,execute `uc` command

	uc
	
result

```
	 somedir git:(master) uc

	> upload-cli@0.1.0 test /Users/sang/workspace/github/uploads
	> node index.js

	[up-cli INFO] It's served! now you can open in browser http://127.0.0.1:3456/
```


## for post

![](doc/json.png)

- url = http://127.0.0.1:3456/post/formdata.json
- filename = xxxx

返回


```
{
    "data": {
        "path": "/Users/sang/workspace/github/uploads"
    },
    "status": {
        "code": 0,
        "msg": "success."
    }
}
```

**使用curl命令**

```
➜  uploads git:(master) ✗ curl -F filename=@/Users/sang/workspace/github/api-test/play/file/da_qin_huang_ling_.mobi http://127.0.0.1:3456/post/formdata.json
{"data":{"path":"/Users/sang/workspace/github/uploads"},"status":{"code":0,"msg":"success."}}%   
```

## Preview 

![](doc/preview.png)


## for dev 

debug with node-inspector

	npm run debug
	
publish to npmjs.org

	npm run deploy 

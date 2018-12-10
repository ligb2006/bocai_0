# bocai_0

## 创建eos账号
    /eos/create_account/{account}/{active}

* 请求实例
```
/eos/create_account/zqwertyuiopo/EOS7LU9DB7ipmPLyYC1RLy3wwNFUAkbPSBM9rKC8DACfUERPiZ4Cr
```
    
* 错误响应
```javascript
{"code":"100","detail":"Internal Service Error: Account name already exists","data":""}
```

* 成功响应
```javascript
{"code":"0","detail":"恭喜你，操作成功","data":["zqwertyuiopo","EOS5yds6uBBVWB2oggJSBVypu7VjRMy3DiW3de7XJtETshE2XfkhJ","EOS7LU9DB7ipmPLyYC1RLy3wwNFUAkbPSBM9rKC8DACfUERPiZ4Cr"]}
```

## 生成keys
    /eos/account/genkey

* 成功响应
```javascript
["5JfcVqdF964Q2QS1HaiCKsc1GAcccTwdyBAMMpeGSPXsNztCQvq","EOS7GYU77S8pJNXnCQvXKrjvfMVcQMw7Yqs1CkwsN2pUm5sJ8AZ88"]
```

## 获取账户信息
    /eos/account/{account}

* 请求实例
```
/eos/account/zqwertyuiopa
```

* 错误响应
```javascript
{"code":"100","data":"","detail":"Internal Service Error: unspecified"}
```

* 成功响应
```javascript
["5JfcVqdF964Q2QS1HaiCKsc1GAcccTwdyBAMMpeGSPXsNztCQvq","EOS7GYU77S8pJNXnCQvXKrjvfMVcQMw7Yqs1CkwsN2pUm5sJ8AZ88"]


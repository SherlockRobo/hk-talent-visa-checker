# 香港优才 / 高才 / 专才互动判断看板

## 核心链接

- 本地工具：`/Users/bytedance/ObsidianVault_LOCAL/wiki/writing/tools/hk-talent-visa-checker/index.html`
- 飞书多维表格后台：https://my.feishu.cn/base/VGJwbw2N7aadQGsG1uIcyLXcnBg
- 飞书客户填写表单：https://my.feishu.cn/share/base/shrcnra78TjubSWw2qhtoezeVtg
- H5客户双栏页：https://sherlockagent.vercel.app/articles/hk-talent-client/
- GitHub客户双栏页：https://sherlockrobo.github.io/hk-talent-visa-checker/customer-page/
- 飞书结果展示：https://my.feishu.cn/base/VGJwbw2N7aadQGsG1uIcyLXcnBg?table=tblF2fxRBVlmwCM5&view=vewFkdrgin
- 飞书官方要求表：https://my.feishu.cn/base/VGJwbw2N7aadQGsG1uIcyLXcnBg?table=tblPRC70YB6P51uy&view=vewWBCmCY7
- Vercel 后台版：https://sherlockagent.vercel.app/articles/hk-talent-visa-checker/
- 线上网页：https://sherlockrobo.github.io/hk-talent-visa-checker/
- GitHub 仓库：https://github.com/SherlockRobo/hk-talent-visa-checker
- 私有提交收件仓库：https://github.com/SherlockRobo/hk-talent-submissions

## 功能

- 优才 QMAS：Must 检查 + 12项综合计分。
- 高才 TTPS：A/B/C 类自动匹配。
- 专才 GEP/ASMTP：按身份、香港 offer、岗位、薪酬、本地劳动力/便利措施判断。
- 学校模糊匹配：内置官方合资格大学清单 200 所。
- 记录保存：浏览器本地保存、载入、删除、导出 JSON。
- 后台提交：Vercel API `/api/hk-talent-submit` 写入私有 GitHub 收件仓库。
- 飞书多维表格版：手机表单填报，提交后在后台记录中自动生成优才分数、优才 Must、高才路径、专才路径和顾问结论。

## 飞书 Base 配置

- Base：`香港人才入境初筛MVP`
- 第一层客户填写：`01客户填写表单` (`vewQhpciTx`)，真实客户填写链接为 `/share/base/shrcnra78TjubSWw2qhtoezeVtg`
- H5客户双栏页：左侧嵌入飞书填写表单，右侧展示优才/高才/专才要求；表单提交仍走飞书原生表单
- 第二层结果展示：`02结果展示` (`vewFkdrgin`)
- 第三层要求和匹配：`03官方要求和匹配表` (`tblPRC70YB6P51uy`)，包含客户可查看的 `客户查看-三类要求`、`客户查看-优才要求`、`客户查看-高才要求`、`客户查看-专才要求`
- 第四层记录：`04提交记录` (`vew4mXnH6v`)
- 表单共享权限：`shared=true`，`shared_limit=anyone_editable`，不限制重复提交
- 结果字段：`优才综合分`、`优才Must`、`优才结果`、`高才路径`、`专才路径`、`顾问结论`
- 后台视图：`优才达标`、`高才匹配`、`专才匹配`、`需人工跟进`
- 表单题目：30 个业务字段；已移除飞书默认空白题，主字段调整为 `姓名/编号`
- 真实表单提交测试：`客户提交测试C`，结果为 `优才:未达(2/12); 高才:A类; 专才:ASMTP匹配`

## 规则口径

- 优才年龄超过50岁不直接否决，只是不拿“50岁或以下”这一项。
- 合资格大学命中后只自动确认“在清单内”，仍需人工核验：
  - 学位由清单内大学正式授予。
  - 不属于继续教育学院、分校、附属学院等不被接纳来源。
  - 联合学位需核验所有授予院校。
- 专才年薪总包 HK$200万或人才清单岗位，只免本地招聘困难证明，不免 offer、岗位真实、岗位相关、薪酬市场水平等条件。

## 官方来源

- 优才 QMAS：https://www.immd.gov.hk/eng/faq/QMAS.html
- 高才 TTPS：https://www.immd.gov.hk/eng/faq/TTPS.html
- 专才 GEP：https://www.immd.gov.hk/eng/services/visas/GEP.html
- 内地专才 ASMTP：https://www.immd.gov.hk/eng/services/visas/ASMTP.html
- 合资格大学清单：https://www.hkengage.gov.hk/en/how-to-apply-for-a-visa/admission-scheme-matching-tool-institutions/

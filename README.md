# GitHub Pages 根域名入口

发布仓库：`zuxiong-luo/zuxiong-luo.github.io`。

作用：访问 `https://zuxiong-luo.github.io/` 时进入现有 `https://zuxiong-luo.github.io/fullstack-atlas/#home`。根站点未找到的路径也通过404.html返回首页。

GitHub Pages 设置：Deploy from a branch → main → /(root)。`.nojekyll` 表示按普通静态文件发布，不需要依赖安装、Node构建或额外工作流。

JavaScript使用location.replace避免返回按钮反复回到跳转入口；HTML的meta refresh提供脚本禁用时的自动跳转，并始终保留手动首页链接。目标固定，不转发查询参数、不从用户输入拼接外站地址。

这是浏览器跳转页，根路径本身返回200；未知路径的404响应在浏览器中跳转，不是服务器301/302规则。当前主站仓库、评论、内容、登录与离线服务均保持独立。

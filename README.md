# obsidian_notes

关于Obsidian安装后无法使用社区插件问题：
大概率是由于DNS解析异常导致
处理方案：
修改hosts文件 
手动查询域名解析地址后插入hosts文件
域名：raw.githubusercontent.com
示例：
140.82.113.3      github.com
140.82.114.20     gist.github.com
 
151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
199.232.28.133     raw.githubusercontent.com 
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
199.232.96.133     avatars.githubusercontent.com


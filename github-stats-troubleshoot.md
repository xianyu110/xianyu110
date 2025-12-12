# GitHub Stats 故障排除指南

## 问题诊断

### 1. 检查仓库状态
- [ ] 确认仓库是公开的（Public）
- [ ] 确认用户名 `xianyu110` 是正确的

### 2. 验证 GitHub Stats 服务状态
访问以下链接检查服务是否正常：
- GitHub Stats API: https://github-readme-stats.vercel.app/api?username=xianyu110
- Top Languages API: https://github-readme-stats.vercel.app/api/top-langs/?username=xianyu110

### 3. 常见解决方案

#### 方案1：清除缓存
在URL后添加时间戳参数来绕过缓存：
```
?username=xianyu110&show_icons=true&theme=tokyonight&t=1234567890
```

#### 方案2：使用备用服务
如果Vercel服务不可用，可以使用其他服务：
- GitHub Profile Summary Cards: https://github-profile-summary-cards.vercel.app/
- GitHub Activity: https://github.com/ashutosh00710/github-readme-activity-graph

#### 方案3：检查网络连接
- 确认能够访问 `vercel.app` 域名
- 检查防火墙或代理设置

### 4. 替代配置

如果上述方案都无效，可以使用以下替代配置：

```markdown
<!-- 使用GitHub Profile Summary Cards -->
<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=xianyu110&theme=tokyonight" />

<!-- 使用GitHub Activity Graph -->
<img src="https://github-readme-activity-graph.vercel.app/graph?username=xianyu110&theme=react-dark" />
```

### 5. 手动刷新步骤

1. 提交并推送当前的README更改
2. 访问GitHub仓库页面
3. 硬刷新页面（Ctrl+F5 或 Cmd+Shift+R）
4. 清除浏览器缓存后再次查看

## 联系支持

如果问题持续存在，请：
1. 查看Vercel状态页面：https://www.vercel-status.com/
2. 在GitHub Issues中搜索相关问题：https://github.com/anuraghazra/github-readme-stats/issues
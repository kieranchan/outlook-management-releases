# Release Checklist / 发版清单

## 中文

### 发版前
- 确认新版与经典版均可启动
- 确认关键功能可用：登录、Token 刷新、邮件拉取、详情查看
- 确认主题、下拉框、分栏布局、窗口缩放无明显异常
- 重新打包 zip 成品
- 按 `RELEASE_NAMING.md` 统一命名文件
- 生成并核对 SHA256
- 更新 `README.md`
- 更新 `RELEASE_NOTES.md`
- 更新 `SHA256SUMS.txt`

### 发布时
- 创建新的 Git tag，例如 `v1.0.1`
- 创建 GitHub Release
- 上传新版与经典版 zip 附件
- 检查 Release 页面展示是否正常
- 检查附件文件名、大小、校验值是否正确

### 发布后
- 本地下载一次附件做回归检查
- 检查 `releases/latest` 是否可正常访问
- 确认 `latest` 已指向最新非草稿版本
- 对外分享 Release 链接，而不是源码仓库链接

---

## English

### Before release
- Confirm both modern and classic editions start correctly
- Verify critical flows: sign-in, token refresh, mail fetching, and detail view
- Check themes, dropdowns, split layout, and window resizing
- Rebuild packaged zip artifacts
- Rename files according to `RELEASE_NAMING.md`
- Generate and verify SHA256 checksums
- Update `README.md`
- Update `RELEASE_NOTES.md`
- Update `SHA256SUMS.txt`

### During release
- Create a new Git tag, for example `v1.0.1`
- Create a GitHub Release
- Upload both modern and classic zip assets
- Verify the Release page renders correctly
- Verify asset names, sizes, and checksums

### After release
- Download the assets once locally for a quick regression check
- Verify `releases/latest` is accessible
- Confirm `latest` points to the newest non-draft release
- Share the Release link publicly instead of the source repository link

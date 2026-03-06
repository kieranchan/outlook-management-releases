# Release Workflow / latest 发布流程

## 中文

### 目标
每次发版后，以下地址应始终可用：
- `https://github.com/kieranchan/outlook-management-releases/releases/latest`

### 推荐流程
1. 打包两个成品：新版与经典版。
2. 按命名规范重命名 zip 文件。
3. 重新生成 `SHA256SUMS.txt`。
4. 更新 `RELEASE_NOTES.md` 中的新版本内容。
5. 创建新的 GitHub Release，例如 `v1.0.1`。
6. 上传两个 zip 作为 Release 附件。
7. 打开 `releases/latest` 检查是否已指向新版本。
8. 再下载一次附件做完整性和启动检查。

### 关键原则
- `latest` 不需要单独维护，它会自动指向最新发布的非草稿版本。
- 不要把 zip 直接提交到 git 历史中，只作为 Release 附件上传。
- 如果只是测试，请先用 draft，确认后再发布。

### 建议命令
```powershell
gh release create v1.0.1 --repo kieranchan/outlook-management-releases --title "Outlook Management v1.0.1" --notes-file RELEASE_NOTES.md

gh release upload v1.0.1 "releases/outlook-management-modern-win64-20260306.zip" --repo kieranchan/outlook-management-releases

gh release upload v1.0.1 "releases/outlook-management-classic-win64-20260306.zip" --repo kieranchan/outlook-management-releases
```

---

## English

### Goal
After each release, this URL should remain valid:
- `https://github.com/kieranchan/outlook-management-releases/releases/latest`

### Recommended flow
1. Build both packaged editions: modern and classic.
2. Rename the zip files according to the naming rules.
3. Regenerate `SHA256SUMS.txt`.
4. Update the new version notes in `RELEASE_NOTES.md`.
5. Create a new GitHub Release, for example `v1.0.1`.
6. Upload both zip files as Release assets.
7. Open `releases/latest` and verify it points to the new version.
8. Download the assets once and do a quick integrity and startup check.

### Key rules
- `latest` does not need separate maintenance; it automatically points to the newest published non-draft release.
- Do not commit zip files into git history; upload them only as Release assets.
- If the release is still under verification, create it as a draft first and publish it after checks pass.

### Suggested commands
```powershell
gh release create v1.0.1 --repo kieranchan/outlook-management-releases --title "Outlook Management v1.0.1" --notes-file RELEASE_NOTES.md

gh release upload v1.0.1 "releases/outlook-management-modern-win64-20260306.zip" --repo kieranchan/outlook-management-releases

gh release upload v1.0.1 "releases/outlook-management-classic-win64-20260306.zip" --repo kieranchan/outlook-management-releases
```

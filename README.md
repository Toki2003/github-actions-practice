# 使用 GitHub Actions 实现自动化测试

对应《开源软件构建技术》第5章第26–35页实践项目1，用于课程实践作业4。

## 本地运行

```sh
python -m pip install -r requirements.txt
python -m pytest -v
```

## 按课件完成平台实践

1. 在自己的GitHub账号中创建公开仓库，例如 github-actions-practice。
2. 将本目录内容上传至仓库根目录。必须包含 `.github/workflows/ci.yml`，不要多嵌套一层目录。
3. 在Actions页面查看“Python单元测试”，保存首次成功运行的截图和日志。
4. 将calculator.py中add函数的 `return a + b` 临时改成 `return a * b`，提交修改。
5. 查看失败运行；test_add中add(2, 3)实际得到6，预期为5。保存失败截图和日志。
6. 恢复 `return a + b` 并提交，确保最后一次运行成功，保存恢复后的截图。
7. 在头歌课程对应任务中提交公开仓库链接，并查看测评结果。

## 报告所需证据

- 公开仓库地址及文件结构。
- 工作流配置及四个执行阶段。
- 正常、故障、修复后三次运行的链接、状态及对应提交。
- 失败断言与原因分析。
- 头歌测评结果。

本地测试通过不能替代GitHub Actions运行成功，也不能代替头歌测评。

## Toki2003 上传步骤

1. 登录 https://github.com/new ，确认Owner为Toki2003，仓库名填写github-actions-practice，选择Public，点击Create repository。若同名仓库已存在，请另取新名称，不要覆盖已有项目。
2. 解压上传包，进入github-actions-practice目录，将calculator.py、test_calculator.py、requirements.txt、README.md上传到仓库根目录并提交。不要将ZIP文件本身上传作为项目代码。
3. 为避免隐藏目录漏传，在仓库点击Add file → Create new file，文件名输入.github/workflows/ci.yml，将本地同路径ci.yml内容完整复制进去并提交。缩进保持不变。
4. 点击Actions查看运行。成功后按上述故障实验步骤修改add函数、提交并查看失败，再恢复正确代码并确认最终成功。
5. 若使用建议名称，仓库地址应为https://github.com/Toki2003/github-actions-practice；此处仅为预期地址，尚未创建或验证。

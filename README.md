# Steam maFile 批量筛选工具

根据账号列表递归查找 maFile 文件，将匹配结果复制到源目录旁的时间戳文件夹。界面使用 Python Tkinter，当前“打开文件夹”功能使用 Windows 的 `os.startfile`。

## 安装与运行

```bash
git clone https://github.com/Lucian-Wang/Steam-maFile-filter.git
cd Steam-maFile-filter
python mafile_filter_gui.py
```

需要 Python 3 和 Tkinter；代码仅使用标准库，无需安装 requirements.txt。旧二进制已移除，请按源码运行或自行打包。

## 使用

1. 选择包含 maFile 文件的源目录。
2. 粘贴账号列表，每行支持账号、`账号:密码`、`账号--密码` 或 `账号----密码`；只取账号部分。
3. 点击“筛选复制”，查看匹配和未匹配记录。
4. 结果保存到源目录同级的 `maFileYYYYMMDD_HHMMSS` 文件夹，不移动源文件。

仅处理文件名为英文字母或数字加 `.maFile` / `.json` 的文件；带括号等其他字符的文件名会跳过。程序读取 JSON 的 `account_name` 并按账号去重，每个账号只复制第一份匹配文件。

## 维护与反馈

维护者：[Lucian](https://lucian.wang/) · 邮箱：im@lucian.wang · [问题反馈](https://github.com/Lucian-Wang/Steam-maFile-filter/issues)

## 许可说明

原 README 声明 MIT License；当前仓库未包含独立 LICENSE 文件。

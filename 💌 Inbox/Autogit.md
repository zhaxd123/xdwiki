``` bat
@echo off
setlocal

:: 设置 Git 仓库目录（修改为你实际的目录）
set REPO_DIR=C:\Users\zhangxiaodong\Documents\documents\Notebook\xdwiki

:: 进入 Git 仓库目录
cd /d "%REPO_DIR%"
if %ERRORLEVEL% neq 0 (
    echo Failed to access dir: %REPO_DIR%
    exit /b 1
)

:: 添加所有更改
echo RUN GIT ADD.
git add .
if %ERRORLEVEL% neq 0 (
    echo Failed to GIT ADD.
    exit /b 1
)

:: 提交更改
echo RUN GIT COMMIT.
git commit -a -m "update"
if %ERRORLEVEL% neq 0 (
    echo Failed to GIT COMMIT.
    exit /b 1
)

:: 推送到远程仓库
echo RUN GIT PUSH.
git push origin main
if %ERRORLEVEL% neq 0 (
    echo Failed to GIT PUSH.
    exit /b 1
)

echo Git commit success！
exit /b 0
```
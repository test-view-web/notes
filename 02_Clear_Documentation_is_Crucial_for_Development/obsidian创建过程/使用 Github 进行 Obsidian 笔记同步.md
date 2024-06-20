> 阅读需要 git 基础
### 在 Windows 中使用
1. 安装 Obsidian Git（第三方插件） 和 git
2. 配置环境
	在安装好 obsidian git 后，进入其设置界面的最上方会提示当前 git 的配置情况，如果没有配置成功远程仓库 或者初始化 git ，会显示 “not already” 且没有 Automatic 选项，当配置成功后，会显示 “Automatic”
	Obsidian 需要使用 git command，如果git的环境变量‘PATH’没有配置正确，在打开 Obsidian 时会在右上角报错"cannot use git command"

3. 在 Automatic 中设置自动推送（push）时间和自动 拉取（pull）时间
![[Pasted image 20231201200010.png|插件设置界面]]


### 在 Android 中使用

1. 安装 Obsidian Git 
2. 安装 Termux
	Termux 是一个 Android 终端仿真应用程序，用于在 Android 手机上搭建一个完整的 Linux 环境。 不需要 root 权限 Termux 就可以正常运行。Termux 基本实现 Linux 下的许多基本操作。因此，我们同样可以通过termux使用git将项目提交到github。[Termux 官网](https://termux.com)

3. 在 Termux 中安装 git
	安装git工具包的命令是 `pkg install git -y` 但是直接安装会 由于使用的镜像源存在问题或者网络连接不稳定导致 仓库签名验证的问题，产生报错信息``Err:1 https://deb.kcubeterm.me/termux-main stable InRelease Clearsigned file isn't valid, got 'NOSPLIT' (does the network require authentication?) Reading package lists... Done E: Failed to fetch https://deb.kcubeterm.me/termux-main/dists/stable/InRelease Clearsigned file isn't valid, got 'NOSPLIT' (does the network require authentication?) E: The repository 'https://deb.kcubeterm.me/termux-main stable InRelease' is not signed. N: Metadata integrity can't be verified, repository is disabled now. N: Possible causes: unstable or tampered Internet connection, wrong sources.list, outdated keyring or host is down currently. N: Please note that all hosting problems or other serious issues we announce on our social media pages. N: Use termux-change-repo for switching to a mirror.``使用 Termux 提供的 `termux-change-repo` 工具来切换到其他镜像源。以下是一些步骤：
	1.  运行以下命令来切换到默认的 Termux 镜像源：`termux-change-repo`
	2. 然后尝试再次安装 Git：`pkg install git -y`

4. 初始化 git 的准备工作
	1. Termux 的安装过程中不会出现权限索取，但是使用 `ls`等 linux 命令需要读取存储权限， 要手动在应用管理中赋予读取权限
	2. 需要在合适位置建立一个空的文件夹来 拉取（pull） 远程仓库


5. 初始化 git 
	1. 运行 `git init -b main`, 命令 `git init -b main` 的目的是在 Git 仓库中初始化一个新的分支，并将其命名为 `main`。
		1. 该命令执行两个主要任务：
		2. **初始化仓库**: `git init` 用于在当前目录中创建一个新的 Git 仓库。如果该目录尚未是 Git 仓库，此命令将创建一个新的仓库。
		3. **创建默认分支**: `-b main` 的作用是在初始化仓库时创建一个名为 `main` 的默认分支。在 Git 的新版本中，为了更好地反映多样性，主分支的名称已从 `master` 更改为 `main`。这个命令确保新创建的仓库使用 `main` 作为默认分支。
		 请注意，这个命令需要在 Git 2.28.0 或更高版本中使用，因为在这个版本之前，并没有直接支持 `-b` 选项来指定初始化时的默认分支。在执行完这个命令后，你的当前目录将成为一个新的 Git 仓库，初始提交将被创建在 `main` 分支上。你可以通过运行 `git branch` 命令来查看当前分支。
	2. 运行 `git remote add origin https://github.com/username/repo_name.git`
		1.
		  在你运行 `git remote add origin` 命令时，Git 会检测到一个问题，提示有可疑的所有权问题。这可能是由于安全性或权限设置引起的。
			根据错误信息，Git 建议你在这个目录上添加一个安全目录的例外情况。你可以按照提供的建议运行以下命令：
			`git config --global --add safe.directory /storage/emulated/0/your_path`
			这个命令将在全局配置中添加一个例外，允许 Git 在 `/storage/emulated/0/velseine` 目录下操作而不再提示错误。
			在这之后，再次运行 `git remote add origin` 命令，应该就不再遇到相同的问题了。确保你有足够的权限访问这个目录，并且已经正确地配置了 Git。
		2.
		  GitHub 移除了使用用户名和密码进行 HTTPS 认证的支持，这可能导致在使用 `git pull` 时出现身份验证失败的问题。现在，GitHub 鼓励使用个人访问令牌（Personal Access Token）进行认证。
			所以再次运行时需要输入你的 GitHub 用户名，但在密码部分输入你生成的个人访问令牌。
	3. 拉取远程仓库的主分支（例如，main 分支）`git pull origin main`


6. 配置 Obsidian Git ，在成功 pull 远程仓库后，意味着 git 配置成功，可以在 Obsidian Git 中配置 push 用户和 邮箱了，当用户设置好后可以在 obsidian 应用中下滑调出命令面板，输入 git 相关命令使用





插件官方的说明文档：<https://publish.obsidian.md/git-doc/Getting+Started >
插件作者在obsidian讨论区的帖子：<https://forum.obsidian.md/t/obsidian-git-plugin-for-automatic-vault-backup-with-git/7790 >
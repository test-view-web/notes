#### 脚手架工具
脚手架工具是一种用于自动化项目搭建和初始化的工具，它可以帮助开发者快速创建项目的基本结构、文件和配置，从而加速项目的启动和开发过程。脚手架工具通常包含了一系列的命令行命令，这些命令可以执行诸如创建文件、安装依赖、运行测试等任务。
脚手架工具的主要目标是：

1. **提供标准化的项目结构：** 脚手架工具定义了一个标准的项目结构，包括目录、文件和配置，使得开发者能够更容易理解和维护项目。
    
2. **简化初始化过程：** 通过脚手架工具，开发者无需手动创建项目的初始结构，而是可以通过运行一个命令来快速初始化一个新项目。
    
3. **自动化配置和依赖管理：** 脚手架工具可以自动配置项目所需的各种设置，并管理项目所依赖的库和工具的安装。
    
4. **提供命令行接口：** 脚手架工具通常以命令行方式提供接口，通过命令行可以执行各种任务，如创建组件、启动开发服务器、运行测试等。
    
5. **支持插件扩展：** 一些脚手架工具允许开发者通过插件机制扩展其功能，以满足特定项目或团队的需求。
常见的脚手架工具包括：

- **Create React App:** 用于创建React项目的官方脚手架工具，快速搭建React应用的基本结构。
    
- **Angular CLI:** 用于Angular项目的官方脚手架工具，简化了Angular应用的开发、构建和测试流程。
    
- **Vue CLI:** 用于Vue.js项目的官方脚手架工具，提供了一套可配置的项目脚手架。
    
- **Express Generator:** Express框架的脚手架工具，用于创建Node.js应用的基本结构。

#### 使用脚手架工具
使用 Create React App (CRA) 可以按照以下步骤进行：

1. **安装 Node.js 和 npm：** 确保在你的计算机上安装了 Node.js 和 npm（Node 包管理器）。你可以从官方网站下载并安装它们：[Node.js](https://nodejs.org/)。
    
2. **安装 Create React App:** 打开终端或命令提示符，并运行以下命令以全局安装 Create React App：

    
    `npm install -g create-react-app`
    
3. **创建新的 React 应用:** 在安装 Create React App 后，你可以使用以下命令创建一个新的 React 应用。将 "my-react-app" 替换为你项目的名称：
    

    
    `npx create-react-app my-react-app`
    
```bash
    npx create-react-app my-app --template typescript //创建使用typescript的react项目
```
    
    这个命令将使用基本的项目结构和开发设置初始化一个新的 React 应用。
    
4. **切换到项目目录:** 进入新创建的项目目录：
    

    
    `cd my-react-app`
    
5. **启动开发服务器:** 进入项目目录后，你可以使用以下命令启动开发服务器：
    

    
    `npm start`
    
    这将启动开发服务器，你可以在浏览器中访问 `http://localhost:3000` 来查看你的 React 应用。
    
6. **探索项目:** 在你喜欢的代码编辑器中打开项目（例如 Visual Studio Code）并探索文件和文件夹。`src` 目录包含主要的 React 组件，而 `public` 目录包含静态资源。
    
7. **构建生产版本:** 当你准备部署你的应用时，可以使用以下命令创建生产版本：
    

    
    `npm run build`
    
    这个命令会在 `build` 目录中生成经过优化和缩小的适用于生产环境的文件。
    
8. **其他命令:** 探索项目的 `package.json` 文件中的 `scripts` 部分中的其他可用命令。这些命令包括测试、eject（弹出配置）等。
    

    
    `"scripts": {   "start": "react-scripts start",   "build": "react-scripts build",   "test": "react-scripts test",   "eject": "react-scripts eject" }`
    

就是这样！你现在已经使用 Create React App 设置了一个新的 React 应用。你可以根据项目的需求开始构建和定制你的应用。

public 下的 index.html 是 html 主文件
![[Pasted image 20231231225243.png|root节点为程序主入口]]

不推荐把 样式文件 和 JavaScript 文件放到 public 文件夹

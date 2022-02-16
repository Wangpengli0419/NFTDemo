# 👨‍🎓 Nasus Build NFT DEMO

## 🎟 NFT Example 🤓

在线预览：[🔗 https://nasus.surge.sh/](https://nasus.surge.sh/)

OpenSea 测试网：[🔗 OpenSea](https://testnets.opensea.io/collection/yourcollectible-5gehed8pkm)

合约地址：[🔗 https://rinkeby.etherscan.io/token/0xcd504daa3f87f2de952625ff7bcb549ebdc61e57](https://rinkeby.etherscan.io/token/0xcd504daa3f87f2de952625ff7bcb549ebdc61e57)

🎫 本项目基于 [👷‍♀️ HardHat](https://hardhat.org/getting-started/) 编译并且部署智能合约.

基于 React 来编写前端界面.

🏆 最终我们的项目会发布到[👷‍♀️ OpenSea](https://testnets.opensea.io/collection/yourcollectible-5gehed8pkm)，欢迎分享给朋友们体验 🚀

---

# 步骤 1: 📦 安装依赖 📚

环境准备:

- [Git](https://git-scm.com/downloads)
- [Node](https://nodejs.org/dist/latest-v12.x/)
- [Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable)

(⚠️ 确保安装 npm 包 `npm i -g yarn` 而不是 linux package `yarn`)

```sh
git clone git@github.com:Wangpengli0419/NFTDemo.git
```

> 安装依赖并启动 HardHat 本地测试环境:

```sh
cd NFTDemo
yarn install
yarn chain
```

> 打开第二个命令行窗口 🛰 部署本地合约

```sh
cd NFTDemo
yarn deploy
```

> 打开第三个命令行窗口并启动前端 📱 :

```sh
cd NFTDemo
yarn start
```

> 执行 `yarn deploy --reset` 部署一个新的本地合约.

📱 打开 http://localhost:3000 预览前端项目

---

# 步骤 2: ⛽️ Gas & Wallets 👛

> ⛽️ 从水龙头获取 Gas。

![image](https://user-images.githubusercontent.com/2653167/142483294-ff4c305c-0f5e-4099-8c7d-11c142cb688c.png)

> 🦊 **不要** 连接 MetaMask. 如果你已经连接了 MetaMask,请点击 **logout**:

![image](https://user-images.githubusercontent.com/2653167/142484483-1439d925-8cef-4b1a-a4b2-0f022eebc0f6.png)

> 🔥 本地开发请使用 **burner wallets** 连接钱包

> 👛 **burner wallets**打开一个新的匿名窗口地址栏导航至 http://localhost:3000.右上角有一个新的钱包地址。复制匿名浏览器的地址，并从第一个浏览器向其发送测试资金：

![image](https://user-images.githubusercontent.com/2653167/142483685-d5c6a153-da93-47fa-8caa-a425edba10c8.png)

> 👨🏻‍🚒 关闭“匿名”窗口时，帐户将永远丢失。本地开发使用 Burner 钱包非常方便，但发布公共网络时，我们会连接其他的钱包。

---

# 步骤 3: 🖨 Mint

> ✏️ Mint NFTs! 点击 `MINT NFT` 按钮.

👀 如下图所示:

![nft3](https://user-images.githubusercontent.com/526558/124386983-48965300-dcb3-11eb-88a7-e88ad6307976.png)

👛 打开一个新的 **匿名窗口** 导航至 http://localhost:3000

🎟 给匿名窗口的地址发送一个 NFT.

👀 如下图所示:

![nft5](https://user-images.githubusercontent.com/526558/124387008-58ae3280-dcb3-11eb-920d-07b6118f1ab2.png)

👛 尝试在 **匿名窗口** Mint Nft.

> 你能在这个地址没有资金的情况下造出 NFT 吗？不能！！ 需要先从水龙头获取 Gas ！

🔏 NFT 智能合约逻辑 `YourCollectible.sol` 在 `packages/hardhat-ts/contracts` 目录.

💼 部署合约逻辑 `00_deploy_your_collectible.ts` 在 `packages/hardhat-ts/deploy`目录.

📝 前端逻辑入口 `YourCollectible.tsx` 在 `packages/vite-app-ts/src/components/pages/your-collectible` 目录.

---

# 步骤 4: 💾 部署到测试网! 🛰

> 在 `packages/hardhat-ts/hardhat.config.ts` 42 行 `defaultNetwork`修改为 `rinkeby`

🔐 使用 `yarn generate`生成一个 **部署合约地址**

![nft7](https://user-images.githubusercontent.com/526558/124387064-7d0a0f00-dcb3-11eb-9d0c-195f93547fb9.png)

👛 使用 `yarn account` 查看生成的 **部署合约地址**

![nft8](https://user-images.githubusercontent.com/526558/124387068-8004ff80-dcb3-11eb-9d0f-43fba2b3b791.png)

⛽️ 水龙头 [faucet.paradigm.xyz](https://faucet.paradigm.xyz/) 获取测试币 **deployer address**.

🚀 部署 NFT 智能合约:

```sh
yarn deploy
```

> 💬 提示: 你可以将`hardhat.config.ts`的`defaultNetwork`修改为`Rinkeby` 也可以使用命令行 `yarn deploy --network Rinkeby`.

---

# 步骤 5: 🚢 启动! 🚁

> ✏️ (目录 `packages/vite-app-ts/src/config`) 修改 `providersConfig.ts` 第 15 行 `targetNetworkInfo` 为你要部署的测试网络

![image](https://user-images.githubusercontent.com/46639943/149599234-55921640-e677-42ca-a4a7-ab1fbca36ec4.png)

能够在前端看到正确的网络 (http://localhost:3000):

![nft10](https://user-images.githubusercontent.com/526558/124387099-9a3edd80-dcb3-11eb-9a57-54a7d370589a.png)

🎫 点击 `MINT NFT` 按钮进行 mint .

![nft11](https://user-images.githubusercontent.com/526558/124387132-b04c9e00-dcb3-11eb-95d1-03b8c272e52f.png)

# 步骤 6: 📜 开源区块链浏览器的合约

将在[etherscan.io](https://etherscan.io/myapikey)申请到的 `api-key` 替换到`packages/hardhat-ts/package.json` 20 行 `verify`命令.

![Screen Shot 2021-11-30 at 10 21 01 AM](https://user-images.githubusercontent.com/9419140/144075208-c50b70aa-345f-4e36-81d6-becaa5f74857.png)

> 使用命令 `yarn verify --network your_network` 在[etherscan.io](https://etherscan.io)提交开源合约 🛰

---

## 🐟 Open Sea

> 将我们的 NFT 项目添加至 OpenSea ( create -> submit NFTs -> "or add an existing contract")

## 🔶 Infura

> 你需要从 [infura.io](https://infura.io)申请自己的 apikey 并且替换到目录 `packages/vite-app-ts/src/models/constants`下`constants.ts`第 2 行:

![nft13](https://user-images.githubusercontent.com/526558/124387174-d83c0180-dcb3-11eb-989e-d58ba15d26db.png)

---

# 恭喜完成 🎉!

📦 构建前端:

```sh
yarn build
```

💽 将前端托管至 surge:

```sh
yarn surge
```

> 🎖 浏览器输入 托管好的 surge 地址 👩‍❤️‍👨 并分享给朋友们，也可以赠送朋友们 NFT🎖

---

![nft15](https://user-images.githubusercontent.com/526558/124387205-00c3fb80-dcb4-11eb-9e2f-29585e323037.gif)

---

> 🏃 本项目基于 [here](https://speedrunethereum.com).

# ð¨âð Nasus Build NFT DEMO

## ð NFT Example ð¤

å¨çº¿é¢è§ï¼[ð https://nasus.surge.sh/](https://nasus.surge.sh/)

OpenSea æµè¯ç½ï¼[ð OpenSea](https://testnets.opensea.io/collection/yourcollectible-5gehed8pkm)

åçº¦å°åï¼[ð https://rinkeby.etherscan.io/token/0xcd504daa3f87f2de952625ff7bcb549ebdc61e57](https://rinkeby.etherscan.io/token/0xcd504daa3f87f2de952625ff7bcb549ebdc61e57)

ð« æ¬é¡¹ç®åºäº [ð·ââï¸ HardHat](https://hardhat.org/getting-started/) ç¼è¯å¹¶ä¸é¨ç½²æºè½åçº¦.

åºäº React æ¥ç¼ååç«¯çé¢.

ð æç»æä»¬çé¡¹ç®ä¼åå¸å°[ð·ââï¸ OpenSea](https://testnets.opensea.io/collection/yourcollectible-5gehed8pkm)ï¼æ¬¢è¿åäº«ç»æåä»¬ä½éª ð

---

# æ­¥éª¤ 1: ð¦ å®è£ä¾èµ ð

ç¯å¢åå¤:

- [Git](https://git-scm.com/downloads)
- [Node](https://nodejs.org/dist/latest-v12.x/)
- [Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable)

(â ï¸ ç¡®ä¿å®è£ npm å `npm i -g yarn` èä¸æ¯ linux package `yarn`)

```sh
git clone git@github.com:Wangpengli0419/NFTDemo.git
```

> å®è£ä¾èµå¹¶å¯å¨ HardHat æ¬å°æµè¯ç¯å¢:

```sh
cd NFTDemo
yarn install
yarn chain
```

> æå¼ç¬¬äºä¸ªå½ä»¤è¡çªå£ ð° é¨ç½²æ¬å°åçº¦

```sh
cd NFTDemo
yarn deploy
```

> æå¼ç¬¬ä¸ä¸ªå½ä»¤è¡çªå£å¹¶å¯å¨åç«¯ ð± :

```sh
cd NFTDemo
yarn start
```

> æ§è¡ `yarn deploy --reset` é¨ç½²ä¸ä¸ªæ°çæ¬å°åçº¦.

ð± æå¼ http://localhost:3000 é¢è§åç«¯é¡¹ç®

---

# æ­¥éª¤ 2: â½ï¸ Gas & Wallets ð

> â½ï¸ ä»æ°´é¾å¤´è·å Gasã

![image](https://user-images.githubusercontent.com/2653167/142483294-ff4c305c-0f5e-4099-8c7d-11c142cb688c.png)

> ð¦ **ä¸è¦** è¿æ¥ MetaMask. å¦æä½ å·²ç»è¿æ¥äº MetaMask,è¯·ç¹å» **logout**:

![image](https://user-images.githubusercontent.com/2653167/142484483-1439d925-8cef-4b1a-a4b2-0f022eebc0f6.png)

> ð¥ æ¬å°å¼åè¯·ä½¿ç¨ **burner wallets** è¿æ¥é±å

> ð **burner wallets**æå¼ä¸ä¸ªæ°çå¿åçªå£å°åæ å¯¼èªè³ http://localhost:3000.å³ä¸è§æä¸ä¸ªæ°çé±åå°åãå¤å¶å¿åæµè§å¨çå°åï¼å¹¶ä»ç¬¬ä¸ä¸ªæµè§å¨åå¶åéæµè¯èµéï¼

![image](https://user-images.githubusercontent.com/2653167/142483685-d5c6a153-da93-47fa-8caa-a425edba10c8.png)

> ð¨ð»âð å³é­âå¿åâçªå£æ¶ï¼å¸æ·å°æ°¸è¿ä¸¢å¤±ãæ¬å°å¼åä½¿ç¨ Burner é±åéå¸¸æ¹ä¾¿ï¼ä½åå¸å¬å±ç½ç»æ¶ï¼æä»¬ä¼è¿æ¥å¶ä»çé±åã

---

# æ­¥éª¤ 3: ð¨ Mint

> âï¸ Mint NFTs! ç¹å» `MINT NFT` æé®.

ð å¦ä¸å¾æç¤º:

![nft3](https://user-images.githubusercontent.com/526558/124386983-48965300-dcb3-11eb-88a7-e88ad6307976.png)

ð æå¼ä¸ä¸ªæ°ç **å¿åçªå£** å¯¼èªè³ http://localhost:3000

ð ç»å¿åçªå£çå°ååéä¸ä¸ª NFT.

ð å¦ä¸å¾æç¤º:

![nft5](https://user-images.githubusercontent.com/526558/124387008-58ae3280-dcb3-11eb-920d-07b6118f1ab2.png)

ð å°è¯å¨ **å¿åçªå£** Mint Nft.

> ä½ è½å¨è¿ä¸ªå°åæ²¡æèµéçæåµä¸é åº NFT åï¼ä¸è½ï¼ï¼ éè¦åä»æ°´é¾å¤´è·å Gas ï¼

ð NFT æºè½åçº¦é»è¾ `YourCollectible.sol` å¨ `packages/hardhat-ts/contracts` ç®å½.

ð¼ é¨ç½²åçº¦é»è¾ `00_deploy_your_collectible.ts` å¨ `packages/hardhat-ts/deploy`ç®å½.

ð åç«¯é»è¾å¥å£ `YourCollectible.tsx` å¨ `packages/vite-app-ts/src/components/pages/your-collectible` ç®å½.

---

# æ­¥éª¤ 4: ð¾ é¨ç½²å°æµè¯ç½! ð°

> å¨ `packages/hardhat-ts/hardhat.config.ts` 42 è¡ `defaultNetwork`ä¿®æ¹ä¸º `rinkeby`

ð ä½¿ç¨ `yarn generate`çæä¸ä¸ª **é¨ç½²åçº¦å°å**

![nft7](https://user-images.githubusercontent.com/526558/124387064-7d0a0f00-dcb3-11eb-9d0c-195f93547fb9.png)

ð ä½¿ç¨ `yarn account` æ¥ççæç **é¨ç½²åçº¦å°å**

![nft8](https://user-images.githubusercontent.com/526558/124387068-8004ff80-dcb3-11eb-9d0f-43fba2b3b791.png)

â½ï¸ æ°´é¾å¤´ [faucet.paradigm.xyz](https://faucet.paradigm.xyz/) è·åæµè¯å¸ **deployer address**.

ð é¨ç½² NFT æºè½åçº¦:

```sh
yarn deploy
```

> ð¬ æç¤º: ä½ å¯ä»¥å°`hardhat.config.ts`ç`defaultNetwork`ä¿®æ¹ä¸º`Rinkeby` ä¹å¯ä»¥ä½¿ç¨å½ä»¤è¡ `yarn deploy --network Rinkeby`.

---

# æ­¥éª¤ 5: ð¢ å¯å¨! ð

> âï¸ (ç®å½ `packages/vite-app-ts/src/config`) ä¿®æ¹ `providersConfig.ts` ç¬¬ 15 è¡ `targetNetworkInfo` ä¸ºä½ è¦é¨ç½²çæµè¯ç½ç»

![image](https://user-images.githubusercontent.com/46639943/149599234-55921640-e677-42ca-a4a7-ab1fbca36ec4.png)

è½å¤å¨åç«¯çå°æ­£ç¡®çç½ç» (http://localhost:3000):

![nft10](https://user-images.githubusercontent.com/526558/124387099-9a3edd80-dcb3-11eb-9a57-54a7d370589a.png)

ð« ç¹å» `MINT NFT` æé®è¿è¡ mint .

![nft11](https://user-images.githubusercontent.com/526558/124387132-b04c9e00-dcb3-11eb-95d1-03b8c272e52f.png)

# æ­¥éª¤ 6: ð å¼æºåºåé¾æµè§å¨çåçº¦

å°å¨[etherscan.io](https://etherscan.io/myapikey)ç³è¯·å°ç `api-key` æ¿æ¢å°`packages/hardhat-ts/package.json` 20 è¡ `verify`å½ä»¤.

![Screen Shot 2021-11-30 at 10 21 01 AM](https://user-images.githubusercontent.com/9419140/144075208-c50b70aa-345f-4e36-81d6-becaa5f74857.png)

> ä½¿ç¨å½ä»¤ `yarn verify --network your_network` å¨[etherscan.io](https://etherscan.io)æäº¤å¼æºåçº¦ ð°

---

## ð Open Sea

> å°æä»¬ç NFT é¡¹ç®æ·»å è³ OpenSea ( create -> submit NFTs -> "or add an existing contract")

## ð¶ Infura

> ä½ éè¦ä» [infura.io](https://infura.io)ç³è¯·èªå·±ç apikey å¹¶ä¸æ¿æ¢å°ç®å½ `packages/vite-app-ts/src/models/constants`ä¸`constants.ts`ç¬¬ 2 è¡:

![nft13](https://user-images.githubusercontent.com/526558/124387174-d83c0180-dcb3-11eb-989e-d58ba15d26db.png)

---

# æ­åå®æ ð!

ð¦ æå»ºåç«¯:

```sh
yarn build
```

ð½ å°åç«¯æç®¡è³ surge:

```sh
yarn surge
```

> ð æµè§å¨è¾å¥ æç®¡å¥½ç surge å°å ð©ââ¤ï¸âð¨ å¹¶åäº«ç»æåä»¬ï¼ä¹å¯ä»¥èµ éæåä»¬ NFTð

---

![nft15](https://user-images.githubusercontent.com/526558/124387205-00c3fb80-dcb4-11eb-9e2f-29585e323037.gif)

---

> ð æ¬é¡¹ç®åºäº [here](https://speedrunethereum.com).

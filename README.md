# Create An Ethereum Dapp with Ethersjs

Ce projet a pour objectif de découvir le fonctionnement basique d'un dApp en intéragissant avec un smart contrat permettant d'envoyer et de récupérer une chaine de caractère.

Pour lancer le prjet il faut tout d'abord:
 - [Metamask](https://metamask.io)
 - [Remix IDE](https://remix.ethereum.org)
 - [Ethersjs](https://github.com/ethers-io/ethers.js/)

# Résumé du projet 

 - Création d'une page html
 - Création d'un smart contrat
 - Connection de la page web avec le smart contract grâce à Ethersjs.  

---

### Preparation

1. **Installer [MetaMask](https://metamask.io)**
   - Si besoin pour comprendre comment utiliser Metamask [vidéo d'explication](https://youtu.be/wlm4QcA8c4Q?t=66)

   - Changer le réseau pour Ropsten Tesnet et copier l'adresse


2. **Récuperer des Ropsten Tesnet Ether pour notre wallet Metamask.**
     - [Lien vers des Faucet pour récuperer des fonds](https://ipfs.io/ipfs/QmVAwVKys271P5EQyEfVSxm7BJDKWt42A2gHvNmxLjZMps/)
     - [Blog expliquant le fonctionnement d'un faucet](https://blog.b9lab.com/when-we-first-built-our-faucet-we-deployed-it-on-the-morden-testnet-70bfbf4e317e)

3. **Télécharger le répertoire et lancer la page via un serveur**

### Créer le smart contrat

1. Vous pouvez utiliser l'éditeur de votre choix mais l'IDE en ligne remix sera utiliser pour faire fonctionner notre dApp [remix.ethereum.org]
   - Vidéo explicative du fonctionnement de Remix [voir plus](https://www.youtube.com/watch?v=pdJttvcAV1c)
3. Clicker sur les onglets "Solidity Compiler" et "Deploy and Run Transactions"
4. Créer un nouveau fichier solidity dans remix, named `mood.sol`
5. Copier coller le code fourni dans le répertoire contrat
6. Déployer le contrat sur Ropsten Testnet. 
   - S'assurer que Metamsk est connecté sur le testnet Ropsen
   - S'assurer d'avoir sélectionner la bonne version du compilateur pour correspondre à celui préciser au début du contrat
   - Compiler le code dans l'onglet "Solidity Compiler"
   - Déployer le contrat dans l'onglet "Deploy and Run Transactions"
   - Sous la section "Deployed Contracts", vous pouvez tester que le contrat fonctionne correctement.

***Déployez bien sur Ropsten via Remix avec l'environnement `Injected Web3` et confirmez la transaction dans Metamask***

Make a new temporary file to hold:
   - The deployed contract's address
      - Copy it via the copy button next to the deployed contracts pulldown in remix's **Run** tab
   - The contract ABI ([what is that?](https://solidity.readthedocs.io/en/develop/abi-spec.html))
      - Copy it via the copy button under to the contract in remix's **Compile** tab (also in Details)

---

### Connecter la page web avec le Smart Contract

Ouvrez `index.html` avec un éditeur de texte, ajoutez les infos suivantes:

1. Dans l'onglet "Deployed Contracts" copier l'adresse du contrat et remplacez celle dans le html par la votre
2. Dans l'onglet "Solidity Compiler" copier l'ABI en cliquant sur le bouton en bas de la section et remplacer dans le html

**C'est terminé vous pouvez tester le dApp**

# Blockchain Data Project

## Initializing

The project uses yarn. Run npm `npm install`or `yarn install`to get dependencies up and running. A node environment is required.

## Using the blockchain

To connect the blockchain to the database it needs to be initialized first:

```
// import Blockchain from dbchain.js. Then:
var bc = new Blockchain();

// Call init to start and load the blockchain. 
// Genesis block will be created
await bc.init();

```

Now blockchain functions can be used like this:


```
// Add blocks
await bc.addBlock(new Block('Remember, remember!'));
await bc.addBlock(new Block('The fifth of November,'));
await bc.addBlock(new Block('The Gunpowder treason and plot;'));
await bc.addBlock(new Block('I know of no reason'));
await bc.addBlock(new Block('Why the Gunpowder treason'));
await bc.addBlock(new Block('Should ever be forgot!'));
await bc.addBlock(new Block('Guy Fawkes and his companions'));
await bc.addBlock(new Block('Did the scheme contrive,'));
await bc.addBlock(new Block('To blow the King and Parliament'));
await bc.addBlock(new Block('All up alive.'));

// Show all blocks (for checking)
bc.chain.printAll();

// Validate the chain
bc.validateChain();
bc.validateBlock(7);
```
# op-cryptomine
crypto mining script
console.log("Hello, World!");
const crypto = require('crypto');

function mine(blockData, difficulty) {
    let nonce = 0;
    let hash = '';

    while (hash.substring(0, difficulty) !== Array(difficulty + 1).join("0")) {
        nonce++;
        hash = crypto.createHash('sha256').update(blockData + nonce).digest('hex');
    }

    console.log(`Nonce: ${nonce}`);
    console.log(`Hash: ${hash}`);
}

const blockData = "example block data";
const difficulty = 4; // Adjust difficulty as needed
mine(blockData, difficulty);


if dont work remove hello world 

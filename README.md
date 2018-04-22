# go-test-blockchain
test blockchain written in go lang
## to run the blockchain in the browser with postman
- download postman https://www.getpostman.com/
- open terminal from repository and enter command 
- - `$ go run main.go`

###### set up
- open chrome and go to http://localhost:8080
- set postman to http://localhost:8080
###### adding on to the blockchain
// in postman
- go to "Body" tab
- imput BPM data in following format "{"BPM": int}"
- - eg. {"BPM":67}
- click Send
- refresh browser

## running from the Networking branch
- open terminal from rempository and enter command
- - `$ go run main.go`
- open another terminal and enter command
- - `$ nc localhost 9000`
- (try in multiple terminal sessoins to see the effect)
- (wait 30 seconds and see the updates broadcast to each client)

## running from the IPFS branch
- need a secondary computer or VM instance to simulate the secure file sharing
- need a test file(superTOPsecret.pdf in this repo, but you can change it) in your directory

###### set up (on both computers)
- `$ brew install gnupg`
- `$ gpg --gen-key` 
- follow the prompts and save the password that you choose for each 
- export public key on the second computer using command
- - `$ gpg --export --armor -email > pubkey.asc`
- move the `pupkey.asc` file to the first computer, and into working directory
- import it into your keyring using command
- - `$ gpg --import pubkey.asc`
- can check if it was imported correctly using `$ gpg --list-keys`

- downloading and installing IPFS
- download IPFS here https://ipfs.io/docs/install/
- initialize IPFS with command
- - `$ ipfs init`
- start the daemon with command
- - `$ ipfs daemon`

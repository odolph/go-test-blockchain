# go-test-blockchain
test blockchain written in go lang
# to run the blockchain in the browser with postman
- download postman https://www.getpostman.com/
- open terminal from repository and enter command 
- - $ go run main.go

# set up
- open chrome and go to http://localhost:8080
- set postman to http://localhost:8080
# adding on to the blockchain
// in postman
- go to "Body" tab
- imput BPM data in following format "{"BPM": int}"
- - eg. {"BPM":67}
- click Send
- refresh browser

# running from the Networking branch
- open terminal from rempository and enter command
- - $ go run main.go
- open another terminal and enter command
- - $ nc localhost 9000
(try in multiple terminal sessoins to see the effect)
(wait 30 seconds and see the updates broadcast to each client)
# Setting up IRC over I2P with IRSSI 
## I2P setup
- Ensure Java is installed.
- [Download latest version of i2p](https://geti2p.net/en/download)
- cd to downloaded file and run
  ```
  java -jar i2pinstall_2.9.0.jar -console
  ```
  replacing `i2pinstall_2.9.0.jar` with actual file name.
- Go through installation prompts
- Run
  ```
  i2prouter start 
  ```
  If this doesn't work, cd to extracted .jar directory and execute directly with start as and argument. ex: `bash i2prouter start`
- After starting, go to your browsers network settings and configure proxy manually. HTTP and HTTPS should both be set to `127.0.0.1:4444` You can find browser specific instructions on the i2p website [here](https://geti2p.net/en/about/browser-config)
- Access router console at `127.0.0.1:7657/home`
- You will need to wait for connection to set up. Keep an eye on the status indicator towards the lower left. This can take 10+ minutes. 
- After status goes green, try clicking one of the links to take you to an eepsite. If it loads, your i2p service is good to go!

## IRC setup
- Open `irssi` in terminal.
- Set your name variables. Do this for OPSEC as irssi will use your systems user name by default potentially compromising anonymnity. 
  ```
  /set nick <name> 
  /set real_name <name> 
  /set user_name <name> 
  ```
- Disable all DCC and CTCPS. This prevents users in servers from making requests to your client directly which can potentially reveal compromising information & create attack surface.
  ```
  /ignore * DCC CTCPS
  ```

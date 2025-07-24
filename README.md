# irc2p-guide
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
  If this doesn't work, cd to extracted .jar directory and run execute directly with start as and argument. ex: `bash i2prouter start`
- After starting, go to your browsers network settings and configure proxy manually. HTTP and HTTPS should both be set to `127.0.0.1:4444` You can find browser specific instructions on the i2p website [here](https://geti2p.net/en/about/browser-config)
  


# Namada Automatic Setup Guide - AdamanLab

This guide walks you through the automated setup process for Namada using the provided script.
Tooling for automatic install namada with 1 command 
## Prerequisites

Before proceeding, ensure you have the following:

- A stable internet connection.
- `curl` installed on your system.

## Usage

1. Open your terminal. Ensure you are in your home directory (`$HOME`)

2. Run the following command to execute the installation script:

    ```bash
    source <(curl -s https://raw.githubusercontent.com/nolan7512/automatic-install-namada/main/autoinstall)
    ```

  
3. After running the script, the Namada logo will be displayed, and you will be prompted to provide the following information:
   
   - **WALLET name**: Enter your wallet name.
   - **ALIAS**: Enter your alias.
   - **Pre-Genesis Validator**: Enter `1` if you are a Pre-Genesis Validator, or `0` if not.
  - **PORT**: Enter your desired port number. The default port is `26`.
    - For example, if you choose the default port `26`, the following ports will be used:
      - RPC port: `26656`
      - P2P port: `26657`
      - gRPC port: `26658`


4. Once you've entered the required information, the script will automatically set the variables and update your `.bash_profile`.

5. The script will then display the entered information along with the configured settings.

6. Various components required for Namada will be installed automatically, including Go, Rust, Cargo, Protocol Buffers, CometBFT, and the Namada binary.

7. If you are a Pre-Genesis Validator, you'll be asked to place the pre-genesis folder at a specific path before proceeding.

8. Custom ports will be configured in the `config.toml` file.

9. A service file will be created for Namada, and the node will be started.

10. Once the setup is complete, you can monitor the service using:

    ```bash
    sudo journalctl -u namadad -f
    ```

## Notes

- Ensure you provide accurate information during the setup process.
- If you encounter any issues, refer to the troubleshooting section or seek assistance from the Namada community.

**Congratulations!** You've successfully set up Namada using the automated installation script. Enjoy using Namada! AdamanLab


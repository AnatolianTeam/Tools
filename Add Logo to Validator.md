## Display Your Logo on Cosmos-Based Chains with Keybase.io

Want to make your validator node stand out on Cosmos-based blockchains? Look no further than Keybase.io! 
This guide will walk you through the process of setting up your Keybase account, obtaining your public key, and using it to update your validator profile with your snazzy logo. By following these steps, you'll create a more visually recognizable presence for your validator across the Cosmos ecosystem.

### Create a Keybase.io account

1. **Navigate to Keybase.io:** [Visit](https://keybase.io/).

![image](https://github.com/AnatolianTeam/Tools/assets/107190154/e1ecb3ed-f1ae-45fe-ad96-60f1d5b410ce)

2. **Sign Up:** Click the prominent "Sign Up" button. You can use your email, phone number, or sign up via existing accounts on GitHub, Twitter, or Reddit for a streamlined process.

<img width="1469" alt="Ekran Resmi 2024-06-30 12 52 26" src="https://github.com/AnatolianTeam/Tools/assets/107190154/ca6135da-a59f-40f2-a650-60c3c37c586f">

3. **Create Your Identity:** Choose a username reflecting your validator node's brand and set a strong password for security.
4. **Verify Your Account:** Follow prompts to verify your email or phone number for account setup completion.
5. **Log In:** Open the Keybase app and log in using your signup credentials.

### Your Validator's Identity Badge

1. **Access Your Profile:** Click on your profile icon or username within the Keybase app.
2. **Find Your Public Key:** Look for "PGP keys" or "Public keys" section on your profile.

<img width="1455" alt="Ekran Resmi 2024-06-30 12 56 40" src="https://github.com/AnatolianTeam/Tools/assets/107190154/42ef5546-9f42-4f4f-bfd4-818b9e52b7db">

3. **Copy Your Key:** Click the "Copy" button next to your public key to copy your Keybase ID.

**Upload Your Validator Logo**

1. **Go to Your Profile:** Stay on your Keybase profile page.
2. **Change Your Profile Picture:** Click on your current profile picture.
3. **Upload Your Validator's Avatar:** Choose your validator node's logo to upload. This logo will represent your validator information on Cosmos-based blockchains.

### Step 4: Update Your Validator with the Keybase ID and Showcase Your Logo (Command Example)

Now that you have your Keybase ID, it's time to integrate it with your validator profile. The following command example utilizes the `mantrachaind` validator node, but the basic structure can be adapted for other chains.

**Remember:** Replace the bracketed placeholders with your specific information.

```
mantrachaind tx staking create-validator \
--amount=1000000uom \
--pubkey=$(mantrachaind tendermint show-validator) \
--moniker=$MANTRA_NODENAME \
--chain-id=$MANTRA_CHAIN_ID \
--commission-rate=0.10 \
--commission-max-rate=0.20 \
--commission-max-change-rate=0.05 \
--min-self-delegation="1" \
--gas-prices=0.002uom \
--gas-adjustment=1.5 \
--gas=auto \
--from=$MANTRA_WALLET \
--details="Always forward with the Anatolian Team 🚀" \
--security-contact="xxxxxxx@gmail.com" \
--website="https://anatolianteam.com" \
--identity="XXXX1111XXXX1111" \
--yes
```

### Brief information about the parameters

Use the following parameters carefully to personalize your validator profile:

1. **details**
   - Description: A brief description to be displayed on your validator profile.
   - Usage: 
     ```shell
     --details="Always forward with the Anatolian Team 🚀"
     ```
   - This description is used for promoting your validator. For example: "Always forward with the Anatolian Team 🚀".

2. **security-contact**
   - Description: An email address for security-related contact.
   - Usage:
     ```shell
     --security-contact="xxxxxxx@gmail.com"
     ```
   - This address is used for security notifications and important communications. For example: "xxxxxxx@gmail.com".

3. **website**
   - Description: The URL of your validator profile's website.
   - Usage:
     ```shell
     --website="https://anatolianteam.com"
     ```
   - This URL directs to the official website of your validator profile. For example: "https://anatolianteam.com".

4. **identity**
   - Description: Your Keybase.io identity verification code.
   - Usage:
     ```shell
     --identity="XXXX1111XXXX1111"
     ```
   - This code verifies your validator profile with your Keybase.io account. For example: "XXXX1111XXXX1111".

By completing these steps, you've linked your validator profile to your Keybase account. This integration allows Cosmos-based blockchains using Keybase.io for identity verification to showcase your validator's logo along with your other information. Now, when delegators explore validators on different Cosmos chains, they can easily recognize and trust your validator through its logo, enhancing its visibility and reputation within the Cosmos ecosystem.

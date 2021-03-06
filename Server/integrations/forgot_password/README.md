# Forgot Password 2FA Token Interception Script

## Description

This script is a 2 in 1. It can be used to enable user to reset its password **or** to enable 2FA sending a token to user's email :

How they work:

### Forgot Password
* Step 1: User enters e-mail and if e-mail exists, user receive a token via email
* Step 2: User enters token received by e-mail
* Step 3: User enters new password

### Email 2FA
* Step 1: User enters username and password
* Step 2: User enters token received by e-mail

## Installation

* Make sure that you have a correct **SMTP settings in Gluu Server** - Navigate to Configuration > Organization Configuration > SMTP Server Configuration
* Set up the script function (Forgot Password or Email 2FA) - Navigate to Configuration > Manage Custom Scripts, choose the script and set a **custom attribute** with key `SCRIPT_FUNCTION` and value `forgot_password` for Forgot Password mode, or `email_2FA` for Email 2FA mode.
* Enable the custom script. 

Please notice the xhtml files for this script are currently located at `oxAuth/Server/src/main/webapp/auth/forgot_password/`

Note: If you want to use both scripts, you'll need to copy it and change the **custom attribute** from the copied script.

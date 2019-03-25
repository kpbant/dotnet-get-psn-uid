# dotnet-get-psn-uid
Solution to retrieve UID for PSN.

    /*
      FOR PSN:
      1. Enable 2FA on your PSN account.
      2. Navigate to https://www.bungie.net/en/User/SignIn/Psnid?code=000000 and login using your PSN account.
      3. When asked for your 2FA code, DO NOT enter it. Instead, look in the URL. You should see a parameter called ticket_uuid.
      4. Get the value of ticket_uuid from the URL (e.g., b7aeb485-xxxx-4ec2-zzzz-0f23bcee5bc5) and the 2FA code from your device.
      5. On your initial run, use getPsnRefreshToken("ticketUuid", "_2fa") to get the value of a refesh_token.
      6. Use the value of the refresh_token to run getPsnUid("user", "refreshToken") from now on (this process can be repeated as necessary).
    */

    getPsnRefreshToken("ticketUuid", "_2fa");
    getPsnUid("user", "refreshToken");

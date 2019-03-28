# dotnet-get-psn-uid (.NET Core 2.2) / Solution to retrieve UID for PSN.

## To-Run:
  1. Enable 2FA on your PSN account.
  2. Navigate to https://www.bungie.net/en/User/SignIn/Psnid?code=000000 and login using your PSN account.
  3. When asked for your 2FA code, DO NOT enter it. Instead, look in the URL. You should see a parameter called ticket_uuid.
  4. Get the value of ticket_uuid from the URL (e.g., b7aeb485-xxxx-4ec2-zzzz-0f23bcee5bc5) and the 2FA code from your device to run.
  
  ```sh
  refreshToken = getPsnRefreshToken("ticketUuid", "_2fa");
  if (refreshToken != null) getPsnUid("user", refreshToken);
  Console.ReadKey();
  ```

### 7z Password:
To obtain the password for the 7z, contact kpbant@gmail.com.

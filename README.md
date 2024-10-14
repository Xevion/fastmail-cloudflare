# fastmail-cloudflare

This is a simple script to update the DNS records of a domain in Cloudflare to point to the Fastmail mail servers.

> [!WARNING]
> This script is not officially supported by Fastmail. Use at your own risk.
> Furthermore, it's currently in development and may not work as expected.

## Requirements

- Node v20+
  - Newer or older may work, but is untested.
- [pnpm][pnpm]
- Cloudflare API Token
  - `DNS Settings:Edit` permission.
  - Ensure the token has access to the domain in question.
  - Create one [here][cf-token].
- The domain you want to onboard, managed by Cloudflare.

<!-- TODO: Test Node.js versions -->
<!-- TODO: Test minimum permission requirements -->

## Usage

1. Clone the repository

```
git clone https://github.com/Xevion/fastmail-cloudflare.git`
```

2. Install dependencies

```
cd fastmail-cloudflare && pnpm install
```

3. Configure environment variables

   - Get your Cloudflare API Token.
   - Copy `.env.example` to `.env` and fill in the values.
   - `TARGET_ZONE_ID` is the ID of the Zone/Domain you want to onboard.
   - If you don't know it, run the app without it, and it will list all your zones with their name and ID.

4. Run the script!

```
pnpm run start
```

[cf-token]: https://dash.cloudflare.com/profile/api-tokens
[pnpm]: https://pnpm.io/installation#using-a-standalone-script

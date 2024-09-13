# nextcloud-keycloak-integration
Integration of Nextcloud with Keycloak as an external login using Social Login Connect for secure authentication
This guide assumes that you have already installed both Keycloak and Nextcloud. The following steps will help you integrate Nextcloud with Keycloak as an external login provider using the OpenID Connect protocol.

### Prerequisites
- Keycloak is installed and how to download keycloak visit [Keycloak URL](https://www.keycloak.org/documentation)
- Nextcloud is installed and running at [Nextcloud URL](https://docs.nextcloud.com/server/latest/admin_manual/installation/)
- Admin access to both Keycloak and Nextcloud


---

## Step 1: Configure Keycloak

### 1.1. Create a Realm
1. Log into Keycloak's Admin Console.

![Uploading image.png…]()

2. On the left sidebar, click on **Realms** and select **Add Realm**.
3. Enter the **Realm Name** (e.g., `company name`) and click **Create**.

### 1.2. Create a Client for Nextcloud
1. In the **nextcloud** realm, go to **Clients** from the left sidebar and click on **Create**.
2. Enter the following details:
   - **Client ID**: `nextcloud`
   - **Client Protocol**: OpenID Connect
   - **Root URL**: `http://10.123.13.113/` (replace with your Nextcloud URL)
3. Click **Save**.

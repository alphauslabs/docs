# Azure CSP Account Registration

To successfully register your Azure CSP account in Octo, there are **pre-requisite steps** that must be completed outside the Octo platform. These steps involve enabling API access in the Microsoft Partner Center and Dev Center to allow Octo to retrieve ERP pricing and billing data.

---

## Setup Partner Center Access

You can follow the steps [here](https://docs.microsoft.com/en-us/partner-center/develop/set-up-api-access-in-partner-center#set-up-your-accounts) and [here](https://docs.microsoft.com/en-us/partner-center/develop/partner-center-authentication#initial-setup) to set up API access to the Partner Center.

> **Note**: Access to the sandbox integration account is not required.

### Enable API Access

Once the account is configured, you must enable API access in advance to use the Partner Center SDK in the integration sandbox. This must be done separately for both the primary partner account and the sandbox account.

1. Sign in to the Partner Dashboard with a Global Administrator account.  
2. From the **Settings** menu (gear icon), select **Partner Settings**.  
3. On the **Account Settings** page, select **App Management**.  
4. If no apps exist, add a new Web App. If an app already exists, click **Add Key**.  
5. When creating a Web App, copy the app registration information (especially the key) and store it securely.  
6. Sign out of the Partner Dashboard.  
7. Sign in with the integration sandbox account and repeat steps 2–5 to enable API access there as well.  

You can write and test code in the integration sandbox. To configure Azure AD authentication for Partner Center access, the following information is required:

| Item Name          | Location                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------|
| App ID / Client ID | Settings > Partner Settings > App Management. Listed under registered applications.                  |
| Key                | The key saved in Step 5 when creating the Web App.                                                    |
| Domain             | The domain of the integration sandbox.                                                                |

Partner Center uses Azure Active Directory for authentication. When interacting with the API, SDK, or PowerShell modules, you must configure the Azure AD application correctly and request an access token.

- You can use **App-only authentication** or **App + User authentication**.
- **MFA is required** if you use App + User authentication.
- Some API operations **do not support App-only authentication**. Refer to scenario documentation to confirm what is supported.

---

## Initial Setup

1. Record the Azure AAD application's Registration ID and Client Secret (Client Secret is required for App-only auth).  
2. Sign in to Azure AD via the Azure portal.  
   - Under **API permissions for other applications**, configure **Windows Azure Active Directory** as **Delegated Permissions**.  
   - Select both:  
     - "Access the directory as the signed-in user"  
     - "Read the signed-in user's profile"  
3. In the Azure portal, add an application.  
4. Search for **Microsoft Partner Center**.  
5. Assign **Delegated Permissions** to "Access Partner Center API".  

---

## Setup Dev Center Access

In order to get ERP price data for Azure, we need to gain access to the Microsoft Dev Center. To do this, we'll use the application user that was created during the onboarding process. The exact steps are listed below:

1. Sign in to your Partner account in the [Azure portal.](https://portal.azure.com/)  
2. Select **Azure Active Directory**.  
3. Choose **App registrations**, then select the application you created for Octo.  
4. Go to **API Permissions > Add a permission > APIs my organization uses**.  
5. Search for: **Microsoft Partner (Microsoft Dev Center)** API (`4990cffe-04e8-4e8b-808a-1175604b879f`).  
    
    ??? info "Click to view image"
        ![microsoft dev center](https://lh3.googleusercontent.com/fife/ALs6j_FGDD8O_-xOg_BjhPQy9LTnKzdrIOTiRCTGxE5XW00I-18f6fSKuEdVv0ecA_qGWnJLn890K-xyvIBmGL52KOgmETMY9ltvzeKoil85Smrt2qn5Oyo81EEToKC3G6EW_XLlFDcaCkjyGyuQsdcLClMn2JFKjsnjw7u8b-Qv59SDVJDpS9BJ29Ix3OLquGAA3E31Tv_jXJqONA-d9sbitUJrA-O_3NgCDoisLOeiQgJMSWqgxsWPGM7rHbWg7Kd2Oa1RCOItIqxjh7y725wtyN4M4uVkxkevKksf0-2RV7dhJw2amqIhvYihHOI4bUKzcAD5olojjU69MWFWx4rXnLxiCI5eNJ0_scW-J7HsN36Z7g1bhMCtpr917DhpV-5yI-QLXDTS2RA4DMyYUXKoIq4_vVCnmzhy_ojXbCEM0yyOLrq4AOqxv839H7-ov0DTFSDNNzej-zO7a8YHdA__fOW-qIuKEuvupU10CiiXOoG_sZJb6e4WQqQytPbST9bA2Pv3_Gw_5QFQyE0skC9qIOyP8HL5xjkTULxUUrmvkUpvCvWfJMwiOPcLTT5UDfILBTCpKnSDZlN_t9B3YW0fLcREF94fEMhafOuEGnaaoRsjOPqBt6i1ilCGw0zhfU2DUejf33YFtD9SbJCcMU0cdSxt3Lsg4T0UTurEg23wmSvcFC1fs62sEDJBhwn6ifT8OuwQ3vkdYkyQw8l69MBT9eybOxGdPhiepgPVr0tCUg2JYE0ZTDgRQdXXN9jTlZpjyGZkrw2UP9lP584_FerLDQWpMWJpbYRGxMfxUrGdhD6Cx_cBg29qDZUyXz9ddZj0EJjk_aqg5RioRyzPrXaG_Z8FyRtavbP4rGMe5xymBmI3vaDpSOt1PTKLcQcf4pxhVEeJ7pssFB02f7vPoiqksyWqD0I9eHemt0N3Vy1wd7KkVwVnVIIcgG5WcfxncDeyqsAAIsuNaICeMzsVYK9MYqycNoWiPcTKKHG3ErkgLyOYuXzC581LE0KSkJIWERvMnlac8_-LC6je9M3ucrzaa6jBYsleU0HqZGSgcMw02TpMExFKF2uVzN-8d-IAnWcglA1UlV0xsJOILTggHxPOx6aiCSJPmblRf1KP_wrkU43CXVmWgYeB6nf9uYhOg9Jdh9hNGzQ9oQa4okEIDZ4AmwbemLjZkgu6LSLT4zS_iP5zl1UFGzmPNqAPgnhztLfJwbfBW7yWu_zfeAY26ndXZTa1r3MV2l4EXNLfoITbn5cq7trHFVX0MzppEWJ8nERh7WZVmNPIB9NuYfjk_lAhYKOiDbn1fM7eN5d_BloRl-qk-4_pNT5L1HRMFqhQjkE2plgYhNNIQT8kd2Uf4T4r5vqOFKgSd2fYDCiaEyEHDQT2IVk8MqB0t4cwB6RZVfYV6mlqXjCsU7xmiOc_S7Z5D_blSdAsvVzeEpofBAAZM4vV7iYxagEJTlnehMp5TqPW1lLcPTR4T0_XCJwi836EoblgvL2bHgf-OMrrYbFgFWg2LBLoUuugQny9cuCHa73iyn-uaH3IJ4C7hOHhXqGZd6M6ixZcLvrzIDbNPEtTPjKyX3O3adLaMMmlKgQirdpyP05mObH_LSnDdUwNDQHFO_QiHNTIGDbR68WjNNDZ=w1920-h970?auditContext=prefetch)

6. Set **Delegated Permissions** to **Partner Center**.
    
    ??? info "Click to view image"
        ![user impersonation](https://lh3.googleusercontent.com/fife/ALs6j_HH6edYvTjepvEe5IB_GJw8B8pi8bRymZ3Futfn5ht7LHDbneQ4KmmcJHv_PsbpRUDuuzdgr2CzfH3eZBYcwhcPi_2tf1LNniLkbMIvpKs70eUa2y2nV8DoBZL8SsdroUvJinxkeM49_2fTLwR1iwRppj9GqvwCuf5_KIDy9TJbkHdj77pdIFyluIKqdhBaNeeObJ_1nnUIOi4CCGs8jbL3dkdyPlJvMXfPww-5Fxr7A_0HmRFOrzu6zLZwAhhTylPH23-U3bHyDwSjroAn013EFTfymA8XAgGIp8stHxP6BR3p__AdjXk1uNo19KY5QYJk3Jq6llzk-taUuGcsfyRPnoilWqGLLENUHVmWV65jDGAx81HGInw0A4tuKErY_newXPhdFxB7nMawQXZvckKhF5ykFmRXKp02cyZB82NIGalHRCoudXEhrAYB2dnp0fyijpnSn9PwybjtqRcEYO1siio74MKZxkGEEXlPdNLrIzyUeO8oG0zEGhAvgecyQlu_iPDs7uRzfXn_hpXiMIivydfjK4XRIEdpJc731XOP1YnTbnfTxx04I_Yiae1TXmYQ6F4gH9gPm3PuxAqBLa7qRmiMrHDqjNv4QV3Xp_p2lKtDKNyKq9s6ZercvosZ3UlPONPA767jfVjFzvhRlS6vIX_4GyxVInvDX2bHQz7pldf913pZ0EdMgIVZLOLoO0QicSOe0dwCE8_THTwrBmXoQEPyMR2496DcntjEJ8E7gkPYpSUdLpcO3mPBrUexCR5FND0xSas4HPUi3BfL7FReqvKtzJX-hDDITC59nFOA9OIWjNEnQHUgTb_xx9_HxKpN0s_b80gYcDbm7Q7GuIEwAyv0E0yk4SXxDHaQJSRdqPUaY8ytJvZ1t9JyWEhkgI_DMazUoOdtvdTJLmD-nh-H0NO9REghFvv0Aa5F6EsDdTZaURty6w8TU9AjU2NMB6yA3UzykELXo_ylowpnV6fMg3nkLZuREbvEMjWJeJzQdkPOeji9HqS279y8D1sEpr-P9wlbdtfhmbJh1KT0WhTsuZur7V-hRHKjb9WwXVCSBS806VDPIqjq84RbBmvZumKy1VeC_kPFSp0GN0p99NCRxjPA7p65gi69d_mKagGRmCGaUsIbWZE2VpvACW50MA6BboqsjPWCm3jtA_PEtBMako7H0vLJzDU90iLGoOXxoaUEjgvHBXxYfnUqnfoYt2zYiSz1pF_ftpNMpRTIL7024Sn_FTPiVNJRRff5hUAK8BB6Yq8YpUSnKwayrPzhIZ8Za8XE6veJkzLb_PjwQ2y8ME-8w1JBdE0Rs9SVjeJts--0OWu6ymXRnpkG5mJSMhB0Qoegx-Ph764vimnPIO4OCz01L36UwbW7uIOvdFnJHljliYf4aya3QPYolEawsQ9ay6ZgCf_mlrJQ2R-D9gM-TjD9rdjIKpeheT5S5xIUSRNtxCkIJzDiAzJfyNXeLI6EuTG2TuXapsCrfjWS_G3S2hTId1HalBH7o5IBhPdHKh5o4DaPo_kwqqz2quXLTWdpR1PmBS4IqmBsm0ZKgr8tzFyIw4SgYDjx53Y8ba3QbhuOQ1u4MGEPyVANVSqNyigINBcGtrQWHuWCusMaOJCaQDBQjTooBeEC1KpO=w1920-h970?auditContext=prefetch)

7. For the application you registered, choose **Overview** and then select **copy the Application ID**. 
8. Now, we need to generate an authorization code. The authorization code is generated by granting the consent to the application used in the API call via the following URL template. You just need to replace the values in the template to create the consent URL for your application:

   ```
   https://login.microsoftonline.com/common/oauth2/authorize?client_id=<Web_App_Client_ID>&response_type=code&redirect_url=<RedirectURI>
   ```

   - Replace `<Web_App_Client_ID>` with the Application (client) ID you copied earlier.
   - Replace `<RedirectURI>` with the Reply URL you set when registering the application (found in Azure portal > Azure Active Directory > App registrations > Select your application > Authentication).
9. Open an InPrivate or Incognito browser window and paste the completed URL into the address bar.  
   Once you have replaced the required values, the URL will look something like this:

   ```
   https://login.microsoftonline.com/common/oauth2/authorize?client_id=<Web_App_Client_ID>&response_type=code&redirect_url=<RedirectURI>
   ```
10. Login using your **Admin account** and click "Accept". This is where you will use MFA to validate your account and authenticate successfully. Note that this account must have the **Admin agent** permission.
11. You will be redirected to your redirect URL once signed in.  
    - If your redirect URL is `https://localhost`, you may see an error message such as “couldn’t find the server” or “can’t establish a connection to the server at localhost.”  
    - However, the address bar will contain the **Authorization Code**.
    
    ??? info "Click to view image"
        ![authorization code](https://lh3.googleusercontent.com/fife/ALs6j_HeXYAjwrucMedROfyROO8gEGK1VqVtg7pQASX28_ywjq0rnD5ms_e0Ehr9uVg3lKCqn36nPVEhePseYslfpJivTWC7GD_kW2fl_4NWrgNuVBbbVZfECbPnNGOOK8nBHf_8njKJ2auV7C4qJJYV-t6tvXSMAagCF4RhhIrhzgvhP8h9b4F8V3FEo9OChjt-2Uwvu3sqBZJ97gqJJhWvYhsfZMG18ftFV3K0iI1MDJTvYeqxtsCEPGJI9qHhMIUnHsKO7ukzMtYKG17cbE-VJM30MEE8sWQyqwgcfMfMd3GdCM_-XtolEyUX4akJ_3b9Ui5eXn7Yhsqh1sIdKwXstQtAaHLQqi37nIww_okpJVYvCKaS6coU65oByyC-nUCd7A_AC1QuTvU_BYUZ5q-gMYdRcWjn09q8a7a2zCzXiwIdB8jIBzUSm9hPkCrPz_2VP_2dfmQ1W0DVPHnHLVBEspn_j4GSgf3fZmQyeuD2lHT78Mf5poOoevfcNgN5fhtMWm0uesJCmtBXUgOsWxg6czkQgklx3VsHkHmnNdDLiWZCQ3mbT3g8R54z-S1m8uNmlyN-R5nrnOnx8uAAl-9pq6tiYGUYHYlWCUGuREbJxhW_qs2kEBpl1KSwwLlNuigj86JzJaR5jt9IR9LZPILtMUZ-XP2qNohNKlzD33VdmUYbRo8NnAes9wfV1KH0vnIe4B72kr42tXT2-o0C2twS3ZFOtqZFNw4jMKRN1ls6GWtdAqm6fEejhiz_YHY7T-q7vTRI8yRKqdIYGtOz6ZLvXz7LsZsP9iSi4sEq8jy2PbaJjKg-0YiNwsa0u97vNQ6cl6-Q-8kg75Q6xsIkRLicpS4TPbzrs1nhs1jXHDkqgwsRnjCdwdCLXsr9KceO3uWwkmEXutCiLOl5JJ_J23gzYjzeU_kPMU1wmWGJEx46Imm_jvbXGcwhpx_yJM4KacdekgLBfu0KsCaZNOimStteHGt_mXvkvJwtMvoK7Su9cKcjB40mMthzXEYGMx4Nf-NGxySXw9UwMbTOYsIWvj0aJANpvdghmTwJivJ5sOcr51lo3Z2bYf9vK5B7GPytv8npXH4deIiU26cSexzZX1XVKCy1KyhUekRP7ochnVOxrNr6-hC_hi5YFkA2aJ2eJS1Wg5k326y9urPrRTl51nmM9TMGurwwLlkvSpzbRkNwRRQ2fKuiX1Zy5nSiGbBw0Ar6jkO6bpyOqqbg_Qh5HmnXLoZrvYlVsnooIzSYIeDkOhW-ftoZ58Ckb88TxZOM_HuIw_5nVhMOd-HM4R6s3fRNCOkHKA5HPQl_yQw76EDAkONLR82L4UnfQq7YS9nr6W2aI6ZVmUPiO2qEK_T1bUm1rekz4NpFJaErk9Al-r5BSiVndpMnnusUnqn7oI_JqaBSi3eROCGdioSZAhoobFCapmFoOnV1-ZhM1GlVEHW32SSS6hLpBbLabB-nM7dMQn9OZlDIV8DqfB5C7_2urT2bvnyT_CVUgw-hb9FF1jdXm_0aR_jQ1ICyRzaSUwCLWYaSWQ_-IzKpPh2-2Q-ftidBnrm6jO59EFC8ms6-7MsKUvevdTzLkWU283cY_ebDQIeh91cgoJtIEBKGFUysyFY7iGIDZCwZfLXZSRlBmubCrw=w1920-h970?auditContext=prefetch)

12. Copy the entire URL from the address bar into a notepad. It will look similar to:

    ```
    <RedirectURI>/?code=<Authorization_Code>&session_state=<GUID>
    ```
13. The **Authorization Code** is the value after `code=` and before `&session_state=` in the URL.  
    - Save this code securely.  
    - **Note:** The Authorization Code is single-use and will expire after it is used, similar to a one-time passcode (OTP).


---

## Azure Account Registration in Octo

Registering Azure CSP Payer Account involves 3 steps: Basic Details, Partner Center Credentials, and Partner API Credentials.

> **Note**: You can only register one payer account as of now.

1. **Basic Details**

    a. Input your preferred account name (Optional).

    b. Click Next.

2. **Partner Center Credentials**

    a. Input your Client ID, Application ID, and Secret key to proceed.

    b. Click Register Credentials. This will verify your input credentials.

    c. If success, you can now click Next.

3. **Partner API Credentials**

    a. On this step, you can verify your MPN ID, Directory (Tenant ID), and Application ID.

    b. Input your secret key.

    c. Click register credentials. This will open a new tab on which you will be required to sign in to your account. The goal of this step is to obtain an authorization code which is needed on the next input.

    d. Input the code.

    e. Click confirm and register.

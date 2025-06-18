# Unit Metrics

To measure *unit cost*, you need two things: the *total cost* and the *number of units* that cost supports. In Octo, the *total cost* is represented by a *cost group*, while the *number of units* is provided by the *Unit Metrics* feature.

The *Unit Metrics* feature enables users to input, link, or stream business metrics—such as the number of API calls, customers, transactions, or active users—on a daily basis. These metrics are then used to calculate *unit cost* by dividing the total cost (from a cost group) by the metric value.

**Unit Cost = Total Cost (Cost Group) ÷ Unit Metric (per day)**


This feature is designed to:

- Help teams measure the *efficiency* of cloud spend.
- Understand cost trends like *cost per customer*, *cost per request*, or *cost per product*.
- Allow *daily tracking* of business metrics alongside cloud costs.
- Enable data-driven decisions for optimizing spend.

You can upload metrics manually (via CSV or Google Sheets), retrieve them from *CloudWatch*, or stream them through our *Telemetry API* — all of which will be covered in the following sections.

## Creating a Unit Metric

To create a new Unit Metric, click the **Create new unit** button in the top-right of the Unit Metrics Management page.

![Create New Unit Metric](https://lh3.googleusercontent.com/fife/ALs6j_G_fzrTxPzJpeXBOYs8wn4EZ7dhgw9-mtE405nWjfNg2QHbGZBSDVaWb5ZrBzK8gZLXvFKzewc9vWsFTdkfna08vW23JzoVaR9WaIiJ51FU-79IsYLciiG0y9Q-P8lkqvGgOT5QjJm3R6E_fuTTk0Kg4nPyOYpEOPORuuax4d2lw88682JxMa5MDueyRPuwIuEHEB2NmZITMkZxcUPFh6RV6eE5izEBZuMHr0nMvUyvuJbK-valvjEO1zn7WtObDY8K681F6PkFpnNpyq5PQRDDpoTFtHKrKp3Qpj-uMOa-lKxjmkrlvAykilNAZzORc3SEdiNGQFrgz7lQHgyRQQhEnZ7Wr37VosQ1ISFKwLU0nKSngXZnw_g5GRFhJHSJH7OF2-LqNMV2pxAoNpLwvZcOuxmUwKi8Z20nOHF9IvSGHVSYmlVMreO_MvD2vRU2s9e4W5awlt3TnjGWd0RbNb7rH034kBf6KUJ-yhVC0Nwco8s69KdJ-CMxNc8hPFERshq1zenpTlcm5sAyg_3tFizXO45-7z-fM8P9pQGmUuE0jdHmFfEyAbRIVEqtaHMwdvTpxPaMHn1yTgTucdjC5XOYMVMbjDCTE-6SVXckmA44lcT5Km4AC8mSdg7tQN20Y7lcvJFj4dJ3AENS_T6EzYq3P18nN8Ga3OkgyfGQi0Ffzoy3XiPU3wLoJKHlZS3IXi91eZxuF60lVf28flXVk-Nu_LALq6A_VaGln44NdkPv6r2A2Z_6Y140uvnpEjZ8eqfoGiv67knRV2gZJdqE_zPRGGWUlftKgtf9lAe8v829ZkXYEuDrLoRtjRAd1sVRqv18p-3uYd5Ide_Iehdb8RZ_n_9kk8ohLwtuzDeB73AkkoF0QPXnpq7jOBC6jKwB5Qa6zE0JmhN4W_UnmQE0y06oNLMd31x9psSEs3HFnJ4IlFNjxT6jg467ut-Ojcn6WZDBMAQDY3xgreOwqWiotbcAZHAtKzGLQ5MGicP60Ad7wq6VIClBh46IJk6dERqQiBpAMqDsYKBsTwS4ephyyi4nQmMKqJSH-EnQKpPPd6S-D7TnHuUld_biAZBEUqBufUjM-3j12Bg1BGWCQGoK_E-pLzkcfWkbwsWZSmX5UbRps9dpVwpK-jYTGlV_oMgrnpvXaBjYH1k1kY1lHzRHKQloya_eW02sQDQrBx5XVeOF3Np5hKeKiAMSVuZsbgPC5Yeuj1W9whOd7IMP_VST6XCgevHrE9qScge3qm7hq9hIRP3EOvkmkRSr53HiqTeKGRw6lk6e4o_XgJta7PUnVLzJ4IyVYe1WV8Eu_wbfuP-AaAQMR9EcH0ykXj8QqWsdKf8pvTQCIXwWyfKwUeq3AVMW_reF_V0q0-oy88JjeeJCTBzOxdDdIISe_kdd1awuxi6v4WnsDrSigIuF4MyEQUt6Ena_QSnTaFHa-bmqn1T6JKmI-S2IuNinjRuEdNHzUvVkDjotnzsefxvvVOetGdgSl9HcEDQKVlA6y9DThDa1wnEmkzriubrpw3dyKcPQ8oRxLFh0wYmhWikD8iUVA5giUdqNVnYgkoBkAyqx0rQdtdaOe4GeS9IhVA7LsaxhGEKbZw9B_8s6rAFdxVh9JkdsZI84AxcVS5sa_T7vtA=w1920-h970?auditContext=prefetch)

You’ll first be asked to choose the **denominator data source**, which defines where the metric values (the number of units) will come from.

> ℹ️ The numerator (total cost) is automatically taken from your selected cost group in a later step.

The available denominator data sources are:

- **Upload CSV file for denominator data**
- **Retrieve data from Google Sheet**
- **Use AWS CloudWatch metric as denominator**
- *(API integration is currently under development)*

![Select Denominator Source](https://lh3.googleusercontent.com/fife/ALs6j_FN8Tr2YE2_2t3ofPf6zsTxifVOeTkMVzUlq02Px1rdFIXMRDTZjQ7TUwmtyVx-8bRZPF1YcqyMGr_8JzfMLNVChUN7Bc95maRynI50n6o27d_H9mMCu_WWP-WTWpHF6aK2ShUX9WtizHoEGCIz6NIwYlh6eZAxHgA-RbKa0dpLRslB7wxW27svNKgH-25sikXMvo1Gi14Re1xvVMjXIJy0mUC217uxZBfPmaKvI7QoHoRWQV7wTe291Adj1L4URrovxQzHoJHNme2le_kE2Eoa5mQUJZL268ny1Kfm0uB0Tq9HT4R2w-NQ2-M6e_Za6Zt4p0crOMBEOwmXGlHcQsV0ZXD707l0XhXBPl0e69C65ZM8oXnvlH-AD5iWWpH99r2155eY2M1k_N5fAKiN61uipSNHK7U7P6Wtb27Zwr0ggyYOYeBcoBVAIynOy8grEhT_5xOHisze5ewUGAnH-MjUm8FfSiKprRRaihp9Nlp9WBFFqKPOshrcy6pSKMa8Yz22dsuKs4jCz7lXkD0CajZE49fyOSb-lSDypj1_sF2xI-2EQbG1SFNvOtJ0JH5rtB--YwBRIAZtqDpMrkwXKxBIjsvvuxhWuY0wEPxIRH5dJznrZ9b0WTgJGIV90qF1T-3MmYzPUPoiwveUX6ihwtHELeE-tlFOMIaX53EmGWnNm4EoWO3zKcRnoghH0FBYvAr2RRlZ1avZwzhDV4MOlvuR__yyk9lpn2Ms0TmqrlHziBY0KkRKOuhXqhEctqmujkKisYqn7kBwY5N067U8vo9oEyBnyRqux76MW9n-2JretpfMAb1HScvxPZx8P-BlI6B_I1O5tRSYRSHbo0O2JOuQhX396cJooFa0BloOAyonsUf4T6Z-GlUBUWCZAQvMOKCzD8gV9BDNOhd3K5cuRth_m85Uyhsf4aNzuVUNuPYOz2JTPYYhwpZitDELy82c512UkKfHNo2HThAR_xAi_8P0Xt6ipIqmGrs9pMD6AWIU_7DoSkRrov7EeUJ2L7qbPYtxaasufvv1wLZVu_rj6MKXXa3CgwSFvztZs-jJHdHW2pjRak_6E6opoxzxYWszqnKuGU9OrhSN8JLHEeb4unO5Yu82TjuQ_tkwVg_QlJ890p-IBDbG1TP9CLLy9p8rhMtgPU_EdR92tUiD4NUZyedm4L7ZvTYaFpMBNy7NKLKzp6GEFmAKe4CaUnhyL8n86xdxs4A40ubaUAcOeN3EJsmfR3pn8Sg8Iu_dTLULtojAjB-DmPoI3G1ImqLQAJj0nSS9jlri8bWmEDZycqdhBX3s7Bt45KljS77EFZB4l8DsK6KqJe9k0RcllQ_YeKvlaXy5aKUEKatk41WIx8puD_2EJYjlU6pMnAS3TJYM2PAIqZ3unJa4M__a044o-V-5XROs0HTa5eER-GghRIJBR71-dGVoMWprf1W8tROR3UfljXGLMNM8FKgZ9ySUvnztZ1tfM3msMTuoO4eTyeKQJxY0p72QAR4k-vMIxIaF0vUy5yeGaiboqmfbGCxFA_JstupU2E7XQMJtZWExkdMR6MzY0ceoSP-V4rDVy4FEYjD8G_B2_oB4SRMqEenQNUf167Udq6LK1ndb_H6ZLH8_O8j3j-m1eLlxVLl6XrI23g=w1920-h970?auditContext=prefetch)

After selecting a data source, you'll be guided through a **5-step creation process** to configure your Unit Metric.

![5 Step Process](https://lh3.googleusercontent.com/fife/ALs6j_HuDUjiu5zmvURO05nsu00TRAhWsWEdV7Md1KM1TjKllOh9KjvwFrl2H6WJtZuses2ALy_UT3d804py6HpV3tq75fV_FZR8mZkpKO7jDgfwfVCGQoR0DiwEKVfSb_iexuNuTcWKO1H3Z1j4_jTsZhyUntBIhPTRXbcLjctFNt1QBoqZ8VUp77HX0PKsy-lJDos7dsUZp7oqpm0d-koGL64Z5vRts5tCRgRqfgNUEIl5mjgt7qL3Q0OIn6eeczK9NmbD6Dprxk8gH1p_ApvEmujL8mgSrtWx4R2P5DggTbBDYqhaAuYlgz9prqHy5EXb58JAVy3a1D08L9tOBTEzMpNJEdquWscndP0834VCiLAUbR_oyKU8VVZ61BD66pmImGtJpOom5JsYbCFOePuhI03TiXyfzGFU1PK7qx2F1u-9-_L-wNOI8nBqkTgW8sa6DLv22hq7OItIVesqwEI3vsDkULsBrSKMkWZVj72r1AN7YwWmntxHnlXel-2E3mi5HSrI4QJXwXj7OZyWBZfKlgsE_5XdLwpO0LxkTE3EJqASQ0QkXK0NJ0exxEnFfoYBaOW0OwCyuZF0dpNoJRAQBfHFeSnbAiFejy7xs7Oo7mpdKCgrtcYdUKwUBiYvGzJis_-yHKlfvkRqkTISVdtA63UblVdxh2weiCZEusOEQod8moLpgD7v-CiAz5c4VgfyRVBAzsVjhlQC_wVkg3czXbtmAC2hhVOYCbxagebblM25vWFpdb8mem2nt390nPITYi5B0rayxXorigXyVjqT4aviZ6ZdHEH5EuAtUIfbnKThRr3IYv3q6tg7yLA2S1JW888FDUKuM_2ELAHgYzYhm58pm81cCQ0gkpNV8hQR9wVPtdEnx_6mlJUwh3RLaN3_G537vyHd0WKpryGm5bR0Hi3_BX56ZQhVz00bo9ksOEILIR588MtP2SO7DhwYbAGMBGZSajugJtgDm5rJYIs5V609bDDJP_ed09rfC8Q98-iVdj9jVSsqFZMJ86fdYFiJt485aQuBKKDaIXzSJMTcLJH2_PEevy22wabVVHYBWXUk6qyw4Urbv1ntBfo6EVELYd_8Gz1_Cl1qCTpHSluoeCa2LOEPp1JB2PnUriT7Ou7w6YCi-G6150viU9x3X9BknXa486xsJLqefUYiILXr0_PGm4rOMDgrmWx8NkciOkbatmJGIuU9LqfU4IWa6jVtlq1-lQYxF6ZdJFv9wIetA5oWgsWnN87lGha7i2w3Bip98qR8wQan_dR6IuSyw5ahm_eLNYE2g_5y-zQlqL5QJ0Dda0vyRPa37fMW-UourfT_H8R2c3mhQhJS5KozzH5jzoPIl6bquvJt3k4cajuaq5gMzr4ZUolpDTS9yAgCDz-gJprohHZ8YRf-ZTxWtjH_ibkoySghd0TZkEU3BUm3kWtLmHiD01pfC6cOC1JFADyvucHlCVIoawCsDqooajlA5JWp6DIzBwaY2fxtKyRpMWAjTrSP18R2js3bIoCx9SmJx1w7SM6IlvHviUnqqE7kJKEY35e0BFueYoWiSGZX7h0A0CX0lNBFTOLrpYWC69u26vJ4jRXTwHLAWEOrLvwGmvwFZopPrJqmVqF4Y4I8ZE9z-GhVy22u9RkLe248Jw=w1920-h970?auditContext=prefetch)

### Step 1: Basic Details

Enter a *Unit Metric Name* and an optional *Description*. This helps you identify and manage your metrics later, especially when you have multiple unit metrics for different teams or products.

We recommend naming your metric based on what it's measuring. A good convention is to use *"Cost per \<unit\>"*, where the unit represents what you're tracking.

#### 💡 Examples:
- Cost per API Call
- Cost per Customer
- Cost per GB Processed
- Cost per Active User
- Cost per Transaction

You can also use the *Description* field to add more context, such as the data source, team, or purpose (e.g., “Metrics from marketing Google Sheet” or “Production API usage from CloudWatch”).

This name will appear in charts and tables, so make it as clear and meaningful as possible.

![Step 1: Basic Details](https://lh3.googleusercontent.com/fife/ALs6j_GMBAkc85eVfxS7rR1gK5UUQ7TXs_W4iUVnTidNK5CITd8r4hc3suFJylj2l0f5HU7vWkiiLhRPx5T97_CwTcVB5M8fWHRMIrq-lBr1zipl-sKsgOf8PO3vKITq3IM4GT6_0f5zMZo2fx2arf9GW2G-MGElewy-RVgQ_tJRh7u_fjXrEct245nHV3enebuwTQD2e_9ptC4WSq9NKioWwloOOp2sCaUmVyVJNnP9qkM4DWdAEuznG_EzvWIez9wwSGpfticxmCG1Lk-Uh4wB0e1JCSQYTe4ba9O1kcOULfOlArgcHGC6aYDAXgrWq8oDgezm5Muugq6N-EqrKFC0BVo8DvIHNOtL7ifk-4hEgOtRtzTvXMwv4lm3kMRGnybuNpUQ9fQ_Ofg4C9786gFIu1BiKN171TmPF5WeoLhZBqaZJIE710IeMGt2-TtWVJ8vxDR_AqQ8qbc1cHzQexVzQ4jLLNFBiaNUWfYVWy6BT312ms7J59B6c_AoeBKDM0CIKRUgSsy_eKgKWRByqqtyXlN1evW72zi_h38oav_LZV1_IAdqWZ25dbK6V8XfqRMNQZiuAfNrGTzkNAS_Hlfc-t5LBZZmTMkniBBF_qahTJBFWK0DDdGVMC7LVIllWxrcbbTNEdSRgMTXRtnKjP_47sbyAaMnVZpmgFot9YsxpcQIxRA0_74jhuAMc3uVlQh1FUGztIn0Q0_gSAT8oJJd9zFxgdRCxos_ibwMTsQNjhsGYTk2j2vOtBOc9Y8YvWtxCh_45BhFSQ4oWBEkTNbtC90L4luqzDWe1kcGCeuGPTLnQY2sWWnbEhTYQTS4N6Hwzf1b2MapYNINPvIwJIUGkvDWcG9MNP8gj7uI8lDG_HuxMV25nAD7zupDUjkUPPUTV8ETivMPi6OVubaBv6gv_CcoywExqjlbfFQsG4QNCZ-pgl3p3aPzzwkHLr-2nqREjzoizphooLyRgJxbTgu--E1Nyxpmzp5OzFEeRGxq4gR61UhcR2QUrlehui7148ei5CYwbt5VC77oFUvrVQjXdOXPhJtL8CbbHAJcJNNbqPb4zp6V23UqeDJQ5z8PMo5nyI1yG4HGhd0JxrqxIYk_uRQnNQzEtTF1aq2lBvQPfgDXAkSiIOE7WeasVJ3klL0JGqwBZfUKWkhYi1qMl9ENrcCGgpgTf9sr-2v-UjuL0P4N0OeX2hhWwCr8ERzJtirMZMUAKgYHst3iw8hGLu-X8Nh559XfrsMvOYVPfUJLRVOqtZ1FZRjT3nY3c41YWSI9u_de43d15ut4Sp2HZtGY8xkRnha_KOkRVn440EecgSKcv2F8-8ILPJAc9lcfk7dpK3ZcgOAph7TVCAj3IuUZBYekvxe-GurzYEXkkA5i2gwB1pcDbdHoTRJ1gP3OFi3aEdgMj1k7GFz7qTmBq8jSuw5F4JB8hJSTvbw09vvZJAFdcsmbj-mbJ9kQhbaEZKopmXMPb3Vw9FEVcnXTnv6xtUlP3_ihgxEYKnhMNBHAKGWanQQcyHuyOQpglVLWzssFBiQ_NoD77MZvZJ5SHC1K2EBr8lBdeW_u0PMcOswiLc_h0ozuIOtZvFrKJIlnGYoJnOze8I2a3SuTdZwNrgSUMuqmwuux2xP0YxEXUDWJUQ=w1920-h970?auditContext=prefetch)

---

### Step 2: Select Cost Group (Numerator)

Choose the *Cost Group* that this unit metric will be tied to. The total cost from this group will serve as the numerator in the unit cost formula.

![Step 2: Select Cost Group](https://lh3.googleusercontent.com/fife/ALs6j_EWo9W5l3kr5oMIJc5yQ0KT7oNKn73U_BDYrfxCLfI5r0Y2bDVdXNfF33XSsakuVb74LAPTL5jThZ1PsSJ6L4zAWyKiqqhWDiJsi20azERP3AWVv_85uwY8a0-4haes4w0m41-0dK0oSIlwqBjPyO2QvAISyV2NzIeZdaUJxI8FVQuqikX2hctvSFC_dANIMhCgCgx6IX7vbOymA8YjzDNvjk5tvL2XqbZON66TVDUTCAT3TS_Ube2bv8O8-JFLlMRPphlqUIM-q8tgMmILYjgwBHOmfZ7a2A09_beKDlc_2fTC1qoG2lNTdmfupg8ioRhPUooRbv2U0q05Lsq4A7bIyYqpryJVb_50xSmPXv2cDKPsLELI8hQM-aafb8kw5_v_QPZj637xGPdNhEKPcyFWfYnliMPfeB113VSzAUu8NFjvrPf4LYQOF4qqGxXoia7CFIx3Em4ut68VrocPI_HgR6D38MTzhO3FMn_c0ktwE7liriasEZF3kBGrp1Ddxcc9KBrxkIdfDcFc9jLxQtFDHitJg5r7nqBTsMc3bN0Ak1KNCa8UNW-w-DuqpA_Te6zj_Z4N_H1q9aVwTOE0-SqLxWr3iFEsDu7c51NV2t2hyTiW9LbCap0DShoBZ5ciF3cGoIWWFqXl8EqhuMIK6CgKo71yB6PUInbJ6JPGjL2aYf53LgKHZ7IyTZGCOq-MJg1k7qS79nJRo6y9CJRmknhReuTAXAgzsgAl9c0k9eDjxj0ueo-mbVdFoiMuCOwemvzB4y2-fCuwxHnp5yRBEpu8XdwvcHGb1IkGzVmE0O53ljJSouBXOUK5lqasZrXL4_yDccH-gfKp88U2aOE7ZtCEN9FnUp42Rpjr4VZOUk1pawvi3vJxPdIaB-Djwr0W7khxynuZ-N0ZejSeFz-qY-ZAtGoW4cAjyyEDIU8r880G7fUzpB6WN7O3zPCS1_9FfuWVLs3WJmep0QgXMVfenfh1KYiw-4Jgu70ZNShmjXOGO7HrsVUh7HflmMTyUcAmevKSRpbsLvAWzTPWiHUjIUPEZE1ftOU97nyW1HCh7wV9hIUxWtAagmYaiMRbDPhglzfxTXrokxGoES_ToL4DNkj9m_C5p-kd3GUyNiPd-ZDU5BO-15ciNM0Di52UaChbLjsQ0cnzMCDO45tpq9u3MKp_f9s2UvUOkFqtXwLFvIqbf9-ARtSiVP6WlwYhgaD04_n9srenS6Nhpf4oRVF8VqzR-sSIKAQoOMkm1eN1svEI8oXgMZbWz4pFNIkiEle2xBNPHkZD40g8OZ_gcRkNHNFUOvEO7RlTKZjw6jWj435KEB-dswDMTTy4EoKD5L41OY9e1m-pFth1bXcISyKQv9wJ1p09LEwiC3yuLjx4xdsvMtddTEgiq-Zn-jiyLCtezbMXfIeWzNSgAUpQfLlzQQASnrAzNBltmh0FbOEiXOuTw81CFxJPHFpTJmygtC6BBjYuTti8Y_yFo4hXRMIjjmnN0byF8gULLsI8ce0k5bpcqTz7f0aFrk3Q_ApupMJK-9XPgVNaKxsb_LQkVX9EALYqdjd-pJQAGYmcqFjTHA2SnhU_mOq1pXg2MgJl-yxi-eWMS_lCrOP0CWxU3IrSD5FVrO5y6zlxqLnHVWaa=w1920-h970?auditContext=prefetch)



### Step 3: Choose Metric Source (Denominator)

Select where your unit metric data will come from. The setup instructions vary depending on the source:

=== "CSV"

    Uploading a **CSV file** allows you to bring in unit metric values from local data exports or reports.

    To ensure accurate processing, your CSV file **must contain at least two columns**:
    1. A **date column** in `YYYY-MM-DD` format.
    2. A **unit value column** representing your metric (e.g., number of API calls, active users, storage used, transactions).

    > ⚠️ Without these two columns, the system won't allow you to proceed.

    ---

    #### 🗂 Upload CSV

    Click the **Upload CSV file** button to import your file.
    ??? info "Click to view image"
        ![Upload CSV](https://lh3.googleusercontent.com/fife/ALs6j_GT0MACRE9V_67qhqJ_njYMwSp2XDY-pCQZuCk4mB835RtzgybfHcfJNuybK9FQ8nlSsbJ0_LwLiYnRp-74UTyFqKWFnfh16_4LBn2M0Gb6ZgXsoZEfa2i2B4FzQDmmwNMj-FSHWbtwf7vdczIJIhZkgq8KvxQbCPfCN6Ukn_jbvld2YoJlau610gDwSl5HbiJ1AUVz7gKnRTKZDcqjTgfICXbyiis2BV1_RabfXtcIx2-6BzLhvTY89glgz4MKnTdE-I6xTLz1IhQHyvuxqmw0MAHQGX97ogFVorsdtmXrwK0pH66IWDnsOJHE-mZO4TmnfXoyXSbnpQ2UMjE65CLjaYI8a41weCbPVR2UNhgCjNFEIUuLLBpFUK_a44k8Q7YS0VU_ltW9yihEmsASF33D7j70cbKNFewZaKwbDvLD4vfmuyo40yTqKkS0lP42I13kqMMQ9zgFp2cZOkV7ppFE7XK9o6pt-eLEmyafyVkiWydrwpJpHIQlacq5Z0UxNqpXb2s9AH_IZVasWfd542YLKbcbJQHnSLLgTHXVEpaLn0y_n1gwHfcF526ZSOBURj_rrUwA5INrCjBrPox4-BcMsl2MdJhployJtPcq53DiX26kaRkc-4ha5au0wS_7Dlz0DLJ0tFpHm_H59atkkaAHADWMobVQYhmYWQdIBvTZEB50TKmMv6qzKtpbBWfa83W8WwCsMwja0ysOU-NZVcV6t_ugWyC82bxwSMAVpXao2PTmxCWGKw92SC1fnne7bPNcObxueJbM_RbjXkNyPtqIuYjha39zweYvRPOc1HXwk3ixAcQlcVI-haZEfYZSarxpSWEIP_OgGsB47LGHSw2EoiKPv_L7H4vQsGLR60S19_a-jcu2miYg4gMb4Fy-qJj0YAGot7V2uCtXc1Pfq_b8caUG3T8XjrxiC8YbceeE85CYRY_wMhVC0-KFM3-NUuNj0MEiZ5chPmAZq9bDPAEh04m0t_YL91q1FzOf8yRROTY56lyx7kF302MjY_tl5_SccrntyoYFcd8LF9OdkP6PABeYsl_nOpIQLc4ukl0Smp_bK1nfqITk5p3cDNSh2ipmxdc5bLThsvqZr3oXqKU0xCcCr1CqH6viAig3UhyUnVSfiba4qVjs3Hdi8_zoIARF-wkQ2XeyYj1YEBlkl_lDcrH1fHhf7ufvMf3yrjCQMv4mchUEBOB0tqGRWE37vRoXhaEQWeU7oXHZU3dhxnjbaurtlx5M_TUz_lebZFPF9USROLJ53Xk_hQyAL9nD6isoXXGt-eHeAceHKUUKF0uScYmS5B8RMENj0tUGQQ_xn7bfngksosRrlCBB7HYYPbK4NPUNImflxl57glQM92l4HA9ZBfNFmGg88JqrW2uhHNuRyU2KxO4Jdoabd9CI_dBHbE4xVFrkLNLEyv6qYqEzqQrQkXKBBs59zCgWNd3r3ziJ84Q_uHNAMOJUCLCFGpfoB1C6wquNnSXbGpk-rcHOO3csBlpj77TkPXYggvgQ5BeHl0pDuk3bc9Tujlh5YkcSMUtNDOu05IOuCGMpvye22tVMCJPqUr3ol_Ec8MJTO_f_7quSVKel3RIhjaxEfEC36KYuAYowcdBTUC3pvdGn0dAIcF5CkUtflr4Jpw=w1920-h970?auditContext=prefetch)

    Before continuing, ensure your file:
    - Contains a column with dates (format: `2025-02-25`)
    - Contains a numeric column for metric values

    ---

    #### 🔗 Map Data Points

    After uploading, you’ll be asked to **map your columns**:

    - **Select timestamp column** – Choose the column that contains the date in `YYYY-MM-DD` format.
    - **Select unit value column** – Choose the column containing the numeric value used as the denominator (e.g., daily_active_users, transaction_count).

    Below the mapping section, you’ll see a **reference table preview** of your uploaded CSV. This lets you verify that the correct columns are selected and the data looks clean.
    ??? info "Click to view image"
        ![Preview & Mapping](https://lh3.googleusercontent.com/fife/ALs6j_HDoLPLlpPxk8Jin9Eg7w9x_q-pHaabV3jIk-dbGMagPgFI0tqQitGrQ9pujzcc6DJpUxsAacsGRQpgt0B4CWLEpKVRJr5kgkB7CbVMn3DgelVjVDeqmnZf4vsTnow7_wvmjCEghwWtg9TfIEO_RrlRG3zObC_YeuHPoUx_PqszBI1QuufGP7bOapffZktdpFxb1Q5SsBVVYjbcqmcItZkrEc3yfs3_TYWVoCor4y6Md-JcNVDH7uUeFG6iWJPYuSht5H_Zl7RSUukKuQen8l_Tw5XsGiHwXlKmkKM9whh9Zafj9YxXu24CyTPii8Dfs6HyWMAHpvrNWU5yCuAE7S4DXH01GEXsVrcyBQyECkzWZY7kI17cS3IKEx0uEaNNG76gagpfMd_FRoPRCcKkKPdD_SxPTpYSc8z8ifS7SLivcYJMw-Qzpvq6vcEeu-i2YbXyWgoqBAdjejNf3btejzZbXRRv5Ee6E3KcB0597fJyEfI4dx4un7yizCJMtVueN4OpH9OcSf5d_kCaEJSE4wBvngBPPoW0G0rU8cnnyYQktzcxheqqu2ejkoHPf3rFB4mAq92D1EJ5fKhghr8CUj4co0amQt_WW8dPn5A14_r0h8X23Lmu_ODRPj1b6BWrvgkd6fiZTyNVv7BcCXWTI1W-GZaKcygTiMBFvDcsMy44VDNm_mnttJG57P96ydKlS78I8dqsNQmD4g-Y87HBqpuPWaqJv92itp9lLhMkXQvHKQZ2Sbma0-j2hqyi0jQQ9omgRDkdHyrzQi9Cnf3uiJLpio-BcK0t0g9GZ5JH4ZDylFmXprnqcPZdRRpWtiOW8WJzotN0OGGX_GU7uG7zHgNDU9_eAUuBE_ekb1u4hmNcxPvgosD8aHvWaOqb9moZ2faidqe4VwQNGMWVd0fWcWQwdc67qFfJ6HFaJXnWjtnf_FXPSIf2aP70OO6XtuVmhyU7M8pt6ve3FsHIgtyS3VSN8n_4esbwDBsfK9UaKKhkx6Q1DlQwzllqr8ouYZqP-9ImmTP_7_5VEOSDLDfHc2EeN7_4-4MUV5IlfH0ZAIMKvgxTKsOzwiyZWHtowIpIA_SYVd3IsWR27HqvsNBbbxPwRnWMVIHnInDeyymF8nb3jgpJZpc8Zn3C3OJ4D6jE9zk31fOV7Rf_MGnajMxRhSBrAxZm1JpeZXsSU0R-da-iZzQRtwkeMRBBp3ytJBCMHXdENrYVsNRlleUQ1CVSctvu7DdGouW8i4qG23MuqwLKCZg4wRT-5K2NQXmt2jJ3Kof4uaByJi1GYDhUT_c_zjHs5uUqIQSWOveM0jXQuUQEvZ77YHyJwItvcJGkjxs7L2kl5LTt23ueMN07gmJxGuLIQWeotqiB-Hvv5_k4_vK4c7an5QBrwkJvOGcgG68guYaDN2XEOMdyd7WczxfBHfj011pR15TwmF6TwvVb8PwfkUbdwh2HV1qmQH9rZP28RpRrPbQJtY7jCCRrd7qtq8VBsq5KVLUJEgUlyJYj0yhb1zv3Dq7r46Znv4oX5r2RslgT3Oneyl8zj17J5j5orbVHHWZ3GGI92RVRqCEJoLCyzt6JbApI_yA5GsuAD5Gm0ZdYavzFSEtHmsENo81f10s-WeZ-E0hm3k2AjiYBcg=w1920-h970?auditContext=prefetch)

    > ✅ You can also re-upload your CSV file at any time if the contents change or if you selected the wrong one.

    ---

    #### 📝 Tips:
    - Additional columns (e.g., region, environment, notes) are **ignored** but helpful for reference.
    - Only the selected date and value columns are used for the actual metric calculation.
    - Avoid blank rows and ensure all dates are valid and continuous if possible.


=== "Google Sheets"

    Using a **Google Sheet** allows you to connect real-time, collaborative metric data directly into Octo.

    Before you begin, make sure:

    - The Google Sheet is accessible to **"Anyone with the link"**
    - Permission is set to **"Viewer"**

    #### 🔗 Link Your Google Sheet

    Paste your Google Sheet URL in the field provided, then click **Confirm and link**.

    > 🔐 *If the sheet is private or restricted, Octo won’t be able to access it.*
    ??? info "Click to view image"
        ![Link Google Sheet](https://lh3.googleusercontent.com/fife/ALs6j_FnB8qWd-h1rpJUwQid9U-dn1Y9R-4ysUp28a7gOuK0R5DmHEKLxgd1VWTXQBBnBrVns5Ip6SRtL06XOBsR4jhI9ab9HBL0gVUft5JDICzoNQx_PWrVF6BPM-SxYZz5brqA6dSIq8f1widnplu66FWvSK0Vkgo3mDKaSxwqDPWBPw8H80s20zAQoD5nbT9_ZN8H19SqDQ8Vj5aoaapBrsEL01EAkYUX3wHTe6sqODIz9B9s2xpibW4kiFgskSTkMFtvazQutC7y74ry6D-Qtp5siOSkZvfGiYWB_kIX4JKAA19YBZBuMYXwZ8ZCia2Jk-MNKDqiwWdsj-yv_YxNeQzOyFVNYBUfuMVtSO_iq7zt53ewOB6gwXeIU0apDvTLbeK9sZDbIIbJq9oq3drlNrR4DRnp2y0iZGdWn-vVd4jW_JPjkKJbfLt2mQlvfeBrTMw1msmIRinGdaRnjr8rr4uV2YsJMxwyJ4CXTjXb_TZtXRD2q0YiKUiPPUDFtQrmdkYXMOzsJedG4pabfkJ0lGLy4SkHZGoY2gifE-mFuPIrCexFCRa_vTPELmv-KrQExkOemxRhLmfSST8y3XksEnagRD26iNnSfEQ0fBvnGw-2v5NGndlLMBLxMkVvKkSpuAmk49jmuOJxesuFgA0wolvhYKFySXz8AO-_JxGjzVJ_0syRQHUSQZJhP9VAs8gLMpdy0_lZBUx8bDsoBZIeDdoNB4zNRraVFHlh6vMjLGeABUm_CBozGwasSVufRn6MGJ1h3DOiZMdEvSHO11l7Nq3BpKHDvbF30_uHX70dicFxNhpTp-GMQOYNknGNY5z8m2HnCTpytwZKPvrO7w0sREvmi53gNEec4s95Ds4UwSnr4NAyZNOE8hQqfmxqSFWtrf0njEkTs6XQpkhACdIbVl0CnUitL4tOvYD0CycnYpM7p6Sap5KztiAgWI3II6tWbkKQeenrZHSe2v92jU_THzAKyqa7Xx_7tZ9TziAfUpjkI1rZ1IdThojefy-si6VOFuXGRgMSBN6oDbJvEEm0HtIpMnq86Qn_sM-d-KM4ArsKRftWTJjLBhCTOzz83UHQRvjlTrwGc_lg46li14nHP_Wzr1J-B0nBzLRoGz0XLojA7FENYqqbaFKPq-igCpnL_Yswjd1Azmi9whSNka2biTN74-aqxt8s0aRv_1ju3L_gUOeAhfnRBAMOnoUCutwaQuCdeweHuGpGfqD1PF7qlg6YcwkTYGRS7uNom0u9oMLa6prz-ZoJ9R6wNRX-6f86jcJAEMEVji2qxuGN5LOLeT_29Wytp0VUrWnuXp5wO5XKrhtfpOlW_RwY5MKs9T4Emy3LC_NMPdFgaEpBn_ap0MVcC-MiO6-Leslhb_6NTMWxNEHStnlZlIEwJnvS_ZP9xToKTGR6tCHfyNR1PJd_ykTshBuLRPTOJt7MqT_p0QW1RDXvjDxMH4DQQ040piM8sDSfc8n4-XoAdoMUiwVM7sLqaq2BgGu7eQKinUJ33typDsEkFPZg37wMisnTOuESAKX35lrp1xz0V93sL03KPs3yLKmdsAeiPQ_ENe6v9F05Q0UiD0-XbR7AREQrhmna6ETvwwDIcILDs7vWG2IrDjv8J9iaMcXHrL7oSrG9=w1920-h970?auditContext=prefetch)

    ---

    Once the sheet is successfully linked, a **3-step configuration process** will appear:
    ??? info "Click to view image"
        ![Steps](https://lh3.googleusercontent.com/fife/ALs6j_FuLtTgWnUk1UlD79qSYZi3NK0rpUFYuGhwRM9VHRYpKEEEjHXcDG5ojXK33LeGm4kebi2g6_yjUWAdjyZ-ytvslI58IF8F20gk0gmJYKJO9WmpS25ty8CSWj8rHZdi8zHJVzZZVpBg0CZEWgys5BnxLkKBikRTzgMf1ElaKrnUVi_fNcmks9egYkxWiJqCKu5_0cleQzKA4FhFthLfDpjAnMLm9daSgAbn5nnwVs0Hkq6cLnAQfD67v6C9SNff7K1Di4J87i9z1dA_OeteG7LH1_DFX6pRHV-9IDqemtYCOflgqBkqN_1ySBm-y2dCRGcZUXQbfOayinAptRUqSZaWvsxBf2kfCeVWgVwSGLYfrTkVWaqWlAs9t2hOzL-6NAiDvbUbJYh31hRKISUShz21sZhyUoBd5nYtaRVJnfik2AGzATuOG6VV_dGSrRzHmnFHY5LAEXFDtU6tUmdRAFdEiiz42NAv_lrNExUg6q6Kib1yPo-cQK9b2Ci0EI4VUsAVQ3aaEmxhjU75bHjlDbdf3qYeId3M5y02X6Q0CVqtQUt3dc9pVNVE_lX_VFHrYnWDyUExvyJx20_hU1Uv_XmwLfz5FHEK6wQTjc6hC7oluyHeryDvLSvADAKHTl4v1W6PeZnxu9p22vJnsQ_7r2lBHb8nBcYqAgxaVqb3SfAdkpii7kfNXDectRZ0djVgbJMhijgLVWEx5I9ov6DFK0o3eXgfFR_evJBbG6bm988qApjZmlml-mo_HUvITKksegZwV1P_aOam1TNcOQJXJIdoWZNPEwwDLahW1YC1zUbA0rP6tHHY9l1YD5aIwZeP2edXH3BCiUSHxb_caw87q8CjENDHb1XfVEcqyQnVLapVEiH6rYTja7HzqcBhAFkEpVsqaEs2N1NOq9rRD1LdWWnCsKDL6tUeaSp68DBDf9L1oCXXvUpNg190OpfSCGfcbG5OAfSK3oSeFQJQd20cTpUzuemKQKPgoXSvemGdcZEY88-4_W3qizudULH9ifVdfMNU1IUtochRlduNeB6H75ndFwHcicU8NuPeyf7PFQyFDzWQK9EUvtFeVsYFiObfwAekrFyY9kChvwrXSoBoosGdn_k09aumLeOf4CRGOP_gbfvPt3Yen3zCd11wr8weaP1bDRQdaQiXhgHouOml1vvwCX0gTWpIrOqQxW1lWHv6Uj81qKbz3I_fXt-0Ablk3MTCkmFI6zOkpXRQQXXE2TfRw7cty6Dgt1xyCKvl0P5aReS9EY4OvGx16M1ejUcaaGPO9TTDJnnrVj5nVlB8g_XQyTQwhMsgdMQSKo7SFqVQen1ceLVtBPhMgwbXGbAXDIEA_Bu-_ORgbR0boFdksCHe3pFZoeqf0WKoqXzsaP7tLjwoyg4mofgKBg3LNsdKcri8zGNcL-fkx7G4BNN7wz7ZGeIEIPrUf1tHFwdruPAk-LZ8VVMizLTIdiraI2uJtIDKDBc7tMOLg6OOgDE-6F_quPmnF_Ls8JgjkPeeuFHmAECLLxHXKpvBq6k-FTT2KR0BL08_EFh9znvuWsndU_R4R_WVQA-0h420I132beRnqB6-LtmUM7DfA1vRRKg0xwFADgjKLHpkhHjZG4HDQHL9_CVEjPiNfA6ZujVi=w1920-h970?auditContext=prefetch)
    ---

    ### Select Sheet Name

    Choose the specific **sheet/tab** within your Google Sheet where your metric data is located.

    This dropdown lists all the tabs available in the document.
    ??? info "Click to view image"
        ![Step 1 - Select Sheet Name](https://lh3.googleusercontent.com/fife/ALs6j_GXSOVDC_5jT18OChiYrPbqCySIvLmPvc1MRspa1ALBp--E6mFN5HMmIOYJkkexq87DbbOGJgynPSiL2Vgmq43ythSVmMMfMFHMOT8-aYWqalwFqHebYJ5iGU_6OROFkU3i-a3dMMpJcINR7N4uQ1qN1CdJq_kBpiFzY6-Ax_knDPwgXxKvx_-yv8zgvoYgdJI7axZd-tjk_2ghiacjVN5x6CYwFvTnYygWCFinq_HX-Lxpcbtcws6dTvBaRBUuyST21EpfAMhXRBzYOtyucEhi8hodEPlO28TwWyvyY23LgiqaBiDlkocqghTusc5EZyMcSuvT54KKBgnK2gsWI3Ub1IZzaKafokUa1glma-5xGWU3YjmarfLl5LXYGkgDPM_2a-PdEc967Z6UA53A8whDniIZJb-cj14RtMfs0wYBNTo1vSCaswqFOpBwaI11sDBECW4O8i3KIZSfMg7BdiiXhzchS5xhfZRl5x9fgMx_1Nxf7mLZJDumjBbbxEPFlMEhvREKJklDOKFRBmVM7b5HvUdZXIkvLKbIelFtqPEJ77HszL6xGq3nVfy2jYRet2fSFByvbuVztnhTHzC5OykBcNDCFsNTDxQFXsN7ZuB7HZ-htGAc7QxdC-FW590-DWN8oZ1R9dUct_rLfCugyBK-tvylv9lQwan3x6K1PRAmF1Dag8RO9_7ZjO_wMOwypHnJIcit56lyHPc4Rt5lT6BlGCVqt0qUukEaW4-kir4ZoKbUpSI-CaFmYN3d_POwuYCbGN61mlvwamDVsm7XOJnY75KoQQbnvhznmCTPbrNC99y16Gfaz_YdrSo_dlhnLHpJwOMtF9FHy5PxHE4vhGWuAejbzIH_Qp3mtE2XWPY8EXXougiD4n6saDLRnPUoRk27XueWJrlujDbBDqC2_7bX-LYMabfVrviSFMa-_NINPEAYy61pinZqa4iWW0O9hzkjhWkLBwe1A589zkOS7qMj-jgd3MQ8eXJKbnVQvZf7tB4b0IBOVKa5_cPBI5awSxsU-xD8azG-fL00HgKBkXOS677VAJpSONEvfoixBUoETYPPjJ_AuaN2Wv54A1SSEQssFvPf8s7CtvjjQby8qwzTPQeb0gow_Eh8lviqLeZhz5IbHA979Z-YHda8z5_UhGP_TG-OlrBIGGGsZbXi86FBduoQDS4r5usx4IhCu7Ls3EOB9bCi_2gCDbdMiwo--8QGm_H11DYeq_eI2_pB5qpdSI8PTu8U0So-qh70SpPTstNKGd-zj9--SKrC3MRPgTtMUx_OsQYaGVTZucLTyDme7WklPc1H_YEmXAhpqUzWAHXAXj-q9XZVvJyimORcuZO3Yoyi6UFffDD9ENA4fssF8S-kDeYI8NQ_5wORDwyhaowk6HEhToASXy9UNFk1jIhoKBdYXlOvo2w2V0004zW5s-oLqUmfTiDa0cJAnUopJ4-9Ip2dkv5txJTmMta9uUn5DG1HCFVOPIaI_UXdY5FkilIrDEptEjlin4tCypyeA7HmZrj89JKV2eMLosEqY8orUU9xr30j6RrMsY3uzEsI5D4sq5fevID9o0PRAvMAhpP-RaKgqkHJ6xEcgqBhR024r9LaHMwC_uL1PhVnJeGNWSvdy_4g-fA4_-Id=w1920-h970?auditContext=prefetch)

    ---

    ### Select Data Range

    Next, decide how much of the sheet to use:

    - **Entire sheet** – Octo will read all rows and columns in the tab.
      ??? info "Click to view image"
          ![Entire Sheet Option](https://lh3.googleusercontent.com/fife/ALs6j_GaGNocbOid0D2cubtTqIMi5p0jBO-dcbaclfAKAnOXtlsjwa-vsIIOMUDWCVWIlqRujzt4iNmU5RSmUtRZZ9mYrBJyUEhbEdBFRIF0VH_k_iNs1Ol5fxziTcKYr3ShdKs1VQujrpj5Uqk1clZSPDtThCmA9nuPf_AMORLMZeB4RAWAts33jHcZ0hkkbQbca_Lat02VuI8Se0C5xhzJN-oE5dKTm4yK0yRmMUFEMqbj-zx91Q5ICjaQ-XSfWnCG7gOrbjXJINIWRMy7TyL1jG84SIg49x1NdZW5x_kh5ycTW6wrvpZdFI7BL1Ca0z84e0yL-getvKWWVjRsV_LuniSaiSxxJQiG4z80ywxMafxSJ_eii-2Bl6zOSN3kWfjDlwUPI0XMef8gAKTuW7ZCVXGfPR7ODr6NX0QIlXofI4F-QTEOS39PypsGb6tq3fn1zIYqvuYj0ahdBMzW6mGzWyV8GhuZUELBYfKJL7h8wNDw4u4iMUjjxdMsf-o8VyHNI91JE56naPc91QKp0PGsJFhpLRX27KzHH909yNRSID6w1hHuNXiK2Xrw3YlT4gIoY4YCfixRPQWzM30gSdSDqyF1WWI55BInZFnq5D4LCCBk_S1BZ5PbuubQKTXRK5A9Qn2PPPQGP9ofkKtKIlrMSAZe_lBtfdlq9Vc9HSDquskYMaSKJ0cNs_fob8HPiZ2PSs6EdpvaFTmgFTrcrN0FWKAuvbPCzsSRCMR712CrxOx_UQ5iI2ezEQDCp652Vg4hMY5N4olmtOrmUQ2LURgIqfyeGzP7_Oiix3bAj5B1jx4MfLVJ6C8zBE-yKpArbY5Ya_fG7n9Imt_BQ2RENNXWue4BkggWYC3SywrI2P0wqhqK1QYti1yK3QFrK-0ZTJAOSNgJv-RUlPmhLCPSzOdUQwXF8fx24Iyy9A_AZDiNGX7Cs4_X5atyjm8WFYvD17hnYpKAepH2UtEY06gcP4-99fqdWhT7amj5BUHiVyzEz5NIamre1ndU5BxS-KnJfqqKskd6jTbzkN8159GnlKJNb1bS4n3NcNBJxOI140mQX3K5VYe4KrldEYioYvr0tET9ea-bC_9yJj3E-xHcAfu_WknHoUTb8B1OmBk3ifI5gD4SIPKvNM-zA26qUemwdz3vln7raVVNDEuyARzrLfWECaXRpOvvg22iiUxGmeR0ZI-EGPii3-5mFQmhcOnqIeh2vsNKgtajl_JKMxbmgQxvvjv_x4cyCemIw1FdMy0Al0_0R_Byq6y-YyZz8MPFxjpwLYeF8VXFg6zCqCxoOhkDYPpqddjqKriY8xk_w6nFgWAuMZjoOTVaSkINFT05UDvMfd4ZbNZ8WE44ZuUdrF8W5z0ORtrs37DGD16zE66wZhnIRIwACWRyUVgjwAKj_tvmTjrnk6_b6mHvMGKS-caezJA8oxbdMrsULgGi_Xz8_IfO-LHX9HiCufc5kAmwGaLivnRrzvV8Bv8mJRVDZrljk2eIRG8YUXB-1uzOoFbHuMZdIcGLK73-qTXbXXOjgyqrAXkYqHakCR8LAnMes-ExJbJtvuMrMX_mQVeCfTAefYoxPm7L9SD7AshyD27UEKEZ5417ddqhl0fCHZJuW8TC8COjpXZK6v12DGpvTBnB=w1920-h970?auditContext=prefetch)

    - **Specific range** – You can enter a custom cell range like `A1:E92`.
      ??? info "Click to view image"
          ![Specific Range Input](https://lh3.googleusercontent.com/fife/ALs6j_FoJ016YCp9FM4cGEIGhAKF4DIFDn0q_7Brh161kBLdO4bYiUGswhf3Go_pIUdInK-Y15JYaSNG4f59BRAOGJOkAZnQPUolL3Duf4dnHVNs8W-VoVnJ64kuHgdBRiAIujE99PtIumGPeGsuc8p3fogFGyW4X1SFL4ur-r8cdhMF5bYBAPIQe8lGXdy5nK90kPJHJ2Gy4wDWdNnra7bkU346nKqDmlWwjZ_D0gVQsaRuudtEhPVsV9-WmpO-sD6citi8dTdDddf8xU6MVQcYN0c35mwQkmYxOzU44930Boujt-qFSq7wvM4je2zPJDN2NqSWzbdBwVnaKkSHKhb8ggkEEocO3wHv36QEzHa5sK-S3JKLr1qA6MPOryYm9g_gy6vZj3ui7VI79emer2CKjnli34iRLkIYuCASpqvHpm3o2BUwb_EnZ_KHgbfnAaKSyOcNkzmZ0QTJ7yu3PsFTYNUHmDQf4LpI20PbRd88YpanZJzcKFHTxJew1Uw0C4yqNQg5wqKXKK1m9yfbeeyeI-NZnhIjOrSTBw3Fbqd3VvyxlZ3fZPErKrpUXBHaSgenUDMVsgENFYWPNf5Q6LN1dFqRn_6ZIGD0tz6obiWqO7CMOCxmxoMSFCM1UOKMpAjzwRnb_f3OJPmQED7REIGubKaHcfYmQSj6sjsmD58TkSVbY-Y0hlMbt3EpexQUJZVUsRchg0Z2eWhhfRzbZJvZOln-MxMRN_JC609uE3e8x4Qsb9kEE4kwszuWNlp0xrAJFm4AAdNUfwIEOe8nJTAnToZAFU9ehi01udqS_OlkT_llyTTusDmwifww3aaswXuBHGMJCMfwT_zAkpcKgW_JIGbL1a0_cRtsvgk22Q1bswYXAqUQHJgWPgJe9xJqCOofz0f4Wt5zesUsGEdgwcNePGgoKKvVuoXJydB07_IQd0zlNG_aX0J_rvx2xFkQEBaJJoreD1bxyQ1Sf6qx8b2rXyvvhSlyjzzapyWA8vpyHmuNy4pZ9G5WD_kr9a7-E62-UXXiTPiMAmZz-bHxZ0L79fVwLWLZ7IXEPulqlWisWH_uzUOsvXGoRDS7AKy6orFXjTgSLY7bs1nEGPkdBK-RSPlvnsIM_giulauEyhS7YVzXIJuNV3Pfn0CenyW0PcYj7c6v_Rk3nibJX_33q1bh_1r6zZwvNf6Vsb8uAHiM33V3UJDPBKmZeaPU7CJugFEO2ImFq-bfzkuQdLS5fWJNY1kwoHp10_2yxI86AEBUcMe_Wro-BnRYprZOJIOcUsq-XPUo4wuqGEhsBq7BwZLUESDROXlG50WFCzZe8ecBqOYQUbtijHKcuUwK57mFNVjj97zZng79118Cgb92xMUfZiJkY1R9otqKkiWLtpL51b3IXllz94bqA_xEAUUVWx3i6vBZI_Y1elo9c3Yk2oHBTGizXYkZ_UBGzTnygW5ZBlCaqiFj_A2SLVaXHu8SO3Yqyb-VadzELHVJ7OFJxDsPS9IEm9Pu5mw1OquILmXphDDmHhf20xx_fyMU2k9lLt6xdsxvweat_fUxkv1nVBBNXQPck-5qws0vXC272zjp-Xfzl5YW78GgvztWTd1u3mDyNz8pUQDt1fU21qy9L_wGQ8WIoN9XoA_K45cJczfaCQ=w1920-h970?auditContext=prefetch)

    > 📌 *The first row of the selected range will be treated as the column headers.*

    #### When to Use Each Option:

    - **Entire Sheet**:
      - Best for **simple tables** where the first row contains column headers (e.g., `timestamp`, `daily_active_users`, etc.).
      - ✅ *Recommended when your data is regularly updated with new rows* (e.g., new daily entries). Octo will **automatically include new rows** in future metric calculations.

    - **Specific Range**:
      - Best for **custom-formatted sheets** where your table doesn't start at the top-left cell (e.g., headers begin at row 5 or column C).
      - ⚠️ *Only the selected range will be used.* If you add rows outside this range later, **Octo will not retrieve them** unless you manually update the range.

    ---

    ### Map Data Points

    After retrieving data, you’ll be asked to map:

    - A **timestamp column** – Must be in `YYYY-MM-DD` format.
    - A **unit value column** – The numeric metric that will be used as the denominator.

    > ✅ *These two fields are required for calculating unit cost. Without them, you can’t proceed.*

    A preview of the data will be shown below the mapping section so you can verify accuracy before moving forward.
    ??? info "Click to view image"
        ![Map Data Points](https://lh3.googleusercontent.com/fife/ALs6j_F_XOhF2B0WE7kzqKjuLwn-jQOk7v97CkPmT6zF6A1ZnVNPhNMYIWGmLKeDV2in6xc11UR1pjpLfy_DKcd754_N5wmpqV8MduOKyg49V9OB5LusLbthJs9czdPEhOznQnqlb_L7rU0o5oIKTFEo1rvovvVDUAUhEAAInnaHdiTwrLIMf-9O8cg7xtQzDh7zMcL6asivwYAfOSTwKmRBeVBzqvQt8sDPY60t9pEAzwt8uUU7mQKVkGbn_KgZC7gyQ8FrGbYyq7S2wZ67WbTxvDy6VL7WYy40-GKBfdvOAsCkvYIndG4nP8o8hsearCIKjEn42fY3wq0bxAW3fhRjbLc9zNFeT1dcIBpdcyQV7gn3i3cpmUxRgHJooWQ4Hgt5MPfOjH-opO6yTAzjj3V6bxaO5Q2UreoJQn_gldrz9CaZu2X4aJudihogu6okG3jWf_2FfgtOyAl-5Kq5PJ94BIIoKomdLqoGKntp_WV7f7T71Q1JX-t-VJskWIfsAaX-k1J1__XAeTlTpIOm87wnd-2rYfmTAzQ-CYfPxvUjs7SR_DLgdN23A8gsVVHShhonPnryeDNZvy1ShoQvskd7B9RpDwf7bFAvku_abfR5zb6N34hsUc1EO8T7jquBnkcTPZD_FSO67aNEWroS4eECmm0PZfWWYFFRuBZ6QzSoo9HmhQ1aUoYy_07oMznm3ACYjwc5delFYrxrvTlm2lANMlYKm6PcDssirG56DtI765AMuVsKBBwq225SAX6q2TFTXiA0rrWPPr_d3x8hbBnajBhfVVfozIsmY1ftDUZJWbv_kpdo2vze88fUu1klTys67AG9xbRu6nQigwA3An8ynm58M0RHrSgZ9Vdw2y6-7io2bFSS1PFCY4emJOIIVg4OsyDljEYcoov3eVN6i1vovObBI_Zho0zGM8Ry4AkJrQmnCl5L3sgyDGMk63mVxmGHWNMDPAN4enHHJsDxR1sz154S_Wm5EzuPD1rjZXsLZeQeMF3yrYjabV6upTLxslSn92f5jRbh9Rr8EKQ2f8m-y4yEZNwxL9CCXQss1RUtxwjdjRkqho06sbognLUAW0p8tqH_gVO-47D9VWwRXH_pHWz2hVs11PZuLNXI2GJr3HalWRyTKGDRYVWAUraTMJnY6oca9qHIaWfsWRXq9EUm4qCjw2IVgWB494SG1rR2ZTLuMEM0fFbsgiUSBe3YBVC8-PSnz1FOXbk-QgAzxnCdI8_yJQMsMEGyHWPqyD5LhGeF5ezd55aKBQzOPzT21J13DuIjZP6NWXleEXzQvzrV_pl0WjlSSM8JU_mabONhS7B35usBjw1T0d9i_DRKVLC9OAr4nHlZ5vBitB9YwweBDuybJOXvDdkLQw5E88A7M3X4jUrIs8hlfgZa5pUavIgYdPnz2azCGAOkHKPZ5B1EWauwIWrehL1mb9cOYPukPDmbpNIUYb3SBpcN0v53EkmIcKj4GxAZs1JDkYQaS1y4dSX9AqEPXjeKGYRL_Wdn7HrUiwGmwDwAaX_x1h4_NVq9sGY8aGIEnR6NsMr8xcc0FEFImHsp4hWrdo9Jo2YEB54WVm0pZmyHK31DHcKyLoConQ2l4kKOPPsd3tXtDpyOiLRn58y-mJvMw1UiKjo0=w1920-h970?auditContext=prefetch)

    ---

    #### 📝 Notes

    - Additional columns like `region`, `environment`, or `notes` are **ignored** in the calculation but may help you visually verify your data.
    - Make sure the **date column contains valid, continuous dates**, and avoid **blank or malformed rows**.
    - You can go back to any step or **re-link your Google Sheet** if needed.



=== "CloudWatch"

    Using **AWS CloudWatch** as a source allows you to fetch live metric data directly from your AWS account.

    You'll be guided through the following steps:

    1. Select an AWS **account** and **region**.
    2. Choose a **namespace**, **metric name**, and optionally a **dimension** for precise filtering.

    ---

    ### Choose Account & Region

    You’ll start by choosing which AWS accounts and regions to browse metrics from.

    There are **two options** available for account and region listing:

    - **AWS accounts within selected cost group**  
      Only shows accounts and regions that are part of the cost group selected in **Step 2**.  
      ✅ *Recommended for scoping metrics to only those relevant to the selected cost group.*

    - **Show all AWS accounts**  
      Displays **all linked AWS accounts** and their respective regions.  
      ⚠️ *Useful for pulling external metrics, but may include data not related to the selected cost group.*
    ??? info "Click to view image"
        ![CloudWatch - Select Account & Region](https://lh3.googleusercontent.com/fife/ALs6j_EeMxF4Q7m-_rIcxY_UdYX35z_4MeIQoARWGpSV_69ZHPqeuW3Q6VhsltxHrVese2f50TjEh4wa9sGG-RRH78q0Q5uIOc0WsYCfMqXP5Ni3vuoAZ2iGbJH1N9QlcXwVpssMHRpM11xXLUUSxGedmJU4LZgpYckbYeOMIwWPgt3r-loUiNuwRHXhI3Yd0gD3T8NUHE_F-yLymtoITGQsfK3bN5APzMZLw241CYZBWeV4aoD-msyQeebNMzS4qJEgwwZ4KrEflb8ofexUGDvZQKbqP0qa7fizttStjRkiLzaSRYbqdT3XtL7GlTDJDBLuTYoqez9R5vwwiveQX6VckhR2Iee_eLEU5Nys3JEAIa4IcHR082YuBo2QUP_DwDSVU3_yuWcpaVsoQwqJuEILPNKyevFcAfUyKPYhUVEjHUVUIUH__FMqUL2HB3El49GcwX6fLC_J1rNCtSCXux8xzjJc305yq1R58KbW2BUsHnneB6LklfP54SSSnRfUVOaKw9mPKZx69lc-vwHc7yMqszpRHV3b2QRatz0XcjhtQ9eCF-EnA90BQVeaUAc36TgL5EbMDLAPP0R9F401MCF-3IftwbGZzjzaUfvfqzO1e566jiEWQH1dRVb8lrIzOXxhjcEtpAAd0pmYdUd6Mm2KA5l4Ce6rc4ABh74SOpdZ3BNi_m8SiHV1t4LrnoriO0d5_2B7d2ncLxyoP_UpDuiYrNx83szgoj5tX3F1lX_2VLsBBH8pTOYKRZ2jZ5pkZ6GfaNYuAS22ALi-4YrzNnhE_kv1tSKk76u3TAAtUUCq3Jb17s3LIt-2-_2cA4eGp9_COE-OViT3VbwJLPxw5PqO-QbWRVmebS6-dcmUiV8BNNW7_asp4lxOMbcDcfa3A-wtoNTIT6JmecR4aRk0jjZmRw3p5RHFITE6aiJ8fx6vaex1RuALLpriIZyX8hsF-ieNZ4RdQT3nbHBh5wJXCvDVysR0UOsE5KiG88IIDZZrN-c70fUfnBtu3Eq9C60a0ffsTodbXycWe19JfGk2CdyCqdUtqWWi5wm-fq7A7qjlvbE45hyfamQunFH2vAC2mlaXymqDMk6m39kmWny9iW77cNeaCickTYg10JrUmOnRzEpLwhoGI_r_isgv16D0uV2Cw0a8-GvoX9-wbsphQBnr8hxKuUMmKrG962jEO645EpkMZtAGwCV9FiEQ-5b5hoMfDBxA3Wk6dBGVXuVcDYA6hpYaHgrIxOtoTOO8KPM-IyT6l1cT3xr6dBJD-rEB9hiJHBnyQ1b4MPKVa9AwNqTRkJo67itvhBgjoL9nQJ4fU_1eDxsd2C_FwQOBrwZiG0JuJ6PgYv1zhUYoZJnjaMGJNqWpU_ifrqulbTirGkcg3GzyCQc2RZsvvs7-VO4n4ApphiAK4sQ2YCi0g0SsOj_Slq8C9gxQ7ak-Fzv2wzBr3Ht3TsbRp3b11hwqp-I2dFeNgVRjxAOeYFNCAgDycxtRKLkvxSFrwo7B5BRLBJPH6_YwQhMcJW7iD0ONbTFJfR8TFy_SWAOcuEXkO7Yc4u3Cti_TzeRVlSHtGxN4u1QvZdzfFCGXJzV9v0jKP4LNahjyYW1cnLteasrdOM9qEssExixiZKoCSZiEMgdJGQKYhw=w1920-h970?auditContext=prefetch)

    ---

    ### Select Namespace and Metric

    After selecting an account and region, you’ll choose a **CloudWatch namespace** (e.g., `AWS/EC2`, `AWS/S3`, etc.) and a **metric name** (e.g., `CPUUtilization`, `RequestCount`, etc.).

    > ℹ️ *Only namespaces and metrics available for the selected account and region will be shown.*
    ??? info "Click to view image"
        ![CloudWatch - Namespace and Metric](https://lh3.googleusercontent.com/fife/ALs6j_Ew1DGmKONxebIhCK6Q4PaPa8a8SkSkRagTA9_N9rjTAz68w2et-Wj5cbYS30joiltuJmw8ENRx-mR7W80ngu6IAmd0YyH7Bhjf_XFhnuQCo2EHLjs84eJ_tcfV8BxqP4dGxNNpbGf_HFa4ESQ3Gu6V46ewNAQIpi00j8fcLNXMRAyhdhS-y_bDZ6wQQlgRqk25E8nl6KbVPH4mlcbQlaUeyggV7yDmEFNirJiK8_OWgWmc9rtNhUYsmJwjmCRpeUpmcoy0nu751gYe4rfHX-sofVtkHnKiUFnXuBkWeJDiA5Qh3lPd2n2WhiDhZUpGdH7Blll0VwdzNb9FmAib3bQl_LRYRY-kfj20o9vEdBRwdxYz4P2yRrKqwf4ZXZmnDTkn6fQhE2hfXgilG6cJP_ViwnKeWj7OZQTQuEYuTWQL0mwYgZMrL6ZtQaf62Mx9gXQ8qiIgr_zJ7fFRBRRmx4XJyiJ-T30icP39OyGzuQD0Bu8r4BLiIUHKVMnwu6zo95oiNL1V2Xj4x9SkIm6typDvKq4yMmDUvoB3sC45m3O6WyLyMgGTK_HBUEtfnkZSaIoEQEm-TjbLHAEcoZNdE2WkyfIn9rOihtEvfVD8THwaP73oDcw09J3_fI3ppeCSWXfEzu2p8rZGdLNOfLeBvR-Zw6m4tar4p4IG8BEuv7g5-6-P6q97LKzamsHiiu-nzuUFkRgx48Jbtdc21rAHgnY0OMZhufsCPKxJa55bJSNJun5gccwmHn4U9G8wV0Hdi1jLkxGaVX8Z-Y_ekOGFuHf6Kvt7T0FicE71aRMZ_NbMKH4Oo0n9zp2ftDGpM0cWckfdnwBNhuTQTEs8JYtx0EAUemCGDRd6vIHlofbRw8-M63MvUEBcLnMkMmgFTBdNBUmBFXPX0mXHpnWGCYCp13YAS5W5JjXuNrEzHLmNVZ_d9ZZ2rNDoOXgzmj4gI1A6gZgdADyff2rRoFaDndZ3_u6aZT_IAdApxO9vm_CPnibtNg0R7zO8CT0jh06ojXpK536NmaY16URHTAK_10eXOJVTcM_3kd4LUHii6FfFGq3jkd_GMwl1-Ahh809A31gCPRTKbDEJASWT6Yzxcs1C_I3GX4NRg1woo7m5HNWv7NWv66BYyW9rSiGcXfZDh_Lxji7rvCL0kctAV3ihFP6kFVaehU7TIwazuBmzrsVzP-YjfmjFTRkn4NSDSQZ7bVA97_O9uZsSwwIsARjx8lG144md1ddvR4qdRLCc6Lbz0MBvNfPhdgaeVFKjf3OW1poQKzb4zzdQPBRewZFFwJvsy0CFMqAJcr1YH0LA-ArfUcssfZYROYqHzsnxNmVJLXAaqgcD8a8OBcEpwUCtHbr3u80bAiqGbtvXNbGwLF8afxHmCqJ1hDts_8JpxsbTqnoup0HH6BtEHu8REBPtUESYFE5JxlNmah6a2W7OwtUkxT8MtavIdUSjitgRkaCU2JTqUyZvavvXQ_rJZ2aCT_0vxQdpC1MZAyyixGxjACfBjujBxrLeNN9mpVpQcuORzzljDwVIJ7Ig17cAQrm5e41x69JwLYRO4IkPw2labuHlGxoOfgc2gw0HFSLbmsI7eIfY9TkyXTJ9y2D9EkQ0o1jQv8TL7y1I7zc2gBzM73eKzw=w1920-h970?auditContext=prefetch)

    ---

    ### Optional: Add Metric Dimension

    If needed, you can refine your metric by applying a **dimension filter**, such as an instance ID, load balancer name, or queue name.

    - Toggle the **Metrics dimension** switch to enable.
    - Choose a **dimension name** (e.g., `InstanceId`)
    - Choose a **value** (e.g., `i-086b2069ed24b542b`)

    > 🧠 *Dimensions help filter metrics more precisely when your cost group uses tags or you want to isolate data to a specific resource.*
    ??? info "Click to view image"
        ![CloudWatch - With Dimensions](https://lh3.googleusercontent.com/fife/ALs6j_E148_NpU4hdeK_dbS-sJWmyMYkmeht8-VOG-UkyGl7zpqiiPlylsei6cNDmZZnvFExI-Iy710A2fPTmi7LvCcLTD0b-UQ_aQL_sCA6nOYV_4I4bfWApdSGkaxGoybxu8lnQwf6L73ZbASLjIfhxYNS94OE0qTVXnznqzQf_w32FovPVQhTFiT8kfgrZUWsLVpok_UjCrADeh0BC9gkF3KDmqWkllDGW9eO4bWJfMTwo4B-VUscJSpak9SQY0dTyk_zufhIL6GlSCVFua-LP1okvsDDD33Q0Zkg9sKIldlgOv5d3d0LH7yxsbXpRaXMB8tjIv_lISmJCdi0rXnFKcZvstMqxKAATsJNwjgs8GfMChrZ94U8Goj78OqbR7COoR4Qvs2Yma_OKOP7DoUbsWGVrVUshG8yBfyZBDpmPChKuQHhd7bgrEN_f30ry2g0YD8MAuBIByaDrx1XYXlII4YZKJSNS8ETs9RLq4hCsXLMOLkH2aATw_cTm1QsdvDzfup5DT9rpT4OrEM0Pn4rqvNyCooueXNXInuHyEwY8ayqpNmhicKiQCUWclh_S_AFG-nC00n7Z63FSIQapvxKkCr-FY_fpT13HB-6QMpvcd58nIs5Qj3FHvyYB5-ZHD1S0SMBp9pJXW2N4lK5Ky0N-p8jOuSa79dm2e7Noo7_KeceCMgGWNaYZLk3Iz293H_99MaPGtZ4ys3tQPogrQy5NpUSBqVRo8yAjK2HlS-V0MmW1cq70M2TwWdRgHSVsNtkqG4lt4xAemDWktHSBIfq_MQr6ZW2OztmsoxVs5yWz2CJI-sgkcAVCVkUta1nWDcKLU7pQwzumq6HfeLoGMUG19as-AP9oeciTfUSd2OIxnP7JwL2hO8AlFmw224TM9eZ2OC1Wzss8b6KTPEPQmaEQTY9A6pwf7ebZiGPJBwZ5-siK_lCNEzb7YclePP_fiZfLdSXZ5r4Di5BNrCafTCXU2GVgtls5cJ-YpPB8iiWNwzgzJYH4fwK2ahiQRvdp3qf5S6QZQcwxEKqCSfDNh4mb1_zwXB_xXW3-cbHA8jDWBYU_CcQ1GA-pgGrhjhODYcKiys6Ph53wYVMAlPblnyAaE_2kzrJsqn9OtjDqzF5tzUVxlbGgNFVuLc9OuoZCSMlCkVoIGBo0ulFbtxw196a-PC7l2vZn80Gsb-P7RnN6G-PeZqdKq4wjk65PGctocMGIex-nroMuusuuMq5PK5od4bI15vhUoubU9HHFQbv6I5VEX2DTFyAihT9GVrJ13on8zF9V3ZPNIRykZMrKCPwEj2E3eOIIkzSpFbjpm781uOWhfyoBHqgNbu4LkCTZ700sPubnMYjhr_tvU0Y3DtpOu8lk0bae7lCTyyP_55Kv1BHE0GJ-adrsIvDYM6Xhxng5FIb3uRdFlzcHTNlPSt66UhcysFVU1_7SnyD0Ff_j-cMYd409RovqE9d7W1ynwikRUpQEKC4N7_uyQJLAvMYmTceFLIfMqC0KhgeSVE3KFnaTuvNlIDFIbuIha7nzHSAhTX_idC8lgdhzwlkepPgn-MnLcR-Se8Cqs47eHZLvL6P7qnQeo_RJOfV9wP0qcTlHcLnzM5of314wNZNXpF2BzEINRbqiZC1orGo3CsG=w1920-h970?auditContext=prefetch)

    ---

    ### 📝 Notes

    - If your cost group uses **services** and not **tags**, dimensions are **optional**.
    - If your cost group is defined using **tags**, it's better to **add dimensions** to filter your metrics more precisely.
    - The account/region selection logic allows flexibility depending on the use case:  
      - **Scoped to cost group**, or  
      - **Global across your AWS organization**.


=== "API"

    Use the **Telemetry API** to stream metric data programmatically into Octo in real time.

    This source is **currently under development**, but once available, it will allow seamless integration between your internal systems and Octo's Unit Metrics engine.

    ---

    #### Status: In Development

    We're actively working on this feature. Once released, you'll be able to:

    - Connect your internal service, application, or data pipeline to Octo via our **Telemetry API endpoint**.
    - **Send daily metric values** (e.g., user count, transactions, API calls) via authenticated API requests.
    - Automate metric reporting without needing CSVs, Google Sheets, or manual uploads.
    - Enable **real-time** and **continuous ingestion** of business telemetry for unit cost tracking.

    > ⚠️ **Stay tuned** — We’ll update this section with full setup instructions, authentication details, and example requests once the API is ready.

    💡 **Interested in early access or want to provide feedback?**  
    Feel free to [contact us](https://www.alphaus.cloud/en/contact).



### Step 4: Aggregation Method

The *aggregation method* defines how Octo should group and calculate metric values when:
- You have *multiple data points in a single day*.
- You switch the *granularity* in charts or reports (e.g., daily → monthly).

You can choose from the following aggregation methods:

- **Sum**: Adds all the values together.
  > Example: If you have 3 entries on the same day with values 5, 10, and 15 → the total is 30.

- **Average**: Takes the mean of all the values.
  > Example: Values 5, 10, and 15 → average is 10.

- **Maximum**: Uses the highest value from the group.
- **Minimum**: Uses the lowest value from the group.

This aggregation setting ensures consistent and meaningful results, especially when:
- Your raw data includes multiple rows per day.
- You're viewing data on a weekly, monthly, or quarterly basis.

> 💡 *If you're calculating unit cost per month, and your unit metric is uploaded daily with multiple values per day, the aggregation method controls how the monthly total is calculated.*

![Step 4 - Aggregation Method](https://lh3.googleusercontent.com/fife/ALs6j_EJ0Qvq_ft6cDvRSvEewbh5e_-kPvvHdqs-_kIrKXpCQZKvUygUlaqO2DYx3oUTgjd_9zpChD8Xm_BWViwEGHCQeDI6adh8sx8Io-YZWEQkXsK6oqup_-g2PiwMZohsZzrkxzirAZGmN8kne4FORkFem122wckjtjzzCLCo57umDB23s4WgsmmgeVOUGDNu-iFqYq17NVwuv6rT8PSpNQWfo029-wUyvrBgNmtOsKIt3VW5fUHB7DGTtoBw-1ANB-s0ZhFLiz5XAPmIKFjC_xNMYZ1Wx4ynonsx7FWoCn8ivt84oaWYMrf8JPULoNy-kqRVrNxgke8lWc5atprIMKbbZn4BqgDqJOb5LRelYbUcoCWXI0OdKcDcee0SzdoWc1JJ0g9I4aQEpNBCPekPgmJcnI25siO2CbqN7u9Unsf6vCtyMh_tIrZ_KMi0n516Nv1llfeaIOCWskZbVKjySHcOdwwtYE9OoBJbLlwvM09IuE-_RdX2aKKQv1J7StQ2uQbuZhrRnOrYLu_wZ1omK9JCcVZPYeK9jRjrv_-MGY5TLzGypbOSFN3NvP7dDaXkynt-kCqxBYI-OqPFZMUiSicXjuA_FLYWyy-BW8DOKCLCfFxFesCE1luQpP9W-Va13egPw_13EXa0_vIV_2Fv2GnBEJQHGP2SBTvV7xR6-obGZkn9DhZf-2PDuQaHGsJtY-AxQ-h6TQaoXTVuOZavwbGZg3YDOuf7ZCVQojdra18HMsU53CBOjC5Csx9CEZ4OQSpK_fnnsDx7myjba-blOCR6B7zvROcdNM95HOuhK18tIOyxuPuowqiyBWJNlqO4MNiBAoPJqctQnovqKIHjbJDcii38sFyiuatEmjMGFfu1FdzmH1Ey-gmW_-KVnwFmo3G9E8Wule-Q-jUyGEbGyTW6z3-60ZWQVBfXHFZxinBnMyjS33iHcwk5qw47njAyY5oe0JbdYecRgcCk1WSu971ezolkzi2XJHFjxkz3jLByeyZCSv_CEfOxFtIbvtZxd_BQxCHgCOWSpiiTNjbvioQXFNEhTZXUwJrCWsl2U7M9JeUZB3BK0HSpU2OIOOEqRQqbvG4J-1hXwdpHvEfhpADexHRAiEK9PyQgXq6Q-9KDRFW2UPAE_DyDeb7-NqA3kMaFMQW8uEvlZesU6XM-bGh1lrFcb_Knmh4z8033jlKSzNAcy7RBkqa2XpKZ2VrDE3F73Ur2JbGRvApKaMMC5X7nDZpb07ANFD7Unxh7f5PZOB2SvLXzztQNUayb3RSIPphetxvO9OhiMD9k78NvytoyiNMejFEDS6IHLIaSq6app1JOgghdTnojl1KNtU52vfFauoA40OqNeSSX25nXZZv_okHYuXsYaOrthmFXQIOtWGMphSb2HLTQ1XoteXod7yrkfhEN0Sv9VWrzZ-hkVYVWjcsr2rgoR9j9vvVuhZ7_46Hq78RzTlSUaAMREJTDa782KaZ42Z6q4fqByYujPTaOUTTJt9QK6ggxbkWU-jM1P6y2gafEAXeScJtzQCKw8rNZtxagpvQwbnrs7xLL3S9zOfygQ9OfC1DpJ6lzySJQLk6h5b5AdIiTO56BWc7W3_qvb1JXwJkV2qQl9O9KMYoT2dkWmafYEbSDmr54=w1920-h970?auditContext=prefetch)

---

### Step 5: Preview & Confirm

Before finalizing, review all the details you've configured:

- **Basic details** — Unit metric name and description
- **Denominator source** — Where the metric values are coming from
- **Aggregation method** — How data will be grouped
- **Cost group** — Which total cost (numerator) will be used

If everything looks correct, click **Confirm and Create**. Your unit metric will now be saved and used in calculating your unit cost.

> ✏️ You can go back and edit any section before confirming if you spot something that needs adjusting.

![Step 5 - Preview & Confirm](https://lh3.googleusercontent.com/fife/ALs6j_Hyjx4QA3h8U8rR1f_dOjqq-O4alcpaxXso3fqdMtPLYdVdj9M32t3l2DOSwYh8QBcY2eAFM1mmumTxKtz_a5pSuvWHsHvMbwMFFcJQ9-t0G1EYbq4OwEsTnIm002vaXwPylRdisJXCvdCxjTqPZwo2LgU8GjZ1_4kRQ5XeR63Zf8uNNw88ToxGb7mBKEIJkqyP5vZ3xFUPW1h8KHLJe1oZDqOHoyF4ozt2ZGWbjtpam72ozHnTBaxYxovDFLrn4dMjDCsYbXd3XIEZDvTroi221chM8oG3exiGcjzw4XGIUEu6agkqJOM0ZNCxnl2nBklN0c1lGym08-hc4n4tQUnq6XJ_hCDgpmgpGNyaj5f4WgJiETMuvl-29RZMXFkUF0SwR_xKKrzmKqTu676gpJ898djLGfmSa8dTh6BfZg5TbvgD5Ta31ibKfnuDtdNuuqrI5WDmE27FzuK78WTtSW_8cp_6L9-LDysRUzkjxMEsVYGgXG2Nfw1IOpJ2WmdaY0xcRM_JaHVFEH3MVzz9W4F08j5xldC8TWDQrEuyZ1ZoaUnOC1-0c5EFzywj1HNYXrRoQf9rzXEYk4pBnmlpvM6E2ELdjlRFN5-MNCaglO-vIEqOr7ADjYuiGOQklpy8gHz7osfn2wUqiJrQVCDEf78f1V-RiurlxM-JpLXEFSTmOzN0Curm3sE_LAVc-cZnLOE7ycBYMEfC5MvsWK60s26FvvRiLtJpDcK0I-pMgZECd9obTOaz8934onFAsJ2YuSEkHoO68rldkNUcbKU8QBEXVnh8VjKqF7A6eqMkF7TEoDzE1h3eIXWVWVPutdi_KqZXsOZk1yFDhcoltic7ftrxwrj1W4-FiEtNSH4U8mEua5HDAbsTdqCzVWd2Zeu4y4IY5WwVxAt17LrvR_lV2UD0ZmKZhf4j0uo8C3os3OHwPHu7O3x96b-RIKALSIlbJuTRVdAZKVoGozJYDSsg9r4QK4tI97P-OeMwUQBxBoP91YPapfqpQ45vks5434nitaJqrnN4etP_omOfU7sIuq-h9V_k5u5RHfC3KYXiFNrRuY76-IaRPfLSHW2mRj4FG4zH929kHjHAucMpoByqv1Am6ymU1DDjtStonVhqb3rtdhNPXnSdLtz-ENTerbr13uQTRuIvQgg1digYWkUBGmKmwgAejzBodHt-v7RN1HuhxtaddUzznCggIGHKVf-1VZzGB9CzHGp89aOOO_v0qPbj7udALkExlhV9ihc6RMe8IQQOkRqa4Mc-NxZx29IK1aD1GR-9YWX1Lx0AGnhSUHicefK3tkGKG2dshVKL-XNDmeROXcx9LjEzOv9b79_k3WFWv7tCn-Qx5XeLUXSMDigeDvgXOm2cYulRpokk_xXasfjm2SjqzeEGKI9RA44Y-PHHZl2d1OpqcaXeYrjRY0U4hdprZx2FMcqdUm8o-w-PElcyLBQfTKD877hfWZ-VKbNNAJld_MB7VvEuSSz569zyyYM5JOte5d7lVQw7rVItNKttS0vIFsQDidKJRXFsYMrCXFwOGF2qhfW_r9zlPbcxlKM9GSIJyEo1Rl6Kn33kNFeRjfYKIaZUWoxOue44yS5IjBDXARYr_oVor3ShUcL78ag6hvm0yL-Wm9dt=w1920-h970?auditContext=prefetch)



## Viewing the Unit Cost in Cost Group Chart

After completing the creation of a **Unit Metric**, Octo automatically applies it to the selected **Cost Group** to visualize the **Unit Cost**.

---

#### How it works:

- Navigate to the **Cost Group** you assigned during **Step 2** of the Unit Metric creation.
- If the Unit Metric data is valid (e.g., dates match and values are present), Octo will automatically **calculate and overlay the Unit Cost**.
- The Unit Cost appears as a **red line graph** on top of the bar chart representing **total daily cost**.
- Just above the chart, you'll see the **Avg. Cost per Unit**, based on the selected date range of the Cost Group.

![Unit Cost Visualization](https://lh3.googleusercontent.com/fife/ALs6j_EWuQ0aR1fooIkwuHBPwyJKEBBiWkF7q7C3t5onbg47GuK87OnVdoql4PbtdPbvvUI60wHLEWi_7vywEJZfD_ECWP7Rc9FX9H19VfXv4hDddmm4ha7jKwllHzbE5nBEwdEtm4dQVw82UT4NnT3LZVSPqXEEr7u6ldvZDPTDCsckYS5_zWBeSrD4h2VgTZRVGDrUVXHDywuYod5kc2_DpYp2d1l1RUlX6Gf1tKjQ02h4Nx9HQ4bM4Y7nIpGjC0FSdoa5AeholHvEB-7pXFgmp1Lw7QUXSr_pJrooGM31BHkM6gruDDklVDEB4GnbO3H6EYjkUg8vaOoTvKuM7pGm9Tl0rNGf90uIUBipKDXSgqlNHmXFMbDKwzUEfURvIL7tjbgXtChFt9QDDbO_mg7uuEZIkdJwRTZAWZm8KsEdGdi-I62Y7Nsk1siK9BuGIPGCaokpOL0kMV0nBkGVIHKTmjIDbLg3wBSgg3D614dHsZnfRZTvIVP52MgvDXOzu15d3IHyQekyl6AHX4Xs_gyod8ZXI974tudzUbltmKQjpI6DEGSr_2Nld9bGU90jxeEu_F4lHTSsgvefdis9Zsb7tVT2uyONdwbjuskBs130Gh4cjd92Atx9W26h_GvmLSfjtuFkG-gxKgNMYuPTUEn4CKnKfQkt8d3I96usmVhbJJJmJkkFHVdptC9_7Wk-jNiwUA-OQ3m3N0SLcnX-8BBW6KfQQ_pWCaNb__3Dg66Ly7rvNme4soUxjIfEyJb8Uq8_G1EvQgPXSizLFEJj9fBCtLoBAo6Ugsnh09ZRzX26B4ts1WHM4dfwhg7fOX6nU3w05SVQbEvCfW_sDrV5Vl5lX479wkWXl0_PErl7ufZM05MtZ_N733UicAiRJulbPwpojcPXvEbXp1hIeIlGwGwfUPNihwmQqMV3ECi7D203e2oUt0l1iJazTLSuRr_ks3KDC8IKqYstJ-Mn-BHP3Zhxj-uX_-2P_wFfi-n6i_I1yAQnNfDiI-yJgQYwLYzhsw-FjrsKyV7YSxmFBQXWNj6_em-cVnuHBzZwf5EUeXeg9V9UOmS_T3c-OfLGL_sifLARbF2CxyBbRlF_2BMvfql82DMoQLCdx3xgS62ttgnflMCzLbO2Qhk0nkkBW0PfAMEmoTDT_gk-2YQ5KcKCwQ3qQ8i9wpC-a3nZ2LZY4I3ndQYVISLa_yxX8Visw0Tp4R5vy-rTUPklhdzLU4vtBMJhnP0MjvUgHtuPuJinmkSMYxEaoLLr6abk2frtPlCfLPQSLG5rkOuc-zrCxtpqlb-VlosZUKkFmFIFTwsfxUKk6mWYXqe-wD3SxnCUuIMMqgK9-Dd1doovo--hBj9yWVVHKthoEBEoJRv3lcKuw02K4QW5KIj029jqMu7hfINYbDYnzWeBMF_I7vROAw81RS8-5jZ9zwgxekREddCRapTF1Fak3TRr1EbSVz7jqcuBcvrrg1AFjjHia-RatasnZm2Xh11u6mBn00nDpdIBYJGZoo0JlQAMhz2MzJ88jgkUOXL495tE8vB7XBpvaFbmGw3jk1LL_rxBqZIG7DOORl23GK_wKZ6bpzGe_67dKxmVZ1FX5KMagRHaTrxK1tfquK1fK3LI6Lr2Xe4eBo5EQ1wutw=w1920-h970?auditContext=prefetch) 

---

#### Example Interpretation

In the image above:

- **Total Cost** is around **$597,378.19** for the selected period.
- **Avg. Cost per Unit** is **$8.44**.
- The red line (**unit cost**) is **declining** over time, even though the stacked bars (**total cost**) appear **stable**.

 **This is a good sign.**

---

#### Here's why:

- A **declining unit cost** means you're getting **more value (more units)** for the same or even increasing cloud spend.
- It reflects **improved efficiency** — you're serving more customers, running more transactions, or delivering more services **without increasing cost proportionally**.

# Forecasting

Octo’s Forecasting helps you **predict future cloud costs** from the **historical spend** of a chosen **Cost Group**. See expected totals and trends in **daily** or **monthly** views, and quickly **compare forecasts with actuals**. If you already know about a launch, migration, or seasonal spike, use **External adjustments** to set the number for those months. The result: **clear budgets**, better **commitment planning**, and **early variance detection**—keeping engineering and finance in sync.


## Create a Forecast

Use this flow to add a new **Forecast** for an existing **Cost Group**—you’ll pick a period and granularity, optionally apply **adjustments** for known events (launches, migrations, seasonality), and save it for ongoing tracking.

**Prerequisites**

- You already have a **Cost Group** (forecasts are always scoped to one).  
  **New to Cost Groups?** See the guide: <https://labs.alphaus.cloud/docs/octo/costgroup/>

  You’ll see one of two entry views when opening **Cost Group → Forecast**:

### First-time (empty state)

If your org has no forecasts yet, you’ll see a welcome card with a short description and a **Create forecast** button.  
![Forecast Empty State](https://lh3.googleusercontent.com/rd-d/ALs6j_EXVT8kGawQUDTeFTRCwBtN_L2KoOMecSXRAeKlbCAkJye1tzrbe5nb566XgjC95HHpZC85uWji8pi2dTOVBvNTE5-uyfnBaZJIhx8kl6HX2lSaiHLk3XhxdJ8JpeOrQbpj7S06K4UYJJGmpUsNb3fUimWnwD4cbvbOoryODnuwjywUwuLXiVHFCdN_zuXDfX7k9RwpXw6lP5ZAGS-uR6CsCSXuKMn3WYTm9tigZRYXVEePlbHFQepASt2ZaBV4nMZqtGYWf7HMr46BVbwTOmGLMuKRxNlOS1vWd838uyeVGPKYzDz9Nrk_Dd1CrMsKwgf0TDwkudzaC71IzfHuXxbnG0OKOZ8ZXTZJfDp8pSnJVAZbN34XLw3p8MQG5C6qbyXPpDMg1vKLJ7yMjpB_CD6rFsiqkSAhIHdX8qrXh_J18PzqTRUpmz7esmh4l0DhZNw1fRmizOD0z4VMlISiSV1mE18GrKmhLADMlXPHsxke3ojnyByKY34KkH3sRih_OV6lhbXOKJR9V-9hXysJxjMCVTeC9md1ZiJ0uLk86RIRaR5MF2Gbt2ox-DYfZeJM0auDc8L-2G3zdUPFx9e9hApc7csvPNLcBzeDBY6PckhqgaLnHVkEesDbSl0J_ApyRk80DW7DTH7yullRoRgv51278JVAlo-N9O7JoP7L0xoqSc8dDDRSdHWfw5QCnHFJA6N7ipxGZkOoayEYD41uDPrHeNG80BpJWGdyDuAjDXcdTl6RBmHuLE8KxnUDSUMOJKhVXFvdHc4N2I3OnRtk-1f59b3vonUf1hTh6E7rCXRBVE7Dj0GQ1i68FUO_24z6MOG1jtNzsO_AHBpFWM5v_1qO6MqJlr0V41Q_mpKA1A_puHtbhjid3zezvCAAP_o92vesRLkzaGF4-EN9CL0D2ZGgmyYrGfPx-EqAEOtTBl6CfhYT6xxJQPpP6hi0tu8Faqvw1CWnCtgBJOtXqlffYucoKLgRYQj7lzmspc9NmT01RwPslUT67QiKHSP1FYMC9lGLumI3=w2940-h1662?auditContext=prefetch)

### Forecast list (when forecasts already exist)

If your org already has forecasts, you’ll see a table of existing items with columns like **Forecast**, **Cost group**, **Period**, **Creator**, **Created on**, **Last updated on**, and **Actions**. Use **Sort**, **Search**, or **Refresh**. To add another one, click **+ Create new forecast** (top-right).  
![Forecast List](https://lh3.googleusercontent.com/rd-d/ALs6j_Fsq5GxeGzFZGmS89e4qJHVTtHxcfZoWVq0Y-JSlMood55BntwfI8Xw_2xbsCa5KgXFtqLGErVuRQS_xDJJthWjpfJlZzgHiKUW_EJX95R0piXSFxkRR5dRNM8UPyui3e0Z39KJdUxiop52Ft5AZ6LCr1LD2J7aYMAHtevd8YCTuIxSFCChzPXpbdUV54T5EZAUBbx5CcQcSLrP0CMkTWoShzlqh8aAtp1gVv-WuT7KwqLEh5GDZhgz747FyhDrfQ7GI93LdUZViArcC8LiPAHpWieYTxsDyT-CYC0rzOav55hsf2lVP678Xoy14wyZE1bMWrqyGWR4zI3dDHCGUpaEKis3NRanwW-6TTzRmBpGrkWXPsQd0ue8slRSzuM-kHtHAo3qMgKquXDN1ZzmxdtLumnu3HGGrrmMvI4szQ7vyokxSSausp8ysL_vJ0JdahhDXiX9-ySz92HPeDx-ylq9y9V5XPrgiccBHf-zjD7jTJeKwV8h3wXKcTo8-id8mTGtF6tw4-kr3QZLzKdU4QlrxAIWlEIxdNmbRkn9HhZfgFR5_aembjwHovuljw-sOsp_iOED7WgnSMz5IvGABFFqanXCQ-7tYZquzlFMU5Wl4RfO5V1-cxA86QmJAEXIb5YKzE-AZiWFHJWqers5olomcW4QX50h1ml8Bs04Xr7c0HnOfZXv6bIrBIglUP0ClZVg4Vd8KEKuu9hbGkHY7yWCLACyUm2hCwVT6fGk27wh0fHDYfThBeCc2-oiAcIBotLQGUwnbO0NGbjUi-zdtCx9Y_bVBBhNuwvInRV6ynL_aOENgUAJNKY9w29t7oneW25MDChM21glwI5kndk3rrFEqTGaM1kHwBG2k_WQGvKwM9vMKaLj1ZBVW3mAsZ4WF-n2GQ9bZ1x8bxhIHaUZJOfqvvV2nr3Aj9ltuordl1mEONUte6A-ZcXzIHgluplbqUrui5k8KlySr1TNTFpssT59dD06n8zMPr3mW29W0d-ryJluIPClivECYodVvSDTcvRZVKyGbQ=w2940-h1662?auditContext=prefetch)

### Configure the forecast (builder view)

After clicking **Create forecast**, you’ll land on the **builder** where you configure the basics and preview results.

> **Default selection:** The **Cost group** defaults to **All Accounts**.  
> This cost group is system-generated during onboarding and **cannot be deleted**.

![Forecast builder](https://lh3.googleusercontent.com/rd-d/ALs6j_HgaGEMjOiHXbZoCx3UQM3HneaYvJfaisTmMXhU2vGPp2ATSYCgv0B68o55KgUZ4gPq3SXyCqZ1EchjM8KJenkZ9ROW3GxrM40n5700OhWv-MSS7h88zpJ687N6dyoZXruSWDBZOntyn1IlSdLRpxIfn_krynsMAuBwa2kr4iohHnFZ09F7ltdVY3ZsO-Q6R_wrlB4YqRZ5goPtpnZtyfd3Jpf8qn-2buDC9CeffluDqMnTPg2MpkLjVkMbgXWS7bgyJvI_uOm3YSZWMvDLyNaERvbZ86lB77rEMa_-abVjSY9BtMV_PvM_HDEStO6fqPzITSmu3vbGOMM2MnxIlj83FGCR7IWiK6sYvErdrgj6TkosP-EOXz4HB-LHEzPWYaeSdfy4oU4oWxGZdmYXuqkJocsR7GW5XVpVdjDNrCsdS7tW3DCieL5ZOjv4FIMoLElZnj26KuNwUFLIyydSu4kft8uAQmmukO5VP7r3LpHn_RPKPpG1xSZFxoz3ie9KdE0i-tK9nlPbQXgszrewcrfrEXkeljutytmwQ4Kpg7cKh9fY2yzp7lUrq_o1lUpf2NxJMDHrk4mtUNS8x3PPzsS65sKNJuIKAfeZRZ2nd8S05_sN1esd1hkBPUxRn5cjEVNm2Ag61nmQLINoceaEAAwr2P6555KQkD3Ns3QTH-1hKvK82jlC52lPbVSQ5EkbFhr0pl17mVLM2agSI12fcWGaj23aKHvOI4vd8DMFSIQpybXwnhczf0wy0PC7Ocbgz5WvdLCY_OyaJ57WOE7dlZ6HDpCU27gXsWajI1zOW-G2m9s7PmujMX-lrBCefCS3lZJudBGqIRUQ1TYQV6CVKlKi9xh83pxI_ITfpP1RaPLP1WkIyVLfavrfR39e45PT-IdEVlh3-gkt9CPwcesddTS-bRNy1ka5PAWDgDuX8OsCINHTpzIP0X_Ibrq7qp2c3lYQ_beZjSvt2z7Hn6-K_V-SI8wF5Ooc1H5Zv4GClMwSvC5p-QIdm7aVd-wsAJaCZV1g92nalw=w2940-h1662?auditContext=prefetch)

### What’s on this page

- **Name** — The forecast title (defaults to **Untitled forecast** until renamed).
- **Data sufficiency banner** — Indicates when cost groups with < 1 month of history are temporarily hidden.
- **Cost group** — The scope of the forecast; Defaults to the system-generated **All Accounts** group.
- **Look-forward period** — The forecast horizon (e.g., 3/6/12 months or custom).
- **Include current month** — Option to include the in-progress month in the forecast window.
- **Lookback period** — How much historical cost to display for context (e.g., last 6 months); does not change the forecast horizon.
- **History overlay** — Quick toggle to show the last 6 months of actual cost for context.
- **Granularity** — Time bucket for values: **Daily** (detail) or **Monthly** (planning).
- **External adjustments settings** — Area to add increases/decreases for specific dates or months; applied on top of the base model.
- **Preview chart & totals** — Visualization of actuals vs. forecast with running totals.

### Name the forecast

- **Default title:** Displays as **Untitled forecast** until you rename it.
- **Rename:** Click the (pencil) icon beside the title to open the rename dialog.
- **Save:** Enter your desired name, then click **Confirm and save**.

![Edit forecast name](https://lh3.googleusercontent.com/rd-d/ALs6j_F-Xe5jfCFmBA6mSbtIEo78RS0QZT3-KiRmHu6A_l8WSHvCgsu2BubolEV7RzDcGY3v_FsCrEHkd5uZuEke0jS7XFj_FOxwwD8lXlgOKUpbZZA8WiWxf5jBiW3MbtAfj1_av1pa2-fzn1cwCoVn6bu76r0k5eede7Nk2k7qQcQHTOUV9H4dHFfugFu-A4WpnjwggbCFmLQz1PPkbrfmF5ahtcUikDx-97ov5hXtuRBjqFRjMRWkwQZCbjEoxcMfNNqGMJTEWkwWHufZX0kjfPGCnJ3kJP3PfhInwN1Hsk3rUU92_npxD7toBn2lOfdMfEITLRIntZQkHtWw_OCgPskFW2da4mJEjmqgvXJ4zRZfAoP9gMXvG0Prn898Z7mnn92cdhRSEmoz7uMx1an0KT0JCIOVYfYbdHTeWGBPydsb3AG8zTsQTuJ-IqjwASVohQk6POm7lNLQdw6xfk9qncQgoyFpH-KCTGuTo8hnj25zgVEuWu3zT_JWIw8ZalI8eJ55TCqCkqmBYMnMnEvUygjwBhXF7h9IbXvBz0l9d30OQcjrBQqI9aLp_SvnQFIrXaqCV8EbAk66HxZ4cHMleMwEDsIh2-MEcbzgU9kDuYvwGZYGGFG0d-o9nVX-QvvaSOVab3HPc63HpjYMrk715FsR0i4umFEltodw1Nh8SG_qn4PNPI3lFqd0axStdCRjyDcu5aMKqp2HbgizQy_9rUPAYJVAHEDPzvOTbkBoaOOOjrAF5O8lnGMp080I9QcqmVycQufc7YRKcN9KICF0mJuwZBtJKlh5a5HqZwJ9irp_tvH3XS_NCN4DckPzhgjnKDDCS_kPKbdiELzzwwduEsX-zd_cXDpiyZD4mNZY2fHHlZEKKPAcRk7fTy1KefuxSG3U4hyErJUfi7RMI2GbOSIwsSbcsJKDYIg7lRTHH4FrJSv1SyKgQuIqOm6FAcFoR9RBMEARzstO3wstGt-3f1wCGdca-vmU41o41wNdKVJurN8r5slXUfFBZr8UF3L4uwlhNZeY=w2940-h1662?auditContext=prefetch)

> **Tip:** Use a clear, unique title that includes the cost group and period, e.g.,  
> `All Accounts — 6-Month Forecast (with adjustments)`.

### Select a cost group

- **Default:** **All Accounts** (system-generated during onboarding; not deletable).
- **Change:** Open the **Cost group** dropdown and pick any available cost group.
- **Scope:** The forecast inherits the selected group’s filters (vendor, accounts, services, tags).
- **Availability note:** Cost groups with less than **1 month** of history are hidden until sufficient data exists.

![Select cost group](https://lh3.googleusercontent.com/rd-d/ALs6j_ERd6M1DlpDtPzWHi_RQ7TS9AnZxzKYwewjhtXKRUTQ1cfrfbBOC-kjN0i4wzzz4PriJUTSoUraNnMYWVj3pAX_OLeoUJy8ABbDi1Z8W3KQgo132McgSbgEsRvm5gT_TmnreOANJD23ConzlxdXIyiVZxxY-MAW2jgtelMMDizLxc_Fy6ODweGgozNSpw8IzhrO0wN55cJzGUte1Fr8XStM26DZajDHqrLnRQBZnMqhtreBlkYUgjn6m9xwxh5J4-AkExRlaZh97BjGQfD15IFkivolI7CjemkM_fgDmHR3VeChn-qiKAtZvVNnwTZm6Lw4i91dpgt8okQuWPXX6i9rZgchmjvBcJXBZ5svzgRgO625LSye0SSj-s24XvLlQns2LjijwD7wTtDA3uevPDVRFi--b2Ya6sFkDlfGg9TBrrWulBxLAs_nw0FXq4p3eZeOlDUNW4UdM4Zp8ZuBceqM1jEVYigUuwe8xXoPLyx-3YL9ydGGQHcKFHJR2ca9dVIPyOOTfcImeTfIx4Pf8LZcstJsQTP9g7ZtVLwCOGyLfQ19fdRVnVMz0LsOt282lIzoL6WsUqOZPaLHOUxIN_H72CX_6sejJeZdcTCmDatFwqxSTmWNkXS86VLfZmIA8I8l5dQPkEcPls7M63EjIKaLrmRQdi4v-SIk0RWSSByX4hXyeuCkQLVgORbH6FP9NfWtrBQRQvc4LZImwZJcEHHRcwaHhuA3A-SHYBrSR6m5_dvBzusnc3Tk4xZb0zwQukK6vBmhQ-i0Vi2JjirUN1UhQYYnwtqvEcA36H0FyJppB_oqr0uZqURuGrzSeozpgHefoweUMERM8TziQPl6V_ji5V9eINcj4NflsYmf-ZlJ3NDG_27wn0zVdclgF2nxOx2_YSZkMVDQqo52BZk27hmHzHhckrxRg89eX6fYX_RdyBt-F4T8U0S8iGOc5NqjF69PSyUCd-gYIowiDHsBm5e06wcUsbdZ6VHogWRiTq9npI8LFMle9ExcV_3E7qlTStGF9Wl1=w2940-h1662?auditContext=prefetch)

### Look-forward period

- Defines how far into the future the forecast projects.
- Options: **1 month**, **3 months**, **6 months**, **12 months (Max)**.
- The picker shows the exact **date range** for each option before you apply it.
- Works with **Include current month**: when enabled, the current in-progress month is part of the window; when disabled, the window starts from the next full period.
- Affects the **forecast line, bounds, and totals** shown in the chart and header; it doesn’t change the historical lookback.

![Look-forward period](https://lh3.googleusercontent.com/rd-d/ALs6j_FT-CEbXumRpuAm03t3ghkC_jyzF1pjJFOV4qZ4uCxsoIXyFj92qVb6waocjeoMV6haRBxqp_gRLO5dC5RCqhhSymesZnNDuIHQYIWEO8on6YOVRJ52zEtuN-xNIwRSviacrseI1qMi_IVQjP20fS43R5R9u_6UCmMCNTpfpVRwe8pnhINWhQxr4K18K9L58AyyOAZBAO55RycOhXXWjqYWmr5Q0OloWSIuuhGvDBGszDw3eWTNFUTHO4BCAS4f-irmzqtg3xVZuG37dmn1jPdFL_Frwnwlrhq2q3DVJ0dkapLjSb4jJ7H1XBrnzV7HUwdN0u9dRKKHVu4wv2DKnrqEhOfoXJk5pvKqUOxGe357tBXVqWf6qDShDtfKdTdpWIOH0NHm8H1Wqll-H08LW0djetl6RCsF68KdqgQ9uIjeDp6aYCS-TDR5WQ-qGmkLWnC3VBDVocquwm7HGae5lCOWEpwJewqRFXgoNoWdy96bvjNphUUgGJ7wIpGgG0O51BRmJttzeMOYeH09LSuZ6ibPbmmZsCLi-Vb00Geg6NdPRBprWdI0I6j2HTj1bYBPvNZuTHkSJnyaTHvrlJh3eOJOMWJ1mDaTW3PfhwyCEooLtLejyk9GhcWcYB_riPjWRZHQ2rVgiv4-JZlIZWOWdxmYosvleYIFjb4hQAHC9FncnWnKREp-6Wq9YRxuJGOLUcNsjdxAC50wYtwJ6QRJHGvso_AhuKyaiaupERfqHXrOdQ-TCXHXZLQsOTkhtPQXBFU5uCp8goyveqyJGQrm9ur43QkEX74wafi1ev-r92cxfbXIuUoaSKbRRCWbKZQ0lWm0E592Pp5fBzsm2_mIqxgHBnw5J_BRvAUc7-sDMFRdhmzbIyWLg997tCSYjz9tgwkpjsjLHj4PrcDXfVrUAjUtE0wHuL1fLrYhvHM89adRKWL6XECwcMmfqYXtU7kjKJj6lweR2UKvUojJ9rGPS_L9hmV8HeduXbslTH1Kmh6QJohf_FO-rgDgPtYyn7p4CV74QIenqA=w2940-h1662?auditContext=prefetch)

### Include current month

- **Purpose** — Controls whether the in-progress month is part of the forecast window.
- **When OFF** — The forecast starts **next month**;
- **When ON** — The forecast includes **this month**;
- **Why use it** — Turn **OFF** for clean, future-only projections; turn **ON** when you want this month’s picture (actuals + remaining forecast) in a single view.

![Include current month — OFF](https://lh3.googleusercontent.com/rd-d/ALs6j_Gyn9lCq4mJrKjCdaEELbIsPZIsvQy8wKcXnPU_m0uZS-jW4MV2bGf2uMFiqhEHILRufBn7xNHPgeWNrojTbG3T9NdGARZtssMq4qmiAK5VnPZrgVvxAaQgCWiEzgk4L1wGda5Je-mF7nQdnUD4eSiK_VFDEVIwZs4jXn5J7sbStasRX4D9D3dKSiDlhK-5wc_-THNYOP5gmBYWFuW3F6Q5XtALhhyFabVvYhcJv3-4XORzO54Inb5YNzw3--uMPkXyVSsP3ccB5x5rufr2RJ8HJOVMgkCbqBdn7xeHpgVYf-SUNWLsQHxVYHYT5awn-ZT20OCDINxSumIWoQXka6VkIsGt9pWkmdNtj3ZPbp46t33aW06K4-MCJV9nyqRtPJW9wy1HcNHqG5LEFDR1ZBtWd9or5CCYiTLs_2aJu8CmSCA1MTkxlVC1o6RnLPXbkSOfwlTp9YQb8A-buDE1pPEUL_hva4VHP049f76mU6sm5rCBA9mnHaV1aSHjT5Ea4I6J72MElmpsruXKURQBOovLuUNDC7y3ke4qm5_q6QAa2ND54Sm5C0JBM_EYca0YiJ_GJOhULkhKyJCGmbsEsy1hy6XOXJyGNHUo7g_jzyEHBKnxBiL0FnLbIZW60DpHkmg4dT2x6RQNfgEYw7dkiEA23IXRABYqQehvFa0G_CD3X_J6D6sLI3xfcyuDWK1qNWqqzPjjZjsEidjvfbmKf29IlYBd32S_UZ8M2K_pQiHdTpbQAFA-oIK2kqKqGoymHULcIRnNc4aG_Rqb-nUeYhcw_Om8pRHCmRdABO8eturplF_B5zggyJoN31N9XIq_bWzRWw2-UdenHwGxOjpdleUJFK6l0Mhrwi6WEmBubfp-BlQDRaMGn5ROZP8JGo1PXPxbUvIM7yRBZKZvSShm5KmHVEkxPCGZrUslcD_zkY0_QMbKWM9qCJmxeZA0K5PkY8k1rC4njLxFRCHPs07nCxjjmpuQaus93MEaySqnmpVx3SPKl0RVeBpFLn7-j6VBdrGjDKzlgQ=w2940-h1662?auditContext=prefetch)

### Lookback period

- **What it does** — Controls how much **historical actual cost** is shown for context above the chart.
- **Options** — **Last 1 month**, **Last 3 months**, **Last 6 months**, **Last 12 months (Max)**. The menu shows the exact date range for each choice.
- **Scope** — Visual-only. It does **not** change the forecast horizon, calculations, or totals; it simply adjusts the history you see.
- **Granularity-aware** — History is displayed in the currently selected **Daily** or **Monthly** view.
- **Use it for** — Quick trend context (short lookback) or seasonality checks (long lookback).

![Lookback period](https://lh3.googleusercontent.com/rd-d/ALs6j_EFGl1eiuiNd5vMeOPr-bI6DGNpryse8aDoa8Ls2HRjD5ZlSet-x5ND5eWkzy0q5E8Y_Myx8x0l5dVsZedP179BkBF8Mr6x_znNKP64dnsVzcv5g7nZ6TURjCpkyNn-XKVY_dOeMUloTFAQ1PLOSyHIGqEbH3TCheOinDn4mJWIU5oKFu0-jOPreGlSE4ikqumZcxs95tRuh-FGwivjZfCZ5N8jjL90F2_cp80RAVCELw-Tkh9NAEU3QHHed6Knn1DWeC260OomLmJyHo--WSeF9qB_Bb0--pQqS9v2-9sHxuuzulQuwjoO9SmjWvD9tOMcW079YomjkZmcJhHacKAfKiJDP_XjyjguwY1YtyNIYiUTxHJwmmlnLgnrR4cFxFY0TnUMGLfyPitgxmXRXsFG8KjwH-GXi40EcuD8bamNotP0m-eI6eGEo-HWzvQDly6B0JUuSGXKBCbt8i4qneRUWuqq-nPdd-Ak9lmhQ9AWnxyUDCrcV_1yz-FYrtGiP4ism4Tb4dtE13akZKTTcAXmXbJN7N7exs9e53SZRjoSFwiwPQ41u_vZ9ZxbUsoF-81JtMBNQrgVWa8Jy5JZKj1s6jxCUUozYYxyaBjOZ8klb1QEAsHn_9aeYE3BTjreaqDtGkXKMffk-TGbfqkAC1qk6MRmPEwFNJQSsYukmGNHaQc_1hUlE1f17gMhHXKgAgOxHF955wmFiQomGD1DnctdvlqhqLOyE1QqGJrTd6mqTehRuGT_UNW_tb1dI0LrB-GCFJWvqub2zBLSuuQAAaOitW5Png4Fh8rRGihsYX_xgfCvhh900fP-aTjpWGdY-lhsefPD4Q9uUhg4dJoAjl3XKP_rsMpsumq05V32L2QljJ57TshzYRTjmxTgWPqxOc5TD7MRyn2Ouxlq71eYtwuZNW1SNbfXZh4P5_ptLk0C19rC7Gwa_LeqT8wUQY6_pn1DhMvwYhv11wWfAsYmTDr9KMg4D2eUfssjG8yVWrBCCIii7Nwnkpa-0N7w1JxwC4kOktINKQ=w2940-h1662?auditContext=forDisplay)

### Granularity

- **What it is** — The time bucket for viewing and totaling values: **Daily** (per day) or **Monthly** (per month).
- **Daily** — Fine-grained view for near-term monitoring and spotting spikes; tooltips and totals reflect daily buckets.  
  _Note:_ Adjustments are defined monthly; when viewing **Daily**, the monthly adjustment is **evenly distributed across days** in the adjustment period.
- **Monthly** — Smoothed, month-over-month view suited for budgeting and executive reviews; totals reflect monthly buckets.
- **Scope** — Switching granularity doesn’t change your look-forward or lookback windows; it only changes how values are bucketed and displayed.

![Granularity — Daily view](https://lh3.googleusercontent.com/rd-d/ALs6j_G2MVeiSpEDfTjW-FSQdGEq7pqLTn82uae4YDbWZC6kNPITVf-plrxn82Bl0LKmR3B37mfDa4Iqzy1QVGDiM5CYzpQoo51zmjI-LtUFejBhgfhUceI9NCJaO4LGdsBad3T1v5CLwf-7fZCvq073QoEf1tFyQksQAPiTgpxAsMr1tWt2w8MxRj4DqNjoYyNVYpRA4xRtjD2z7XNHwqT5IK-1XPtgwbZvRBNmFc7pTdUBC5UqdGfxL9522hcNI29_Fne7KZDvFD_BgvhLBaL9a9iKvtPMBexOzbYLdM1DK93-BgRuDUVs89ezTeF6U43b3wyJ8Q7cCkJkrITWpr8f_bSwy0971GIjl7YJQW_oQY0MMoMC17vBIq1MEQry3jq3oYDI9ysIAX7YZkdoKcF28b4OS1NP1pbPfzP0GRaUyj_Xac2YDoEHCH4okGRjtAS9fYmVqIvY7WQ3z-mP_dwFDrpYKE_EoUotwXzC__OX99XY0JzFaQn8bcgWhOyziBNpoWlZhEQQnkZpXsvOKYfqQAVMnSRufRS9D29x71gzc6Jsgqre20RNNUFq3egRKmBU4neCpkW8A2KAGovoRuflwpftYfwKbSDzJn-mEIaw3u0-zF0RcXpHVjNewfVdWcSzgA12zGoaSHG306Nlt4tIrpvlkFng_M6RQKEtegp2vEXtfK9YgvcohdNjBWwUXygeqFc4U8rVjuWJtFhSvnutMMiW5q7uZ5gln7awwHr6mUG2xOFiglR_f6P1WHKfjA-lZ0shKuuNvI-aM6UKis0pA_BMIIFIjxwm0ABUlbV7pga4sfvBvDhgmCAzfrXuue8ZR4jH6ypGL6VkwfMmQDcLoMZOg3MKHmt3eTSW81u-TMbpBn1po6Mv-hIXur8u2zYOsQ6_ISQKXRTzunx_5cEUGEQHVWYbAwTGtTI6-j0B98ntTRPSDwvxPsP-qtjzGKrujagSSVzdMISp_DGkPRMobITFD8_jxOohR0Yy6seGjnMwdC9sDdDL6N_feZPkiRqhFnC1EI7S=w2940-h1662?auditContext=prefetch)

### External adjustments

Use **External adjustments** to set the **monthly forecast value(s)** for specific months when you already know the outcome will differ from the model. Adjustments are **monthly**; in **Daily** view their effect is **evenly distributed across days**.

![External adjustments dialog](https://lh3.googleusercontent.com/rd-d/ALs6j_EOp9ffwTyVfHtmLB0Bxr0gFxrGQw8HnPwdPEWFGqv42mBoL2tE_hrBoIHMO2jZqdfSE0R9Ctp0g9kdcc1RdkL4aQvnA4mWPQfmCYwiQ5vgK07n9MMu29q_JK95HIgCFwClnCrZNAUZuzrkdXkEETJroT0Ulj_4Ojxty1t2LAHeoRxHIUMrOyWIBrX9VOLxpALD8-cRVUZnkCdM5YzG78wZRgqWW8nwKyINyoa4hhDemo8QDQIpGPm_Y6x7rvx7X_Bz09Cu68jO1dYnKFMdheYRvlGAaUvk9XTbIZqRA42z4xm1iTwqexcs5-bXJTvkzhunQtE4ewNi5u2FtsScRBnB3-AqFRUi6CPDshMP58ieCt8DuDszyVxBKggO7Onq_NtTiWafkvuNhVx2KeUTyMP7-zfNYhSGeuyKWB87NWBh357l0n8-Fb3XjtAZuagJV2MJeWYUG2-AKiMZAiVvJANWXM1YMhRR7p0gx0HbiUsjB0KQro6vL9ARpv21MkIx4VHslHmqZgiMa4YpkLeQHqgtepctX2nYODvyaisVfyYfNlcMvvzKrbicaPnEFAyTSC9yfb1CAelPsqI205ZAnFO_vvN1uicMFFG4ZA1J_Y3aj0fEdP1RP15T30kjXH_UXgtwVUNr0Xo93sagCiGJ9EtNwcTKmhOfC0YawF63Dvsqvsltq07YGlWA6810z6rUqpwKYqozwesYQ03SdvqJ737-dst4i_t6TtdEqnO61tMXTC6gD5GXfdhVRS5PoQz0v1bgGeH4p5K0WKImRm85yHGktneuBjl84DzC8yUsllxmnuoxV25K2Ao4naUGtC0TK4YWFfsoaQ5mXMlwtGz_yzle0VO3Xw6zfMuHLsOKm5Qbcibw1TPnlPto8SMOFqX4UjRHpsZSt4l4RmwdMIV1vzbIWZMMv3k8b4UKZ82wuWbd0z5ys_5pcz-Vy4mmoS3TURiXlm1fk6cs9xlrxtwELenWDUF8ee7isyZP92OstfnSOq5Y8_oUBkriHbI7WQjtFfbCiavj3Q=w2940-h1662?auditContext=prefetch)

**What you define**

- **Adjustment name** — A clear label (e.g., “Q4 Launch Ramp”).
- **Period** — **Custom period** (start/end month) or **Entire period** (the whole look-forward window).
- **Amount** — The **absolute monthly amount** you want applied to each selected month.  
  _(You can add more than one adjustment for the same month.)_

**How it behaves**

- If a month has **no adjustments**:  
  `Final Forecast (month m) = Baseline (month m)`
- If a month has **one or more adjustments**:  
  `Final Forecast (month m) = SUM(all adjustments for month m)`  
  _(This **replaces** the baseline for that month.)_

**Example**

- Baseline for next month = **$400**
- Add Adjustment A = **$450** → Final = **$450**
- Add Adjustment B = **+$20** → Final = **$470** (450 + 20)

**Tips**

- Add a **single absolute** number when you already know the target (e.g., “June = 450”).
- Add **incremental adjustments** (e.g., `20`, or `50`) if expectations change; they **stack** by summation.
- Name adjustments descriptively so teammates understand the assumptions.

---

External adjustments can be applied over a **Custom period** or the **Entire period** of the forecast. In both modes you enter **absolute monthly values** that override the model for the selected months. If multiple adjustments target the same month, their **values are summed** and the sum becomes that month’s final forecast.

#### Custom period

Apply an adjustment to a **specific window** inside the look-forward period.

- **Select range:** Choose **Start period month** and **End period month**.
- **Per-month inputs:** A table lists the months in that range with **Original value** (baseline) and an editable **New value**.
- **Confirm:** Click **Confirm and add** to create the adjustment.

![External adjustments — Custom period](https://lh3.googleusercontent.com/rd-d/ALs6j_GeKYNIuPSjkJdDoSYS7zRChrbYQbW79n-wcOhrZjrwW3aBXuKrN4EQ3bex0Mt0HYMuMkVPszCkmB3rOiKh6cqEJaB74-ztoG3MKf_YSzJkNkAl6C13kQNC4r3owcLskpLuTfu808vpP9tMAfV5ExMkdCbopKi5XjW455conr6zOPPWYQ74rBKSFilWDGTSsmHM0e--LiKDCyiIkUbxeBlyEDJkCm2piUtPZZjGNVpXIXbRdmTaprm-SePiLhF-5DWxEmqTrU7PCYI_cCvH9S52SqdBvarwd1qDOKpbcivczYZwWUD2_vTwvciz9ie-IFIOG-77W1NMCF_yUzI6ho5pEuAIuN18lQx70SFWZ4edOQu52mZeps_6RKgFPqVUlhDfms9TdEUHgVHLkE4ZpeYz4MFSAQxAYo6mGmRYqIjkqrj5csArnxDq8xTZxNmWyzN7oB1t2nbWZV-tGdmbkoZBIFLp8EPqWiC3uu38iGtilRS8W-oJg8afD7nyhL4qnZw3IYq1Axko5TejbPiIhl5AaS5Hb6pPDYogIhD9hPc21zw1h7ghOXmZ3BmoDFesQQGyP7VgPYpMGVW_gGizbjUPqpCNKiA2R-avpdbqG2CVAYSxUcEJ56_OMRE7I-dargGivRd0EtkIVbunBZesvusxPqoTAkcPe8EwzTfQC2UgRA9hRX5sbX4yTbZyJEKuOWmzG0Scj6Bivw9Wl2WfuJhQ9_outbxxVjg2ECS2-0vsbn8YN2NLXWK-60YoE6pI4_cG1_s6l4sAP1Vn_q0IqH4X2MEzVr0z5c_NokeOdek0nc_giV3q-2ukgCpfCTOUZUVFqvi34h8dOQgCWQ7oRqPvCSk_vH7QJolfxlOU3YOCVhImiKy4TKLp3UbGkNVnnOQe2d6LSdAPOo7ZdyxhWKMvnBuT0aVEw40UIeOVzfRDkpitSEyTwaexFL4BOC72HfgBghXgwTdbMbrTjBxXG5BHs3EUM7Iztygc1r5ghtAUCOleiGdQhuGbkeThL9LwCIZHEY9xwQ=w2940-h1662?auditContext=prefetch)

#### Entire period

Apply an adjustment across the **whole look-forward window** at once.

- **All months visible:** The table shows every month in the forecast horizon with **Original value** and **New value**.
- **Confirm:** Click **Confirm and add** to apply.

![External adjustments — Entire period](https://lh3.googleusercontent.com/rd-d/ALs6j_G5kZSBPVCHQfPUCxXNYJ4-adXJtnefNfQCxSAQ-vgCkQppCS4dz5zx8fEQQW1bxJvVs-XbtxykQor4AyWI1JOlAMBYgKUS5832lVmRL9e8ruGmQKBTI7UIswVu0TnOwHL3T7fdMnwsa6DrdtE_BaIh7-3nDsqC_UyurkafMoSKRAwlF1iHuZ8TbuZRL97TLyfE7-clPiRgBJj0hM8hv5-1OIwvDdAG0JvvDc5O_nkzRDO4v8VX5bPNm7twDtAKshDo0d_9ie510CQKbhdAXa88c28B3-iRjcnZUO7CtOZHQgJv5tIsvzgJH_qT6iMSc96Es7AMt6AKzdvdgLqLvSvI3pHRoOVwL7J0cH6z93Jat0UGtENv9giveWK6eXREFeu6JyQunNPMlBsS7eI7Kkx8Oyfk7UeXQj6gZuFCFseQZPjxLny-VYVCIMyFd3VOtEWcxJAY8DgYcfvrMYrnlyqB5zKpkJbZxKPWX_04uHLwJNYIwqZNtfq1EROBGLI4__gcui9zmO1Bl3_Vb4RMBHJA8JqybHH32aOmQcmPM8aHq3GYaaqafSDI0eJ7XHhD12C2j5rf8-Zj-xem7Spw5HmaJGwic-7WC66oEw2YySI3SaH9_mCYa93PRlZ6cDMI_QsTv8KfOjlsDwVi_rJBHBeaZj5ItNWv-dhacm06wlVO1U11FXhpG1f_bzxFhcCPZ4qRyXN568CTdSlSrTMz7MtHgWCk9-pdAD9GfnUb3cmn_6dKcv8oBD5Zc_NpPNk_5ZdU5T197jFq0qc_gc_KWuCA-dQ-pa-t0UyFw3b1OGJ6fbSym_iuY8jOrp66-SjUDcVsC_cH3WYdbPpaOce57dYWO3Zmv5WboaXjyUOMFF8pKY1kcaRjxzzHFZHBO-7UJKViRFBKQRksQMUJhOD2xfERx1RI0Iirs7dHQ_4bueu1aW-9jF_QIZkg1OeiKhFGHuj04cmWuJTkQmfhZCtsk-rqQOy_oDvZvHtkA1Opxt2ixDqXYBMTU2M8_QykvQAv5crspsm7Dw=w2940-h1662?auditContext=forDisplay)

---

### Review before saving

This preview reflects your current configuration (cost group, look-forward, include current month, granularity, and any external adjustments).

- **Forecast (total amount)** — Sum of all months in the look-forward window, using your **overrides** where present and the **baseline** elsewhere.
- **Total actual cost in forecast period** — Sum of actuals within the same window (shown when the period includes months with actual spend).
- **Chart** — Solid line for **Actual**, dashed line for **Forecast**. Months with **adjustments** are highlighted with markers.
- **Table** —
  - **Forecast** row shows the final per-month values. A small note icon indicates a month has adjustments.
  - **Actual** row shows realized spend for months that have elapsed (or are in progress when “Include current month” is on).

> When everything looks right, click **Save forecast** (top-right) to create it. You can edit or add more adjustments later.

![Review before saving](https://lh3.googleusercontent.com/rd-d/ALs6j_EbpreRzFdFJPm1ny14vLztmNlOuOXmEdyaf-pTxxlMJkxXlHCdTsQDxJFUL0Gm4LqjWFYI8aG0HJOmompfM1XYHZQUoWpEqD73N--nFMwm3f174VmGCkuAcMoY-AHC0bishKswa9_OetQ_thIo4tqZmYScwa4R1qBIhrI-Fw62-osAccUVxK4ZYA6JIZnx02ExZY7wmVZplABsKVxI6CDJYZOAGTBd_9e2I_ZiyKGhj1rlHAxHPTvWNL_uAkuSGVg9mLVTXIJLToXjM9mrMW2061ysPjI5Xed970gYLSwMur4AseplInzxlsEbVI8F5LVhS89Lpxg5Qd9f-iWUDirdQ4vtpK2U_nU1IlHpBDVbzRSEjldyn2mZJK84iZ3SBj2avqoBX7TFwCAA7j4Tg_kQ-YeHkk8saoE908Pp1iimzvMMlfsr011wRZ_4ReH6Mi7n3d3JW5SjqtVN5mcH_rOHs-L6Vp4O4yM4-a_fNixXWM_DL2xxZwH1MCsMhLJFDZue_ByEttIyb0wjN35-j6nehoJJIC1UYPTEz6ekECy3opHW7K3yRw725jYKNkC69uD3DMLyQwTSuWVCcM8l9agLh4VKMkzV_ZVDosqC6zORaGkuHempHV5DCkv2wPu9p_SBUf5gSP_AV2-0e0rtR8Sp7Y7rgEu4hiVPxZnI3SRNOIdJcNBoal8kLKlZYdwWrP8RGT1rHM2XpD_fKYOSCJp3nB_gJdJR3cKDQx6i-QDKqgynOFx0pRbG3TuedSmUq3Y4CNsTYo9goWn__p_TdRXTVZL2TFK4KgB5MzG7q63WAKPPyGBFEBuoBzkvQC7fC7jWv0mpp4DknVdxkVBag6DP1ZkFhCbLVdERkk1II9U4_6LtQp9Uq-Clzb4G39XiYwaWpoyA0NKSPrKs335Qp8HEfxtVOq_b3pi5U13I2rMFUF6CqoJA50OPauah4G57luS-uH_ZlwsUpQ4I6Em9jz4baHHTea0L_kt5DgYHX8qpTnPfBgExSCm5eG_KjyTmZZdrIknR8g=w2940-h1662?auditContext=prefetch)

### Save the forecast

Click **Save forecast** (top-right). A confirmation note explains that some settings become locked to keep the forecast comparable over time.

![Save forecast confirmation](https://lh3.googleusercontent.com/rd-d/ALs6j_EZC90e1DSWOIloJj8XQDg5LwWaRsvke-07KHph1PGIKerKSKjSux4_Csboql00X2--FlVkk3vObQcYFhcXfNyPDGKcSDhOsaKs3d1HfJf-tm4PpLPd-EHEiKVMvoJFlG4PAXPtZo0lVz77de4ywRGy2suw6PD3xz__cKVgpzqqzktja33Ju_nr_YKhYz9mV_YSiGlZFGkLx0Gl-SFAWE98HrP8e6R6rfZ1f9-qa7hMjHnK9oE6ir7HGrSAZe9C5kmKHlAbzRhq4O4Z5jNXc5lzDWO_POyySRwqGoJSKsYA6zWenDNsgO9kkg28QKHPXf_zaijdfUPpfiHHrjhzJyse03eeVKOsgMDKOGoHUdF0vgHyBjZzxLbwi5RSN-YMyjlksEo0O4O32_V2XVTLGGKceQapoBAYS5ES4nES2vBMxotisurz7VGTYVnlBWl_p6a90ncIbxiTdE1kKyrKLotOvB_7BxOpZdIj9qyZzk_jT2pa3BaQdAhIP-r7eIZzgrKrivLO8ZoaU_Rm5zrLsEHRm0UBT88B3zXTCQJqGbxdDeAbtL57jS3BZ_lHrVKr9MFW3qtt5mVUD0M_FOqv-PGXPcFwgdAwZqkboJq5bidfBt8-aZR1ZK_DT8zkRprzxsNBOhTu7zLXsATgvB7pM64D8RfvosLjdF8yvWnFTXz1OtUAzr03tCvIQOYp9u1uGpUdUcIW5d4-gX9R5X3llRsJ5kZU_suw94s3ldM3b7yqbvZK0g4uGsDu5pECASwio25kimsE_QdZSMyhpXP1mQzCT6MlMoTvLKG76kabKVnrRnxcU1OroymWdNiWgXo89pI3pA0LA4xaGC6jBQCp3_8ALRWy5JH1YEjWc-BY--aF-WIhFTRAqRGXY-25yVd25VCVLzawYr8cTkSfpmVFsLA2L5hxsvrlzcX7CddVeYjsLO1cFJmFGlVnpAgqNm9cG6Y8_GYDd0p1ZbR4DHL0yTVVK856WMKMNe1jloteZ62-opwKgsVsjFFLu8FVfGhHIp_JBAy9=w2940-h1662?auditContext=prefetch)


> **Note – Forecast availability**
> After creating/saving a forecast, results may **not appear immediately**—especially if the Cost Group is new or hasn’t generated forecast data yet. Octo refreshes forecasts on a daily schedule, so values should populate **within the next day (≈24 hours)**.

---

## View a Forecast

On the **Forecast** page you’ll see a table of saved items with columns for **Forecast**, **Cost group**, **Period**, **Creator**, **Created on**, and **Last updated on**.  
To open a forecast, **click the red-circled View icon (ℹ︎) in the Actions column**.

![Forecast list — click the red-circled View icon to open details](https://lh3.googleusercontent.com/rd-d/ALs6j_FJQFEC_2e7LG3vfluT67f3PfQcF9phpTUnBDfTz-sJZwjO8xSErrN1gSt0jxNp44XSKmmqO8R62Sz6SUPntzkmcRPypbUo32ncL1AF9E6RANaS6C-5Zcg4updtIe54mHN6eBvsBpG8YvJjZSBoX7C83Zg0yx7yI8_S8N1JJnvs9lZ5t6OUDHDtKev45cMFD6oNnd_ahTnX-8TYkM6faGj0nQd0XKe8Iw6_27y-wnJBIq4ESqaKjed5W-LyO9jdl7H2gAn97ATL3poZvc_c8eHpeeUfbc76Lgzn5E3d8KbSdDgql9Tj1HsdkLcCaljgNNEzw6Ag5n8BzTRBqn3M148TeKK1j2mxBJjyCn-jvUIzvr3NlSkVqsbu_0_3y2XGDGuo0PER-hfVvVeYxSZz49cU2gixGOf5Zl-nkxMAXVh-kyOobquXB_0LFRW-SwELeCwG8xFc6xxkO-CEOm1_o8HE4vyG86lD6Sn4Jc0icvcK5GHxWZWZM5mAusQkMWLnn3mLDXx15f0AvIiCr8oCvi5SLEFFcJ0NJiSHbsSlfqMQswjJUPm0BUxldLGuY4JvKeqqmHyC6s040YOdzm0dJizb0HfSRg78pbbh8990_GpgoGhJcnSf9JqKR9z32hQsqGOrnEhfkNbuziCMdTJzMITrSWXbZATSGo3DQZaPrqUtf98eLJEuKt7rvVtL5OhRdmPJWyNZIkYAqxbQ0UDh_Wj8b-Rh34ricvY4sHHSFdlRr_5WIJWKyevxk5JkmuYDK9pl-2Nt7DJNl5Y4QtsVLddDCX9lmplbf-43yV5oSETx6o8B_rFHOg3r8p-ckG5CTs3K5iERnpSe-pf264ghB9IuwHqlILZHD-YQQTwI7FgBjjEAJEA2z4Ke_Fe9kBf4DoovD3KUTevqdIS3qL0VAKdjamjiAqA4Y00fo2HXWl40IIK6urA4oexakEOjg6-dEaEiMu-s9Bz676DK6FX7fgUUJeS3KQXEWTe3-0_Q-SACjZPVH0Ti-cSwsj7gMmF5311K7w-wXw=w2940-h1662?auditContext=prefetch)

---

## Edit a forecast

Editing uses the same builder as **Create**, with most fields editable.

1. In the **Forecast** list, click the **pencil** icon (✏️) in the **Actions** column.
2. Update fields as needed:
   - **Name**
   - **Look-forward period**
   - **Include/Exclude from lookback display**
   - **External adjustments** (add, edit, remove)
3. Click **Save forecast**.

> **Locked after creation:**  
> You **cannot** change the **Cost group** or the **Include current month** toggle on an existing forecast.

![Forecast list — click the pencil icon to edit](https://lh3.googleusercontent.com/rd-d/ALs6j_G3Sii1T2pvtn3KrHXJjhPm34UAEPzPzCTL_5zrWjYqfuNezTc0g0EcrKPEYhTcXKzfFRraYhVwOEsTpbik7O_Ve0f47kpOnODWZnk_Fkk8Ed5eji-QgPiCOiu2XSQbsSZZobbp18v1BL3VyKP6ZtlFN-XUN1G4UwiJaOCUAJi-lMMiq8Za2ReZRTm5erEOKric0tkKWHUvaE_bqP_VSep-Ff8Et3FDkwcr-QyYjbSniNNfgyUSCu7qY8fEy33IPUmChAPt6yK5FaW-2WfwnCQ_D7kjZlEzZRzJjPhWnFcSieOqB5ljvvzgAucFoopfMYf-oHf-Xh8-OAEEksOX5vDM4dnhKIAShbXpo4Dt1blhzhnCDz_qtIYuJTh44RYxax-uYlM8YjEUqNywTHQjtuC_IwouU9JLd-ptHP2VJYA9acG44Joi2rb6p2WFJxywrrlPAwcXI7jGkoIjoatI4w8lXTL7fF5oYSi0xvTE9nEHWDnW7F0tdp4QRvV0y2GpiHXawQEIRszf8-Uva2FDd36aRkfWpQ5xJwDAA7brwNF2i_ubYTB1F1jMYyOd0Y1uY_As8uNpBynt_piolPtux6qEycBtOzi0SYd1xQs2YHYsN1gBHMvI9L_D3bUY0BV2lwbEwo2paw-M8mDEctLzKxBx4yfAg0Eh6aRMNi0lPSWRngyh8RbpRvQJfXCD7Q5k6-YHKro9gNGQauGOAfJuonDDOESGdDCOPMd8IA86Kkg6Taxxbxt5VHFxr1MeJsWpAxGEwupqHPi7juJxCmmruFwFi-4A38kjh9a3Yj5Ig2zwc2WG6-uxY_X5HwByGMEmNZDP2sX12a7a9QH0Cn8Q3VS7MN1s3dN8UxbEWNyvEQin_gWQub4dmCTz4aaYDQfIoFhvnnYSshE55ZdZ06YAHeiBFmlvIIO_FCC1mI_Xoz--Tp85DtyNvwhQJR4asYT2JXUVA2joXzeot1o5uM9YcioX5_Qq_pRi9RrUQj6DLQdAZR-EmxWQ0lE7QRVntpUjaDABPhFCEQ=w2940-h1662?auditContext=prefetch)
*Screenshot: the edit (pencil) icon is encircled in red.*

---

## Delete a forecast

1. In the **Forecast** list, click the **trash** icon (🗑️) in the **Actions** column.
2. Confirm the deletion.

> **Note:** Deleting a forecast removes only the forecast configuration.  
> It does **not** delete your Cost Group or any historical cost data.

![Forecast list — click the trash icon to delete](https://lh3.googleusercontent.com/rd-d/ALs6j_ENAZvsywJndzS1F8SzvqzYd1v1GkfHQT3QMit0bdrDhPxKjALjy7lXT33eLoBm0O1IU1vD9CxdiNtq5UEfp4pX_xhl9qvCtTT9ZFjxm0WWrJmiMQfxEACEF9UY_2EyWIQbEDHPKdgyRGgEhKzI_WLozI2mmGUsAJ32S_AwY8JjtJalIWeXAD5gva-ZRCysOkouoXelUWvslpP3sTpPr-t7wLhKzHIFs9WItkOMzeGlTEqwny9YUt6LY6Wei213_NgECnXPh62fSukySCYIwO6rpTVCBxnZTRTAykQLEBPq0kVZ3TIn8-qwFrLuh1qXRTZTlwYgo8ulyIuOcRFAtrTLf5eTTt_xjNphyJicpnixZXDXaptKP9prwFKfRg_CdjeQEP9iwmuqXZyOMAgOmP5ouUu--PfgDKA0ZtOkRVkHbDfj2FDWg7n7JZu-ReWQA3S8ZOcy9LiYg5jeHN_NRjV-BfCIeRjKzHY-qxIFDCT4pHl9glBqPyBv2BmMXcU5FacSRL_4WKdmTWXXYXyjsWZrTmyv8wiXKkwTvZd5aU5TQtBe8E7-RwW7Fi-kq-pgoaVao2DrAQytuwCPJlER4yc0PN7_sMbqnLq_oCpgtIm35TcDmL8ok4C3_bLpyVYR-ePFBRcK1zkBO7SvIvBtuG0SHF9rN9-0TgiqBxHJILrVaLOQrYmArclXL6pKnHwW0JX5lHGgc0n-n5AW6yc5apTE-M6Phm8zFhZw8fLzZIEK_cFlqKtmZivx2zFW2KQ3vzi5n7Lai_4vyfPI-RbVp2GBCeH00jUFDiJqHubqSjLPwOrWUlwLPP60zbtFN24E3hNeE5rCnKX4gn7I_xiV4f4XGAM4ZnsMV-cAOGMMRPGfn2V90tNP2Cy74bP-M65pHbIWylDenpLzDwzAMGoAR2KOa0E1F0DmzZzzjz1jgDYOB1BwgCBf-yrdn4RAenxvUX75_AYxR6-9O9jdHz_3m4yTfdzrIzYyH7Q_AiZEh5mCZKjjBDiQdm-O-1qH-BbKoNDUoiPZ=w2940-h1662?auditContext=prefetch)
*Screenshot: the delete (trash) icon is encircled in red.*


## View Forecast Data in CostGroup Overview

Other way to view forecast data, follow these steps:

1. **Navigate to the CostGroup Overview Page:**

   - The forecasting data is primarily displayed on the "Overview" page within the cost group.

2. **Adjust the Date Range to Include Future Dates:**

   - The forecast cost will only appear if the selected date range includes future dates.
   - Click on the date range selector.
   - Choose a date range that extends into the future (e.g., select the current month to the end of the month, or a future month).
   - Click "Apply" to update the view.

3. **Identify Forecasted Costs:**

   - Once the date range is adjusted, you will see a "Forecast Cost" line or section, typically colored gray, on the cost chart and in the data table.
   - This "Forecast Cost" represents the predicted future spending.

4. **Understand Grouping Limitations:**
   > **Note:**
   >
   > - A text indicator is displayed to inform users that the graph includes forecast data.
   > - There's a forecast data shown in the graph for the current day since the Cost and Usage Report (CUR) is still being processed.

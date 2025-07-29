# Cost Groups

## Overview

A Cost Group in OCTO is a powerful feature that provides a customized view of your cloud costs and usage. They are essentially filters that allow you to break down your cloud expenses according to various dimensions, offering a granular perspective on your spending.

> **Important:** This feature is only available to Admins in your OCTO organization. This is to ensure that cost data and financial information is managed and viewed by authorized personnel only, thus maintaining data integrity and security within your organization.

---

## Understanding Combinations in Cost Groups

### What are Combinations?

Combinations are the fundamental building blocks of Cost Groups in OCTO. They enable users to customize which accounts, services, regions, usage, instance, availability zone, API operation, invoice, tags and resources are included in a specific cost group by defining precise filtering criteria. Think of combinations as advanced filters that let you break down and analyze your cloud costs across multiple dimensions and providers.

As cloud computing expanded, managing costs across multiple services and providers became increasingly complex. Many organizations struggle to control spending and use resources efficiently as their cloud usage grows. Monitoring and organizing resources across different platforms can be difficult and time-consuming. OCTO simplifies this process with combinations, allowing for smarter and more efficient cost management.


### How Combinations Work

Combinations work across all three cost group creation methods:

- **Manual Creation**: Direct attribute selection using combinations of vendor, account, service, region, usage type, instance, availability zone, API operation, invoice and tags.
- **AI-Cost Group**: Pre-configured combinations focused on AI and ML services across cloud providers. For detailed instructions, refer to **[AI Cost](aicost.md)** documentation.
- **Container-Cost Group**: Specialized combinations for containerized workloads and Kubernetes environments. To learn how to set this up, visit **[Container Cost](container-cost.md)** guide.

In the combination interface, you'll find:

- **Vendors**: Support for AWS, Azure, and GCP.
- **Attributes**: Specific resources within each category that can be included or excluded. Options including account, product/service, region, usage types, instance, availability zone, API operation, invoice and tags.
- **Operations**: Logical operators (`is`, `is not`, `AND`, `OR`) to create advanced filtering rules.

### Creating Combinations

When creating any type of cost group, you'll work with combinations to define your filtering criteria:

1. **Select Vendor**: Choose from AWS, Azure, or GCP.
2. **Choose Attributes**: Specify which resources to include or exclude. Pick from  account, product/service, region, usage types, instance, availability zone, API operation, invoice and tags.
4. **Apply Operations**: Use logical operators to create advance rules.
5. **Combine Multiple Filters**: Layer different combinations for precise cost grouping.

The chosen category and attributes determine which resources will be included in your cost group. You can refine your selection by specifying subjects, choosing from all available options or selecting specific accounts, products, regions, tags, and other attributes based on your registered cloud accounts and requirements.

---

## Managing Cost Groups

Cost Groups is a key feature in OCTO as discussed in this article. This section covers how to manage your cost groups efficiently, including how to create, edit, remove, and view cost groups.

> **Note:** Only Admin accounts can create, edit, and remove cost groups.

### Creating a Cost Group

Head to the left side panel section and select **Cost Group**. 

![CostGroup Management](https://lh3.googleusercontent.com/d/1WxnW6Ffhb4UmtddolM_mcfgPoI0dbx5U
)

---

### Step 1: Create a New Cost Group

- Click on **+ CREATE COST GROUP** to start.

![Create Cost Group](https://lh3.googleusercontent.com/d/1ePgZP_HZX6fnHp1IonSg_AVpdBDTIDBa
)

---

### Step 2: Select a Cost Group Type

Select the type of Cost Group you want to create. The steps below show how to create a Manual Creation cost group, which is the default option and gives you full control over your cost group configuration.

### Manual Creation

Choose **Manual Creation** to have full control over which AWS or cloud resources to include.

This option allows you to manually select cloud assets by applying filters based on multiple attributes and operations to create precise cost groupings.

![Manual Creation](https://lh3.googleusercontent.com/d/1S5Y4Z8Oep06X246gzSBSU0cOqqzwfIo1
)

#### Define Cost Group Details

Provide a name and description for the cost group, then customize it by selecting an avatar and color.

![Fill CostGroup Details](https://lh3.googleusercontent.com/d/13sy-FQStIMCRwj_ja9_iee34buahklDd
)

#### Add Filters

Select from the available attributes and combine them using logical operations to define your cost group criteria:

| Attribute | Example Value | Description |
|-----------|---------------|-------------|
| **Account ID** | `123456789012` | AWS account number |
| **Service** | `Amazon EC2`, `Amazon S3` | AWS services |
| **Region** | `us-east-1`, `ap-southeast-1` | AWS region |
| **Usage Type** | `BoxUsage:m5.large` | Type of usage measured |
| **Instance Type** | `t3.micro`, `m5.large` | EC2 instance types |
| **Availability Zone** | `us-east-1a` | Specific zone within the selected region |
| **API Operation** | `RunInstances`, `GetObject` | The AWS API request performed |
| **Invoice ID** | `1234-5678` | Invoice identifier for cost grouping |

**Available Operations**: Use these logical operators to create advance filtering rules:

- **`is`** (exact match)
- **`is not`** (exclude match)
- **`AND`** (combine multiple conditions that must all be true)
- **`OR`** (combine multiple conditions where at least one must be true)

![Manual Filter](https://lh3.googleusercontent.com/d/1a5XzcQi9zORjVRRM6iySeldSTNfjApag
)

#### Optional: Add Tag Filters

Add **Tag Filters** to include/exclude resources based on cost allocation tags such as:

- `Environment = Production`
- `Project = Alpha`

#### Change Cloud Provider

If you need to modify your cloud provider selection during the setup process:

**Delete Current Provider**: Click the trash icon to remove and change the current cloud provider or vendor.

![Delete Vendor](https://lh3.googleusercontent.com/d/1JhT7cNAyFvpAn8E0yVINnat7OVQwWPQY
)

**Add New Provider**: Click the **+Add Provider** button to select a different cloud provider.

![Add Provider](https://lh3.googleusercontent.com/d/1BNaKBBqfAGjZffwBL0HTICN91odifl1S
)

**Select and Confirm**: Choose your desired provider from the available options and click the **Confirm** button to apply the changes.

![Select Provider](https://lh3.googleusercontent.com/d/14uBpfoyMBLn33TTgkXZkaDS0N_JtyiQE
)

Click **CREATE COST GROUP** to finalize the cost group setup.

---

## Viewing a Cost Group

Once your cost group is created, click on it to view comprehensive insights and analytics. The Cost Group dashboard provides multiple ways to analyze and understand your cloud spending:

### Time Range Filtering

Filter your cost data by different time periods (daily, monthly, or custom range) to analyze spending patterns over specific timeframes.

![Filter Time](https://lh3.googleusercontent.com/d/1k_eZP_pkLFS6TMIuJ-xQh316QwhOh1Lb
)

### Cost Visualization Graphs

View your cost data through various chart types and visualizations to better understand spending trends and patterns:

![Cost Overview Graph1](https://lh3.googleusercontent.com/d/1v9cLezcnC9Fa01oji--287Tg8JIys4SV
)

![Cost Overview Graph2](https://lh3.googleusercontent.com/d/1NLrxmKgaqhKlG2pwia7_xYWB8nO0T4IP
)

![Cost Overview Graph3](https://lh3.googleusercontent.com/d/16dFJXx_2tFBrGqmaJL4dN4VjAKcgeghP
)

![Cost Overview Graph4](https://lh3.googleusercontent.com/d/1OikN_IcZBHLXewFhyvu8iyoI0fxmjweI
)

### Filtering and Grouping Options

Customize your cost analysis by applying additional filters and grouping data by different dimensions such as account, product/service, region, usage type, charge type, billing account, category and vendor.

![Filter and Group Options](https://lh3.googleusercontent.com/d/1bNkU1ot3xk3Ztdt04fLwpAUVVZCE-5LR
)

## Edit and Delete Cost Group

Only Admin OCTO accounts can edit cost groups which can then edit combinations and change anomaly threshold. Click the **Action** button and now you can select between editing the combination info, the combination itself, change anomaly threshold, or delete it.

![Edit and Delete Cost Group](https://lh3.googleusercontent.com/d/10d4J6gg3MKf8rGZkHnN0aPEwyb5dUcXC
)
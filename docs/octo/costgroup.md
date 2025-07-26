# Cost Groups - Complete Guide

## Overview

A Cost Group in OCTO is a powerful feature that provides a customized view of your cloud costs and usage. They are essentially filters that allow you to break down your cloud expenses according to various dimensions, offering a granular perspective on your spending.

## What are Cost Groups?

Cost Groups in OCTO are groupings that can be defined based on specific criteria. They allow you to analyze and manage your cloud costs and usage in a way that aligns with your business needs and structure. Whether it's by cloud provider accounts, services, regions, or tags, cost groups help you understand where your money is going and how resources are being utilized.

## Detailed Analysis

Cost Groups offer the flexibility to view your cloud costs and usage across a multitude of dimensions, such as specific cloud provider accounts, services, regions, or tags. This allows you to 'slice and dice' your costs, providing a granular analysis of your cloud spending. It helps you uncover hidden costs, identify trends, or spot inefficiencies, thus contributing to a more comprehensive cloud cost management strategy and in-depth analysis of your cloud spending.

> **Important:** This feature is only available to Admins in your OCTO organization. This is to ensure that cost data and financial information is managed and viewed by authorized personnel only, thus maintaining data integrity and security within your organization.

Cost groups in OCTO are a flexible and powerful tool designed to help you better understand and manage your cloud costs. By providing the ability to visualize and customize your cost analysis, cost groups empower you to make more informed decisions about your cloud expenditure.

---

## Understanding Combinations in Cost Groups

### What are Combinations?

Combinations are the fundamental building blocks of Cost Groups in OCTO. They enable users to customize which accounts, services, regions, or resources belong to a specific cost group by defining precise filtering criteria. Think of combinations as advanced filters that allow you to slice and dice your cloud costs across multiple dimensions and providers.

With the rise of cloud computing came the challenge of managing costs across different services and providers. As demand for cloud resources increases, companies struggle to manage their expenses, leading to unoptimized usage. The complexity of tracking cloud resources from different providers can be overwhelming and time-consuming. OCTO solves this problem through the power of combinations.

### How Combinations Work

Combinations work across all three cost group creation methods:

- **Manual Creation**: Direct attribute selection using combinations of vendor, account, service, region, usage type, and tags
- **AI-Cost Creation**: Pre-configured combinations focused on AI and ML services across cloud providers  
- **Container-Cost Creation**: Specialized combinations for containerized workloads and Kubernetes environments

In the combination interface, you'll find:

- **Vendors**: Support for AWS, Azure, and GCP
- **Categories**: Options including account, product/service, region, tags, usage types, and more
- **Attributes**: Specific resources within each category that can be included or excluded
- **Operations**: Logical operators (`is`, `is not`, `AND`, `OR`) to create complex filtering rules

### Creating Combinations

When creating any type of cost group, you'll work with combinations to define your filtering criteria:

1. **Select Vendor**: Choose from AWS, Azure, or GCP
2. **Choose Category**: Pick from account, product, region, tag, etc.
3. **Define Attributes**: Specify which resources to include or exclude
4. **Apply Operations**: Use logical operators to create complex rules
5. **Combine Multiple Filters**: Layer different combinations for precise cost grouping

The chosen category and attributes determine which resources will be included in your cost group. You can refine your selection by specifying subjects, choosing from all available options or selecting specific accounts, products, regions, tags, and other attributes based on your registered cloud accounts and requirements.

---

## Managing Cost Groups

Cost Groups is a key feature in OCTO as discussed in this article. This section covers how to manage your cost groups efficiently, including how to create, edit, remove, and view cost groups.

> **Note:** Only Admin accounts can create, edit, and remove cost groups.

### Creating a Cost Group

Head to the left side panel section and select **Cost Group**. 

![CostGroup Management](https://drive.google.com/uc?export=view&id=1WxnW6Ffhb4UmtddolM_mcfgPoI0dbx5U)

---

### Step 1: Create a New Cost Group

- Click on **+ CREATE COST GROUP** to begin

![Create Cost Group](https://drive.google.com/uc?export=view&id=1ePgZP_HZX6fnHp1IonSg_AVpdBDTIDBa)

---

### Step 2: Select a Cost Group Type

You can create a cost group using one of three approaches:

### 1. Manual Creation

Choose **Manual Creation** to have full control over which AWS or cloud resources to include.

This option allows you to manually select cloud assets by applying filters based on multiple attributes. These attributes include:

- **Account ID**
- **Service**
- **Region**
- **Usage Type**
- **Instance Type**
- **Availability Zone**
- **API Operation**
- **Invoice ID**

You can define each filter using the operations:

- `is` (equals to the value)
- `is not` (not equals to the value)
- `AND` (combine multiple conditions that must all be true)
- `OR` (combine multiple conditions where at least one must be true)

![Manual Creation](https://drive.google.com/uc?export=view&id=1S5Y4Z8Oep06X246gzSBSU0cOqqzwfIo1)

#### Define Cost Group Details

Provide a name and description for the cost group, then customize it by selecting an avatar and color.

![Fill CostGroup Details](https://drive.google.com/uc?export=view&id=1QvT9lnq3_-aUR0LOCCV1yWeh5FL6crpx)

#### Add Filters

Select attributes from the following options and apply operations:

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

Supported operations for all filters:

- **`is`** (exact match)
- **`is not`** (exclude match)
- **`AND`** (combine multiple conditions that must all be true)
- **`OR`** (combine multiple conditions where at least one must be true)

![Manual Filter](https://drive.google.com/uc?export=view&id=1a5XzcQi9zORjVRRM6iySeldSTNfjApag)

#### Optional: Add Tag Filters

Add **Tag Filters** to include/exclude resources based on cost allocation tags such as:

- `Environment = Production`
- `Project = Alpha`

Click **CREATE COST GROUP** to finalize the cost group setup.

---

### 2. AI-Cost Creation

Use **AI-Cost** to intelligently group and analyze services related to AI and ML workloads across cloud vendors.

This method helps identify and track costs related to AI-specific services like Amazon SageMaker, Bedrock, Polly, and others.

![Ai Cost](https://drive.google.com/uc?export=view&id=1IUc7EP-vPagZKe_jJzWoTlW3a8l3bBO5)

#### Select AI Services

Choose one or more AI-related services from your connected cloud providers.

![Ai Services](https://drive.google.com/uc?export=view&id=1MnMjkeGUk3PBbSXCJl5FmVWVe1hSqBO3)

#### Fill in Cost Group Details

Add the required information (Name, Avatar, Color and Description)

![Fill CostGroup Details - AI](https://drive.google.com/uc?export=view&id=1H9MarEynfcERw1fpTtZSa_ztxcQngIC0)

Click **CONFIRM AND CREATE** to finish.

![Create Cost Group - AI](https://drive.google.com/uc?export=view&id=1Q9A87hwfSwMT61s_whXDJsFGRSxmpj-H)

---

### 3. Container-Cost Creation

Use **Container-Cost** to track costs related to **Amazon ECS**, **Amazon EKS**, or other containerized workloads across multiple cloud environments.

![Container-Cost](https://drive.google.com/uc?export=view&id=1PL8MfEtCY6JXt5vvaSLfN-xQfcj0mCvH)

#### Select Container Services

Choose workloads running on:

- Amazon ECS
- Amazon EKS

![Select Container Services](https://drive.google.com/uc?export=view&id=1w5GPb76F8LLMcJk0l0JyFtz2DemDC-mF)

#### Fill in Cost Group Details

Add the required information for your container cost group.

![Fill CostGroup Details - Container](https://drive.google.com/uc?export=view&id=1rjQ9cgdtwqV2lQplAzU4Uk2QOQOcYG60)

Click **CONFIRM AND CREATE** to complete setup.

![Create Cost Group - Container](https://drive.google.com/uc?export=view&id=10cM8dS_mqs98IG9MJ43adybke38DqNRo)

---

## Viewing a Cost Group

Once your cost group is created, click on it to view comprehensive insights and analytics. The Cost Group dashboard provides multiple ways to analyze and understand your cloud spending:

### Time Range Filtering

Filter your cost data by different time periods (daily, monthly, or custom range) to analyze spending patterns over specific timeframes.

![Filter Time](https://drive.google.com/uc?export=view&id=1k_eZP_pkLFS6TMIuJ-xQh316QwhOh1Lb)

### Cost Visualization Graphs

View your cost data through various chart types and visualizations to better understand spending trends and patterns:

![Cost Overview Graph](https://drive.google.com/uc?export=view&id=1v9cLezcnC9Fa01oji--287Tg8JIys4SV)

![Service Breakdown Chart](https://drive.google.com/uc?export=view&id=1NLrxmKgaqhKlG2pwia7_xYWB8nO0T4IP)

![Regional Cost Distribution](https://drive.google.com/uc?export=view&id=16dFJXx_2tFBrGqmaJL4dN4VjAKcgeghP)

![Usage Trends Analysis](https://drive.google.com/uc?export=view&id=1OikN_IcZBHLXewFhyvu8iyoI0fxmjweI)

### Filtering and Grouping Options

Customize your cost analysis by applying additional filters and grouping data by different dimensions such as services, accounts, or tags.

![Filter and Group Options](https://drive.google.com/uc?export=view&id=1bNkU1ot3xk3Ztdt04fLwpAUVVZCE-5LR)

### Anomaly Detection and Data Management

- **Display Anomalies**: Click the gear icon to enable anomaly detection and identify unusual spending patterns
- **Reload Data**: Use the reload icon to refresh the cost data with the latest information

![Anomaly Detection and Reload Options](https://drive.google.com/uc?export=view&id=1Uxv03WhJ8KDHzAFqxbqPXNBGwDJbrrzs)

### Search and Export Features

- **Search Functionality**: Search by specific services or vendors to quickly find relevant cost data
- **CSV Download**: Click the download button to export your cost data in CSV format for further analysis

![Search and Download Features](https://drive.google.com/uc?export=view&id=16mO-wMdYvwMPQCrTlOBcrI1bAq0xFgEW)

### Detailed Service Information

Click the **Details** button to access comprehensive information about specific services, including names, descriptions, and the ability to search and sort based on your preferences.

![Service Details View](https://drive.google.com/uc?export=view&id=1Ua7sZNwC6IfzB0FJwYvyZ7bET2_P3VID)

### Additional Cost Group Features

The Cost Group dashboard provides access to several specialized views and features:

#### Discount Plans
View and manage discount plans associated with your cost group.

![Discount Plans](https://drive.google.com/uc?export=view&id=1KvBPRkRBvCUmduVgQ7rRo20rO99fSSDy)

#### Assets Inventory
Access a comprehensive inventory of all assets included in your cost group.

![Assets Inventory](https://drive.google.com/uc?export=view&id=1sxAXMyRmScErfYgt3T92mfZ02OF70aca)

#### Budget Management
Monitor and manage budgets associated with your cost group.

![Budget Management](https://drive.google.com/uc?export=view&id=1xM-KImCj4mBkoh7D52h8WMOT8ezPlQaM)

#### Anomaly Analysis
Review detailed anomaly detection results and investigate unusual spending patterns.

![Anomaly Analysis](https://drive.google.com/uc?export=view&id=1tYHAfuPLH2_R6CC1gTw9g2xuSciZd2Zh)

#### Charge Breakdown
Analyze detailed charge information and billing components.

![Charge Breakdown](https://drive.google.com/uc?export=view&id=1W0Md26GCaa4SJelL38GZxpz3EPGIxFQR)

### Cost Group Configuration

#### Combination View
Review the filter combinations and criteria used to create your cost group. Available in two formats:

**Default View**: User-friendly display of your cost group configuration
![Default Configuration View](https://drive.google.com/uc?export=view&id=1I37vqrCo4o6FjovFLWzwrrrp2UTs8W8r)

**JSON View**: Technical representation of your cost group settings for advanced users
![JSON Configuration View](https://drive.google.com/uc?export=view&id=1o6DOVqmahUT_pbmlCvidmNQAEPSkw-F_)

#### Cost Group Information
Access basic information and metadata about your cost group, including creation date, description, and configuration details.

![Cost Group Information](https://drive.google.com/uc?export=view&id=1TK9XVM1D_vd6PtkHvWUbSzpve3LEfAbK)

### Complete Cost Group Dashboard

The main Cost Group dashboard brings together all these features in a comprehensive interface for complete cost analysis and management.

![Complete Cost Group Dashboard](https://drive.google.com/uc?export=view&id=1HYIA5EI6ctsjBzw_zSdtfc89TXv-LK0x)

---

## Edit and Delete Cost Group

Only Admin OCTO accounts can edit cost groups which can then edit combinations and change anomaly threshold. Click the **Action** button and now you can select between editing the combination info, the combination itself, change anomaly threshold, or delete it.

![Edit and Delete Cost Group](https://drive.google.com/uc?export=view&id=10d4J6gg3MKf8rGZkHnN0aPEwyb5dUcXC)
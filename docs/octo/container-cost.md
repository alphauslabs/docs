# Container Cost

**Container Cost** in OCTO is a specialized feature that provides deep, granular visibility into the costs of containerized workloads running in **Amazon ECS and EKS**. It helps teams accurately track, analyze, and optimize container resource usage and associated cloud spend — which are often hidden within broader infrastructure costs.

Built on **AWS Split Cost Allocation Data (SCAD)**, this feature brings transparent, workload-level attribution to your container infrastructure costs, allowing you to understand what you're spending, where, and why.

<div style="border-left: 4px solid #007acc; padding: 0.75em 1em; background-color: #f0f8ff;">
  <strong>Note:</strong> Container Cost supports <strong>AWS</strong> only, with plans to support other cloud platforms in the future.
</div>

## What is Container Cost?

In traditional cloud billing models, container costs are difficult to isolate because containers share compute and memory resources. Container Cost solves this problem by utilizing AWS SCAD to break down shared infrastructure costs and attribute them to individual containers, tasks, pods, or services.

With Container Cost, you can:

- Track costs at the **task**, **pod**, and **workload** level
- Attribute EC2 and Fargate costs based on actual usage or resource requests
- Analyze container spend using granular filters
- Empower engineering and finance teams with accurate visibility and accountability

Currently supported services:

- **Amazon ECS** (EC2 and Fargate)
- **Amazon EKS**

---

## Enabling Split Cost Allocation Data (SCAD) in AWS

To use Container Cost, **Split Cost Allocation Data (SCAD)** must be enabled in your AWS Billing settings. SCAD is what allows container-level cost attribution in CUR (Cost and Usage Report) data. SCAD data is not available through AWS Cost Explorer. It is only accessible via Cost and Usage Reports (CUR or CUR 2.0 with Data Exports).

### Step 1: Opt in to SCAD

1. Go to [AWS Billing and Cost Management Console](https://console.aws.amazon.com/costmanagement/) using a payer account. Only **payer accounts** can enable SCAD. Linked/member accounts can view data but cannot manage these settings.

2. In the left navigation, select **Cost Management preferences**

3. Under **Split cost allocation data**, select the services to enable **(Amazon ECS and/or Amazon EKS)**:
   ![Split Cost Allocation Data Settings](https://lh3.googleusercontent.com/d/1hIFzAIkuFSJPzD3Dz-Tb20KeAMGHlMgS)

4. If enabling for **EKS**, choose one of the following cost allocation methods:

    - **Resource requests**  
        Allocates EC2 costs based on CPU and memory requests per pod.  
        _Recommended as a baseline to get started._

    - **Amazon Managed Service for Prometheus**  
        Allocates EC2 costs based on the higher of resource requests or actual utilization.  
        _Requires additional setup._

    - **Amazon CloudWatch Container Insights**  
        Offers deeper visibility into shared EC2 costs for EKS clusters.

    You may choose **Resource requests** at the very least to enable basic container-level cost tracking.

---

### Step 2: Configure Your Cost and Usage Report (CUR)

1. In the AWS Billing Console, under **Legacy Pages**, open **Cost and Usage Reports**

    ![Legacy Pages - Cost and Usage Reports](https://lh3.googleusercontent.com/d/1WRTBwTUr-_TS87JP8k-Y5QpUe1rFAXbI)

2. Create a new report or edit an existing one
3. On the **Specify report details** page:

    - Enable **Split cost allocation data**
        ![Split Cost Allocation Data Option in CUR](https://lh3.googleusercontent.com/d/1KUyrn9nQOPjJ-857WHdoEKd9Zbd7dmd9)
    - Ensure your CUR includes:
        - **Resource IDs**
        - **Hourly granularity**

<div style="border-left: 4px solid #007acc; padding: 0.75em 1em; background-color: #f0f8ff;">
  <strong>Note:</strong> SCAD data may take up to <strong>24 hours</strong> to begin appearing in your Cost and Usage Report (CUR).
</div>


---

## Creating a Container Cost Group

After enabling SCAD and allowing time for the data to populate in your Cost and Usage Report (CUR), you can now create a **Container Cost Group** in OCTO to visualize your container cost and usage.

1. **Navigate to Cost Group Manager** in OCTO and click **Create Cost Group**
      ![Step 1: Create Container Cost Group](https://lh3.googleusercontent.com/d/14UqAxhDJDgyydCncgip87LPv7n8S1cHu)
2. **Choose the _Container Cost_ option**
      ![Step 2: Select Container Cost Option](https://lh3.googleusercontent.com/d/1-jJwaTdGrAAP_Gq5aJsRTMP7iZ8ibu8i)
3. **Select supported services** (ECS and/or EKS) to include in your cost group
      ![Step 3: Select Supported Services (ECS/EKS)](https://lh3.googleusercontent.com/d/1yzhKbDpBBPbKoZ36qilNaDfoJJw9cJer)
4. **Fill out the basic details**, then continue through the remaining setup steps
5. **Click _Confirm and create_** to finalize the container cost group
      ![Step 5: Create](https://lh3.googleusercontent.com/d/1YLcELFX-DxyBB2Qqh_95pGtVLM2XLdyR)

6. **Once created**, your cost group will appear in the list with a **dedicated Insights tab**, where you can explore container-level cost and usage across multiple dimensions.
      ![Step 6: Container Cost Group Overview](https://lh3.googleusercontent.com/d/1Q8s0qTFFaZrdSHAgzrPciN63MwJJ1z5Y)


---

## What You’ll See

When viewing a **Container Cost group**, you’ll access a dedicated **Insights** tab that displays container-level cost and usage data.
      ![Container Cost Group - Main View](https://lh3.googleusercontent.com/d/1gjSTmT8kdnEcVXGo6F5VlXyiVgfEG5uo)

For **ECS workloads**, you can group costs and usage by:

- Cluster
- Service
- Task
- EC2 Instance
- Tagged

![ECS Cost](https://lh3.googleusercontent.com/d/1Ka1L8L2nJ-JDtPztOCWeSiqcp7v9kk9Z)
![ECS Usage](https://lh3.googleusercontent.com/d/1oOGdAGtuo7KAMxssjR8IymTldnTcQHvU)


For **EKS workloads**, you can group costs and usage by:

- Cluster
- Namespace
- Deployment
- Workload name
- Workload type
- Node
- Pod
- EC2 Instance
- Tagged

![EKS Cost](https://lh3.googleusercontent.com/d/1b-Gj529LRL9c5iVHrUexstBmqHxJDsVO)
![EKS Usage](https://lh3.googleusercontent.com/d/1_zBQr66jII9G8_oyev4ZFvg1NImJ6pS1)


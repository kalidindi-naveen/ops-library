# AWS – enable Cost Explorer

Billing and Cost Management - Cost Explorer - Enable/Launch Cost Explorer.
- For AWS Cost Explorer -- the console UI is free to enable and use; you only pay for certain advanced features.
- UI usage: Viewing charts/tables, creating saved views, and using default reports in the AWS console costs 0 USD.
- API calls: Cost Explorer APIs (e.g., GetCostAndUsage, GetCostForecast) cost 0.01 USD per request; heavy dashboards or frequent jobs can add up but are still usually low.
- Hourly granularity: Optional [EC2 only -- get cost details per instance]; priced at 0.01 USD per 1,000 hourly usage records per month, which is extremely cheap (about 0.003 USD/month for one always‑on EC2 instance).

Cost Allocation Tags
- Decide the exact tag keys [Ex: Environment, Application, Owner, and CostCenter]
- Tag your AWS resources [Ex: For bulk tagging existing resources you can use: Tag Editor in AWS console, Terraform default_tags, Scripts with boto3 / AWS CLI]
- Activate them as cost allocation tags [Ex: AWS Console → Billing & Cost Management → Cost allocation tags → User-defined cost allocation tags, locate the keys: Environment, Application, Owner, CostCenter (may take up to 24 hours after first use to appear) → Activate]
- Use tags in Cost Explorer [Ex: Cost Explorer → use 
    - Group by → Tag: Environment / Application / Owner / CostCenter to see cost by that tag
    - Filters → Tag to restrict, for example, only Environment = prod or CostCenter = CC1234]

Enable AWS Budgets
- Monthly account budget
- Service-level budgets (EC2, RDS, NAT Gateway)

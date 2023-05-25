---
layout: page
title: Genomics Analysis Service
description: Practice with AWS!
img:
importance: 1
category: course proj
---

Final Project for MPCS 51083 Cloud Computing at the University of Chicago.

Step by step we built a fully functional and scalable SaaS-based application for genomics data analysis by implementing both front and back ends, and leveraging AWS features including:
- EC2
- object storage (S3, Glacier)
- message queues (SQS with SNS)
- email service (SES)
- elastic load balancer (ELB)
persistence of application achieved via DynamoDB.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/GAS_basic_components.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Diagram showing the basic components of the application
</div>

After adding features of archival (S3 Glacier), email notification (SES), load balancer (ELB), and authorization and payment services (not really going to pay), the diagram becomes:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/GAS_migration.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Diagram showing the various GAS components/services and interactions (final ver)
</div>

# Dataverse Schema v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

Schema principles:

- Reuse standard Dynamics entities first
- Add custom entities only where differentiation exists
- No duplicate customer master data
- Multi-tenant safe naming
- Publisher prefix: axs
- Managed solution only
- Environment variable driven configuration

Primary entity groups:

Standard entities

AXSource custom entities

Configuration entities

Audit entities

## Standard Dynamics Entities

Lead

Purpose:

Primary qualification record


Account

Purpose:

Customer and hierarchy context


Contact

Purpose:

Lead and customer relationships


Opportunity

Purpose:

Future conversion target

No autonomous creation in v1


Product

Purpose:

SKU and product-line intelligence


Price List

Purpose:

Product pricing context


Activity

Purpose:

Tasks, notes, qualification actions


System User

Purpose:

Seller ownership


Team

Purpose:

Branch and routing logic
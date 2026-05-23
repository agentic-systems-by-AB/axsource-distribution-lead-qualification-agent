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

## AXSource Custom Entities

axs_QualificationHistory

Purpose:

Stores qualification runs, confidence scores, narratives, and audit history


axs_DistributorPartner

Purpose:

Represents distributor partner and channel relationships


axs_BranchTerritory

Purpose:

Stores branch ownership, routing rules, and territory assignments


axs_ChannelClassification

Purpose:

Stores direct, inbound, partner, and channel classifications


axs_QualificationConfiguration

Purpose:

Stores distribution-specific BANT+ settings and configurable scoring rules

## Entity Relationships

Lead

1:N

axs_QualificationHistory

Reason:

A lead may be evaluated multiple times


Account

1:N

axs_DistributorPartner

Reason:

An account can participate in multiple partner relationships


Team

1:N

axs_BranchTerritory

Reason:

Branch routing and ownership


Lead

N:1

axs_ChannelClassification

Reason:

Each lead receives one channel classification


axs_QualificationConfiguration

1:N

axs_QualificationHistory

Reason:

Qualification runs should retain configuration context

## axs_QualificationHistory Columns

qualificationhistoryid

Type:

GUID

Purpose:

Primary key


axs_name

Type:

Text

Purpose:

Qualification run name


axs_lead

Type:

Lookup → Lead

Purpose:

Related lead


axs_qualificationscore

Type:

Whole Number

Purpose:

Overall qualification score


axs_confidencescore

Type:

Decimal

Purpose:

Confidence level


axs_confidenceband

Type:

Choice

Values:

High

Medium

Low


axs_qualificationnarrative

Type:

Multiline text

Purpose:

Generated explanation


axs_recommendedbranch

Type:

Lookup → Team

Purpose:

Suggested branch assignment


axs_recommendedowner

Type:

Lookup → System User

Purpose:

Suggested seller


axs_channelconflictfound

Type:

Yes/No

Purpose:

Conflict detection result


axs_crediteligible

Type:

Yes/No

Purpose:

Eligibility status


axs_runcompletedon

Type:

Date Time

Purpose:

Audit timestamp

## axs_BranchTerritory Columns

branchterritoryid

Type:

GUID

Purpose:

Primary key


axs_name

Type:

Text

Purpose:

Territory name


axs_branchteam

Type:

Lookup → Team

Purpose:

Owning branch


axs_region

Type:

Text

Purpose:

Region name


axs_country

Type:

Text

Purpose:

Country


axs_stateprovince

Type:

Text

Purpose:

State or province


axs_postalcoderange

Type:

Text

Purpose:

Routing range


axs_defaultowner

Type:

Lookup → System User

Purpose:

Fallback seller assignment


axs_active

Type:

Yes/No

Purpose:

Routing availability
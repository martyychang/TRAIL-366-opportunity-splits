# SFDX App

This repo highlights the question: How does one enable [Opportunity Splits][2] in a scratch org?

## Dev, Build and Test

1. Clone this repo
2. Create a new scratch org using **config/project-scratch-def.json**
3. Push source to the new scratch org using `sfdx force:source:push`

At this point you will see the error below, caused by the fact that
Opportunity Splits is _not_ enabled in the scratch org.

```txt
PROJECT PATH                                                                   ERROR
─────────────────────────────────────────────────────────────────────────────  ─────────────────────────────────────────────────────────────────
force-app/main/default/layouts/Opportunity-Opportunity Layout.layout-meta.xml  Invalid field:SplitOwner in related list:RelatedOpportunitySplits
```

## Workaround

Before pushing source to the scratch org, open the org first and enable Opportunity Splits.

## Resources

* "[Push Source to the Scratch Org][1]." _Salesforce DX Developer Guide_.

[1]: https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_push_md_to_scratch_org.htm
[2]: https://help.salesforce.com/articleView?id=teamselling_opp_splits_overview.htm&type=5

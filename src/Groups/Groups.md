# Groups

This directory contains common [AutoREST.PowerShell](https://github.com/Azure/autorest.powershell) configurations for Groups v1.0 and/or beta modules.

## AutoRest Configuration

> see <https://aka.ms/autorest>

``` yaml
require:
  - $(this-folder)/../readme.graph.md
```

### Directives

> see https://github.com/Azure/autorest/blob/master/docs/powershell/directives.md

``` yaml
directive:
  - remove-path-by-operation: group\.groupLifecyclePolicy_.*$|group_(Get|Create|Update|Delete)GroupLifecyclePolicies$|group\.team.*$|user\.joinedGroup.*$|group\.site\.onenote.*$|.*\.onenote\..*parent.*|.*\.calendarView.*|.*\.notebook\.section.*|.*\.sectionGroup\.section.*|.*\.section\.page.*|.*\.calendar\.event\..*$|.*\.event\..*$
  - where:
      verb: Get
      subject: ^(GroupLifecyclePolicy)$
      variant: ^List$
    set:
      subject: $1ByGroup
  - where:
      subject: ^(GroupLifecyclePolicy)(\1)+
    set:
      subject: $1
  - where:
      verb: Test
      subject: ^GroupProperty$
      variant: Validate1|ValidateExpanded1
    remove: true
  - where:
      verb: Test
      subject: ^(GroupDynamicMembership)$
      variant: Evaluate1|EvaluateExpanded1
    set:
      subject: $1Rule
  - where:
      verb: Remove
      subject: ^(Group)(LifecyclePolicy)Group$
    set:
      subject: $1From$2
  - where:
      verb: Add
      subject: ^(Group)(LifecyclePolicy)Group$
    set:
      subject: $1To$2
  - where:
      verb: Invoke
      subject: ^(RenewGroup)(LifecyclePolicy)Group$
    set:
      subject: $1$2
  - where:
      verb: Get
      subject: ^(GroupOnenote)Notebook(RecentNotebook)$
    set:
      subject: $1$2
  - where:
      verb: Update
      subject: ^(GroupOnenotePage)$
    set:
      subject: $1Content
  - where:
      verb: Update
      subject: ^(GroupOnenoteSectionPage)$
    set:
      subject: $1Content
  - where:
      verb: Update
      subject: ^(GroupOnenoteNotebookSectionPage)$
    set:
      subject: $1Content
  - where:
      verb: Update
      subject: ^(GroupOnenoteSectionGroupSectionPage)$
    set:
      subject: $1Content
  - where:
      verb: Update
      subject: ^(GroupOnenoteNotebookSectionGroupSectionPage)$
    set:
      subject: $1Content
  - where:
      verb: Get
      subject: ^(GroupSite)$
    set:
      subject: All$1
```

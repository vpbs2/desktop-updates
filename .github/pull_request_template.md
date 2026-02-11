# Description

> You can add the purpose of the change here or another context relevant to this PR. If any section does not make sense for your PR, please remove it. Also, take some care and 5 min to structure the PR description as this is usually the first thing the developer lands on while researching a bug.

## Documentation

- DevRev Work item: Required
- Figma:
- Technical Design Doc:
- Dependencies:
  1. List any other PRs that should be merged before this PR is merged

# Changes

## In Scope

- Provide a list of changes made in this PR

## Not In Scope

- Provide a list of changes that would make sense to have, but are not part of this PR and why

# Media (Screenshots or Videos)

> Provide screenshots or videos about the change made in this PR. For bugs, provide before and after so that reviewers can try it out themselves.

# Select What Tests Should Run For This PR

- [ ] accounts
- [ ] accounts-vista
- [ ] agent
- [ ] agent-builder
- [ ] article-content
- [ ] article-content-block
- [ ] article-directory-translations
- [ ] article-templates
- [ ] articles
- [ ] articles-vista
- [ ] chat-view
- [ ] commands
- [ ] commerce
- [ ] connections
- [ ] custom-objects-gantt-view
- [ ] custom-objects-list-view
- [ ] customer-portal
- [ ] customer-portal-auth
- [ ] customer-portal-knowledge-base
- [ ] customer-portal-search
- [ ] customer-portal-tickets
- [ ] customer-widget
- [ ] customers-list
- [ ] cz-admin
- [ ] cz-engine
- [ ] dashboard-builder
- [ ] dashboarding
- [ ] dbm
- [ ] directories
- [ ] domain-identity
- [ ] email-composer
- [ ] email-integration
- [ ] engagements
- [ ] error-screens
- [ ] fast-data-layer
- [ ] identity-dev-members
- [ ] identity-dev-orgs
- [ ] identity-dev-users
- [ ] imports
- [ ] incidents
- [ ] insights
- [ ] invitations
- [ ] issue-sidepanel
- [ ] issues-gantt-view
- [ ] issues-kanban-view
- [ ] issues-list-view
- [ ] jobs
- [ ] left-panel
- [ ] meetings
- [ ] notification
- [ ] notification-preferences
- [ ] onboarding
- [ ] opportunity
- [ ] opportunity-sidepanel
- [ ] part
- [ ] part-enhancement
- [ ] part-sidepanel
- [ ] part-widget
- [ ] parts-discovery
- [ ] parts-list
- [ ] parts-mfz-auth
- [ ] plug-for-devrev
- [ ] plug-inbox
- [ ] plug-inbox-options
- [ ] plug-platform-sdk
- [ ] plug-platform-widget
- [ ] portal-settings
- [ ] query-cache
- [ ] record-template
- [ ] rev-users
- [ ] rev-users-mfz-auth
- [ ] rev-users-vista
- [ ] search
- [ ] security
- [ ] sessions
- [ ] settings
- [ ] settings-mobile
- [ ] setup
- [ ] slas
- [ ] snap-ins
- [ ] snapkit-product-comments
- [ ] sprints
- [ ] tags
- [ ] tasks
- [ ] telephony
- [ ] ticket-sidepanel
- [ ] timeline
- [ ] trails-mfz-auth
- [ ] trails-v2
- [ ] translations
- [ ] user-access-mgmt-customer-roles
- [ ] user-access-mgmt-groups
- [ ] user-access-mgmt-segments
- [ ] user-access-mgmt-user-roles
- [ ] vista-gantt-view
- [ ] vista-nnl
- [ ] vista-shared
- [ ] widgets
- [ ] work
- [ ] work-creation
- [ ] work-creation-action
- [ ] work-filters
- [ ] work-kanban-vista
- [ ] work-merge
- [ ] work-sidepane
- [ ] work-vista
- [ ] workflows-config
- [ ] workflows-creation
- [ ] workflows-runs
- [ ] works-clustering
- [ ] works-table

# Checklist

## Author checklist

- [ ] I have focused the PR on one thing
- [ ] I have handled the `isLoading` and `isError` states of data-layer hooks
- [ ] I have only exported members that are needed
- [ ] I have considered using `React.memo`, `useMemo` and `useCallback` where appropriate
- [ ] I have considered adding a [feature flag](https://www.notion.so/devrev/How-to-add-and-use-feature-flag-in-devrev-web-7470932a75e74c97b4e5f0d08ee91178) if this is a feature
- [ ] I have considered updating/adding documentation (README.md, Storybook stories, …)
- [ ] I have considered updating/adding tests (unit, integration, e2e)
- [ ] I have considered removing possible dead code after I have removed the code
- [ ] I have considered adding a test suite in [run.yml](https://github.com/devrev/devrev-web/blob/main/.circleci/run.yml#L534), [e2e-qa.yml](https://github.com/devrev/devrev-web/blob/main/.circleci/e2e-qa.yml#L131) and [Aviator](https://app.aviator.co/github/rules)

## Code reviewer checklist

> As a code author, you can add an additional description here if you want the code reviewer to check additional things. Ex: As I made some changes in the plug platform, please check out that more thoroughly as I am not very confident with the changes there.

- [ ] I am able to understand the purpose of the PR
- [ ] I am able to read the code and understand it confidently
- [ ] I have checked newly generated libraries are properly [tagged and structured](https://www.notion.so/devrev/UI-Modules-and-Libraries-a81177e8ed4e4696ac84440aebafa47b)
- [ ] I have checked for the possibility of reusing existing code
- [ ] I have checked it follows our current [best practices](https://www.notion.so/devrev/Best-Practices-1096a44d6e674c99b347e5bb3ee2ff4b)

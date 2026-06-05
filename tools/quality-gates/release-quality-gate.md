# Release Quality Gate

Use this checklist before releasing 1C changes to production.

## Functional readiness

- [ ] Main business scenario tested
- [ ] Edge cases tested
- [ ] Regression risks checked
- [ ] User roles tested

## Code quality

- [ ] Code review completed
- [ ] No duplicated critical logic
- [ ] Queries reviewed for performance
- [ ] Server/client separation checked
- [ ] Error handling checked

## Data safety

- [ ] Backup plan prepared
- [ ] Data migration tested
- [ ] Rollback scenario prepared
- [ ] No destructive operations without confirmation

## Documentation

- [ ] Changes documented
- [ ] User instruction prepared if needed
- [ ] Technical notes added
- [ ] Release notes prepared

## Approval

- [ ] Developer approval
- [ ] Consultant approval
- [ ] Client/business owner approval, if required
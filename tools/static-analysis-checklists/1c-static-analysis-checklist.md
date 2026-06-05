# 1C Static Analysis Checklist

## Module structure

- [ ] Module has clear responsibility
- [ ] Export procedures and functions are justified
- [ ] Common logic is not duplicated
- [ ] Temporary logic is marked with TODO/FIXME
- [ ] Code does not contain client confidential data

## Naming

- [ ] Procedure names describe actions
- [ ] Function names describe returned values
- [ ] Variable names are meaningful
- [ ] Prefixes are used consistently where required

## Queries

- [ ] Query selects only required fields
- [ ] Query has necessary filters
- [ ] Joins are justified
- [ ] Temporary tables are used where helpful
- [ ] Query aliases are readable
- [ ] Complex logic is commented

## Error handling

- [ ] Exceptions are not silently ignored
- [ ] Error messages are understandable
- [ ] Critical errors are logged
- [ ] User-facing errors do not expose technical secrets

## Performance

- [ ] Large datasets are not processed on client side
- [ ] Loops do not execute unnecessary database queries
- [ ] Background jobs are used where needed
- [ ] Data is cached only when safe and justified

## Security

- [ ] Access rights are checked
- [ ] External input is validated
- [ ] Sensitive data is not logged
- [ ] Integration tokens are not stored in source code
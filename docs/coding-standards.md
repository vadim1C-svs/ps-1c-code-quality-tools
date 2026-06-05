# 1C Coding Standards

This document describes practical coding standards for 1C:Enterprise projects.

## General principles

1. Code should be readable and predictable.
2. Business logic should be separated from user interface logic.
3. Common logic should be moved to common modules.
4. Queries should be optimized and easy to understand.
5. Functions and procedures should have clear names.
6. Temporary workarounds should be marked clearly.
7. Client confidential data must not be included in code examples.

## Naming

Use meaningful names for procedures, functions, variables, and modules.

Bad:

```bsl
Процедура Выполнить()
    // ...
КонецПроцедуры

Good:
Процедура ps_ОбновитьСтатусыЗаказовКлиентов() Экспорт
    // Copyright (c) ТОО "PSGroup"
    // Обновляет статусы заказов клиентов по данным внешней системы.
КонецПроцедуры

## Server and client code separation

Avoid mixing user interface logic with server-side business logic.

Recommended approach:

- Client procedures should handle user actions.
- Server procedures should process data.
- Common modules should contain reusable business logic.

## Queries

Recommendations:

- Use clear aliases.
- Avoid unnecessary fields.
- Filter data as early as possible.
- Avoid selecting large datasets without conditions.
- Use temporary tables for complex calculations where appropriate.
- Comment non-obvious query logic.

## Error handling

Use clear error handling and meaningful messages.

Bad:
Попытка
    ВыполнитьОбмен();
Исключение
КонецПопытки;
Good:
Попытка
    ВыполнитьОбмен();
Исключение
    ТекстОшибки = ОписаниеОшибки();
    ЗаписьЖурналаРегистрации(
        "ps_CodeQualityTools.Exchange",
        УровеньЖурналаРегистрации.Ошибка,
        ,
        ,
        "Ошибка выполнения обмена: " + ТекстОшибки
    );
КонецПопытки;


## 7. `tools/code-review-prompts/1c-code-review.md`

```markdown
# 1C Code Review Prompt

You are a senior 1C:Enterprise developer and code reviewer.

Review the following 1C code according to these criteria:

1. Correctness
2. Readability
3. Maintainability
4. Performance
5. Query optimization
6. Server/client code separation
7. Transaction safety
8. Error handling
9. Naming conventions
10. Security and access rights
11. Compatibility with typical 1C configurations

Return the result in this structure:

## Summary

Briefly describe the overall code quality.

## Critical Issues

List serious problems that must be fixed before release.

## Maintainability Issues

List issues that make the code harder to support.

## Performance Issues

List possible performance bottlenecks.

## Security / Access Rights Issues

List potential security risks.

## Recommendations

Suggest practical improvements.

## Refactored Example

Provide an improved version of the code if possible.
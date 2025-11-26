# Branching Report

## Merge Statistics
- Total number of merges: 5
- Fast-forward merges: 2
- 3-way merges: 3
- Merges with conflicts: 2

## Branch History
* dc61705 (HEAD -> main, origin/main, origin/HEAD) add BRANCHING_REPORT.md
*   b449ae7 Merge branch 'documentation'
|\
| * a48a956 (documentation) add documentation
|/
*   f797787 Merge feature/header-update with conflict resolution
|\
| * 8c8d3a1 Update header to v2.0
* | 4b4c01f Customize blog title
|/
*   25ba27d Merge branch 'feature/design'
|\
| * 88b36cb Improve design and add navigation
* | 68f5055 Add comments section
|/
* 1680f8c Add posts page and functionality
* 289b431 Initial project setup


## Lessons Learned
1. если создали новую ветку и несколько коммитов в ней, а на мейн ветке ничего не делали тогда вариант слияния будет:
- fast-forward обычный, то есть созданная ветка полностью переходит в мейн линейно со всеми коммитами, в истории нет ответвлений
- --no-ff создаётся дополнительный коммит слияния и в истории появляется ответвление
2. При слиянии 2х веток где в каждой есть коммиты, происходит слияние 3way.
- При таком варианте возможны конфликты если есть расхождения в файлах или их колличестве.
- При конфликте 3xway merge создаётся некий временный слой Merging где можно менять файлы как нужно чтобы предотвратить конфликт.
- Так же можно замержить сразу с политикой разрешения конфликта --theirs --ours
- И если что то пошло не так можно откатить фазу merging, git merge --abort

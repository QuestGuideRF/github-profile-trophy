# Введение

<p align="center"><img src="logo.png"><p>

> Знаете ли вы версию [Github Profile Trophy](https://github.com/maurodesouza/profile-readme-generator)

Итак, эта версия позволит вам показывать все секретные трофеи вместо их скрытия. [Системы рангов](#системы-рангов)

Она также снижает их сложность, чтобы вы могли легко настроить более красивый профиль! [Журнал изменений](#журнал-изменений)

Более того, в этом файле добавлены некоторые модификации и улучшения! [Журнал изменений](#журнал-изменений)

## Быстрый старт

```
![](https://github-profile-trophy.screw-hand.vercel.app/?username=вашеимяпользователя)
```

[![](https://github-profile-trophy.screw-hand.vercel.app/?username=lucthienphong1120)](https://github-profile-trophy.screw-hand.vercel.app/?username=lucthienphong1120)

О полном использовании вы можете узнать в [Как использовать](/USAGE.md).

## Рекомендуемое использование

Использование параметра строки запроса `want[XX]` позволяет вам получить указанный секретный трофей безусловно.

```
https://github-profile-trophy.screw-hand.vercel.app/?username=screw-hand&rank=SECRET&wantMultipleOrganizations=true
```

Полный список `want[xx]`:
```ts
wantAchieveSuperRank=true
wantMultipleLang=true
wantLongTimeAccount=true
wantAncientAccount=true
wantNewAccount=true
wantMultipleOrganizations=true
```

Особенно, использование wantALL позволяет вам использовать один параметр и получить все секретные трофеи.

```
https://github-profile-trophy.screw-hand.vercel.app/?username=screw-hand&rank=SECRET&wantAll=true
```

Фильтрация трофеев указанного уровня (UNKNOWN, C)

```
https://github-profile-trophy.screw-hand.vercel.app/?username=screw-hand&rank=-UNKNOWN,-C
```

## Системы рангов

Базовые трофеи требуют

| Название трофея | C | B | A | AA | AAA | S | SS | SSS | Сложность |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TotalStarTrophy | 1 | 10 | 20 | 50 | 100 | 250 | 500 | 1200 | Нормальная |
| TotalCommitTrophy | 1 | 10 | 100 | 200 | 500 | 700 | 1000 | 2000 | Нормальная |
| TotalFollowerTrophy | 1 | 10 | 20 | 50 | 100 | 200 | 500 | 1000 | Очень сложная |
| TotalIssueTrophy | 1 | 5 | 10 | 20 | 50 | 100 | 200 | 500 | Сложная |
| TotalPullRequestTrophy | 1 | 5 | 10 | 20 | 50 | 100 | 200 | 500 | Сложная |
| TotalRepositoryTrophy | 1 | 10 | 20 | 30 | 40 | 50 | 70 | 100 | Легкая |

Секретные трофеи требуют

| Название трофея | Требуется для активации |
| --- | --- |
| MultipleLangTrophy | минимум 5 языков |
| AchieveSuperRankTrophy | иметь ранг SSS |
| NewAccountTrophy | зарегистрирован после 2020 |
| AncientAccountTrophy | зарегистрирован до 2010 |
| LongTimeAccountTrophy | более 3 лет |
| MultipleOrganizationsTrophy | присоединился к 3 организациям |

## Самостоятельная модификация

Вам придется развернуть самостоятельно, для [Vercel](/VercelDeployGuide.md) или [localhost](/LocalDeployGuide.md)

## Журнал изменений

- Фильтрация по рангам поддерживает UNKNOWN
- `want[XX]` и `wantAll` строки запроса для получения секретного трофея
- показывать все трофеи включая секретные и недостигнутые (условия остаются теми же)
- обновление трофея "AchieveSuperRankTrophy" вместо "AllSuperRankTrophy"
- условие "AchieveSuperRankTrophy" с `every` на `at least one`
- обновление трофея "NewAccountTrophy" вместо "NewAccountTrophy"
- условие "NewAccountTrophy" с `==2020` на `>=2020`
- система единиц "LongTimeAccountTrophy" с `pt` на `year(s)`
- условие "LongTimeAccountTrophy" с `10years` на `3years`
- Открытие трофеев "wantAllSuperRank" и "wantMultipleLang" по умолчанию (условия равны 0)
- условия "MultipleOrganizations" с `3` на `1` (открыто по умолчанию)
- изменение расстояния между условиями и снижение сложности "TotalStarTrophy"
  - Ранг A с `30` на `25`
  - Ранг S с `200` на `250`
  - Ранг SS с `700` на `500`
  - Ранг SSS с `2000` на `1200`
- изменение расстояния между условиями и снижение сложности "TotalCommitTrophy"
  - Ранг S с `1000` на `700`
  - Ранг SS с `2000` на `1000`
  - Ранг SSS с `4000` на `2000`
- изменение условия "TotalFollowerTrophy"
  - Ранг SS с `400` на `500`
- изменение расстояния между условиями и снижение сложности "TotalIssueTrophy"
  - Ранг B с `10` на `5`
  - Ранг A с `20` на `10`
  - Ранг AA с `50` на `20`
  - Ранг AAA с `100` на `50`
  - Ранг S с `200` на `100`
  - Ранг SS с `500` на `200`
  - Ранг SSS с `1000` на `500`
- изменение расстояния между условиями и снижение сложности "TotalPullRequestTrophy"
  - Ранг B с `10` на `5`
  - Ранг A с `20` на `10`
  - Ранг AA с `50` на `20`
  - Ранг AAA с `100` на `50`
  - Ранг S с `200` на `100`
  - Ранг SS с `500` на `200`
  - Ранг SSS с `1000` на `500`
- изменение расстояния между условиями и снижение сложности "TotalRepositoryTrophy"
  - Ранг AAA с `50` на `40`
  - Ранг S с `80` на `50`
  - Ранг SS с `90` на `70`

Если вы решите использовать мое развертывание, было бы очень приятно, если бы вы поставили мне звездочку :star:

Подпись относится к текущей версии проекта.

---

Автор: legenda  
Telegram: [@LEGENDA_SD](https://t.me/LEGENDA_SD)

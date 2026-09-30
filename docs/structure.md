# Структура проекта

## Сцены

- `PlatformerDemo` — демонстрационный вариант платформера.
- `SampleScene` — пустая сцена, создающаяся по умолчанию.

## Объекты основной сцены

- `Main Camera`
- `Managers`
- `Lights`
  1. `Directional light`
- `CharacterPlatformer` *(Prefab)*
  1. `Hand`
- `Scene`
  1. `TilemapGrid` → `Tilemap`
  2. `TreeBackground` *(Prefab)* → `Tree1`, `Tree2`, `Tree3`
  3. `Grass` → `Grass`, `Grass (1)`, …, `Grass (10)`

# Player

Игровой персонаж называется `CharacterPlatformer` и имеет дочерний объект `Hand`.

## Компоненты

### `CharacterPlatformer`

- `Transform`
- `SpriteRenderer`
- `Animator`
- `Rigidbody 2D`
- `CapsuleCollider`
- `PlayerCharacter` *(Script)*
- `CharacterAnim` *(Script)*
- `CharacterHoldItem` *(Script)*

### `Hand`

- `Transform`

## Параметры компонентов

### Transform

1. Позиция (`Position`)
2. Поворот (`Rotation`)
3. Размер (`Scale`)

### SpriteRenderer

1. Спрайт (`Sprite`)
2. Цвет (`Color`)
3. Отражение по X или Y (`Flip`)
4. Способ отрисовки спрайта (`Draw Mode`)
5. Взаимодействие со `Sprite Mask` (`Mask Interaction`)
6. Тип сортировки относительно других спрайтов (`Sprite Sort Point`)
7. Материал для отрисовки спрайта (`Material`)
8. Крупный слой отрисовки (`Sorting Layer`)
9. Порядок внутри одного `Sorting Layer` (`Order in Layer`)

### Animator

1. Выбор `Animator Controller` (`Controller`)
2. Соответствие костей (`Avatar`)
3. Будет ли анимация передвигать объект (`Apply Root Motion`)
4. Тип обновления анимации (`Update Mode`)
5. Обновление анимации, если объект не виден (`Culling Mode`)

### Rigidbody 2D

1. Тип взаимодействия с физикой (`Body Type`)
2. Физический материал (`Material`)
3. Взаимодействие с физикой (`Simulated`)
4. Автоматическое определение массы (`Use Auto Mass`)
5. Масса объекта (`Mass`)
6. Сопротивление линейному движению (`Linear Drag`)
7. Сопротивление вращению (`Angular Drag`)
8. Множитель гравитации (`Gravity Scale`)
9. Способ обнаружения столкновений (`Collision Detection`)
10. Просчёт физики при отсутствии движения (`Sleeping Mode`)
11. Сглаживание движения (`Interpolate`)
12. Запретить движение по оси (`Freeze Position`)
13. Запретить вращение по оси (`Freeze Rotation`)

### CapsuleCollider 2D

1. Изменить границы коллайдера (`Edit Collider`)
2. Физический материал (`Material`)
3. Возможность столкновения с другими коллайдерами (`Is Trigger`)
4. Возможность работать с `Effector`-компонентами (`Used By Effector`)
5. Смещение коллайдера относительно `GameObject` (`Offset`)
6. Размер (`Size`)
7. Направление коллайдера (`Direction`)

### Player Character (Script)

1. `Player_id`
2. `Max_hp`
3. `Invulnerable`
4. `Move_accel`
5. `Move_deccel`
6. `Move_max`
7. `Can_jump`
8. `Double_jump`
9. `Jump_strength`
10. `Jump_time_min`
11. `Jump_time_max`
12. `Jump_gravity`
13. `Jump_fall_gravity`
14. `Jump_move_percent`
15. `Ground_layer`
16. `Ground_raycast_dist`
17. `Can_crouch`
18. `Crouch_coll_percent`
19. `Reset_when_fall`
20. `Fall_pos_y`
21. `Fall_damage_percent`

### Character Anim (Script)

Параметров нет.

### Character Hold Item (Script)

1. `Hand`

# Скрипты

| Скрипт | Назначение |
|---|---|
| `CarryItem` | Скрипт для предмета, который можно подобрать |
| `CharacterAnim` | Смена анимации персонажа |
| `CharacterHoldItem` | Взаимодействие персонажа с объектом, который можно подобрать |
| `FollowCamera` | Перемещение камеры за игроком |
| `Lever` | Логика работы рычага |
| `ParallaxBackground` | Движение фона при смещении камеры |
| `PlayerCharacter` | Скрипт управления персонажем |
| `PlayerControls` | Считывание нажатия клавиш |
| `TheAudio` | Управление аудиофайлами |
| `ImportPackage` | Первоначальная настройка импортированного пакета |

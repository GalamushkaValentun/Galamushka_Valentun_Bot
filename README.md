# Galamushka_Valentun_Bot

game_title = "My game"
game_version = "1.0"
levels = {
    1: "Рівень 1",
    2: "Рівень 2",
    3: "Рівень 3",
}

print(game_title)
print(game_version)

print("Виберіть рівень:")
for key, value in levels.items():
    print(f'{key} - {value}')

while True:
    try:
        level_choice = int(input())

        if level_choice in levels:
            print(f'Ви вибрали рівень: {level_choice}')
            break
        else:
            raise Exception()
    except:
        print("Неправильний рівень")

from level_select import show_levels_select


def intro():
    """Function asks for user name to play game."""

    print("Введіть ім'я:")
    name = input()
    print(f"Привіт: {name}")


def show_game_info(title, version):
    """Shows game info to the user"""
    print(f"{title} v{version}")


game_title = "My game"
game_version = 1.0

# Show game info
show_game_info(game_title, game_version)

# Show user intro
intro()

# Ask user to select game level
level = show_levels_select()
print(f'Ви вибрали рівень: {level}')

level_select.py

levels = {
    1: "Рівень 1",
    2: "Рівень 2",
    3: "Рівень 3",
}


def show_levels_select():
    print("Виберіть рівень:")
    for key, value in levels.items():
        print(f'{key} - {value}')

    while True:
        try:
            level_choice = int(input())

            if level_choice in levels:
                return level_choice
            else:
                raise Exception()
        except:
            print("Неп9равильний рівень")

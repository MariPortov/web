# web

 with open('private_keys.txt', 'r', encoding='utf-8-sig') as file:
        private_keys_list: list[str] = [f'0x{row.strip()}' if not row.strip().startswith('0x') else row.strip() for row
                                        in file]

    cycled_proxies_list = itertools.cycle(proxies_list) if proxies_list else None

    logger.info(f'Загружено {len(accounts_list)} аккаунтов / {len(proxies_list)} '
                f'прокси / {len(private_keys_list)} приват-кеев')

    user_action: int = int(input('\n1. Запуск накрутки MEMELand\n'
                                 '2. Подписка между аккаунтами Twitter\n'
                                 '3. Say GM\n'
                                 'Введите ваше действие: '))

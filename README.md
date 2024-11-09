import telebot
    
# Инициализация бота с использованием его токенаhttps://github.com/MAKSIMRESIK228/M1M1cvcv/tree/main
bot = telebot.TeleBot("7884832305:AAGIXnsiWVKBXEDMNZtmR9De0B-uBFvhqH8")
    
# Обработчик команды '/start' и '/hello'
@bot.message_handler(commands=['start', 'hello'])
def send_welcome(message):
    bot.reply_to(message, f'Привет! Я бот {bot.get_me().first_name}!')
    
# Обработчик команды '/heh'
@bot.message_handler(commands=['heh'])
def send_heh(message):
    count_heh = int(message.text.split()[1]) if len(message.text.split()) > 1 else 5
    bot.reply_to(message, "he" * count_heh)
    аааа
# Запуск бота
bot.polling()

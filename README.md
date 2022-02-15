# -
Бот, который копирует твои ответы

import telebot

bot = telebot.TeleBot("5252413153:AAHsp--_cubchoL8I5rcgA5P9tewryicEdA")

@bot.message_handler(commands=['start', 'help'])
def send_welcome(message):
    bot.reply_to(message, "Howdy, how are you doing?")

@bot.message_handler(func=lambda m: True)
def echo_all(message):
    bot.reply_to(message, message.text)

bot.polling()

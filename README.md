import time
from datetime import datetime

# Imposta la data di destinazione (20 dicembre 2024)
target_date = datetime(2024, 12, 20)

# Funzione per il countdown
def countdown_timer(target_date):
    while True:
        current_date = datetime.now()
        time_remaining = target_date - current_date
        days = time_remaining.days
        hours, remainder = divmod(time_remaining.seconds, 3600)
        minutes, seconds = divmod(remainder, 60)

        # Visualizza il countdown
        print(f"Tempo rimanente: {days} giorni, {hours} ore, {minutes} minuti, {seconds} secondi", end="\r")
        time.sleep(1)

# Avvia il countdown
countdown_timer(target_date)

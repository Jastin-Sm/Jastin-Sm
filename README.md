import sys
from time import sleep

def print_lyric():
    lyrics = [
        ("Do you think I have forgotten?", 0.11),
        ("Do you think I have forgotten?", 0.11),
        ("Do you think I have forgotten", 0.18),
        ("About you..", 0.3),
        ("There was something 'bout you that now I can't remember", 0.1),
        ("It's the same damn thing that made my heart surrender", 0.1),
        ("And I miss you on a train, I miss you in the morning", 0.1),
        ("I never know what to think about", 0.12),
        ("I think about you....", 0.14),
    ]
    
    # Delay between lines
    line_delays = [1.2, 1.2, 1.2, 0.5, 3.4, 0.5, 0.5, 0.5, 0.5]
    
    for i, (line, char_delay) in enumerate(lyrics):
        for char in line:
            print(char, end='')
            sys.stdout.flush()
            sleep(char_delay)
        print()  # New line after each lyric line
        sleep(line_delays[i])

print_lyric()

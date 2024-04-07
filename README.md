# unixx
#!/bin/bash

function guessing_game {
    local files=$(ls -1 | wc -l)
    local guess=-1

    echo "Welcome to the guessing game!"

    while [[ $guess -ne $files ]]; do
        read -p "How many files are in the current directory? " guess

        if [[ $guess -lt $files ]]; then
            echo "Too low! Try again."
        elif [[ $guess -gt $files ]]; then
            echo "Too high! Try again."
        else
            echo "Congratulations! You guessed correctly!"
        fi
    done
    } 
    README.md:
    echo "# Guessing Game" > README.md
    echo "" >> README.md
    echo "Date and time when make was executed: $$(date)" >> README.md
    echo "" >> README.md
    echo "Number of lines of code in guessinggame.sh: $$(wc -l < guessinggame.sh)" >> README.md

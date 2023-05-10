- 👋 Hi, I’m @only6t
- 👀 I’m interested in hentai
- 🌱 I’m currently learning hentai
- 💞️ I’m looking to collaborate on hentai

<!---
only6t/only6t is a ✨ special ✨ repository be link to



#!/bin/bash

# Definizione del menu
menu() {
    echo "Menu:"
    echo "1. Genera un file"
    echo "2. Elimina un file"
    echo "3. Modifica i permessi di un file"
    echo "4. Esci"
}

# Funzione per la generazione di un file
generate_file() {
    echo "Inserisci il nome del file da generare:"
    read filename
    if [ -f "$filename" ]; then
        echo "Il file $filename esiste già."
    else
        touch "$filename"
        echo "Il file $filename è stato generato."
    fi
}

# Funzione per l'eliminazione di un file
delete_file() {
    echo "Inserisci il nome del file da eliminare:"
    read filename
    if [ -f "$filename" ]; then
        rm "$filename"
        echo "Il file $filename è stato eliminato."
    else
        echo "Il file $filename non esiste."
    fi
}

# Funzione per la modifica dei permessi di un file
change_permissions() {
    echo "Inserisci il nome del file di cui modificare i permessi:"
    read filename
    if [ -f "$filename" ]; then
        echo "Inserisci i nuovi permessi per il file $filename:"
        read permissions
        chmod "$permissions" "$filename"
        echo "I permessi del file $filename sono stati modificati."
    else
        echo "Il file $filename non esiste."
    fi
}

# Ciclo principale del programma
while true; do
    menu
    read choice
    case $choice in
        1) generate_file;;
        2) delete_file;;
        3) change_permissions;;
        4) exit;;
        *) echo "Scelta non valida";;
    esac
done

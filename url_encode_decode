#!/bin/bash

# URL encode function
url_encode() {
    local encoded=""
    local length="${#1}"
    for (( i = 0; i < length; i++ )); do
        local c="${1:i:1}"
        case $c in
            [a-zA-Z0-9.~_-]) 
                encoded+="$c" 
                ;;
            *)
                encoded+=$(printf '%%%02X' "'$c")
                ;;
        esac
    done
    echo "$encoded"
}

# URL decode function
url_decode() {
    local decoded="${1//+/ }"
    printf '%b' "${decoded//%/\\x}"
}

# pase arguments
while getopts "e:d:" opt; do
    case $opt in
        e)
            url_encode "$OPTARG"
            ;;
        d)
            url_decode "$OPTARG"
            ;;
        *)
            echo "usage: $0 -e string 或 $0 -d string"
            ;;
    esac
done

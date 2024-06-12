create() {
    echo "Enter the file name to be created"
    read fname
    if [ -e "$fname" ]; then
        echo "File is present :: Enter another name"
    else
        echo "File is not present"
        touch "$fname"
        echo "File is created"
    fi
}

display() {
    echo "Enter the file name to be displayed"
    read fname
    if [ -e "$fname" ]; then
        echo "File is present"
        cat "$fname"
    else
        echo "Error :: File is not present"
    fi
}

insert() {
    echo "Enter the file name to be inserted into"
    read fname
    if [ -e "$fname" ]; then
        echo "File is present"
        echo "Enter roll number"
        read rollno
        if grep -q -w "$rollno" "$fname"; then
            echo "Roll number is present"
        else
            echo "Roll number is not present"
            echo "Enter name"
            read name
            record="$rollno $name"
            echo "$record" >> "$fname"
            echo "Record is successfully inserted"
        fi
    else
        echo "Error :: File is not present"
    fi
}

modify() {
    echo "Enter the file name for modification"
    read fname
    if [ -e "$fname" ]; then
        echo "File is present"
        echo "Enter roll number to be modified"
        read rollno
        if grep -q -w "$rollno" "$fname"; then
            echo "Roll number is present"
            old=$(grep -w "$rollno" "$fname")
            echo "Old record = $old"
            echo "Enter new name"
            read newname
            new="$rollno $newname"
            echo "New record = $new"
            sed -i "s/^$old\$/$new/" "$fname"
            echo "Record is modified"
        else
            echo "Roll number is not present"
        fi
    else
        echo "Error :: File is not present"
    fi
}

delete() {
    echo "Enter the file name to delete from"
    read fname
    if [ -e "$fname" ]; then
        echo "File is present"
        echo "Enter roll number to be deleted"
        read rollno
        if grep -q -w "$rollno" "$fname"; then
            echo "Roll number is present"
            old=$(grep -w "$rollno" "$fname")
            echo "Deleted record = $old"
            sed -i "/^$old\$/d" "$fname"
            echo "Record is deleted"
        else
            echo "Roll number is not present"
        fi
    else
        echo "Error :: File is not present"
    fi
}

search() {
    echo "Enter the file name to search from"
    read fname
    if [ -e "$fname" ]; then
        echo "File is present"
        echo "Enter roll number to be searched"
        read rollno
        if grep -q -w "$rollno" "$fname"; then
            echo "Search result:"
            grep -w "$rollno" "$fname"
        else
            echo "Roll number is not present"
        fi
    else
        echo "Error :: File is not present"
    fi
}

while true; do
    echo "MENU"
    echo "1) Create address book"
    echo "2) Display address book"
    echo "3) Insert a record"
    echo "4) Modify a record"
    echo "5) Delete a record"
    echo "6) Search a record"
    echo "9) Exit"
    echo "Enter your choice"
    read choice
    clear
    
    case $choice in
        1) create ;;
        2) display ;;
        3) insert ;;
        4) modify ;;
        5) delete ;;
        6) search ;;
        9) exit ;;
        *) echo "Wrong choice entered" ;;
    esac

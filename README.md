# Theme2.3
MOV AX, 7 ; загружаем количество очков команды за игру

CMP AX, 3 ; сравниваем количество очков с количеством очков за выигрыш
JE won ; если количество очков равно 3, то команда одержала победу

CMP AX, 1 ; сравниваем количество очков с количеством очков за ничью
JE draw ; если количество очков равно 1, то команда сыграла в ничью

JMP lost ; если ни одно из условий не выполнилось, то команда проиграла

won:
; Вывод на экран сообщения: "Команда выиграла игру"
JMP end

draw:
; Вывод на экран сообщения: "Команда сыграла в ничью"
JMP end

lost:
; Вывод на экран сообщения: "Команда проиграла игру"
JMP end

end:

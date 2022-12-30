alph = ["A", "B", "C"]
lst= ['A0', 'A1', 'A2', 'A3', 'A4', 'A5', 'A6', 'A7', 'A8', 'B0', 'B1', 'B2', 'B3', 'B4', 'B5', 'B6', 'B7', 'B8', 'C0', 'C1', 'C2', 'C3', 'C4', 'C5', 'C6', 'C7', 'C8']
brd = {'A0': 0, 'A1': 1, 'A2': 2, 'A3': 3, 'A4': 4, 'A5': 5, 'A6': 6, 'A7': 7, 'A8': 8, 'B0': 0, 'B1': 1, 'B2': 2, 'B3': 3, 'B4': 4, 'B5': 5, 'B6': 6, 'B7': 7, 'B8': 8, 'C0': 0, 'C1': 1, 'C2': 2, 'C3': 3, 'C4': 4, 'C5': 5, 'C6': 6, 'C7': 7, 'C8': 8}
if alph[0] == 'A' and len(alph) > 1:
    print('A', end='      ')
if len(alph) == 1 and alph[0] == 'A':
    print('A', end='')
    print()
if len(alph) == 3 and alph[1] == 'B':
    print('B', end='      ')
if len(alph) == 2 and alph[0] == 'B':
    print('B', end='      ')
if len(alph) == 2 and alph[1] == 'B':
    print('B', end='')
    print()
if len(alph) == 1 and alph[0] == 'B':
    print('B', end='')
    print()
if len(alph) == 3 and alph[2] == 'C':
    print('C')
if len(alph) == 2 and alph[1] == 'C':
    print('C')
if len(alph) == 1 and alph[0] == 'C':
    print('C')
for x in range(0, 9, 3):
    t=1
    for i in range(3):
        gap = 1
        for j in range(x, x + 3):
            if gap < 3:
                print(brd[(alph[i] + str(j))], end=" ")
                gap += 1
            else:
                if t < len(alph):
                    print(brd[(alph[i] + str(j))], end='  ')
                    t += 1
                else:
                    print(brd[(alph[i] + str(j))], end='')
    print()


def deletable():
    for i in alph:
        if ((brd[i + str(0)] == 'X') and (brd[i + str(4)] == 'X') and (brd[i + str(8)] == 'X')) or ((brd[i + str(2)] == 'X') and (brd[i + str(4)] == 'X') and (brd[i + str(6)] == 'X')):
            if i in alph:
                alph.remove(i)
                return True
            else:
                continue
        for j in range(0, 9, 3):
            row_1 = 0
            for p in range(j, j + 3):
                if (brd[i + str(p)] == 'X'):
                    row_1 += 1
                    if row_1 == 3:
                        if i in alph:
                            alph.remove(i)
                            return True
                        else:
                            continue
        for j in range(0, 3):
            column_1 = 0
            for p in range(j, j + 7, 3):
                if (brd[i + str(p)] == 'X'):
                    column_1 += 1
                    if column_1 == 3:
                        if i in alph:
                            alph.remove(i)
                            return True
                        else:
                            continue

game= False
while game== False:
    if game ==True:
        break
    test= True
    while test== True:
        player1= input("Player 1: ")
        if (player1 in lst) and (brd[player1] != 'X') and (player1[:1] in alph):
            brd[player1]= "X"
            if len(alph) == 1 and deletable() == True:
                print('Player 2 wins game')
                game = True
                check = False
                break
            else:
                deletable()
                if alph[0] == 'A' and len(alph) > 1:
                    print('A', end='      ')
                if len(alph) == 1 and alph[0] == 'A':
                    print('A', end='')
                    print()
                if len(alph) == 3 and alph[1] == 'B':
                    print('B', end='      ')
                if len(alph) == 2 and alph[0] == 'B':
                    print('B', end='      ')
                if len(alph) == 2 and alph[1] == 'B':
                    print('B', end='')
                    print()
                if len(alph) == 1 and alph[0] == 'B':
                    print('B', end='')
                    print()
                if len(alph) == 3 and alph[2] == 'C':
                    print('C')
                if len(alph) == 2 and alph[1] == 'C':
                    print('C')
                if len(alph) == 1 and alph[0] == 'C':
                    print('C')

                for x in range(0, 9, 3):
                    t=1
                    for i in range(len(alph)):
                        gap = 1
                        for j in range(x, x + 3):
                            if gap < 3:
                                print(brd[(alph[i] + str(j))], end=" ")
                                gap += 1
                            else:
                                if t < len(alph):
                                    print(brd[(alph[i] + str(j))], end='  ')
                                    t += 1
                                else:
                                    print(brd[(alph[i] + str(j))], end='')
                    print()
                test = False
        else:
            print('Invalid move, please input again')

    if game== True:
        break
    test= True
    while test == True:
        player2= input("Player 2: ")
        if (player2 in lst) and (brd[player2] != 'X') and (player2[:1] in alph):
            brd[player2] = 'X'
            if len(alph) == 1 and deletable() == True:
                print('Player 1 wins game')
                game = True
                test = False
                break
            else:
                deletable()
                if alph[0] == 'A' and len(alph) > 1:
                    print('A', end='      ')
                if len(alph) == 1 and alph[0] == 'A':
                    print('A', end='')
                    print()
                if len(alph) == 3 and alph[1] == 'B':
                    print('B', end='      ')
                if len(alph) == 2 and alph[0] == 'B':
                    print('B', end='      ')
                if len(alph) == 2 and alph[1] == 'B':
                    print('B', end='')
                    print()
                if len(alph) == 1 and alph[0] == 'B':
                    print('B', end='')
                    print()
                if len(alph) == 3 and alph[2] == 'C':
                    print('C')
                if len(alph) == 2 and alph[1] == 'C':
                    print('C')
                if len(alph) == 1 and alph[0] == 'C':
                    print('C')

                for x in range(0, 9, 3):
                    t = 1
                    for i in range(len(alph)):
                        gap = 1
                        for j in range(x, x + 3):
                            if gap < 3:
                                print(brd[(alph[i] + str(j))], end=" ")
                                gap += 1
                            else:
                                if t < len(alph):
                                    print(brd[(alph[i] + str(j))], end='  ')
                                    t += 1
                                else:
                                    print(brd[(alph[i] + str(j))], end='')

                    print()
                test = False
        else:
            print('Invalid move, please input again')

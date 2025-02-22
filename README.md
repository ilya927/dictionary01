# dictionary01
correct = 0
wrong = 0

eword = []
gword = []

f = open('words.txt', 'r')
f1 = open('history.txt', 'a')
for line in f:
    line = line.replace('-', '\n').split()
    word1 = str(line[0])
    word2 = str(line[1])
    eword.append(word1)
    gword.append(word2)

name = input('your name - ')
while True:
    output = 'Not Found'
    a = str(input('word - '))
    low = a.lower()
    if a == 'stop':
        break
    if low in eword:
        i = eword.index(low)
        output = gword[i]
    f1.write(f'{a}\n')
    print(output)

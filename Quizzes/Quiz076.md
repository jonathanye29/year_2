# Quiz 076
<img width="991" alt="Screen Shot 2023-09-12 at 11 23 04 PM" src="https://github.com/jonathanye29/year_2/assets/111751273/4e773614-8f35-4186-b922-f61afffde5b2">

## Code
```.py
class ErrorChecker():
    def __init__(self, input:str):
        self.input = input

    def error_check(self):
        out = False
        correct = ""
        for i in range(len(self.input)//3):
            length = int(len(self.input)//3)
            if self.input[i] == self.input[i+length] == self.input[i+2*length]:
                correct += self.input[i]
                pass
            else:
                out = True
                if self.input[i] == self.input[i+length] or self.input[i] == self.input[i+2*length]:
                    correct += self.input[i]
                elif self.input[i+length] == self.input[i+2*length]:
                    correct += input[i+length]
        return out, correct

    def error_check_v2(self):
        length = len(self.input) // 3
        correct = []

        for i in range(length):
            a = int(self.input[i])
            b = int(self.input[i + length])
            c = int(self.input[i + 2 * length])

            correct.append('1' if sum([a, b, c]) > 1 else '0')

        return ''.join(correct)

data = "011101111101110111110111001111"
boi = ErrorChecker(data)
print(boi.error_check())
```

<img width="1043" alt="Screen Shot 2023-09-12 at 11 26 47 PM" src="https://github.com/jonathanye29/year_2/assets/111751273/3affd6ad-06f9-474a-8c56-357a1bbe247d">


## Paper Code
![IMG_1211](https://github.com/jonathanye29/year_2/assets/111751273/b8044d11-d35f-4761-9716-0409302cba12)

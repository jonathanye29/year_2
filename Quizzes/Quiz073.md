# Quiz 073
<img width="994" alt="Screen Shot 2023-09-12 at 11 00 10 PM" src="https://github.com/jonathanye29/year_2/assets/111751273/8512c909-5db6-4b2a-8a39-a2cfec2b3fd5">

## Code
```.py
class RoutingTable():
    def __init__(self):
        self.routing_table = {}

    def check_mac(self, MAC:str)->bool:
        return len(MAC) == 17 and MAC.count(":") == 5

    def ipv4machine(self, N:int)->str:
        import random
        output = set()
        while len(output) < N:
            temp = ""
            for i in range(4):
                temp += str(random.randint(0, 255))
                if i != 3:
                    temp += "."
            output.add(temp)
        return output.pop()

    def get_ip(self, MAC:str)->str:
        ip_out = "Error"
        if self.check_mac(MAC):
            if MAC in self.routing_table.keys():
                ip_out = self.routing_table[MAC]
            else:
                while True:
                    ip = self.ipv4machine(N=1)
                    if not ip in self.routing_table.values():
                        self.routing_table[MAC] = ip
                        ip_out = ip
                        break
            return ip_out
```
<img width="1017" alt="Screen Shot 2023-09-12 at 10 59 28 PM" src="https://github.com/jonathanye29/year_2/assets/111751273/419b6bf9-96b1-4338-b4b8-8ef5ac4df8fa">

## Paper Code

![IMG_1204](https://github.com/jonathanye29/year_2/assets/111751273/e8e8c0ef-2173-452e-9217-84998a05151d)

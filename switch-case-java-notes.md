```
shared scope:

switch (x) {
    case 1:
        int a = 10;
        break;
    case 2:
        int a = 20;   // duplicate variable, fails
        break;
}

isolate scope using {...}

fall through : all after first match get executed (until break seen)

switch(x) : x can be : byte, short, int, char, enum, String(since java 7)
x cannot be : long, float, double, boolean

case A: A must be compile time constant (final)


int result = switch (x) {
    case 1 -> 10;
    default -> 0;
};
(java 14+)


int result = switch (x) {
    case 1 -> {
        int temp = 5;
        yield temp * 2;
    }
    default -> 0;
};
```



# assignment2-kolla
# Anil Kolla
### My favorite place in the world is New Zealand<br>
**New Zealand** One of the **most unpolluted countries in the world** where spectacularscenary bounds. 90% of immigrants state that they would certaily **recommend the land of kiwis to their families and friends.** <br>New Zealanders get generous leave benifits so they have plenty of time to enjoy the landscape and sports facilities.


## Maryville to New Zealand
1. Maryville to Kansas International Airport(MCI)
    1. Travel by Car
2. MCI to AKL(Auckland, New Zealand)
    1. Direct Flight
    2. Connecting Flight (Maryville to Los Angeles and Los Angeles to Auckland)
## List of items that should be brought to your favorite place for maximum enjoyment
* Jacket
* Shoes
* Sun Glasses
* Cap

[Click here to see About Me](./AboutMe.md)

**
## Food And Drinks
The below are the list of Food/drinks I would recommed to try !!
| Item | Location | Cost |
|------|----------|------|
| Choclate Almond Jar | Cream Stone | $10 |
| Cheeza | KFC | $12 |
| Tacos | Tacobell | $3.45 |
| Mushroom Spice Pizza | AppleBees | $14 |

**
## Pithy Quotes
> "Simplicity is the ultimate Sophistication"  - Lenardo da vinci

> "Be Stubborn" - Anil Kolla

**
## Quick information about Dynamic Programming
>Dynamic programming is both a mathematical optimization method and a computer programming method. The method was developed by Richard Bellman in the 1950s and has found applications in numerous fields, from aerospace engineering to economics.

[Quick-link for the source](https://en.wikipedia.org/wiki/Dynamic_programming)


bool next_balanced_sequence(string & s) {
    int n = s.size();
    int depth = 0;
    for (int i = n - 1; i >= 0; i--) {
        if (s[i] == '(')
            depth--;
        else
            depth++;

        if (s[i] == '(' && depth > 0) {
            depth--;
            int open = (n - i - 1 - depth) / 2;
            int close = n - i - 1 - open;
            string next = s.substr(0, i) + ')' + string(open, '(') + string(close, ')');
            s.swap(next);
            return true;
        }
    }
    return false;
}

[Quick-link for the source code](https://cp-algorithms.com/combinatorics/bracket_sequences.html)
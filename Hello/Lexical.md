# LEXICAl
- Lexical scope means a function can use the variaable that are created in the function and outside of i(its parent function).
- Inner function access parent function or global variable but outer function not access ineer function variable.

```javascript
function subtract(){
    const x=3;
    const y=6;
    console.log(x-y);

    function child(){
        const name = "ankit";
        console.log(name);
        console.log(x);
        function Mchild(){
            const Sname = "bolo";
            console.log(Sname);
            console.log(name);
            console.log(x);
        }
        Mchild()
    }
    {
        const num1 = 56;
    }
    child()
}
subtract ()
```

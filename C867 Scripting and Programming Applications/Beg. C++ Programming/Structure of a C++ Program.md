### #include Preprocessor Directive

Programs that process your source code before you compile it 
Looks for preprocessor commands 
Directives begin with `#`
	`#include ...`

### Comments
`//` for single lines
`/* */` for multiple lines

### main() function 
every c++ program must have exactly 1 main() function 
starting point for a program
return 0 indicates successful program execution 
2 versions that are both valid 
```
int main(){
//code
return 0;
}
```
```
int main(int argc, char *argv[]){
//code
return 0;
}
```
2nd version has argc (argument count) and *argv[] which is an argument vector that  holds all the arguments 

### Namespaces
stuff like `std::cout` and not just `cout` 
can use stuff like `ussing namespace std;` at the top of the program 
# [elite](https://github.com/ferhatgec/elite)tod
## [elite](https://github.com/ferhatgec/elite) -> d converter

### input:
```rs
required_version is 0.1

set ProjectName as "elitetod"
set HOME        as env "HOME"


for argument "install" [
    use exec "cargo install --path ."

    for exists "{HOME}.cargo/bin/{ProjectName}" [
        println "{ProjectName} installed to {HOME}.cargo/bin/{ProjectName}."
    ]

    use signal "exit"
]
```

### output
```d
import std.file, core.stdc.stdlib, core.cpuid, std.process, std.stdio, std.string;
alias stderr = makeGlobal!(StdFileHandle.stderr); 
void main(string[] argv) {
if("0.1" != "0.1")
{
 stderr.writeln("elite: Required higher version");
 exit(1);
}
string ProjectName = "elitetod";
string HOME = "/home/gech";
if(argv.length >= 2 && argv[1] == "install")
{
 executeShell("cargo install --path .");
 if("/home/gech/.cargo/bin/elitetod".exists)
{
  writeln("elitetod installed to /home/gech/.cargo/bin/elitetod.");
}
 exit(1);
}
}

```

### elitetod licensed under the terms of MIT License

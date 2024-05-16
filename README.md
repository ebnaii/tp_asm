# tp_asm
TP_ASM 3SI

Discord : 
> .naii.

Some exercices in assembly x64 NASM

![tp](https://github.com/ebnaii/asm_tp/assets/82275372/6efe2c32-d185-4e9d-bc6f-0baac5de8239)


Compiled with : 
.bashrc
```
function asm()
{
  if [ $# -ne 1 ]; then
    echo "Usage: asm <file.s>"
    return 1
  fi

  filename="${1%.*}"
  nasm -f elf64 -o "$filename.o" "$1" && ld -o "$filename" "$filename.o" 

}

alias asm='asm'
```

# LABEXER1

A 32-bit NASM Linux program that uses procedures to perform addition, subtraction, multiplication, and division.

## Files

- `LABEXER1.asm` — program source.
- `LABEXER1.docx` — source code, brief explanation, compilation process, and test screenshots.
- `README.md` — program overview and compilation instructions.

## Compile and run

Place the project folder at `hjtnasm/LABEXER1`. From the existing `hjtnasm` folder, open a terminal with Docker Desktop running:

```powershell
docker compose run --rm nasm
```

Inside Docker, enter these commands one at a time:

```bash
cd /work/LABEXER1
nasm -f elf32 LABEXER1.asm -o LABEXER1.o
ld -m elf_i386 LABEXER1.o -o LABEXER1
file LABEXER1
./LABEXER1
```

## Use

Choose `A`, `S`, `M`, or `D`, then enter two whole numbers from `0` to `99`. Subtraction supports negative results. Division displays an integer quotient and remainder, and rejects division by zero. Invalid input prompts another attempt.

Enter `Y` to clear the screen and return to the menu, or `N` to exit. The Word document contains three test cases for each operation.

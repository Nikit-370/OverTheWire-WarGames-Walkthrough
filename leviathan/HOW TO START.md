# Leviathan — How to Start

Leviathan is an OverTheWire wargame focused on Linux, SUID binaries, program analysis, and basic exploitation.

## Official Resources

- [OverTheWire Wargames](https://overthewire.org/wargames/)
- [Leviathan](https://overthewire.org/wargames/leviathan/)

## Connection

Leviathan uses SSH on port `2223`:

```bash
ssh leviathan0@leviathan.labs.overthewire.org -p 2223
```

Use the starting credentials provided by the official challenge.

## Useful Commands

```bash
ls -la
file <binary>
strings <binary>
ltrace ./<binary>
strace ./<binary>
readelf -a <binary>
objdump -d <binary>
```

`gdb` and `radare2` are also useful for binary analysis.

## What You Will Learn

- Hidden files and directories
- Linux permissions
- SUID binaries
- `ltrace` and `strace`
- Input validation
- Command execution
- Symbolic links
- Race conditions
- Basic reverse engineering

> Try each challenge yourself before reading its walkthrough.

## Walkthroughs

- [Level 0](./level0.md)
- [Level 1](./level1.md)
- [Level 2](./level2.md)
- [Level 3](./level3.md)
- [Level 4](./level4.md)
- [Level 5](./level5.md)
- [Level 6](./level6.md)
- [Level 7](./level7.md)

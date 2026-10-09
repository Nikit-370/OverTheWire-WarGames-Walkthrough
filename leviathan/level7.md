# Leviathan Level 7

## Objective

Apply binary-analysis techniques to the final Leviathan challenge.

## Walkthrough

Start by inspecting the target:

```bash
ls -la
file <target>
```

Use static-analysis tools:

```bash
strings <target>
readelf -a <target>
objdump -d <target>
```

You can also load the executable into `radare2` or `gdb`:

```bash
r2 <target>
```

Follow the program's validation logic and identify the value used for its four-digit verification.

Pay attention to how the value is stored and represented. The value found during binary analysis may need to be converted into the decimal form expected by the program.

Run the executable with the resulting code.

## Key Concepts

- Reverse engineering
- Disassembly
- Integer representation
- `radare2`
- `gdb`
- Static analysis
- Dynamic analysis

Leviathan provides a useful introduction to the binary-analysis techniques used in more advanced OverTheWire games.

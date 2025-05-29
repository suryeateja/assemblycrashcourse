# Assembly Course WriteUps

```python
import pwn

pwn.context.update(arch="___")
code = pwn.asm("""
# your assembly instructions here
""" )
process = pwn.process("___")
process.write(code)

print(process.readall())
```

the above python code is used for solving the challenges 

in the above code import pwn means we are importing libraries in pwn tools libraries. 
arch stands for our computer architecture. pwn.asm gives assembly code instructions. and onsidr the process we will write the binary program or shell which we need to run.

challenge no. 1

in this challenge we were told to setup the register. in order to do that we can use the mov command. 

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 
here we are asked to set the register so we use mov command

```python
mov rdi , 0x1337
```

and we will get our flag 

challenge no. 2

in this challenge we were told to setup the multiple registers. in order to do that we can use the mov command. 

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 
here we are asked to set multiple registers so we use mov command

```python
mov rax , 0x1337
mov r12, 0xCAFED00D1337BEEF
mov rsp, 0x31337
```

and we will get our flag.

challenge no. 3

in this challenge we were told to add a value to rdi. in order to do that we can use the add command. 
add command is used to add.

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 
here we are asked to add a value to rdi so we use add command.

```python
add rdi, 0x331337
```

and we will get our flag.

challenge no. 4

in this challenge we were told to write linear equations. in order to do that we can use the mov add and imul commands. imul command is used to multiply.

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 
here we are asked to set up linear equations so we use mov, add and imul commands.

```python
mov rax , rdi
imul rax , rsi 
add rax , rdx 
```

and we will get our flag.

challenge 5

in this challenge we were told to compute speed = distance/time formula where speed is rax , distance is rdi and time is rsi and in order to solve that we will be using div instruction . 

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 

```python
mov rax , rdi 
div rsi
```

and we will get our flag 

challenge 6

in this challenge we were told to use the modulo operator. modulo (%) operator gives the remainder. in order to solve this challenge we will use mov and div commands. 

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 

```python
mov rax , rdi 
div rsi 
mov rax , rdx 
```

and we will get our flag. 

challenge 7 

in this challenge we were told to set the upper 8 bits of ax register. the upper 8 bits of ax register is ah and the lower 8 bits of ax is al . in order to access them we will use mov command

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 

```python
mov ah, 0x42
```

and we will get our flag 

challenge 8 

in this challenge we were told to perform the modulo operator .in order to solve this we are supposed to use the mov command.

for solving the challenge we open VScode workspace. here we can use the above python code to solve the challenge and we are supposed to write our assembly code in the code section. 

```python
mov al , dil
mov bx , si
```

and we will get our flag.
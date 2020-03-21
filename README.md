# x86-custom-kernel
> Custom kernel for a x86 system as part of Computer Engineering Operating System mini project in 2nd year.

**Requirements** :
1. NASM assembler
2. gcc
3. ld
4. qemu

**Steps to run** :
1. Create object files for `kernel.c` and `kernel.asm`
    * nasm -f elf32 kernel.asm -o kasm.o
    * gcc -m32 -c kernel.c -o kc.o
2. Link both the object files
    * ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o
3. Run the kernel on `QEMU emulator`
    * qemu-system-i368 -kernel kernel


gdb getflag
disassemble
// break after ptrace for hide injection
break *main+72
// break after getuid for changing user
break *main+444
// run program
run
// show result ptrace
print $eax
// set it to 0
set $eax=0
next
// show result getuid (current user)
print $eax
// set it to user for what we want token
set $eax=3000
next


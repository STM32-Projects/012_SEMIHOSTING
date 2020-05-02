# SEMIHOSTING

To illustrate the use of semihosing mechanism for stm32f446re(Nucleo)


The below steps are required to enable semihosting
 
 1. Set the linker arguments as follows
    --specs=rdimon.specs -lc -lrdimon
 
 2. Select the debugger as OpenOCD and add semihosting run command in the
    debug configuration(startup section)
    monitor arm semihosting enable

 3. Add the below functions with prototype to main.c
    extern void initialise_monitor_handles();
    initialise_monitor_handles();
   
 4. Exclude syscalls.c from the builds

################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
012_SEMIHOSTING.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
012_SEMIHOSTING.list \

OBJCOPY_BIN += \
012_SEMIHOSTING.bin \


# All Target
all: 012_SEMIHOSTING.elf secondary-outputs

# Tool invocations
012_SEMIHOSTING.elf: $(OBJS) $(USER_OBJS) /home/super/Desktop/Mastering_STM32_Projects/012_SEMIHOSTING/STM32F446RETX_FLASH.ld
	arm-none-eabi-gcc -o "012_SEMIHOSTING.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/super/Desktop/Mastering_STM32_Projects/012_SEMIHOSTING/STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="012_SEMIHOSTING.map" -Wl,--gc-sections -static --specs=rdimon.specs -lc -lrdimon --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

012_SEMIHOSTING.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "012_SEMIHOSTING.list"
	@echo 'Finished building: $@'
	@echo ' '

012_SEMIHOSTING.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "012_SEMIHOSTING.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

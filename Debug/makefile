################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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
distance_input_capture_mode.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
distance_input_capture_mode.list \

OBJCOPY_BIN += \
distance_input_capture_mode.bin \


# All Target
all: distance_input_capture_mode.elf secondary-outputs

# Tool invocations
distance_input_capture_mode.elf: $(OBJS) $(USER_OBJS) D:\stm32Project\distance\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "distance_input_capture_mode.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\stm32Project\distance\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="distance_input_capture_mode.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

distance_input_capture_mode.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "distance_input_capture_mode.list"
	@echo 'Finished building: $@'
	@echo ' '

distance_input_capture_mode.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "distance_input_capture_mode.bin"
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

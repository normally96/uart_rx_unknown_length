################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
uart_rx_unknown_length.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
uart_rx_unknown_length.list \

OBJCOPY_BIN += \
uart_rx_unknown_length.bin \


# All Target
all: uart_rx_unknown_length.elf secondary-outputs

# Tool invocations
uart_rx_unknown_length.elf: $(OBJS) $(USER_OBJS) G:\workspace\stm32\uart_rx_unknown_length\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "uart_rx_unknown_length.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"G:\workspace\stm32\uart_rx_unknown_length\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="uart_rx_unknown_length.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

uart_rx_unknown_length.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "uart_rx_unknown_length.list"
	@echo 'Finished building: $@'
	@echo ' '

uart_rx_unknown_length.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "uart_rx_unknown_length.bin"
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

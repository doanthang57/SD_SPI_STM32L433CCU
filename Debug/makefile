################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FatFs/src/option/subdir.mk
-include Middlewares/Third_Party/FatFs/src/subdir.mk
-include FATFS/Target/subdir.mk
-include FATFS/App/subdir.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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
SD_STM32L433CCU.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
SD_STM32L433CCU.list \

OBJCOPY_BIN += \
SD_STM32L433CCU.bin \


# All Target
all: SD_STM32L433CCU.elf secondary-outputs

# Tool invocations
SD_STM32L433CCU.elf: $(OBJS) $(USER_OBJS) C:\Users\Admin\Documents\Keil5\CubeIDE\SD_STM32L433CCU\STM32L433CCUX_FLASH.ld
	arm-none-eabi-gcc -o "SD_STM32L433CCU.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Admin\Documents\Keil5\CubeIDE\SD_STM32L433CCU\STM32L433CCUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="SD_STM32L433CCU.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

SD_STM32L433CCU.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "SD_STM32L433CCU.list"
	@echo 'Finished building: $@'
	@echo ' '

SD_STM32L433CCU.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "SD_STM32L433CCU.bin"
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

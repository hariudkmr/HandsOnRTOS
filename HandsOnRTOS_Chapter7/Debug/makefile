################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Middlewares/SEGGER/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
HandsOnRTOS_Chapter7.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
HandsOnRTOS_Chapter7.list \

OBJCOPY_BIN += \
HandsOnRTOS_Chapter7.bin \


# All Target
all: HandsOnRTOS_Chapter7.elf secondary-outputs

# Tool invocations
HandsOnRTOS_Chapter7.elf: $(OBJS) $(USER_OBJS) C:\Users\uidn9556\STM32CubeIDE\workspace_1.4.0\HandsOnRTOS_Chapter7\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "HandsOnRTOS_Chapter7.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\uidn9556\STM32CubeIDE\workspace_1.4.0\HandsOnRTOS_Chapter7\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="HandsOnRTOS_Chapter7.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

HandsOnRTOS_Chapter7.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "HandsOnRTOS_Chapter7.list"
	@echo 'Finished building: $@'
	@echo ' '

HandsOnRTOS_Chapter7.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "HandsOnRTOS_Chapter7.bin"
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

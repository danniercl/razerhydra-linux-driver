-include ../makefile.init

RM := rm -rf

-include sources.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
endif

-include ../makefile.defs

all: razer_linux_driver

razer_linux_driver: $(OBJS) $(USER_OBJS)
	g++-4.8 -L../../../../../lib/linux_x64/glibc4.6/release -L/usr/lib64/ -L../../../../../src/sixense_simple3d/Eclipse/freeglut/Release_x64 -o"razer_linux_driver" $(OBJS) $(USER_OBJS) $(LIBS) -lYARP_OS -lYARP_init

clean:
	-$(RM) $(OBJS)$(C++_DEPS)$(C_DEPS)$(CC_DEPS)$(CPP_DEPS)$(EXECUTABLES)$(CXX_DEPS)$(C_UPPER_DEPS) razer_linux_driver

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

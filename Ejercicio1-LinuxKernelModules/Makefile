obj-m += simple.o
CLANGDOPTIONS := ../clangd_options

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	if [ -d $(CLANGDOPTIONS) ]; then \
		cp compile_commands.json $(CLANGDOPTIONS)/compile_commands.json ; \
	fi
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
	if [ -f $(CLANGDOPTIONS)/compile_commands.json ]; then \
		cp $(CLANGDOPTIONS)/compile_commands.json compile_commands.json ; \
	fi
	

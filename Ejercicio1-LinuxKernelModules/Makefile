obj-m += simple.o
CLANGDOPTIONS := ../clangd_options

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	cp compile_commands.json $(CLANGDOPTIONS)/compile_commands.json
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
	cp $(CLANGDOPTIONS)/compile_commands.json compile_commands.json
	

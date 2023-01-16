KERNEL_TREE_PATH?=/lib/modules/$(shell uname -r)/build
EXTRA_CFLAGS="-DDEBUG"

obj-m+=gpio_test.o

all: gpio_test.ko

gpio_test.ko: gpio_test.c
	make -C $(KERNEL_TREE_PATH) M=$(PWD) modules

clean:
	make -C $(KERNEL_TREE_PATH) M=$(PWD) clean

.PHONY: all clean	
	

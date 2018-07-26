ifeq ($(KERNELRELEASE),)
KERNELRELEASE = $(shell uname -r)
endif

obj-m := hid-gcore.o hid-gfb.o hid-g110.o hid-g13.o hid-g15.o hid-g15v2.o hid-g19.o 
KDIR := /lib/modules/$(KERNELRELEASE)/build
PWD := $(shell pwd)

default:
	$(MAKE) -C $(KDIR) M=$(PWD)

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean

install:
	$(MAKE) -C $(KDIR) M=$(PWD) modules_install

TAGS:
	$(MAKE) -C $(KDIR) M=$(PWD) TAGS


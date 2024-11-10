#obj-m := main.o
#ARCH=arm
#CROSS_COMPILE=arm-linux-gnueabihf-
#set KERN_DIR to linux source location 
#TARGET_KERN_DIR = /home/sanath/LDD-1/sanath_LDD/linux-5.10.83/   #/home/sanath/LDD-1/sanath_LDD/linux-master
#HOST_KERN_DIR = /lib/modules/$(shell uname -r)/build/
#BUILD_DIR =  $(PWD)/build

#all:
#	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(TARGET_KERN_DIR) M=$(PWD) modules
#	mkdir -p $(BUILD_DIR)
#	mv *.o *.ko *.order *.symvers *.mod *.dwo .*cmd $(BUILD_DIR)/
#clean:
#	make -C $(HOST_KERN_DIR) M=$(PWD) clean
#	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(TARGET_KERN_DIR) M=$(PWD) clean
#	rm -rf $(BUILD_DIR)/*
#help:
#	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(TARGET_KERN_DIR) M=$(PWD) help
#host:
#	make -C $(HOST_KERN_DIR) M=$(PWD) modules
	
obj-m := main.o
SRC := $(shell pwd)

all:
	$(MAKE) -C $(KERNEL_SRC) M=$(SRC)

modules_install:
	$(MAKE) -C $(KERNEL_SRC) M=$(SRC) modules_install

clean:
	rm -f *.o *~ core .depend .*.cmd *.ko *.mod.c
	rm -f Module.markers Module.symvers modules.order
	rm -rf .tmp_versions Modules.symvers

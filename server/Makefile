ifndef DISABLE_MYSQL
CFLAGS+=$(shell mysql_config --cflags)
LDFLAGS+=$(shell mysql_config --libs)
endif
CFLAGS+=-lm -lpthread
LDFLAGS+=-lm -lpthread

serprobe:  $(wildcard *.c) $(wildcard *.h)
	$(CC) $^ -o $@ $(CFLAGS) $(LDFLAGS)

clean:
	-@rm  -rf serprobe *.o

# 假如有3个头文件，和8个C文件
# 最开始的第2版本（使用了变量）
# 能提高代码的兼容性，而且省时间

objects = main.o kbd.o command.o display.o insert.o search.o files.o utils.o

edit:$(objects)
	cc -o $(objects)

main.o:main.c defs.h
	cc -c main.c
kbd.o:kbd.c defs.h command.h
	cc -c kbd.c
command.o:command.c defs.h command.h
	cc -c command.c
display.o:display.c defs.h buffer.h
	cc -c display.c
insert.o:insert.c defs.h buffer.h
	cc -c insert.c
search.o:search.c defs.h buffer.h
	cc -c search.c
files.o:files.c defs.h buffer.h command.h
	cc -c files.c
utils.o:utils.c defs.h
	cc -c utils.c

clean:
	rm edit $(objects)

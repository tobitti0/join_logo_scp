PROGRAM = join_logo_scp
OBJS = CnvStrTime.o JlsAutoReform.o JlsAutoScript.o JlsCmdSet.o JlsDataset.o JlsIF.o JlsReformData.o JlsScript.o JlsTop.o

CC = gcc
CFLAGS = -O2
LDLAGS = -lstdc++

.SUFFIXES: .c .o

$(PROGRAM): $(OBJS)
	$(CC) -o $(PROGRAM) $^ $(LDLAGS)

.cpp.o:
	$(CC) $(CFLAGS) -c $<

.PHONY: clean
clean:
	$(RM) $(PROGRAM) $(OBJS)

# executable files for this directory
OBJECTS = FolderMain.exe HasPtrUseCount.exe \
		  HasPtrValueLike.exe \
		  moveHP.exe serial.exe StrFolderMain.exe \
		  useStrVec.exe substr.exe 

# the corresponding source file uses c++ 11 features
C11_OBJECTS = copyNoMove.exe 

# tells make to use the file "..\MS_makefile_template", which
# defines general rules for making .obj and .exe files
include ../MS_makefile_template

LOCFLAGS = -I../7 -I../1

Folder.o FolderMain.o: Folder.h
StrFolder.o StrFolderMain.o: StrFolder.h String.h
String.o: String.h
useStrVec.o StrVec.o: String.h StrVec.h

useStrVec.exe: StrVec.o useStrVec.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) useStrVec.o StrVec.o

FolderMain.exe: Folder.o FolderMain.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) FolderMain.o Folder.o

StrFolderMain.exe: StrFolder.o StrFolderMain.o String.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) StrFolderMain.o StrFolder.o String.o


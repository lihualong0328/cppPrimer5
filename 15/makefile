# executable files for this directory
OBJECTS = andQueryTest.exe and_orQueryTest.exe \
		  Basket_main.exe wordQueryTest.exe \
		  sample.exe scope.exe useQuote.exe \
		  vecBasket.exe virtualsNscope.exe

# tells make to use the file "..\MS_makefile_template", which
# defines general rules for making .obj and .exe files
include ../MS_makefile_template

LOCFLAGS = -I../12 -I../6

sample.o useQuote.o Quote.o: Quote.h
vecBasket.o Basket_main.o Basket.o: Basket.h Quote.h

get_print.o andQueryTest.o and_orQueryTest.o \
wordQueryTest.o Query.o: Query.h ../12/TextQuery.h

wordQueryTest.exe: Query.o wordQueryTest.o ../12/TextQuery.o get_print.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) wordQueryTest.o Query.o \
		../12/TextQuery.o get_print.o

andQueryTest.exe: Query.o andQueryTest.o ../12/TextQuery.o get_print.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) andQueryTest.o Query.o \
		../12/TextQuery.o get_print.o 

and_orQueryTest.exe: and_orQueryTest.o Query.o ../12/TextQuery.o \
		get_print.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) and_orQueryTest.o Query.o \
		../12/TextQuery.o get_print.o

useQuote.exe: useQuote.o Quote.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) useQuote.o Quote.o

vecBasket.exe: Basket.o vecBasket.o Quote.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) vecBasket.o Basket.o Quote.o 

Basket_main.exe: Basket.o Basket_main.o Quote.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) Basket_main.o Basket.o Quote.o

sample.exe: sample.o Quote.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) sample.o Quote.o


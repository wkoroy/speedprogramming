CPPFLAGS=-Wall -g
OBJECTS=main.o painter.o ship.o game.o bullet.o asteroid.o star.o
TARGET=asteroids
%.o: %.cpp
	g++ -c $(CPPFLAGS) -o $@ $<
$(TARGET): $(OBJECTS)
	g++ $(OBJECTS) -o $(TARGET) -g -lGL -lGLU  -lglut
main.o: main.cpp painter.hpp keys.hpp bullet.hpp asteroid.hpp game.hpp
painter.o: painter.cpp painter.hpp jet.hpp
ship.o: ship.cpp ship.hpp keys.hpp vector.hpp jet.hpp game.hpp painter.hpp game.hpp
game.o: game.cpp game.hpp bullet.hpp asteroid.hpp star.hpp
bullet.o: bullet.cpp bullet.hpp vector.hpp painter.hpp game.hpp
asteroid.o: asteroid.cpp asteroid.hpp vector.hpp painter.hpp game.hpp
star.o: star.cpp star.hpp vector.hpp painter.hpp game.hpp

PROJECT_NAME = Team

BUILD = build

SRC = src/Stepin-Unit-Converter-and-Calculator.c\
main.c\

TEST_SRC = src/Stepin-Unit-Converter-and-Calculator.c\
unity/Stepin-Unit-Converter-and-Calculator.c\

INC = -Iinc\

PROJECT_OUTPUT = $(BUILD)/$(PROJECT_NAME).out

TEST_OUTPUT = $(BUILD)/Test_$(PROJECT_NAME).out

DOCUMENTATION_OUTPUT = documentation/html

$(PROJECT_NAME):all

#.PHONY: all test doc run clean

all: $(SRC) $(BUILD)
	gcc $(SRC) $(INC) -o $(PROJECT_OUTPUT) -lm

run:$(PROJECT_NAME)
	./$(PROJECT_OUTPUT)

test:$(BUILD)
	gcc $(TEST_SRC) $(INC) -o $(TEST_OUTPUT) -lcunit -lm
	./$(TEST_OUTPUT)

doc:
	make -C documentation

clean:
	rm -rf $(BUILD) $(DOCUMENTATION_OUTPUT)

$(BUILD):
	mkdir build

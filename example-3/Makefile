.PHONY: all debug release clean

# Параметры компиляции для разных версий
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall

# Названия исполняемых файлов
RELEASE_EXEC  = example3
DEBUG_EXEC    = example3-dbg

# Исходный файл программы
SOURCE        = Kazino-Royal.cpp  # Переменная для исходного файла

# Цель для сборки всех версий
all: debug release

# Цель для сборки отладочной версии
debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCE)
	g++ $(DEBUG_FLAGS) $(SOURCE) -o $(DEBUG_EXEC)

# Цель для сборки релизной версии
release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCE)
	g++ $(RELEASE_FLAGS) $(SOURCE) -o $(RELEASE_EXEC)

# Цель для очистки всех сгенерированных файлов
clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)

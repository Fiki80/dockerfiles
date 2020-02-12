URL:="https://armkeil.blob.core.windows.net/developer/Files/downloads/gnu-rm/9-2019q4/RC2.1/gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2"
FILE:="gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2"
DIR:="gcc-arm-none-eabi-9-2019-q4-major"
SCRIPT:="arm-gcc-script"
LOCAL_BIN:="${HOME}/bin"

.phony: all build clean install

all: build

build: $(DIR)
	docker build -t arm-gcc .

$(DIR): $(FILE)
	@echo "Extracting $(FILE)"
	@tar -xf $(FILE) > /dev/null
	@rm -rf $(DIR)/share/doc

$(FILE):
	@echo "Downloading archive..."
	@curl -O $(URL)

install:
	@cp $(SCRIPT) $(LOCAL_BIN)
	@echo "Done!"

clean:
	@rm -rf $(DIR) && rm $(FILE)


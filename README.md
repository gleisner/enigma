# Enigma
An [Enigma](https://en.wikipedia.org/wiki/Enigma_machine) emulator written in Go.
## Status
Currently only supports the M3 with simple stepping

TODO
- set return message chunks (3/4/5/6). -1 = one long string 
- double step mechanism
- shiftable static rotor
- additional machine types (M4 up first)

## Features
- Can be extended through the use of JSON configuration files (see config directory)
- Logging to file/stdout so the machine execution can be traced.
- Tests for each machine type 

## Usage
Example:
```go
func main() {
  e := loadConfig("config/M3.json")
  e.Log.Println(e.code("super secret message"))
}
```
Run the tests with `go test`
## Resources
http://users.telenet.be/d.rijmenants/en/enigmatech.htm

http://people.physik.hu-berlin.de/~palloks/js/enigma/enigma-u_v20_en.html


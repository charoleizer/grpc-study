## Go
```bash
cd go-server
go get
protoc -I .. ../protos/example.proto --go_out=plugins=grpc:.
go run server.go

```

## Python
```bash
cd python-client
python3 -m venv venv
. venv/bin/activate
pip install -r requirements.txt
python -m grpc_tools.protoc -I .. ../protos/example.proto --python_out=. --grpc_python_out=.
python main.py

```
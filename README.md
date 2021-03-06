# Camera Proxy

Camera Proxy is a Python webserver which can display a video stream from the reolink argus 2 camera over http.

## Dependencies

```console
pip install av
pip install flask
pip install pillow
```

## Usage

Create a settings.json with one or more camera entries:
```json
{
    "cameras": [
        {
            "name": "camera1",
            "deviceSid": "12345678910ABC5D",
            "username": "admin",
            "password": "password",
            "backupImage": "../public/images/klingel.jpg"
        }
    ]
}
```

Just run the main.py from the root directory:

```console
python src/main.py
```

Access is then possible through:

|Type|url|
|---|---|
|single image | http://localhost:8000/api/v1/camera1|
|jpeg stream | http://localhost:8000/api/v1/camera1/stream|

## License
[MIT](license.txt)

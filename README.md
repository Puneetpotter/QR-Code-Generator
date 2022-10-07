# QR-Code-Generator




QRCode : Pure python QR Code generator

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install qrcode.

```bash
pip install qrcode
```

## Usage

```python
#import the library 
import qrcode 

#link to the website 
input_data = "https://car-price-prediction-project.herokuapp.com/"
Creating object 

#version: defines size of image from integer (1 to 40), box_size = size of each box in pixels, border = thickness of the border 
qr = qrcode.QRCode(version=1,box_size=10, border=5) 

#add_date : pass the input text 
qr.add_data(input_data) 

#converting into Image 
qr.make(fit=True) 

#specify the foreground and background color for the img 
img = qr.make_image(fill='black', back_color='white') 

#store the image 
img.save('qrcode_img.png')
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

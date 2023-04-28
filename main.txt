# This is your python coding test
from PIL import Image
import numpy as np

class ImagePrinter:

    def _init_(self):
        self.max_width = 1920
        self.max_height = 1080

        self.max_width = 1920
        self.max_height = 1080
        pass

    def load_image_from_file(self, file):
        i = Image.open(file)
        self.opened_Image =  i

    def openImageWindow(self):
        self.opened_Image.show()

    def rotate(self, angle):
        assert angle%90 == 0
        self.opened_Image.rotate(angle)

    def resizeImageToFitMaxSize(self, keep_props=100):
        width , height = self.opened_Image.size
        width_diff = width - max_height
        height_diff = height - max_width

        # resize image if it is bigger than maximum proportions
        if keep_props and height_diff  >= 0 or width_diff  >= 0 and width_diff > height_diff :
            new_width = max_width
            new_height = max_width/width  * height
            self.opened_Image = self.opened_Image.resize((new_width, new_height))
        elif keep_props and a <= 0 or b <= 0:
            new_width = max_height / height * width
            new_height = max_height
            self.opened_Image = self.opened_Image.resize((new_width, new_height))
        elif a <= 0 or b <= 0:
            new_width = max(x, self.max_width)
            new_height = max(y, self.max_height)
            self.opened_Image = self.opened_Image.resize((new_width, new_height))


if __name__ == '__main__':
    imp = ImagePrinter()
    imp.load_image_from_file("C:\\Users\\Ernst\\Pictures\\Capture.JPG")
    imp.rotate(90)
    imp.resizeImageToFitMaxSize(True)
    imp.openImageWindow()



from PIL import Image
from removebg import RemoveBg

# Change photo's color tone
def change_bgcolor(file_in, file_out, api_key, color):
    rmbg = RemoveBg(api_key, 'error.log')
    rmbg.remove_background_from_img_file(file_in)
    no_bg_image = Image.open(file_in)
    x, y = no_bg_image.size
    new_image = Image.new('RGBA', no_bg_image.size, color=color)
    new_image.paste(no_bg_image, (0, 0, x, y), no_bg_image)
    new_image.save(file_out)

# Photo Resizing
def change_size(file_in, file_out, width, height):
    image = Image.open(file_in)
    resized_image = image.resize((width, height), Image.ANTIALIAS)
    resized_image.save(file_out)

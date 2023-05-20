# GIF
import glob
from PIL import Image


def make_gif(frame_folder):
    frames = [Image.open(pic) for pic in glob.glob(f"{frame_folder}/*.jpeg")]
    frame_one = frames[0]
    frames[0].save("download.gif", format="GIF", append_images = frames[1:], save_all = True, duration=400, loop=0)


if __name__ == "__main__":
    print("inside main")
    make_gif("C:/Users/PC/PycharmProjects/CatGif/pic")
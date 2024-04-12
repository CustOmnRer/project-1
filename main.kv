

from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.lang import Builder
from kivy.properties import StringProperty
from kivy.uix.button import Button
from kivy.uix.textinput import TextInput
from kivy.uix.camera import Camera
from kivy.uix.image import Image
from kivy.uix.label import Label
import requests
import socket

WEBSITE_URL = "http://127.0.0.1:5000/"

KV = """

MyBL:

        orientation: "vertical"
        size_hint: (0.95, 0.95)
        pos_hint: {"center_x": 0.5, "center_y":0.5}

        Label:
                font_size: "15sp"
                multiline: True
                text_size: self.width*0.98, None
                size_hint_x: 1.0
                size_hint_y: None
                font_size: 30
                height: self.texture_size[1] + 15
                text: root.data_label

        FloatLayout:
                Button:
                        text: "Поиск по фото"
                        bold: True
                        background_color: '#ef7215'
                        size_hint: (1,0.8)
                        pos_hint: {'center_x': 0.5, 'y': 0.1}
                        font_size: 30
                        on_press: root.photo_capture()

        FloatLayout:
                Button:
                        text: "Поиск по описанию"
                        bold: True
                        background_color: '#ef7215'
                        size_hint: (1,0.8)
                        pos_hint: {'center_x': 0.5, 'y': 0.1}
                        font_size: 30
                        on_press: root.send_description()
                        

        FloatLayout:
                TextInput:
                        id: Inp
                        multiline: False
                        padding_y: (5,5)
                        size_hint: (1,0.8)
                        pos_hint: {'center_x': 0.5, 'y': 0.1}
                        font_size: 30
"""

class MyBL(BoxLayout):

    data_label = StringProperty("ПОГРИБЫ! или MUSHROOMS")

    def photo_capture(self):
         camera = Camera(play=False)
         camera.start()
         camera.export_to_png("photo.png")
         camera.stop()
         self.process_photo("photo.png")

    def process_photo(self, img_path):
          files = {'photo': open(img_path,'rb')}
          response = requests.post(WEBSITE_URL, files=files)
          if response.status_code == 200:
                result_text = response.text
                self.data_label = result_text
          else:
                self.data_label = "ОШИБКА. ОСТОРОЖНО!!! НЕОПОЗНАННЫЙ ГРИБ!!! БЕГИТЕ!!!"


    def send_description(self):
          description = "data_label"
          response = requests.post(WEBSITE_URL, data={"description": description})
          if response.status_code == 200:
                result_text = response.text
                self.data_label = result_text
          else:
                self.data_label = "Я ничего не понимаю. Видимо ваш гриб выдуманный. Скорректируйте описание или обратить к специалисту (по грибам)"

class PhotoProcessingApp(App):
      def build(self):
            return Builder.load_string(KV)
            if __name__ == "__main__":
                PhotoProcessingApp().run()

class TextProcessingApp(App):
      def build(self):
            return Builder.load_string(KV)
            if __name__ == "__main__":
                  TextProcessingApp().run()
      

class MUSHROOMS(App):

        def build(self):
              
              return Builder.load_string(KV)
        
MUSHROOMS().run()
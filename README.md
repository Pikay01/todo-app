# import libraries
from flet import *

# defining the function
def main(page: Page):
    # setting up the page title
    page.title = "To-Do APP"

    # helps you set the theme mode which is either light or dark mode
    # page.theme_mode = "light"

    # taking input from the user using a textfield
    input_text = TextField(
        hint_text= "What do you want to do today...", 
        width= 350
        )

    def button_clicked(event):
        page.add(
            Checkbox(
                label= input_text.value
            )
        )
    # aligning the input text and button in a row
    page.add(
        Row(
            controls=[
                input_text,
                ElevatedButton(
                    text= "Add",
                    on_click= button_clicked
                )
            ]
        )
    )

# call the function
app(target=main)

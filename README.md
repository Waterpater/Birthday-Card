> ### 🔱 About this fork
> 
> This is a fork of [JJ's Birthday Card](https://github.com/jansendejong/JJs-Birthday-Card).  
> The only addition (made with help of Claude Opus 4.7) is a **"deceased"** checkbox per person.  
> When enabled, the festive emoji is replaced by a memorial candle 🕯️ and the age display changes from *"(45 years)"* to *"(would have been 45 years)"* — a respectful way to remember loved ones on their birthday.
> 
> All credit for the original card goes to [JJ](https://github.com/jansendejong). 💛





# JJ's Birthday Card // Waterpater Version

A simple and user-friendly Lovelace card for Home Assistant that displays upcoming birthdays. The card is designed to give you a quick overview of who has a birthday soon. The visual editor makes it easy to customize the card to your liking.

## 🎉 Features

✅ Both the card and the editor support English, Dutch, German, French and Spanish (automatically adjusts to user's language – default English)  
✅ Use the default header, create your own custom header, or hide the header entirely  
✅ Display birthdays within a configurable number of upcoming days  
✅ Sort by name or date  
✅ Choose your own highlight color for people who have their birthday today  
✅ Customize background color and text color (including transparent background)  
✅ Fully configurable via the Lovelace UI editor (visual editor)  
✅ Compatible with HACS  
✅ Hide card if empty  
✅ **NEW:** Mark people as deceased – shows a candle 🕯️ instead of a festive emoji and displays "would have been X years"

## 📁 File structure

```
www/jjs-birthday-card/   
├── jjs-birthday-card.js          
├── hacs.json                         
├── README.md                       
└── LICENSE
```

## ⚙️ Manual Installation

1. Create the folder:

   ```
   /config/www/jjs-birthday-card/
   ```

2. Place the following file inside this folder: `jjs-birthday-card.js`

3. Add this resource to Home Assistant:  
   Via UI: **Settings → Dashboards → Resources → + Add**

   ```
   URL: /local/jjs-birthday-card/jjs-birthday-card.js  
   Type: JavaScript Module
   ```

4. Reload the browser or press **CTRL+F5**

## 🚀 Installation via HACS

1. Open HACS
2. Search for 'JJ's Birthday Card'
3. Install
4. Reload the frontend

## 💻 Usage in Lovelace

### Via YAML:

```yaml
type: custom:jjs-birthday-card
birthdays:
  - name: Jan
    date: "1985-10-20"
  - name: Lisa
    date: "1992-12-05"
  - name: Opa
    date: "1935-04-12"
    deceased: true
days_ahead: 7
sort_by: date  # or 'name'
```

### Via UI (Visual Editor):

1. Open your dashboard
2. Click **Edit Dashboard → Add Card → Custom: JJ's Birthday Card**
3. Add birthdays, choose sorting and set the number of days ahead
4. Check the "Deceased" box for people who have passed away, to show a memorial candle instead of a festive emoji

## ⚙️ Configuration Options

### Card options

| Option                  | Type   | Description                                  | Example               |
| ----------------------- | ------ | -------------------------------------------- | --------------------- |
| show_header             | toggle | Show or hide the header                      | on / off              |
| custom_header           | string | Use your own custom header                   | "Birthdays this week" |
| sort_by                 | string | Sort by `name` or `date`                     | "name"                |
| days_ahead              | number | Number of upcoming days to display           | 7                     |
| today_color             | color  | Background color for today's birthday        | "#ab8b3a"             |
| card_background         | color  | Background color of the card                 | "#ffffff"             |
| transparent_background  | toggle | Make card background transparent             | on / off              |
| card_text_color         | color  | Text color of the card                       | "#000000"             |
| hide_if_empty           | toggle | Hide card when there are no upcoming entries | on / off              |
| birthdays               | list   | List of people and their birthdates          | [{name, date}]        |

### Birthday entry options

| Option   | Type    | Description                                                                          | Example        |
| -------- | ------- | ------------------------------------------------------------------------------------ | -------------- |
| name     | string  | Name of the person                                                                   | "Lisa"         |
| date     | string  | Date of birth (YYYY-MM-DD)                                                           | "1989-12-06"   |
| deceased | boolean | If `true`, shows a candle 🕯️ and "would have been X years" instead of a festive emoji | true           |

## 🕯️ About the deceased option

When you mark a person as deceased:
- The festive emoji (🎉, 🎂, 🎁, etc.) is replaced with a memorial candle 🕯️
- The age display changes from "(45 years)" to "(would have been 45 years)"
- The "today" highlight color is not applied to deceased entries, keeping the display respectful

This makes the card a nice way to remember loved ones on the day they would have celebrated their birthday.

## 🖼️ Screenshots

*jjs-birthday-card multilanguage*

*jjs-birthday-card-editor multilanguage*

## 📄 License

This project is licensed under the MIT License. You are free to use, modify, and distribute it.

## ❤️ Credits & Contact

Created by: **J. de Jong (J.J.)**  
Feedback or ideas? Feel free to open an issue or pull request on GitHub.

Enjoy the card! 🎂

[Buy Me A Coffee]

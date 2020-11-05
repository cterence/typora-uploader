﻿# typora-nextcloud-uploader

Uploads local images included in a [Typora](https://typora.io/) markdown document into a Nextcloud instance and generates a sharing link

It allows you to visualize the images included in your markdown documents from any device

## Installation

- Install dependencies

```
pip install -r requirements.txt
```

- Set your environment variables

- In Typora, Go to Files -> Preferences -> Image
  - Set When Insert... to Upload image
  - Set Image Upload Setting to Custom Command
  - put `python3 <path/to/script>` as your command

## Troubleshoot

If you are encountering an error like such when testing the script in Typora :

```
File "path/to/owncloud.py",
line 910, in share_file_with_link
'name': data_el.find('name').text
AttributeError: 'NoneType' object has no attribute 'text'
```

The error seems to come from the library, so then comment the faulty line in the library and you should be good to go !

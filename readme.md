##About

Calibre Web is a web app providing a clean interface for browsing, reading and downloading eBooks using an existing [Calibre](https://calibre-ebook.com) database.

*This software is a fork of [library](https://github.com/mutschler/calibreserver) and licensed under the GPL v3 License.*

![screenshot](https://raw.githubusercontent.com/janeczku/docker-calibre-web/master/screenshot.png)

##Features
- Bootstrap 3 HTML5 interface
- User management
- Admin interface
- OPDS feed for eBook reader apps
- Filter and search by titles, authors, tags, series and language
- Create custom book collection (shelves)
- Support for editing eBook metadata
- Support for converting eBooks from EPUB to Kindle format (mobi/azw)
- Restrict eBook download to logged-in users
- Support for public user registration
- Send eBooks to Kindle devices with the click of a button
- Support for reading eBooks directly in the browser
- Upload new books in PDF format
- Support for Calibre custom columns
- Fine grained per-user permissions

## Quick start

1. Rename `config.ini.example` to `config.ini` and set `DB_ROOT` to the path of the folder where your Calibre library (metadata.db) lives
2. Execute the command: `python cps.py`
3. Point your browser to `http://localhost:8083` or `http://localhost:8083/feed` for the OPDS catalog 

**Default admin login:**    
*Username:* admin   
*Password:* admin123

## Runtime Configuration Options

`PUBLIC_REG`    
Set to 1 to enable public user registration.    
`ANON_BROWSE`    
Set to 1 to allow not logged in users to browse the catalog.    
`UPLOADING`    
Set to 1 to enable PDF uploading. This requires the imagemagick library to be installed.    

## Requirements

Python 2.7+
     
Optionally, to enable on-the-fly conversion from EPUB to MOBI when using the send-to-kindle feature:     

[Download](http://www.amazon.com/gp/feature.html?docId=1000765211) Amazon's KindleGen tool for your platform and place the binary named as `kindlegen` in the `vendor` folder. 

## Docker image

Calibre Web can be run as Docker container. The latest image is available on [Docker Hub](https://registry.hub.docker.com/u/janeczku/calibre-web/).
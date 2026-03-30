# libros-de-salud.github.io

## Adding new books
The process of adding new books for this website involves generating the appropriate links for your media, then adding them to the books.json file provided in the root directory of this repository. Automatically, github will build and redeploy the website at libros-de-salud.github.io. The following steps assume you're using google drive (drive.google.com) to host your media.

### Generating a PDF link
1. Upload your book pdf to a google drive account
2. Generate a shareable link to your pdf. Make sure to mark it as "Anyone with the link" can access, or you will face issues down the line
3. Step 2 will give you a link like this: https://drive.google.com/file/d/FILE_ID/view?usp=sharing. Extract the entire FILE_ID between /d and /view. FILE_ID in this case is a placeholder -- in reality, you'll have a random mix of letters and numbers for your FILE_ID. 
4. Fill in the FILE_ID placeholder of this link with what you extracted in step 3: https://drive.google.com/uc?export=download&id=FILE_ID
5. The link above can be used to directly download your media. To test it, copy and paste it into your browser and verify you start downloading the pdf
6. Save this link for section "Configuring the website to show your media"

### Generating a thumbnail photo link
1. Upload your book thumbnail photo to a google drive account
2. Generate a shareable link to your photo. Make sure to mark it as "Anyone with the link" can access, or you will face issues down the line
3. Step 2 will give you a link like this: https://drive.google.com/file/d/FILE_ID/view?usp=sharing. Extract the entire FILE_ID between /d and /view. FILE_ID in this case is a placeholder -- in reality, you'll have a random mix of letters and numbers for your FILE_ID. 
4. Fill in the FILE_ID placeholder of this new link with what you extracted in step 3: https://drive.google.com/thumbnail?id=FILE_ID&sz=w1000
5. The link above can be used to directly view your media. To test it, copy and paste it into your browser and verify that your desired photo pops up
6. Save this link for section "Configuring the website to show your media"

### Configuring the website to show your media
1. Make sure you have handy your PDF_LINK (what you got from "Generating a PDF link") and your PHOTO_LINK (what you got from "Generating a thumbnail photo link")
2. Navigate to the books.json file in the github repository (https://github.com/libros-de-salud/libros-de-salud.github.io/blob/main/books.json). If you don't have access, contact jacktimothynorris@gmail.com. 
3. Click the edit button to tweak the JSON (the pencil icon)
4. Create a new entry in the JSON file. Make sure there's a comma after the previous entry. You can follow the template outlined below:
```
[
    .
    .
    .
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "YOUR TITLE", "link": "PDF_LINK", "image": "PHOTO_LINK"}, 
]
```
5. Click "Commit Changes"
6. Wait a minute or two
7. Visit libros-de-salud.github.io to see your changes. You might need to open in a incognito browser if you're device has cached the page

### From start to finish example
#### PDF upload
1. I just uploaded a pdf to my google drive. 
2. After selecting "Anyone with the link" can access for the pdf I uploaded, I have the following link:  https://drive.google.com/file/d/1uDMr4_fszpSzWJH9z51UABHR0z64RniX/view?usp=sharing
3. I take this link and extract the file id between /d and /view: 1uDMr4_fszpSzWJH9z51UABHR0z64RniX
4. Using that file id, I now feed it into the template provided above to get this link: https://drive.google.com/uc?export=download&id=1uDMr4_fszpSzWJH9z51UABHR0z64RniX
5. I just checked and verified that the link above automatically downloads the PDF
6. I have now noted down the following for future use: https://drive.google.com/uc?export=download&id=1uDMr4_fszpSzWJH9z51UABHR0z64RniX

#### Thumbnail image upload
1. I just uploaded a image to my google drive. 
2. After selecting "Anyone with the link" can access for the pdf I uploaded, I have the following link:  https://drive.google.com/file/d/1rcOHuu7J2JEUktyOEFnBZAGCzkGtyR-F/view?usp=sharing
3. I take this link and extract the file id between /d and /view: 1rcOHuu7J2JEUktyOEFnBZAGCzkGtyR-F
4. Using that file id, I now feed it into the template provided above to get this link: https://drive.google.com/thumbnail?id=1rcOHuu7J2JEUktyOEFnBZAGCzkGtyR-F&sz=w1000
5. I just checked and verified that the link above automatically brings up the image
6. I have now noted down the following for future use: https://drive.google.com/thumbnail?id=1rcOHuu7J2JEUktyOEFnBZAGCzkGtyR-F&sz=w1000

#### Feeding your links into the website
1. I have my PDF_LINK: https://drive.google.com/uc?export=download&id=1uDMr4_fszpSzWJH9z51UABHR0z64RniX and I have my PHOTO_LINK: https://drive.google.com/thumbnail?id=1rcOHuu7J2JEUktyOEFnBZAGCzkGtyR-F&sz=w1000
2. I navigate to https://github.com/libros-de-salud/libros-de-salud.github.io/blob/main/books.json
3. I click the edit button (the pencil)
4. This is the json file before: 
```
[
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"} 
]
```
5. This is the json file after (added a comma on proceeding line, followed the template from above): 
```
[
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"},
    {"title": "Salud Femenina 1", "link": "https://drive.google.com/uc?export=download&id=1uDMr4_fszpSzWJH9z51UABHR0z64RniX", "image": "https://drive.google.com/thumbnail?id=1rcOHuu7J2JEUktyOEFnBZAGCzkGtyR-F&sz=w1000"},
]
```
6. I click "Commit Changes" (you can put a descriptive message of what you did if it asks, use default settings in form)
7. I wait about 1-2 minutes
7. I libros-de-salud.github.io and see my changes (perhaps in an incognito browser)
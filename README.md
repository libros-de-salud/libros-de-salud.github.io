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
2. Navigate to the books.json file in the github repository (https://github.com/libros-de-salud/libros-de-salud.github.io). If you don't have access, contact jacktimothynorris@gmail.com. 
3. Create a new entry in the JSON file. Make sure there's a comma after the previous entry. You can follow the template outlined below:
```
[
    .
    .
    .
    {"title": "prev_entry title", "link": "prev_entry link", "link": "prev_entry link", "image": "prev_entry image"}, 
    {"title": "YOUR TITLE", "link": "PDF_LINK", "image": "PHOTO_LINK"}, 
]
```



https://drive.google.com/uc?export=download&id=1uDMr4_fszpSzWJH9z51UABHR0z64RniX
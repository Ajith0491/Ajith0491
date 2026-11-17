# Add a Profile Photo to a Resume PDF

A small Python script that places a profile photo in the upper-right header area
of page 1 of a resume PDF. It uses PyMuPDF.

## Requirements

- Python 3.9+
- PyMuPDF

Install the dependency:

```bash
python -m pip install pymupdf
```

## Run

```bash
python add_photo_to_resume.py --input "Updated Resume (1).pdf" --photo "profile.jpg" --output "Resume_with_Photo.pdf"
```

The script does not modify the original PDF. It creates the output file at the
path supplied with `--output`.

## Adjust photo position

The photo placement is controlled by `photo_box` in the script:

```python
photo_box = fitz.Rect(468, 34, 552, 118)
```

These are PDF point coordinates on the first page. Change the four values to
move or resize the photo.

## GitHub

Create a new GitHub repository, then upload `add_photo_to_resume.py` and this
`README.md`. Keep your resume and personal photo private unless you intend to
publish them.

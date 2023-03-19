.DEFAULT_GOAL := book

content:                     		## Make markdown.contents file
	cat preface.md introduction.md python-primer.md ecommerce-automation.md web-forms-automation.md social-media-automation.md api-automation.md web-scraping.md test-suites.md best-practices.md advanced.md > contents.md

pdf: content						## Make PDF
	pandoc -f markdown+smart --toc -V documentclass=report --pdf-engine=xelatex --epub-embed-font='fonts/*.ttf' --template pdf-book-template.tex  -o book.pdf  metadata.txt contents.md
	rm contents.md

book: content						## Make EPUB
	pandoc -f markdown+smart --toc -V documentclass=book --epub-embed-font='fonts/*.ttf' -o book.epub metadata.txt contents.md
	rm contents.md

clean:                        		## Clean up
	rm -f book.epub book.pdf contents.md


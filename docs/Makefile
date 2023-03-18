.DEFAULT_GOAL := book

content:                     		## Make markdown.contents file
	cat author.md introduction.md python-primer.md ecommerce-automation.md web-forms-automation.md social-media-automation.md api-automation.md web-scraping.md test-suites.md best-practices.md advanced.md > contents.markdown

pdf: content						## Make PDF
	pandoc -f markdown+smart --toc --epub-embed-font='fonts/*.ttf' -o book.pdf metadata.txt contents.markdown

book: content						## Make EPUB
	pandoc -f markdown+smart --toc --epub-embed-font='fonts/*.ttf' -o book.epub metadata.txt contents.markdown

clean:                        		## Clean up
	rm -f book.epub book.pdf contents.markdown


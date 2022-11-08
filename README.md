# Dog API Images

This is the collection of all images served by [Dog API](https://dog.ceo/dog-api/) sorted by breed.

If you would like to contribute towards this open source project with pictures of your own dog, submit your image as a Pull Request and we will review.

All images you submit will be made available via the [Dog API endpoints](https://dog.ceo/dog-api/documentation).

## Submission guide

- We will only accept JPG images which are smaller than 300kb
- Please ensure your photos are of a good quality and the dog is easily identifiable in the photo
- Please ensure your photo features one dog only (although additional dogs can be in the background)
- If your dog breed does not exist in our collection you can suggest breeds for us to include by creating a new directory for it
- We love mixed breeds too! They can be included under [/mix](https://github.com/jigsawpieces/dog-api-images/tree/master/mix)


Original images provided by the [Stanford Dogs Dataset](http://vision.stanford.edu/aditya86/ImageNetDogs/).

```
# Remove spaces from filenames
find . -type f -name "* *" | while read file; do mv "$file" ${file// /_}; done

# Find uppercase
find . -name "*.*[A-Z]*" ! -name "*.*[^A-Z]*"
```

# Find uppercase and rename to lowercase
```bash
find . -depth -name '*.JPG' -type f -exec bash -c 'base=${0%.*} ext=${0##*.} a=${base,,}.${ext,,}; [ "$a" != "$0" ] && mv -- "$0" "$a"' {} \;
```
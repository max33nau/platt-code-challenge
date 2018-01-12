# platt-code-challenge

This is the first time I have ever used Vue.js and I am really starting to love the framework.

With the autocomplete for dogs api, if you choose a dog and press enter or click on the search icon a modal will pop up showing you a picture of the dog.
I added that functionality to make it do a couple more things.

Tested on latest versions of IE, Chrome and Firefox

## Notes

1. I noticed the "Live Help" icon changes whether it is on mobile vs. tablet, not sure if that was inentional or not but I made it work.
2. Some things I would like to do in the future is I noticed some of the components I was using were very similiar so I would probably try
to make them more modular and reusable
3. I used flexbox with the understanding that there may be issues in browsers that use less than IE 11, I just figured for the time scope
of this project it was the best thing to use, and bootsrap 4 uses flexbox now so I wanted to make myself more familiar with it.
4. The autocomplete uses two npm modules that allow me to make my Ajax request to get all dog breeds and then I am able to filter them
out based on the user input. Again given the time constraint, I would probably clean up that search box filtering more if I was going to continue with this project.
5. I really enjoyed completing this challenge and learned a lot along the way. It was really a lot of fun.
6. I found out there was some issues with flex box on iOS devices so I added webkits to all flex box attributes, given more time. I would probably move these to a scss
file and import these into each place flex box is used but I just left it as is for now.

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```


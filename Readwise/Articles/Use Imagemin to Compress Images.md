# Use Imagemin to Compress Images

**Author:** Katie Hempenius  
**Full title:** Use Imagemin to Compress Images  
**URL:** https://web.dev/use-imagemin-to-compress-images/  
**Source:** #articles #instapaper #readwise

- Uncompressed images bloat your pages with unnecessary bytes. 
   
- Run Lighthouse to check for opportunities to improve page load by compressing images. These opportunities are listed under "Efficiently encode images 
   
- Imagemin is an excellent choice for image compression because it supports a wide variety of image formats and is easily integrated with build scripts and build tools. 
   
- Plugins 
   
- Imagemin is built around "plugins." A plugin is an npm package that compresses a particular image format (e.g. "mozjpeg" compresses JPEGs) 
   
- In lossless compression, no data is lost. Lossy compression reduces file size, but at the expense of possibly reducing image quality 
   
- Imagemin CLI 
   
- The Imagemin CLI works with 5 different plugins: imagemin-gifsicle, imagemin-jpegtran, imagemin-optipng, imagemin-pngquant, and imagemin-svgo. 
   
- Imagemin uses the appropriate plugin based on the image format of the input. 
   
- You can also use Imagemin by itself as a Node script. 
   
- const imagemin = require('imagemin');
  const imageminMozjpeg = require('imagemin-mozjpeg');
  (async() => {
  const files = await imagemin(
  ['source_dir/*.jpg', 'another_dir/*.jpg'],
  {
  destination: 'destination_dir',
  plugins: [imageminMozjpeg({quality: 50})]
  }
  );
  console.log(files);
  })(); 
   

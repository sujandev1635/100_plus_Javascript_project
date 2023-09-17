```javascript
let overlay = document.querySelector('.galleryOverlay');
let imgBox = document.querySelector('.imgBox');
var img = document.querySelector('.imgBox img');
let close = document.querySelector('.imgBox span');

let gallery = document.querySelector('#gallery');
gallery.addEventListener('click', (e) => {
  let currentImagePath = e.target.src;
  if (currentImagePath !== undefined) {
    overlay.classList.add('galleryOverlayShow');
    imgBox.classList.add('imgBoxShow');
    img.src = currentImagePath;
    console.log(currentImagePath);
  }
});

close.addEventListener('click', () => {
  overlay.classList.remove('galleryOverlayShow');
  imgBox.classList.remove('imgBoxShow');
});
```

---
layout: default
title: Apartment Floorplans
---

<script>
if (sessionStorage.getItem("authenticated") !== "true") {
  window.location.href = "login.html";
}
</script>


# Building exterior and floorplan

## Apartment Type: Standard

![Standard Floorplan](images/floorplan.png)

## Building features

The ground floor of the building has a common area with a study room, community kitchen and a small gym which is accessible to all residents. Attached here are the images of the common areas.


<!-- Begin Image Carousel -->
<div class="lightbox-gallery">
    <img src="images/ext1.png" alt="Common area 1">
    <img src="images/ext2.png" alt="Common area 2">
    <img src="images/ext3.png" alt="Common area 3">
    <img src="images/ext4.png" alt="Common area 4">
    <img src="images/ext5.png" alt="Common area 5">
    <img src="images/ext6.png" alt="Common area 6">
    <img src="images/ext7.png" alt="Common area 7">
    <img src="images/ext8.png" alt="Common area 8">
</div>


---

<style>
.lightbox-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 15px;
  margin-top: 20px;
}
.lightbox-gallery img {
  width: 100%;
  border-radius: 8px;
  cursor: pointer;
  transition: transform 0.2s;
  box-shadow: 0 2px 6px rgba(0,0,0,0.15);
}
.lightbox-gallery img:hover { transform: scale(1.03); }

.lightbox {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0; top: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.9);
}
.lightbox-content {
  display: block;
  margin: auto;
  max-width: 90%;
  max-height: 85%;
  border-radius: 8px;
  box-shadow: 0 0 25px rgba(0,0,0,0.6);
}
.close, .prev, .next {
  color: white;
  position: absolute;
  font-size: 2rem;
  cursor: pointer;
  user-select: none;
}
.close { top: 20px; right: 35px; }
.prev, .next {
  top: 50%; transform: translateY(-50%);
  padding: 16px;
  font-weight: bold;
  background: rgba(0,0,0,0.4);
  border-radius: 50%;
}
.prev:hover, .next:hover { background: rgba(0,0,0,0.7); }
.prev { left: 20px; } .next { right: 20px; }

@media (max-width: 768px) {
  .lightbox-content { max-width: 95%; max-height: 80%; }
  .prev, .next { font-size: 1.5rem; padding: 12px; }
}
</style>

<div id="lightbox" class="lightbox">
  <span class="close" onclick="closeLightbox()">&times;</span>
  <img id="lightbox-img" class="lightbox-content">
  <a class="prev" onclick="changeImage(-1)">&#10094;</a>
  <a class="next" onclick="changeImage(1)">&#10095;</a>
</div>

<script>
let currentIndex = 0;
const galleryImages = document.querySelectorAll('.lightbox-gallery img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');

galleryImages.forEach((img, i) => {
  img.addEventListener('click', () => { currentIndex = i; openLightbox(); });
});

function openLightbox() {
  lightbox.style.display = 'block';
  showImage(currentIndex);
}
function closeLightbox() { lightbox.style.display = 'none'; }
function showImage(index) { lightboxImg.src = galleryImages[index].src; }
function changeImage(step) {
  currentIndex = (currentIndex + step + galleryImages.length) % galleryImages.length;
  showImage(currentIndex);
}
document.addEventListener('keydown', e => {
  if (e.key === 'Escape') closeLightbox();
  if (e.key === 'ArrowLeft') changeImage(-1);
  if (e.key === 'ArrowRight') changeImage(1);
});
lightbox.addEventListener('click', e => {
  if (e.target === lightbox) closeLightbox();
});
let startX = 0;
lightbox.addEventListener('touchstart', e => startX = e.changedTouches[0].screenX);
lightbox.addEventListener('touchend', e => {
  const diff = e.changedTouches[0].screenX - startX;
  if (Math.abs(diff) > 50) diff > 0 ? changeImage(-1) : changeImage(1);
});
</script>

---
[⬅ Back to Home](index.md)
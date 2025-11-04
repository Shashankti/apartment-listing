---
layout: default
title: Current Apartment Photos
---

<script>
if (sessionStorage.getItem("authenticated") !== "true") {
  window.location.href = "login.html";
}
</script>

<!-- Restrict direct access unless coming from gallery -->
<script>
const ref = document.referrer;
if (!ref || (!ref.includes("gallery.md") && !ref.includes("gallery.html"))) {
  window.location.href = "gallery.html";
}
</script>


# Current photos

These are *recent real photos* of the apartment.  
Please note: the apartment is currently in use, so it may not appear fully clean and organized.

---

<div class="current-gallery">
  <figure><img src="images/current1.png" alt="Bed1"><figcaption>Bed</figcaption></figure>
  <figure><img src="images/current2.png" alt="Desk"><figcaption>Desk</figcaption></figure>
  <figure><img src="images/current3.jpg" alt="Wardrobe"><figcaption>Wardrobe </figcaption></figure>
  <figure><img src="images/current4.png" alt="Mirror"><figcaption>Mirror and coat hanger</figcaption></figure>
  <figure><img src="images/current5.png" alt="Storage1 "><figcaption>Shelf1</figcaption></figure>
  <figure><img src="images/current6.png" alt="Storage2 "><figcaption>Shelf2</figcaption></figure>
  <figure><img src="images/current9.png" alt="Storage3 "><figcaption>Shelf3</figcaption></figure>
  <figure><img src="images/current8.png" alt="headrest "><figcaption>bed head</figcaption></figure>
  <figure><img src="images/bathroom1.jpg" alt="shower "><figcaption>Shower</figcaption></figure>
  <figure><img src="images/bathroom2.jpg" alt="bathroom "><figcaption>Bathroom</figcaption></figure>
  <figure><img src="images/bathroom3.jpg" alt="bathroomnoch "><figcaption>Still Bathroom</figcaption></figure>
  <figure><img src="images/bathroom4.jpg" alt="bathstore"><figcaption>bathroom storage</figcaption></figure>
  <figure><img src="images/kitchen1.png" alt="kitcheup"><figcaption>kitchen up</figcaption></figure>
  <figure><img src="images/kitchen2.png" alt="kitchedown"><figcaption>kitchen down</figcaption></figure>
  <figure><img src="images/kitchen3.png" alt="kitcheside"><figcaption>kitchen side</figcaption></figure>
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
[⬅ Back to Gallery](gallery.md)
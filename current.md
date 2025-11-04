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
.current-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.current-gallery figure {
  margin: 0;
  border: 1px solid #ddd;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  background-color: #fafafa;
}
.current-gallery img {
  width: 100%;
  height: auto;
  display: block;
}
.current-gallery figcaption {
  padding: 10px;
  font-size: 0.9rem;
  color: #333;
  background-color: #fff;
  text-align: center;
}
</style>

---
[⬅ Back to Gallery](gallery.md)

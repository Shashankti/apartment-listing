---
layout: default
title: Current Apartment Photos
---

<script>
if (sessionStorage.getItem("authenticated") !== "true") {
  window.location.href = "login.html";
}
</script>

# Current photos

These are *recent real photos* of the apartment.  
Please note: the apartment is currently in use, so it may not appear fully clean and organized.

---

<div class="current-gallery">
  <figure><img src="images/current_2.png" alt="Current photo 2"><figcaption>View 2 – desk and storage</figcaption></figure>
  <figure><img src="images/current_3.png" alt="Current photo 3"><figcaption>View 3 – wardrobe and miror</figcaption></figure>
  <figure><img src="images/current_4.png" alt="Current photo 4"><figcaption>View 4 – Desk </figcaption></figure>
  <figure><img src="images/current_5.png" alt="Current photo 5"><figcaption>View 5 – more storage</figcaption></figure>
  <figure><img src="images/current_6.png" alt="Current photo 6"><figcaption>View 6 – bed</figcaption></figure>
  <figure><img src="images/current_7.png" alt="Current photo 7"><figcaption>View 7 – bed</figcaption></figure>
  <figure><img src="images/current_8.png" alt="Current photo 8"><figcaption>View 8 – overall room layout</figcaption></figure>
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

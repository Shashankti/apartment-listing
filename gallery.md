---
layout: default
title: Interior Gallery
---

<script>
if (sessionStorage.getItem("authenticated") !== "true") {
  window.location.href = "login.html";
}
</script>

# Apartment Interiors

These are the stock images which show the furniture and layout of the apartment.

---

<div class="gallery">
  <figure>
    <img src="images/interior_1.png" alt="Living Area">
    <figcaption><b>Living Area</b> – spacious and bright, includes bed, study desk, and wardrobe.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_2.png" alt="Work Desk">
    <figcaption><b>Work Desk</b> – includes chair, pull-out storage unit, and overhead shelves.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_3.png" alt="Kitchen Area">
    <figcaption><b>Kitchenette</b> – equipped with sink, induction stove, and microwave oven.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_4.png" alt="Bathroom">
    <figcaption><b>Bathroom</b> – private ensuite with shower, mirror, and storage cabinet.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_5.png" alt="Sideboard and mirror">
    <figcaption><b>Sideboard & Mirror</b> – located near the entrance, useful for storage and daily essentials.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_6.png" alt="Dining area">
    <figcaption><b>Dining Corner</b> – includes compact dining table with bar stool seating.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_7.png" alt="Wardrobe area">
    <figcaption><b>Wardrobe Section</b> – built-in storage with shelves and hanging space.</figcaption>
  </figure>

  <figure>
    <img src="images/interior_8.png" alt="Overall view">
    <figcaption><b>Full Room View</b> – overall layout showing how all furniture fits in the space.</figcaption>
  </figure>
</div>

---

For the current images [click here](current.md)
!! Warning it is not very clean and organised



---

<style>
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.gallery figure {
  margin: 0;
  border: 1px solid #ddd;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  background-color: #fafafa;
}
.gallery img {
  width: 100%;
  height: auto;
  display: block;
}
.gallery figcaption {
  padding: 10px;
  font-size: 0.9rem;
  color: #333;
  background-color: #fff;
  text-align: center;
}
</style>

---
[⬅ Back to Home](index.md)



<!-- | Living Area | Work Desk | Kitchen | Bathroom |
|--------------|------------|----------|-----------|
| ![Living](images/inerior1.png) | ![Desk](images/interior2.png) | ![Kitchen](images/interior3.png) | ![Bathroom](images/interior5.png) | -->

<!-- Overview:
<!-- 
![Interior 4](images/interior4.png)

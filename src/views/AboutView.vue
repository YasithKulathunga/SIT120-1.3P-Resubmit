<script>
  export default {
    data() {
      return {
        packages: [
          { name: 'Bronze', price: 500 },
          { name: 'Silver', price: 800 },
          { name: 'Gold', price: 1500 },
        ],
      }
    },
  }
</script>

<template>
  <section>
    <section class="gallery">
        <div class="gallerytext">
            <h1>Projects</h1>
        </div>
        <div class="row"> 
            <div class="column">
              <img class="gimg" src="https://images.unsplash.com/photo-1611930022073-b7a4ba5fcccd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1567721913486-6585f069b332?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=688&q=80" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1571781926291-c477ebfd024b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=688&q=80" style="width:100%">
             
            </div>
            <div class="column">
              <img class="gimg" src="https://images.unsplash.com/photo-1617355405361-29f0f0a3d737?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTR8fHBvc3RlcnN8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1543487945-139a97f387d5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8cG9zdGVyc3xlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1508161773455-3ada8ed2bbec?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8cG9zdGVyc3xlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1511466431307-d603e868975c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fHBvc3RlcnN8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              
            </div>  
            <div class="column">
              <img class="gimg" src="https://images.unsplash.com/photo-1541506618330-7c369fc759b5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8YXBwJTIwZGVzaWdufGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8YXBwJTIwZGVzaWdufGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1551721434-8b94ddff0e6d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Nnx8YXBwJTIwZGVzaWdufGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=60" style="width:100%">
              <img class="gimg" src="https://images.unsplash.com/photo-1547658719-da2b51169166?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8YXBwJTIwZGVzaWdufGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=60" style="width:100%">
            </div>
        </div>
        <div class="packages">
          <h1 class="title">Our Packages</h1>
          <div>
            <li v-for="item in packages">
              {{ item.name }}
              <span v-if="item.price <= 1000">: Recomended</span>
              <span v-else>: Enterprise</span>
            </li>
            <h4>More Details in the Contact Page</h4>
          </div>
        </div>
    </section>
  </section>
</template>

<style>

.package_list{
  font-size: 30px;
  font-weight: 400;

}

li{
  list-style: none;
}

.packages{
  margin-top: 2rem;
}

.gallery {
  max-width: 1000px;
  margin: 0 auto;
  padding: 20px 0; 
}

.row {
  display: flex;
  flex-wrap: wrap; 
  gap: 4px;
}

.gimg{
  border-radius: 5px;
}

.column {
  flex-basis: calc(33.33% - 8px);
  margin-right: 8px;
  border-radius: 30px;
}

.column:last-child {
  margin-right: 0; 
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
}

@media screen and (max-width: 800px) {
  .column {
      flex-basis: calc(50% - 8px); 
  }
}

@media screen and (max-width: 600px) {
  .column {
      flex-basis: 100%; 
      margin-right: 0; 
  }
}


.gallerytext {
  text-align: left;
  font-size: 2rem;
  font-weight: bolder;
}
</style>

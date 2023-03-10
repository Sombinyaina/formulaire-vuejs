<template>
  <div class="content">
    <div class="card">
      <button class="x">x</button>
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ipsa in,
        tempore magni quibusdam aliquam perferendis dolore natus repudiandae
        dolorem sunt temporibus veritatis et nulla harum! Ipsam unde
        perspiciatis consequuntur ratione!
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "ModalForm"
};
</script>
<style>
.content {
  display: flex;
  position: absolute;
  background-color: black;
  opacity: 75%;
  width: 100vw;
  height: 100vh;
  top: 0;
  align-items: center;
}
.x {
  position: absolute;
  right: 10px;
  top: 10px;
  width: 20px;
}

.card {
    position: relative;
  background-color: antiquewhite;
  margin: 0 auto;
  width: 500px;
  align-content: center;
  border: solid 1px black;
  border-radius: 10px;
  padding: 30px;
}
</style>

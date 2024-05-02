<template>
  <section>
    <div class="container">
      <USectionTitle title="Contact Us" sub-title="Let's talk"/>
      <form action="#">
         <div class="form-row">
            <div class="input-data">
               <input type="text" required>
               <div class="underline"></div>
               <label for="">Your Name</label>
            </div>
            <div class="input-data">
               <input type="text" required>
               <div class="underline"></div>
               <label for="">Your Email</label>
            </div>
         </div>
         <div class="form-row">
            <div class="input-data">
               <input type="text" required>
               <div class="underline"></div>
               <label for="">Your Phone</label>
            </div>
            <div class="input-data">
               <input type="text" required>
               <div class="underline"></div>
               <label for="">Your Subject</label>
            </div>
         </div>
         <div class="form-row">
         <div class="input-data textarea">
            <textarea rows="8" cols="80" required></textarea>
            <br />
            <div class="underline"></div>
            <label for="">Your Message</label>
            <br />
            <UButton :title="'Отправить'"/>
          </div>
          </div>
      </form>
      </div>
  </section>
</template>

<script setup lang="ts">
import USectionTitle from '@/ui/USectionTitle.vue'
import UButton from '@/ui/UButton.vue'
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,700&display=swap');

section {
    position: relative;
    z-index: 1;
    background: #fff url(../../public/images/contactUsBg.png) no-repeat fixed center;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
}

* {
  margin: 0;
  padding: 0;
  outline: none;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body{
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  padding: 10px;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(115deg, #56d8e4 10%, #9f01ea 90%);
}

.container{
  max-width: 800px;
  background: #fff;
  width: 800px;
  padding: 25px 40px 10px 40px;
  margin: 0 auto;
}

.container .text{
  text-align: center;
  font-size: 41px;
  font-weight: 600;
  font-family: 'Poppins', sans-serif;
  background: -webkit-linear-gradient(right, #56d8e4, #9f01ea, #56d8e4, #9f01ea);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.container form{
  padding: 30px 0 0 0;
}

.container form .form-row{
  display: flex;
  margin: 32px 0;
}

form .form-row .input-data{
  width: 100%;
  height: 40px;
  margin: 0 20px;
  position: relative;
}

form .form-row .textarea{
  height: 70px;
}

.input-data input,
.textarea textarea{
  display: block;
  width: 100%;
  height: 100%;
  border: none;
  font-size: 17px;
  border-bottom: 2px solid rgba(0,0,0, 0.12);
}

.input-data input:focus ~ label, .textarea textarea:focus ~ label,
.input-data input:valid ~ label, .textarea textarea:valid ~ label{
  transform: translateY(-20px);
  font-size: 14px;
  color: #3498db;
}

.textarea textarea{
  resize: none;
  padding-top: 10px;
}

.input-data label{
  position: absolute;
  pointer-events: none;
  bottom: 10px;
  font-size: 16px;
  transition: all 0.3s ease;
}

.textarea label{
  width: 100%;
  bottom: 40px;
  background: #fff;
}

.input-data .underline{
  position: absolute;
  bottom: 0;
  height: 2px;
  width: 100%;
}

.input-data .underline:before{
  position: absolute;
  content: "";
  height: 2px;
  width: 100%;
  background: #3498db;
  transform: scaleX(0);
  transform-origin: center;
  transition: transform 0.3s ease;
}

.input-data input:focus ~ .underline:before,
.input-data input:valid ~ .underline:before,
.textarea textarea:focus ~ .underline:before,
.textarea textarea:valid ~ .underline:before{
  transform: scale(1);
}

@media (max-width: 700px) {
  .container .text{
    font-size: 30px;
  }
  .container form{
    padding: 10px 0 0 0;
  }
  .container form .form-row{
    display: block;
  }
  form .form-row .input-data{
    margin: 35px 0!important;
  }
  .submit-btn .input-data{
    width: 40%!important;
  }
}
</style>
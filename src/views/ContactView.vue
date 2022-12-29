<template>
  <div class="contactContainer">
    <div class="contactText">
      <h2>Адрес</h2>
      <p>Официальные запросы и письма можно направлять по адресу 220051, г.Минск, ул. Слободская, 115</p>
      <p>Контактные номера</p>
      <p>+375 29 663-09-66</p>
      <p>+375 25 681-84-75</p>
      <p>emailfcsparta2021@gmail.com</p>
      <textarea class="textareaContact"></textarea>
      <button class="btn btn-success" @click="DialogShow">Написать нам</button>
    </div>
    <div>
      <div>
            <img src="/img/children-cup.png" alt="coach">
      </div>   
    </div>
  </div>
  <div class="map">
    <div class="container">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2353.3510518659687!2d27.433945315709998!3d53.85440528008862!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46dbdbcadfca4a6d%3A0xcb49ce4caa3e48b0!2z0KTRg9GC0LHQvtC70YzQvdCw0Y8g0YjQutC-0LvQsCDQodC_0LDRgNGC0LA!5e0!3m2!1sru!2sby!4v1672253562549!5m2!1sru!2sby" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
  </div>
    <MyDialog class="dialogWindow" v-model:show="DialogVisible">
    <div>
      <p>Login</p>
      <FormInput v-model:modelValue="ContactAddr"/>
    </div>
    <div>
      <p>Password</p>
      <FormInput v-model:modelValue="ContactAddr1"/>
    </div>
      <FormButton nameValue="SingUp" @click="SendData"/>
  </MyDialog>
</template>

<script>
import{ref} from "vue";
export default{
  name: "HomeView", 
  setup(){
    const DialogVisible = ref(false);
    const ContactAddr = ref('');
    const ContactAddr1 = ref('');
    const DialogShow = () => {
      DialogVisible.value = true;
    };
    const SendData = () => {
      console.log(ContactAddr.value);
      console.log(ContactAddr1.value);
    }
    return{
      DialogVisible,
      ContactAddr,
      ContactAddr1,
      DialogShow,
      SendData
    }
  }
}
</script>
  
<style scoped>
  p{
    margin-bottom: 5px;
  }
  img{
        width: 500px;
    }
  
  .map {
    padding: 40px 0;
    text-align: center;
  }

  .container {
    max-width: 1000px;
  }
</style>
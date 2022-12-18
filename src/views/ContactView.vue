<template>
  <div class="contactContainer">
    <div class="contactText">
      <h2>Адрес</h2>
      <p>Официальные запросы и письма можно направлять по адресу 220013, г.Минск, ул. Я.Коласа, 32а</p>
      <p>Контактные номера</p>
      <p>+375 29 663-09-66</p>
      <p>+375 25 681-84-75</p>
      <p>Emailfcsparta2021@gmail.com</p>
      <textarea class="textareaContact"></textarea>
      <button class="btn btn-success" @click="DialogShow">Написать нам</button>
    </div>
    <div>
      <div>
            <img src="/img/children-cup.png" alt="coach">
      </div>   
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
</style>
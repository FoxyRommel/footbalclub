<template>
  <div class="header">
    <div class="pages-name">
      <nav>
        <router-link to="/">Главная</router-link> | 
        <router-link to="/about">О нас</router-link> |
        <router-link to="/coach">Тренеры</router-link> |
        <router-link to="/contact">Контакты</router-link>
      </nav>
      <div class="menu-phone">
        +375256465196
      </div>
      <div class="menu-links">
        <ul>
          <li>
            <a href="https://github.com/FoxyRommel/footbalclub.git">
              <img src="/svg/vkontakte_kpokrqfsqn1o_32.png" alt="github">
            </a>
          </li>
          <li>
            <a href="https://github.com/FoxyRommel/footbalclub.git">
              <img src="/svg/facebook_4zke2svviczk_32.png" alt="github">
            </a>
          </li>
          <li>
            <a href="https://github.com/FoxyRommel/footbalclub.git">
              <img src="/svg/logotip_instagram_vtyznosn9smg_32.png" alt="github">
            </a>
          </li>
        </ul>
      </div>
    </div>
    <div class="enter">
      <button class="btn btn-success" @click="DialogShow">Войти</button>
    </div>
    <MyDialog class="dialogWindow" v-model:show="DialogVisible">
    <div class="login">
      <p>Login</p>
      <FormInput v-model:modelValue="ContactAddr"/>
    </div>
    <div>
      <p class="password">Password</p>
      <FormInput v-model:modelValue="ContactAddr1"/>
    </div>
      <FormButton nameValue="SingUp" @click="SendData"/>
  </MyDialog>
  </div>  
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
.login{
    margin: 5px;
  }
.password{
    margin: 5px;
  }
</style>
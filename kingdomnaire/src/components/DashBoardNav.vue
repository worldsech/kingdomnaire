<template>
    <div class="">
      <div class="vertical-nav bg-blue-950 text-gray-100 text-xl font-bold">
        WHO WANT'S TO BE A RABBI
      </div>
  
     <div class="settings-nav text-gray-100">
      <nav class="horizontal-nav bg-blue-800 -ml-2">
        <p class="nav-title">DashBoard</p>
      <router-link class="router h-10 font-bold items-center hover:bg-gray-400 hover:text-blue-900" to="/dashboard/panel" >Control Panel</router-link>
      <router-link class="router h-10 font-bold items-center hover:bg-gray-400 hover:text-blue-900" to="/dashboard/question" >Add Question</router-link>
      <router-link class="router h-10 font-bold items-center hover:bg-gray-400 hover:text-blue-900" to="/dashboard/message" >Message</router-link>
      
        <p class="nav-title">Game</p>
      <router-link class="router h-10 font-bold items-center hover:bg-gray-400 hover:text-blue-900" to="/dashboard/fastest" >Fastest Finger</router-link>
    </nav>
    <div class="content"><slot /></div>
     </div>
      </div>
    </template>
  
  <script>
  export default {
      name: 'DashBoardNav',
  }
  </script>
    
    <style scoped>
  .logo{
    width: 40px;
  }
  .content{
    position: relative;
  }
  .vertical-nav{
    display: flex;
    justify-content: space-between;
    padding: 10px;
    align-items: center;
    height: 10vh;
  }
  .router-link-active {
  background-color: #f7fafc; /* Gray 300 */
  color: #2b6cb0; /* Blue 700 */
}
  .horizontal-nav{
    padding: 2%;
    height: 90vh;
  }
  
  .close-icon:hover{
    transform: scale(.9);
  }
  
  .settings-nav{
    display: grid;
    position: relative;
    grid-template-columns: 200px 1fr;
    gap: 10px;
    padding: 0 5px;
  }
  
  .settings-nav.admin{
    grid-template-columns:auto;
  }
  
  .nav-title{
    font-size: 20px;
    font-weight: bold;
    opacity: .9;
    padding: 10px;
  }
  
  .router{
    display: flex;
    text-decoration: none;
    font-size: 14px;
    border-radius: 10px;
    padding: 10px;
  }

  @media screen and (max-width:600px) {
    .settings-nav{
      grid-template-columns:  1fr !important;
    }
    
  }
  
    </style>
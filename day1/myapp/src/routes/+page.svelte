<main>
  <div class="container-main">
      <img src={OIP} alt="asf">
      <div class="overlay">
        <p class="id_1">TellYourSelf</p>
        <p class="id_2">"나만의 상태메시지"</p>
        <PrimaryButton name="만들러 가기" url="https://www.naver.com" on:multiplyclick={aa}/></div>
  </div>
</main>

<script>
  // @ts-nocheck
  import OIP from '$lib/images/OIP.jpg'
  import { goto } from '$app/navigation';
  import PrimaryButton from './PrimaryButton.svelte'
  

  let a = 2;
  $: b = a * a

  function aa(event) {
      console.log(a + " + " + b + " = " + a + b)
      goto(event.detail.uri);
  }
 
</script>

<style>
  img {
      width: 100%;
      height: auto;
      display: block;
    }
    
  .overlay {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
    }
  .id_1 {
    color: white;
    font-size: 2.4em;
    font-weight: bold;
    color: white;
    
  }
  
  .id_2 {
    color: white;
    font-size: 1.1em;
    font-weight: bold;
    color: white;
    margin-top: -30px;
    margin-bottom: 30px;
  }
</style>



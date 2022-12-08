<template>
  <dialog open onclick="{(event) => {
    if(event.currentTarget === event.target){
      event.currentTarget.close();
    } }}">
  <p>Greetings, one and all!</p>
  <form method="dialog">
    <button>OK</button>
  </form>
  </dialog>
</template>
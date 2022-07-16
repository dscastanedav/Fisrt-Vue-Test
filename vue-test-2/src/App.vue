
<template>
  <div>{{greet}} {{name}}</div>
  <div v-html="channel"></div>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 v-bind:style="{
    color: colorTexto,
    fontSize: tamanoTexto + 'px',
    padding: '20px'
  }">Linea de prueba</h2>
  <h2 :style="headerStyleObject">Styled Object</h2>
  <h2 :style="[succesStyleObject, headerStyleObject]">Array Styled Object</h2>
  <h2 :style="[succesStyleObject, dangerStyleObject]">Danger Styled Object</h2>
  <h2 :id="headingId">This is a Heading</h2>

</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'Davy Jem',
      greet: 'Hellow',
      channel: '<b>Codeevolution</b>',
      isDisabled: false,
      colorTexto: 'purple',
      tamanoTexto: 50,
      headerStyleObject: {
        color: 'blue',
        fontSize: '70px',
        padding: '10px'
      },
      succesStyleObject: {
        backgroundColor: 'pink',
        font: 'arial',
        border: '10px solid grey'
      },
      dangerStyleObject: {
      backgroundColor: 'magenta',
      fontFamily: 'Lucida Handwriting, cursive',
      border: '20px solid darkblue',
      padding: '150px'
      },
      headingId: 'heading'
     
    };
  },
 
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

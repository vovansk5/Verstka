<template>
  <div class="mainDiv">
      <div id="mainMenu">
        <ul>
            <li>
                <a href="#">Home</a>
            </li>
            <li>
                <a href="#">Galery</a>
            </li>
            <li>
                <a href="#">Members</a>
            </li>
            <li>
                <a href="#">Logout</a>
            </li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
  name: 'MyComp',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  #mainMenu {
    background: url("../../images/logo.png") no-repeat 12% 50%, linear-gradient(180deg, #fff,rgb(189, 186, 186));
    height:100px;
    border: solid black 1px;
    padding: 0px;
    margin: 0px;
  }
  a {
    text-decoration: none;
    color:grey;
  }

  ul {
    float:right
  }

  li {
    display: inline-block;
    list-style: none;
    width: 120px;

  }
</style>

<script>
import Header from "../components/Header.svelte";
let keywordSrc = "assets/Keyword.png";
let relationSrc = "assets/Relation.png";
let linkSrc = "assets/Link.png";
</script>

<Header navLoc=""/>
<div class="screen">
<div class="menu"></div>
<div class="index-bar"></div>
<div class="tool-nav">
  <div class="tool-bar">
    <div class="keyword"><img src={keywordSrc} alt=","></div>
    <div class="relation"><img src={relationSrc} alt=","></div>
    <div class="link"><img src={linkSrc} alt=","></div>
  </div>
</div>
</div>


<style>
.screen {
  position: absolute;
  width: 1140px;
  height: 750px;
  left: 150px;
  top: 200px;
  border: 1px solid;
}
.menu {
  position: absolute;
  width: 1140px;
  height: 70px;
  left: 0px;
  top: 0px;
  border-bottom: 1px solid;
}
.index-bar {
  position: absolute;
  width: 50px;
  height: 680px;
  left: 0px;
  top: 70px;
  border-right: 1px solid;
}
.tool-nav {
  position: absolute;
  width: 180px;
  height: 40px;
  left: 940px;
  top: 75px;
}
.tool-bar {
  position: absolute;
  left: 0%;
  right: 0%;
  top: 0%;
  bottom: 0%;

  background: #FFFFFF;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 20px;
}
.keyword {		
  position: absolute;
  left: 16.67%;
  right: 66.67%;
  top: 12.5%;
  bottom: 12.5%;
}
.relation {
  position: absolute;
  left: 41.67%;
  right: 41.67%;
  top: 12.5%;
  bottom: 12.5%;
}
.link {
  position: absolute;
  left: 66.67%;
  right: 16.67%;
  top: 12.5%;
  bottom: 12.5%;
}
</style>

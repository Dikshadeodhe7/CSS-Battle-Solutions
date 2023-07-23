Solution 1
<div class="half-circle left"></div>
<div class="half-circle center"></div>
<div class="half-circle right"></div>
<style>
      * {margin: 0;}
      body{
          background-color: #F5D6B4;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-top: 50px;
      }
      .half-circle{
          width: 100px;
          height: 50px;
          box-sizing: border-box;
          border: 20px solid #D86F45;
          box-sizing: border-box;
          border-bottom-left-radius: 100px;
          border-bottom-right-radius: 100px;
          border-top:0;
          position: relative;
      }
      .half-circle.center {
         transform: scale(-1);
         margin: 0 -20px 99px -20px;
      }
      .half-circle.left::after,
      .half-circle.right::after {
          content: "";
          position: absolute;
          width: 20px;
          height: 10px;
          background-color: #D86F45;
          border-top-left-radius: 10px;
          border-top-right-radius: 10px;
      }
      .half-circle.left::after {
          left: -20px;
          top: -10px;
      }
      .half-circle.right::after {
          top: -10px;
          right: -20px;
      }  
</style>

Solution 2
<div id="l"></div> 
<div id="c"></div> 
<div id="r"></div> 

<style>
  *{ background: #F5D6B4; position: fixed; } 
  #l,#r,#c { 
      width:60px; 
      height:30px; 
      border: 20px solid #D86F45; 
  } 
  #l,#r { 
      border-radius: 0 0 50px 50px; 
      border-top:0; 
  } 
  #l{ 
      margin: 142px 0 0 62px; 
  } 
  #r{
      margin: 142px 0 0 222px; 
  } 
  #c{ 
      border-radius: 50px 50px 0 0; 
      border-bottom:0; 
      margin:92px 0 0 142px; 
  } 
  #l:before, #r:after{ 
      content: ""; 
      width: 20px; 
      height: 10px; 
    position: absolute; 
    background: #D86F45; 
    border-radius: 20px 20px 0 0; 
    top: -10px;
  } 
  #l:before{ 
    left: -20px; 
  } 
  #r:after{ 
    left: 60px; 
  } 
</style>

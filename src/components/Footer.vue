<template>
  <body>
    <div id="page-container">
      <div id="content-wrap">
        
      </div>
    <footer id="footer">
      <div id='content-left'>
          <span>@2022 Christian Rhodes</span>
      </div>
      <div id='content-right'>
        <div class="footer-social-links">
            <a href="https://github.com/christianrhodes18" title="Github" target="_blank"><i class="fa fa-github"></i></a>
            <a href="https://twitter.com/chrisrhodesy" title="Twitter" target="_blank"><i class="fa fa-twitter"></i></a>
        </div>
      </div>
    </footer>
    </div>
  </body>

</template> 

<script>
  export default { }
</script>

<style scoped>
#page-container {
  position: relative;
  column-count: 2;
  column-width: 80vh;
  /* min-height: 60vh; */
}

/*#content-wrap {
  padding-bottom: 5.5rem;    /* Footer height 
} */

#footer {
  position: absolute;
  min-height: 5vh;
  column-count: 2;
  /* bottom: 0; */
  width: 100%;
  height: 2.5rem;            /* Footer height */
  color: white;
}
body {
  width: 100%;
}




#content-left {
    font-size: 20px;
    padding-top: 10px;
}
#content-right {
  padding-top: 10px;

}

/* Social Links */
@import url("//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css");

body { background-color: #eee; }

.footer-social-links{
    font-size: 20px;
    text-align: center;
    /* margin-top: 20%; */
}
.footer-social-links a{
    width: 25px;
    height: 25px;
    line-height: 25px !important;
    position: relative;
    margin: 0 5px;
    text-align: center;
    display: inline-block;
    color: #111;
    
    -webkit-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000);  
    -moz-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000); 
    -o-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000);
    -ms-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000); 
    transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000);
}
.footer-social-links a i,
.footer-social-links a span{
    position: relative;
    top: 2px;
    left: 1px; 
}
.footer-social-links a:before{
    content: "";
    display: inline-block;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    border: 1px solid #111;
    
    -webkit-border-radius: 2px;
    -moz-border-radius: 2px;
    border-radius: 2px;
    
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
    
    -webkit-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000);  
    -moz-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000); 
    -o-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000);
    -ms-transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000); 
    transition: all 0.27s cubic-bezier(0.300, 0.100, 0.580, 1.000);
    
}
.footer-social-links a:hover{
    color: #fff;
}
.footer-social-links a:hover:before{
    background: #111;
} 

/* Media Queries */ 
/* @media (max-width: 980px){
   
} */
</style>
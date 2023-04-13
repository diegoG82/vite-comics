<script>
export default{
    name:"appFooter"
}
</script>

<template>
 <div class="footer">
   <div class="top-footer flex">
    <div class="footer-list flex"></div>
    <div class="footer-logo flex"><img src="../img/dc-logo-bg.png" alt=""></div>
   </div>
   <div class="bottom-footer"></div>
 </div>
</template>


<style scoped lang="scss">

.footer-list{
    width:50%;
}
.footer-logo{
    width: 50%;
    justify-content: center;
  
}


.top-footer{
    background: url(../img/footer-bg.jpg);
    background-size: cover;
    height: 700px;
   
}
.bottom-footer{
    height:100px;
    background-color:darkgrey;
}

</style>
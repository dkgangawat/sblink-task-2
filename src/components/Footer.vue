<template>
    <div class="footer">
        <div class="footer-content">
          <p>2021-2022 © Course Pro Private Limited</p>
        <div class="policys">
            <a href="#">Term & Condition</a>
            <a href="#">Privacy Policy</a>
        </div>  
        </div>
        
    </div>
</template>

<script>
export default{
    name:"Footer",
}
</script>
<style>
.footer{
  width: 100%;
  height: 80px;

}
.footer-content{
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: auto;
    padding: 15px;
    color: #1F2532;
    font-weight: 700;
}
.policys{
    display: flex;
    gap: 20px;
}
</style>
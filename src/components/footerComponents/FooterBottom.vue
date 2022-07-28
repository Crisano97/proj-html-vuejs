<template>
  <div class="footer-bottom">
      <div class="copyright">
        <span>
           @ Copyright 2012 - 2020
        </span>
        <span> | Avada Theme by Theme fusion</span>
        <span> | all Rights Reserved</span>
        <span>|Powered by Wordpress</span>
      </div>
      <div class="return-top">
        <a href="#header">
          <i class="fa-solid fa-angle-up"></i>
        </a>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">

  @import "../../styles/general.scss"; 


    div.footer-bottom{
      height: 10vh;
      background-color: $grayBgColor;
      position: relative;
      display: flex;
      align-items: center;

      div.copyright{
        padding-left: 1.5rem;
        
        font-size: .7rem;
        color: gray;
      }

      div.return-top{
        width: 3rem;
        height: 2rem;
        background-color: $arrowButtonColor;
        position: absolute;
        bottom: 0;
        right: 5rem;
        text-align: center;
        line-height: 2rem;
        cursor: pointer;

        a{
          text-decoration: none;
          color: white;
        }
      }
    }
</style>
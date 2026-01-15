<template>
    <div class="footer">
      <div class="footer_inner">
        <div class="footer_inner__aboutme">
          <h4>About Me</h4>
          <p class="footer_inner__para">
            We have tested a number of registry fix and clean utilities and present our top 3 list on our site for your
            convenience.
          </p>
          <p>
            Copyright ©2026 All rights reserved | This template is made with
            <a href="https://colorlib.com" target="_blank" class="footer_inner__link">Colorlib</a>
          </p>
        </div>
        <div class="footer_inner__newsletter">
          <h3>Newsletter</h3>
          <p>Stay updated with our latest trends</p>
          <div class="footer_inner__newsletter-input">
            <input type="text" placeholder="Enter Email Address" />
            <button>&rarr;</button>
          </div>
        </div>
        <div class="footer_inner__followme">
          <h3>Follow Me</h3>
          <p>Let us be social</p>
          <div class="footer_inner__icons">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-dribbble"></i></a>
            <a href="#"><i class="fab fa-behance"></i></a>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style lang="scss">
  @import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
  
  $footer_bg: #04091e;
  $footer_color: white;
  $footer_link_color: #6c63ff;
  $footer_input_bg: #f5f5ff;
  $footer_input_color: #333;
  $footer_button_bg: #6c63ff;
  $footer_button_color: white;
  
  
  
  .footer {
    background-color: $footer_bg;
    color: $footer_color;
    padding: 50px 50px 50px 250px;
    // margin-top: auto;
    height: 300px;
    

  
    &_inner {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 30px;
      
  
      &__aboutme,
      &__newsletter,
      &__followme {
        font-size: 16px;
        font-family: sans-serif;
        display: flex;
        flex-direction: column;
        gap: 10px;
        
        h3,
        h4 {
          font-size: 20px;
          font-weight: bold;
          margin-bottom: 10px;
        }
  
        p {
          font-size: 14px;
          line-height: 1.5;
        }
  
        &__link {
          color: $footer_link_color;
          text-decoration: none;
  
          &:hover {
            text-decoration: underline;
          }
        }
      }
  
      &__newsletter-input {
        display: flex;
        gap: 10px;
  
        input {
          flex: 1;
          padding: 10px;
          border: none;
          border-radius: 5px;
          background-color: $footer_input_bg;
          color: $footer_input_color;
          font-size: 14px;
        }
  
        button {
          padding: 10px 20px;
          border: none;
          border-radius: 5px;
          background-color: $footer_button_bg;
          color: $footer_button_color;
          font-size: 16px;
          cursor: pointer;
  
          &:hover {
            background-color: darken($footer_button_bg, 10%);
          }
        }
      }
  
      &__icons {
        display: flex;
        gap: 15px;
  
        a {
          color: $footer_color;
          font-size: 18px;
          text-decoration: none;
  
          &:hover {
            color: $footer_link_color;
          }
        }
      }
    }
  }
  </style>
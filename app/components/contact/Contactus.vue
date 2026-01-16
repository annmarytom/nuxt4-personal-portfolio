<template>

    <section class="contact-section">
        <div class="contact-section__map">
          <!-- Google Maps Embed -->
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3151.835434509374!2d144.9537353153168!3d-37.81627974202198!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6ad642af0f11fd81%3A0xf577f3c3e4c0b9b!2sFederation%20Square!5e0!3m2!1sen!2sau!4v1634567890123!5m2!1sen!2sau"
            width="100%"
            height="400"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
    
        <div class="contact-section__content container">
          <div class="contact-section__info">
            <div class="info-item">
              <i class="fas fa-map-marker-alt"></i>
              <div>
                <h4>Binghamton, New York</h4>
                <p>4343 Hinkle Deegan Lake Road</p>
              </div>
            </div>
            <div class="info-item">
              <i class="fas fa-phone-alt"></i>
              <div>
                <h4>00 (958) 9865 562</h4>
                <p>Mon to Fri 9am to 6pm</p>
              </div>
            </div>
            <div class="info-item">
              <i class="fas fa-envelope"></i>
              <div>
                <h4>support@colorlib.com</h4>
                <p>Send us your query anytime!</p>
              </div>
            </div>
          </div>
    
          <div class="contact-section__form">
            <form>
              <div class="form-group">
                <input type="text" placeholder="Enter your name" />
                <input type="email" placeholder="Enter email address" />
              </div>
              <div class="form-group">
                <input type="text" placeholder="Enter subject" />
                <textarea placeholder="Enter message"></textarea>
              </div>
              <button type="submit" class="btn-submit">Send Message</button>
            </form>
          </div>
        </div>
      </section>
    
    </template>
    
    <script setup>
   
    </script>
    
    <style lang="scss" scoped>
    
    
    .contact-section {
    background-color: #f9f9f9;
    padding: 50px 20px;
    
    &__map {
      margin-bottom: 30px;
      iframe {
        border: none;
        border-radius: 8px;
      }
    }
    
    &__content {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: space-between;
    }
    
    &__info {
      flex: 1;
      min-width: 300px;
    
      .info-item {
        display: flex;
        align-items: flex-start;
        margin-bottom: 20px;
    
        i {
          font-size: 24px;
          color: #6c63ff;
          margin-right: 15px;
        }
    
        h4 {
          font-size: 18px;
          font-weight: bold;
          margin: 0;
          color: #333;
        }
    
        p {
          font-size: 14px;
          color: #666;
          margin: 5px 0 0;
        }
      }
    }
    
    &__form {
      flex: 1;
      min-width: 300px;
    
      form {
        display: flex;
        flex-direction: column;
        gap: 20px;
    
        .form-group {
          display: flex;
          flex-wrap: wrap;
          gap: 20px;
    
          input,
          textarea {
            flex: 1;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 14px;
            color: #333;
          }
    
          textarea {
            resize: none;
            height: 100px;
          }
        }
    
        .btn-submit {
          background-color: #6c63ff;
          color: white;
          padding: 10px 20px;
          border: none;
          border-radius: 5px;
          font-size: 16px;
          cursor: pointer;
          align-self: flex-start;
    
          &:hover {
            background-color: #5a54d1;
          }
        }
      }
    }
    }
    </style>
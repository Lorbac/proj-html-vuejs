<template>
    <section id="newsletter">
          <div class="container">
              <h2>Subscribe To My Newsletter</h2>
              <p>BE NOTIFIED ABOUT BOOK SIGNING TOUR DATES</p>
              <div class="InsertMail">
                  <input type="text" placeholder="Insert your email...*">
                  <button>Subscribe</button>
              </div>
              <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt</p>
          </div>
    </section>
</template>

<script>
export default {
    name: "Newsletter",
}
</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';

    #newsletter {
        background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.9) 100%), url("../assets/images/banner-2.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        background-position: top;

        .container {
            width: 20%;
            text-align: center;
            margin: 0 auto;
            padding: 80px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;

            h2 {
                font-family: none;
                font-size: 40px;
                color: $white;
            }

            p:nth-child(2) {
                color: $saffron;
                width: 130%;
                letter-spacing: 2px;
                margin: 20px 0;
            }

            .InsertMail {
                margin-top: 10px;
                display: flex;
                align-items: center;
                
                input[type=text] {
                    padding: 14px 40px;
                    border-radius: 5px;
                    margin-right: 20px;
                }

                button {
                    background-color: $keppel;
                    border: none;
                    padding: 11px 35px;
                    color: $white;
                    border-radius: 5px;
                    font-size: 18px;
                    cursor: pointer;
                    transition: 0.1s ease-out;

                    &:hover {
                        transition: 0.1s linear;
                        background-color: $blueLagoon;
                    }
                }
                
            }
            
            p:nth-child(4) {
                width: 120%;
                color: $osloGray;
                font-size: 17px;
                margin: 30px 0;
                line-height: 30px;
            }
        }
    }
</style>
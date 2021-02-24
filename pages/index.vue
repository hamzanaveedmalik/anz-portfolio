<template>
  <div>
    <div
      class="hero container-inner mx-auto flex flex-col sm:flex-row justify-between py-16"
    >
      <div class="text-4xl font-bold w-full sm:w-3/5 text-center sm:text-left" :class="theme">
        <div class="leading-tight">Anza Khalid</div>
        <div class="flex flex-row items-center mt-1 work" :class="theme">
          <div class="leading-snug text-lg py-4">
            Technical Editor @
          </div>
          <div :class="theme"> 
            <a v-if="theme === 'theme-light'" href="https://www.i2cinc.com/" target="_blank">
              <img
                src="~/assets/img/i2c-logo.png"
                alt="logo"
                class="w-12 h-8 ml-2"
              />
            </a>
            <a v-else href="https://www.i2cinc.com/" target="_blank">
              <img
                src="~/assets/img/i2c-logo.png"
                alt="logo"
                class="w-12 h-8 ml-2"
              />
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="overflow-x-hidden">
      <div
        class="projects container-inner mx-auto text-xl border-t border-gray-500 border-b py-10 mb-16 relative"
      >
        <h2 class="font-bold mb-6 interest-mobile" id="projects">
          Here are some of my interests:
        </h2>

        <div
          class="absolute right-0"
          style="top: 50px; transform: translate(100%) rotate(180deg)"
        >
          <svg width="170px" height="170px">
            <use xlink:href="#dots-triangle" />
          </svg>
        </div>
           <div class="interests-container interest-container-mobile"> 
             <div class="interests product-communications">
                <h1> Product Communications </h1>
                <img 
                  src="~/assets/illustrations/product-communications.svg" 
                  width="100px" 
                  height="100px"
                  class="illustration"
                />
             </div>
             <div class="interests design">
               <h1>Design</h1>
                <img 
                  src="~/assets/illustrations/designs.svg" 
                  width="140px" 
                  height="140px"
                  class="illustration"
                />
             </div>
             <div class="interests photography">
               <h1>Photography</h1>
                  <img 
                  src="~/assets/illustrations/photography.svg" 
                  width="140px" 
                  height="140px"
                  class="illustration"
                />
             </div>
           </div>
      </div>
      <!-- end projects -->

    </div>
    <div class="overflow-x-hidden border-gray-200 border-b">
      <div
        class="get-to-know-me container-inner mx-auto text-xl pb-16 relative"
      >
        <h2 class="font-bold mb-6 know-me" id="about">Get to know me:</h2>

        <div
          class="absolute left-0"
          style="top: 50px; transform: translateX(-100%)"
        >
          <svg width="170px" height="170px">
            <use xlink:href="#dots-triangle" />
          </svg>
        </div>

        <div
          class="flex flex-col sm:flex-row justify-between items-center mb-16"
        >
          <div>
            <img
              src="~assets/img/anza-avatar.png"
              alt="avatar"
              class="w-24 h-32 rounded-full mb-8 lg:mb-0"
            />
          </div>
          <div class="flex-1 text-xl sm:text-xl ml-6">
            I'm a Technical Editor based in London. I black box complex technical jargon to simpler, easier to understand documentation. A hobbyist photographer who is always up for a good conversation as long as there's orange 🍊 / pineapple 🍍 juice on the table.
          </div>
        </div>
      </div>
      <!-- end get-to-know me -->
    </div>

    <div class="overflow-x-hidden">
      <div class="contact-me bg-background-secondary pt-16">
        <div class="container-inner mx-auto text-xl pb-4 relative">
          <h2 class="font-bold mb-6" id="contact">Get in touch!</h2>

          <div
            class="absolute right-0 top-0"
            style="transform: translate(100%) rotate(180deg)"
          >
            <svg width="170px" height="170px">
              <use xlink:href="#dots-triangle" />
            </svg>
          </div>

          <div class="text-lg sm:text-lg mb-16">
            <form
              id="my-form"
              action="https://formspree.io/f/xrgodpeo"
              method="POST"
              class="mb-12"
            >
              <div class="flex flex-wrap mb-6 -mx-4">
                <div class="w-full md:w-1/2 mb-6 md:mb-0 px-4">
                  <label class="block mb-2 text-copy-primary" for="name">
                    Name
                  </label>
                  <input
                    type="text"
                    name="name"
                    id="name"
                    placeholder="Your Name"
                    class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-green-700 mb-2 p-4"
                    required
                  />
                </div>
                <div class="w-full px-4 md:w-1/2">
                  <label class="block text-copy-primary mb-2" for="email">
                    Email Address
                  </label>
                  <input
                    type="email"
                    name="email"
                    id="email"
                    placeholder="youremail@example.com"
                    class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-green-700 mb-2 p-4"
                    required
                  />
                </div>
              </div>

              <div class="w-full mb-12">
                <label class="block text-copy-primary mb-2" for="message">
                  Message
                </label>

                <textarea
                  id="message"
                  rows="5"
                  name="message"
                  class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none appearance-none focus:border-green-700 mb-2 px-4 py-4"
                  placeholder="Enter your message here."
                  required
                ></textarea>
              </div>

              <div class="flex justify-end w-full">
                <input
                  type="submit"
                  value="Send"
                  class="block submit-btn text-white text-sm font-semibold tracking-wide uppercase shadow rounded cursor-pointer px-6 py-3"
                />
              </div>
            </form>
          </div>
        </div>
      </div>
      <!-- end contact-me -->
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.theme = localStorage.getItem("theme") || "theme-light";
  },
  data() {
    return {
      theme: "",
    };
  },
};
</script>

<style scoped>
.leading-snug {
  color:#6D214F;
}

.submit-btn {
  background-color: #6D214F;
}

 .submit-btn:hover  {
  background-color: #4e1136;

 }

 .interests-container {
   display:flex;
   flex-direction: row;

   margin: 10px;
   padding-left: 10px;
   margin-right:10px;
 }

 .interests {
   width: 230px;
   height:230px;
   border-radius:10px;
   background-color: grey;
   margin: 10px;
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
   transition: transform 0.5s;

 }
 
 .illustration {
   margin-left: 20%;
   margin-top: 25px;
 }

.interests:hover {
  transform: scale(1.1);
}
 .product-communications {
   background-image: linear-gradient(320deg, #0071ff, #9d00ff);
   color: white;
   font-weight: bold;
   text-align: center;
   padding-top: 30px;
   border-color: #ea8685;
 }

 .design {
  background-image: linear-gradient(320deg, #f8a5c2, #ee588c); 
  color: white;
  font-weight: bold;
  text-align: center;
  padding-top: 30px;
  border-color: #ea8685;

 }

 .photography {
    background-image: linear-gradient(320deg, #f5dead, #ffb71d); 
    color: white;
    font-weight: bold;
    text-align: center;
    padding-top: 30px;
    border-color: #ea8685;
 }

 .find-more-btn {
   width: 80px;
   height: 50px;
   background-color: rgb(202, 103, 46);
   border-radius: 5px;
   color: #000;
   font-size: 1.2rem;
   font-weight:400;
 }

@media (max-width: 640px) {
  .work {
    margin-left: 23% !important;
  }
  
  .interest-mobile {
    margin-left: 15%;
    margin-right: 15%;
  }

  .interest-container-mobile {
    display:flex;
    flex-direction: column;
    margin-left: 15%;
    margin-right: 15%;
  }

  .product-communications {
    margin-bottom: 10px;
  }

  .design {
    margin-bottom: 10px;
  }

  .photography {
    margin-bottom: 10px;
  }

  .know-me {
    margin-left: 9%;
    margin-right: 15%;
  }
}
</style>
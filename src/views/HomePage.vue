<template>
  <section>
    <div class="row text-start justify-content-center">
      <div class="col-8">
        <div class="row">
          <div class="col-12 mb-3 text-center">
            <h2 class="fw-semibold">Information About Me</h2>
          </div>
          <div class="col-12">
            <div class="accordion" id="accordionExample">
              <div class="accordion-item">
                <h2 class="accordion-header">
                  <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                    Introduce who iam
                  </button>
                </h2>
                <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
                  <div class="accordion-body">
                    <p>Introducing my name is Muhammad Ivan Verdyansyah, I am a Web Developer with experience in UI/UX Designer, Front-end Developer and Back-end Developer. I am very interested in this field of Programming and happy to be able to join this community to learn and collaborate.</p>
                    <p>I have an educational background in Software Engineering. I have the ability to communicate, and work with teams that I can apply to help in various projects. I also really enjoy meeting and interacting with new people. Feel free to contact me if you have any questions or would like to collaborate on a project. Thank You!</p>
                  </div>
                </div>
              </div>
              <div class="accordion-item">
                <h2 class="accordion-header">
                  <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Reason why iam learning Vue JS
                  </button>
                </h2>
                <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                  <div class="accordion-body">
                    <p>Easy to learn and understand: Vue.js is very easy to learn and understand. In no time, you can master the basics of Vue.js and start building web applications.</p>
                    <p>Good performance: Vue.js is designed to perform well, even in complex applications.</p>
                    <p>Scalability: Vue.js is designed to easily adapt to your project needs and the scale of your application.</p>
                    <p>Flexibility: Vue.js allows you to use other libraries or frameworks if needed, or even to build an application from scratch.</p>
                    <p>Good documentation: The Vue.js documentation is very complete and easy to understand, making it easy to learn and use.</p>
                    <p>Active community: Vue.js has an active and fast-growing community, making it easy for you to get support and resources when you need them.</p>
                    <p>Used by large enterprises: Vue.js is used by large companies such as Alibaba, Xiaomi, and Baidu, demonstrating the reliability and superiority of this framework.</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'HomePage',
}
</script>

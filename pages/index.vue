<template>
  <main>
    <img src="~/assets/images/star.png" alt="star" class="star" id="star">
    <nav class="navbar">
      <img src="~/assets/images/logo.png" alt="">
      <ul>
        <li>
          <a href="">Jobs</a>
        </li>
        <li>
          <a href="">Companies</a>
        </li>
        <li>
          <a href="">About</a>
        </li>
      </ul>
    </nav>
    <section class="hero">
      <div>
        <h1>
          Remote Jobs <br>
          for anyone <br>
          anywhere
        </h1>
        <p>Thousnads of jobs here, find your job</p>
        <button class="btn">Get Started</button>
        <div class="logos">
          <img src="~/assets/images/google.svg" alt="google logo">
          <img src="~/assets/images/microsoft.svg" alt="microsoft logo">
          <img src="~/assets/images/netflix.svg" alt="netflix logo">
        </div>
      </div>
      <div class="illustration">
        <img src="~/assets/images/illustration.png" alt="">
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'IndexPage',
  mounted () {
    let x, y;
    // get mouse position
    document.addEventListener('mousemove', (e) => {
      x = e.clientX
      y = e.clientY

      // move the star with easing
      TweenMax.to(this.$refs.star, 0.5, {
        x: x - 100,
        y: y - 100,
        ease: Power2.easeOut
      })
      // let star = document.getElementById('star');
      // star.style.left = x + 'px'
      // star.style.top = y + 'px'
    })
  }
}
</script>

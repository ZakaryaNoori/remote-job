<template>
  <main>
    <img src="~/assets/images/star.png" alt="star" class="star" id="star" ref="star">
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
      <div id="ls">
        <h1 id="heading">
          Remote Jobs <br>
          for anyone <br>
          anywhere
        </h1>
        <p ref="paragraph">Thousnads of jobs here, find your job</p>
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
import gsap from "gsap";

export default {
  name: 'IndexPage',
  mounted () {
    // get mouse position
    document.addEventListener('mousemove', (e) => {
      x = e.clientX
      y = e.clientY

      // move the star to mouse position with easing
      // gsap.to(this.$refs.star, {
      //   x: x,
      //   y: y,
      //   ease: "power3.inOut"
      // })
    })

    gsap.from(this.$refs.star, {
      opacity: 0,
      duration: 3,
    })

    // animate the star
    gsap.to(this.$refs.star, {
      duration: 5,
      repeat: -1,
      yoyo: true,
      scale: 1.5,
      ease: "power3.inOut",
      y: 80,
    })

    // animate the heading
    gsap.from("#ls", {
      opacity: 0,
      duration: 2.2,
      y: -50,
      ease: "power3.inOut",
    })

    // animate the paragraph
    // gsap.from(this.$refs.paragraph, {
    //   opacity: 0,
    //   duration: 2.2,
    //   y: -50,
    //   ease: "power3.inOut",
    // })

    // animate the button
    // gsap.from(".btn", {
    //   opacity: 0,
    //   duration: 2.2,
    //   y: -50,
    //   ease: "power3.inOut",
    // })

    // animate the logos
    gsap.from(".logos img", {
      opacity: 0,
      duration: 2,
      y: -50,
      ease: "power3.inOut",
      stagger: 0.2,
    })

    // animate the illustration
    gsap.from(".illustration", {
      opacity: 0,
      duration: 1.5,
      x: 100,
      scale: 0.9,
      ease: "power3.inOut",
    })

  }
}
</script>

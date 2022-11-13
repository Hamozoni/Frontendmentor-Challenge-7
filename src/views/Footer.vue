<template>
  <footer>
    <div class="container">
      <div class="logo">
        <h3>Shortly</h3>
      </div>
      <div class="info">
        <div class="con features">
          <h4>Features</h4>
          <ul>
            <li><a href="#">Link Shortening</a></li>
            <li><a href="#">Branded Links</a></li>
            <li><a href="#">Analytics</a></li>
          </ul>
        </div>
        <div class="con resources">
          <h4>resources</h4>
          <ul>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Developers</a></li>
            <li><a href="#">Support</a></li>
          </ul>
        </div>
        <div class="con company">
          <h4>Company</h4>
          <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Our Team</a></li>
            <li><a href="#">Careers</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </div>
      </div>
      <ul class="socials">
        <li>
          <a href="#"
            ><img src="@/assets/icon-facebook.svg" alt="facebook"
          /></a>
        </li>
        <li>
          <a href="#"><img src="@/assets/icon-twitter.svg" alt="twitter" /></a>
        </li>
        <li>
          <a href="#"
            ><img src="@/assets/icon-pinterest.svg" alt="pinterest"
          /></a>
        </li>
        <li>
          <a href="#"
            ><img src="@/assets/icon-instagram.svg" alt="instagram"
          /></a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComp",
};
</script>

<style>
footer {
  background-color: var(--very-dark-violet);
}
footer .container {
  text-align: center;
  padding: 40px 20px;
}
footer .container .logo h3 {
  font-size: 32px;
  color: var(--weight);
}
footer .container .info {
  margin-top: 30px;
}
footer .container .info .con {
  margin-bottom: 30px;
}
footer .container .info h4 {
  margin-bottom: 15px;
  font-size: var(--font-size);
  color: var(--weight);
}
footer .container .info ul li a {
  color: var(--gray);
  font-size: 12px;
  padding: 15px 0;
}
footer .container .socials {
  display: flex;
  justify-content: center;
  gap: 30px;
}
@media (min-width: 575px) {
  footer .container .info {
    display: flex;
    justify-content: center;
    gap: 70px;
  }
}
@media (min-width: 992px) {
  footer .container .logo {
    flex: 1;
  }
  footer .container .info {
    margin-top: 0;
  }
  footer .container {
    text-align: unset;
    display: flex;
    justify-content: space-between;
    gap: 70px;
  }
}
</style>

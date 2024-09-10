<template>
    <section id="about">
        <div class="about-text">
            <p class="animated-text-wrapper">
                Ich bin <strong class="animated-text">{{ currentText }}</strong>
            </p>
            <p>
                Derzeit absolviere ich eine Ausbildung zum Fachinformatiker für Anwendungsentwicklung, mit dem
                Schwerpunkt auf der Entwicklung von Webseiten und Online-Shops.<br>
                Zusätzlich beschäftige ich mich leidenschaftlich viel mit meinem Home-Server.
            </p>
            <button class="btn">
                <a href="#contact">Kontakt</a>
            </button>
        </div>
        <div class="about-head">
            <div>
                <h2>Über mich</h2>

                <div class="social-media-icons">
                    <a href="https://github.com/lytexdev/" target="_blank" title="Github: lytexdev">
                        <img src="../assets/images/icons/github.svg" alt="Github: lytexdev" height="42px">
                    </a>
                    <a href="https://www.instagram.com/ximmanuelm/" target="_blank" title="Instagram: ximmanuelm">
                        <img src="../assets/images/icons/instagram.svg" alt="Instagram: ximmanuelm" height="42px">
                    </a>
                    <a href="https://x.com/ximmanuelm/" target="_blank" title="X: ximmanuelm">
                        <img src="../assets/images/icons/x.svg" alt="X: ximmanuelm" height="48px">
                    </a>
                </div>
            </div>
        </div>
    </section>
    <hr>
    <section id="skills">
        <h4>Meine Skills</h4>
        <b>(oder zumindest was ich benutze)</b>
        <div class="skills-row">
            <div class="skill">
                <h3>
                    <a href="https://www.python.org/" target="_blank" class="python">Python</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://www.djangoproject.com/" target="_blank" class="django">Django</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://flask.palletsprojects.com/" target="_blank" class="flask">Flask</a>
                </h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3>
                    <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank"
                        class="javascript">JavaScript</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://vuejs.org/" target="_blank" class="vuejs">Vue.js</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://nuxt.com/" target="_blank" class="nuxt">Nuxt</a>
                </h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3>
                    <a href="https://www.shopware.com/" target="_blank" class="shopware">Shopware</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://sass-lang.com/" target="_blank" class="scss">SCSS</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://getbootstrap.com/" target="_blank" class="bootstrap">Bootstrap</a>
                </h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3>
                    <a href="https://git-scm.com/" target="_blank" class="git">Git</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://www.docker.com/" target="_blank" class="docker">Docker</a>
                </h3>
            </div>
            <div class="skill">
                <h3>
                    <a href="https://nodejs.org/" target="_blank" class="nodejs">Node.js</a>
                </h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3>
                    <a href="https://www.linux.org/" target="_blank" class="linux">Linux</a>
                </h3>
            </div>
        </div>
    </section>
    <hr>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const texts = ref([
  "Immanuel Mruk",
  "lytex",
  "17 Jahre alt",
  "angehender Fachinformatiker",
  "fullstack Webentwickler",
  "Linux-Enthusiast",
  "Privacy-Freak",
  "Koffein-Suchti",
  "großer Fan von FOSS",
  "Computer-Geek",
]);
const currentText = ref("Immanuel Mruk");
const textIndex = ref(0);

onMounted(() => {
  startTextRotation();
  getDarkMode();
});

function startTextRotation() {
  setInterval(() => {
    textIndex.value = (textIndex.value + 1) % texts.value.length;
    currentText.value = texts.value[textIndex.value];
  }, 3000);
}
</script>

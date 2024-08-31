<template>
    <section id="about">
        <div class="about-text">
            <p class="animated-text-wrapper">
                Ich bin <strong class="animated-text">{{ currentText }}</strong>
            </p>
            <p>
                Derzeit absolviere ich eine Ausbildung zum Fachinformatiker für Anwendungsentwicklung, mit dem
                Schwerpunkt auf der Entwicklung von Webseiten und Online-Shops.<br>
                Zusätzlich beschäftige ich mich leidenschaftlich viel mit meinem Arch Linux Home-Server.
            </p>

            <button class="btn">
                <a href="#contact">Kontakt</a>
            </button>
        </div>

        <div class="about-head">
            <div>
                <h2>Über mich</h2>

                <div class="social-media-icons">
                    <a href="https://github.com/ximmanuel/" target="_blank" title="Github: ximmanuel">
                        <img src="../assets/images/icons/github.svg" alt="Github: ximmanuel" height="42px">
                    </a>
                    <a href="https://www.instagram.com/ximmanuelm/" target="_blank" title="Instagram: ximmanuelm">
                        <img src="../assets/images/icons/instagram.svg" alt="Instagram: ximmanuelm" height="42px">
                    </a>
                    <a href="https://x.com/ximmanuelm/" target="_blank" title="X: ximmanuelm">
                        <img src="../assets/images/icons/x.svg" alt="X: ximmanuelm" height="48px">
                    </a>
                </div>
            </div>
            <img class="about-avatar" src="../assets/images/logo.png" alt="lytex avatar" height="301" />
        </div>
    </section>

    <hr>

    <section id="skills">
        <h4>Meine Skills</h4>
        <b>(oder zumindest was ich benutze)</b>

        <div class="skills-row">
            <div class="skill">
                <h3 style="color:#234b6b">Python</h3>
            </div>
            <div class="skill">
                <h3 style="color:#35b87d">Vue.js</h3>
            </div>
            <div class="skill">
                <h3 style="color:#00ff95">Nuxt</h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3 style="color:#1b6d74">Flask</h3>
            </div>
            <div class="skill">
                <h3 style="color:#189eff">Shopware</h3>
            </div>
            <div class="skill">
                <h3 style="color:#890bfc">Bootstrap</h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3 style="color:#cd6699">SCSS</h3>
            </div>
            <div class="skill">
                <h3 style="color:#f1d30c">JavaScript</h3>
            </div>
            <div class="skill">
                <h3><span style="color:#f16529">HTML</span> & <span style="color:#3498DB">CSS</span></h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3 style="color:#fc2a05">Git</h3>
            </div>
            <div class="skill">
                <h3 style="color:#008cff">Docker</h3>
            </div>
            <div class="skill">
                <h3 style="color:#8BC34A">Node.js</h3>
            </div>
        </div>
        <div class="skills-row">
            <div class="skill">
                <h3 style="color:#1793D1">Arch Linux</h3>
            </div>
            <div class="skill">
                <h3 style="color:#E95420">Ubuntu</h3>
            </div>
            <div class="skill">
                <h3 style="color:#A81D33">Debian</h3>
            </div>
        </div>
    </section>

    <hr>
</template>

<script>
export default {
    data() {
        return {
            texts: [
                "Immanuel Mruk",
                "17 Jahre alt",
                "angehender Fachinformatiker",
                "fullstack Webentwickler",
                "Linux-Enthusiast",
                "Cybersecurity-Verfechter",
                "Privacy-Freak",
                "Koffein-Suchti",
                "lytex",
                "großer Fan von FOSS",
                "Computer-Nerd",
                "Kaffee-Liebhaber"
            ],
            currentText: "Immanuel Mruk",
            textIndex: 0,
        };
    },
    mounted() {
        this.startTextRotation();
    },
    methods: {
        startTextRotation() {
            setInterval(() => {
                this.textIndex = (this.textIndex + 1) % this.texts.length;
                this.currentText = this.texts[this.textIndex];
            }, 3000);
        },
    },
};
</script>

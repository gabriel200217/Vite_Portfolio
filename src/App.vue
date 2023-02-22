<template>
  <v-app id="home">
    <!-- <v-main>
      <HelloWorld/>
    </v-main> -->
    <Navbar/> <!--About="#About" Home="#Home" portfolio="#portfolio"/-->
    <v-container fluid  style="background-color: rgb(9, 45, 83)">
      <div class="head">
        <v-row id="Home">
          <v-col cols="5px">
            <div style="position: relative" class="mt-18">
              <h1 class="text-grey">
                Hi
              </h1>
              <h1 class="text-grey" id="NamePresentation">
                Hi, I'm Gabriel Chacon
              </h1>
              <span class="tex-grey" id="ShortDescription">
                Frontend and Backend Developer 
              </span><br/>
              <a href="#contact" style="text-decoration: none">
                <v-btn title dark class="text-white mt-8" style="background: red" id="ContactMe">
                  Contact Me
                </v-btn>
              </a>
            </div>
          </v-col>
          <v-col cols="2px">
            <v-btn @click="send">
              <div style="position: absolute; 
              z-index: 9999; bottom: 0; 
              margin-right: auto; 
              left: 0; right: 0; top: -14px;
              text-align: center;">
                <v-icon color="red" size="40">
                  fas fa-duotone fa-language
                </v-icon>
              </div>
            </v-btn>
            <div style="position: absolute; 
            z-index: 9999; bottom: 0; 
            margin-right: auto; 
            left: 0; right: 0; top: 190px;
            text-align: center;">
              <v-icon color="red" size="40">
                fas fa-angle-double-down
              </v-icon>
            </div>
          </v-col>
          <v-col cols="5px">
            <div style="position: relative; 
            z-index: 9999; left: 200px" class="mt-4">
              <v-img src="Principal2.png"
              contain max-width="220"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="About">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="Blob.png"
                contain max-height="370"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="text-white mt-16 " id="about">About Me</h5>
              <div style="width: 30%">
                <v-slider v-model="slider2" color="red" label="">

                </v-slider>
              </div>
              <h4 class="text-white mt-n4" id="PresentationTecnologies">I'm creator of apps web developed in Javascript, PHP or Python</h4>
              <h4 class="text-white" id="Tecnologies">Developer Rust, Python, Javascript and PHP</h4>
              <p class="text-grey" id="siteContent">I have been programming since 2020 starting with c++ and then php, 
                which I used for 2 years while I was studying at the university, making inventory systems</p>
              <br/>
              <p class="text-grey" id="staticContent">
                In my professional practices of the third year of study, I created for various systems for various companies, specifically Branar, Corporacion Bel and Tecnosistemas
              </p>
              <a href="./components/Gabriel_Chacon_Curriculum.docx" style="text-decoration: none" download="CV.docx">
                <v-btn title dark color="red" class="mt-4" id="CV">
                  Download CV
                </v-btn>
              </a>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2 class="text-white" id="WhatIDo">What i Do</h2>
        <div style="width: 12%; margin: 0 auto">
          <v-slider v-model="slider2" color="red" label=""></v-slider>
        </div>
      </div>
      <v-col cols="12" id="portfolio">
        <div class="first mb-6" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop mr-1" color="red" class="text-white"></v-btn>
                <h3 class="text-white ml-3 mt-4" id="DesignWeb">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption" id="TextDesign">
                  Web pages designed with, Vue, React and using css frameworks
                  such as Material UI, Bootstrap, Font Awesome 
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-desktop" color="red" class="text-white"></v-btn>
                <h3 class="text-white ml-3 mt-4" id="DesktopApp">Desktop App</h3>
                <p class="text-grey ml-3 mt-4 text-caption" id="TextDesktop">
                  Made with Python in Tkinter or rust with tauri, 
                  making optimal use of system resources 
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-microchip" color="red" class="text-white"></v-btn>
                <h3 class="text-white ml-3 mt-4" id="API">API Programmer</h3>
                <p class="text-grey ml-3 mt-4 text-caption" id="TextAPI">
                  Developed in Python with frameworks such as 
                  Django, Django Rest Framework or FastApi and Rust with Actix Web
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6 mt-4">
          <v-btn color="red" class="mr-2" id="allPort">All</v-btn>
          <v-btn class="mr-2 bg-black" id="" variant="tonal" @click="images = !images">E-commerce</v-btn>
          <v-btn class="mr-2 bg-black" id="" variant="tonal" @click="design = !design">Web Design</v-btn>
          <v-btn class="mr-2 bg-black" id="" variant="tonal" @click="all = !all">API</v-btn>
          <v-btn class="bg-black" id="" variant="tonal" @click="inventory = !inventory">Inventory App</v-btn>
        </div>
      </v-col>
      <!-- <img id="siteImg" src="https://firebasestorage.googleapis.com/v0/b/sistema-72889.appspot.com/o/23ff3dd8-10ae-4353-b8a5-0511fd68b4f2?alt=media&token=7cc4aa3d-4950-4dd0-86eb-4721380ff2b2"> -->
      <v-col cols="12" class="imgHover">
        <v-row v-if="images" class="fill-height" align="center" justify="center" >
          <template v-for="(item, i) in items2" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover': isHovering}" v-bind="props" >
                  <v-img :src="item.img" height="225px" cover ></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
        <v-row v-else-if="design" class="fill-height" align="center" justify="center" >
          <template v-for="(item, i) in items5" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover': isHovering}" v-bind="props" >
                  <v-img :src="item.img" height="225px" cover ></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
        <v-row v-else-if="inventory" class="fill-height" align="center" justify="center" >
          <template v-for="(item, i) in items4" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover': isHovering}" v-bind="props" >
                  <v-img :src="item.img" height="225px" cover ></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
        <v-row v-else-if="all" class="fill-height" align="center" justify="center" >
          <template v-for="(item, i) in items3" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover': isHovering}" v-bind="props" >
                  <v-img :src="item.img" height="225px" cover ></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
        <v-row v-else class="fill-height" align="center" justify="center" >
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover': isHovering}" v-bind="props" >
                  <v-img :src="item.img" height="225px" cover ></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="red" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col  cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="E-Commerce-2.png" 
                height="200px" cover></v-img>
                <v-card-title >E-Commerce React, JS, Firebase</v-card-title>
                <v-card-subtitle id="DateEC">
                  Carried out from 12-09-2022 to 20-01-2023
                </v-card-subtitle>
                <v-card-text id="TextEC">
                  Thought as a solution for the online sales of the branar company, this website was made with React js, Sales graphics made with Chart JS and Firebase was used as Baas, The application consists of administrative modules, sales carts and user authentications using oauth.
                  Repository Link:
                </v-card-text>
                <a href="https://github.com/AceGambino7/teg" target="blank">
                  <v-btn icon="fas fa-brands fa-square-github"></v-btn>
                </a>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="API.png" 
                height="200px" cover></v-img>
                <v-card-title>API Django/Django Rest</v-card-title>
                <v-card-subtitle id="DateAPI">
                  Carried out from 25-10-2022 to 14-12-2022
                </v-card-subtitle>
                <v-card-text id="TextAPI2">
                  Made for the "Corporacion Bel" that arose due to the need to efficiently manage stock, equipment such as printers and computers,
                  in addition to managing the company's personnel related to the use of this equipment. Due to the privacy policies of the company I cannot place the link to the repository.
                  To make the API, Django and its metaframework Django Rest Framework and libraries such as Django Rest Knox were used.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="PHP-App-3.png" 
                height="200px" cover></v-img>
                <v-card-title>Inventory App</v-card-title>
                <v-card-subtitle id="DatePHP">
                  Carried out from 04-09-2022 to 20-09-2022
                </v-card-subtitle>
                <v-card-text id="TextPHP">
                  It was built thinking of managing the inputs and outputs of the equipment which was repaired within the company 
                Tecnosistemaslara such as printers or computers. Developed in PHP and using MySql as a database, 
                the system can print invoices, manage equipment and personnel. Link Repository
                </v-card-text>
                <a href="https://github.com/gabriel200217/Electiva_Php" target="blank">
                  <v-btn icon="fas fa-brands fa-square-github"></v-btn>
                </a>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="blog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="text-white mt-2" id="WhyHire">Why hire me for your projects?</h1>
              <p class="text-white" id="SkillsHere">
                I have programming skills, in addition to the fact that I can adapt within a short period of time both to the work environment and to the methodology with which I work, consequently I am a person who is aware of new technologies, whether they are frameworks, AI and new programming languages, I am always willing to learn and meet new challenges, so mastering new languages ​​or technologies is not difficult for me, if this convinces you, you can contact me through my linkedin
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <a href="https://www.linkedin.com/in/gabriel-chacon-39a882200/" target="blank" style="text-decoration: none">
                <v-btn color="red" class="mt-15" id="HireMe">Hire Me</v-btn>
              </a>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact" style="color:white">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1 Id="infoContact">Contact info.</h1>
              <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn><br/>
              <span class="text-caption">Barquisimeto. Venezuela</span><br/>
              <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn><br/>
              <span class="text-caption">0414-5519064</span><br/>
              <span class="text-caption">0414-5519064</span><br/>
              <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn><br/>
              <span class="text-caption">gabrielchacon200269@gmail.com</span><br/>
              <span class="text-caption">gabrielchacon200269@gmail.com</span><br/>
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8" id="SendMessage">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption" id="MessageEmail">
              You can contact me by email by filling out this form, which will ask you for a captcha to send, the email will reach me immediately
            </span>
            <form action="https://formsubmit.co/6b1906045151445a90f5774ad2c8604c" method="POST">
              <v-row class="mt-10">
                <v-col cols="12" sm="6">
                  <v-text-field label="Name" persistent-hint variant="outlined" name="name"></v-text-field>
                  <!-- <input style="background-color: white" type="text" name="name" required> -->
                </v-col>
                <v-col cols="12" sm="6">
                  <v-text-field label="Phone Number" persistent-hint variant="outlined" name="Phone"></v-text-field>
                  <!-- <input style="background-color: white" type="email" name="email" required> -->
                </v-col>
              </v-row>
              <v-textarea label="Message" persistent-hint variant="outlined" name="message"></v-textarea>
              <button style="background-color: red; margin-top: 2; padding: 8px; border-radius: 7px" id="SendNow">Submit Now</button>
              <!-- <v-btn color="red" class="mt-2">Submit Now</v-btn> -->
              <!-- <input type="hidden" name="_next" value="http://127.0.0.1:5173"> -->
            </form>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue'
import FooterView from './components/FooterView.vue'
import Push from "push.js"

Push.create(
  "Para Traducir el texto Presionar el boton del medio con simbolo de traductor o recargar la pagina\n" +
  "\nTo translate the text, press the middle button with the translator symbol or reload the page"
)

export default {
  name: 'App',
  methods: {
    send(){
      let Texts = {
        siteContent: {
          text: "He estado programando desde 2020 comenzando con c ++ y luego con php," +
          "que utilicé durante 2 años mientras estudiaba en la universidad, haciendo sistemas de inventario"
        },
        staticContent: {
          text: "En mis practicas profesionales del tercer año de estudio cree para varias sistemas para diversas empresas," + 
          "especificamente Branar, Corporacion Bel y Tecnosistemas"
        },
        NamePresentation: {
          text: "Hola, soy Gabriel Chacon"
        },
        ShortDescription: {
          text: "Desarrollador Backend y Frontend"
        },
        ContactMe: {
          text: "Contactame"
        },
        about: {
          text: "acerca de mi"
        },
        PresentationTecnologies: {
          text: "Soy creador de aplicaciones web desarrolladas en" +
          "Javascript, PHP o Python"
        },
        Tecnologies: {
          text: "Desarrollador en Lenguajes como Rust, Javascript, Python y PHP"
        },
        CV: {
          text: "Descargar CV"
        },
        WhatIDo: {
          text: "Lo que hago"
        },
        DesignWeb: {
          text: "Diseño Web"
        },
        DesktopApp: {
          text: "Aplicaciones De Escritorio"
        }, 
        API: {
          text: "Programar API's"
        },
        TextDesign: {
          text: "Paginas web diseñadas con \n" +
          "Vue, React y utilizando frameworks de css\n" +
          "como Material UI, Bootstrap, Font Awesome"
        },
        TextDesktop: {
          text: "Hechas con Python en Tkinter o rust con tauri," +
          "aprovechando los recursos del sistema de manera optima"
        },
        TextAPI: {
          text: "Desarrolladas en Python con frameworks como Django," + 
          " Django Rest Framework o FastApi y Rust con Actix Web"
        },
        DateEC: {
          text: "Realizado desde el 12-09-2022 al 20-01-2023"
        },
        TextEC: {
          text: "Pensado como una solución para las ventas online de la empresa branar, " +
          "está web se realizo con React  js, Graficos de ventas realizados con Chart JS y se uso Firebase como Baas, " + 
          "La aplicacion consta de modulos administrativos, carritos de venta y autenticaciones de usuarios usando Oauth. Link del Repositorio:"
        },
        DateAPI: {
          text: "Realizado desde el 25-10-2022 al 14-12-2022"
        },
        TextAPI2: {
          text: "Realizado para la Corporacion bel que surgio debido a la necesidad de manejar el stock eficientemente, " + 
          "equipos como impresoras y computadoras, además de manejar el personal de la empresa relacionado al uso de estos equipos. Por politicas de Privacidad de la empresa no puedo colocar el link hacia el repositorio. " + 
          "Para realizar la API se uso Django y su metaframework Django Rest Framework y librerias como Django Rest Knox"
        },
        DatePHP: {
          text: "Realizado desde el 04-09-2022 al 20-09-2022"
        },
        TextPHP: {
          text: "Se construyo pensando en administrar las entradas y salidas de los equipos los cuales se reparaban dentro de la empresa tecnosistemaslara, " + 
          "como impresoras o computadoras. Desarrollado en PHP y usando como base de datos MySql," + 
          "El sistema puede imprimir facturas, administrar equipos y personal"
        },
        WhyHire: {
          text: "¿Por que contratarme para sus proyectos?"
        },
        SkillsHere: {
          text: "Poseo aptitudes para programar además de que puedo adaptarme dentro de un corto periodo de tiempo "+ 
          "tanto al ambiente laboral como a la metodologia con la que se trabaje, consecuente a eso soy una persona que " +
          "está al tanto de nuevas tecnologias, ya sean frameworks, AI y nuevos lenguajes de programación, " +
          "siempre estoy dispuesto a aprender y atender nuevos desafios, por lo que dominar nuevos lenguajes o tecnologias" + 
          "no me es dificil, si esto le convence puede contactarse conmigo mediante mi linkedin "
        },
        HireMe: {
          text: "Contactar"
        },
        infoContact: {
          text: "Informacion de contacto"
        },
        SendMessage: {
          text: "Enviame tu mensaje"
        },
        MessageEmail: {
          text: "Puedes contactarme mediante correo electronico llenando este formulario," + 
          "el cual te pedira un captcha para enviar, el correo me llegara inmediatamente"
        },
        SendNow: {
          text: "Enviar Mensaje"
        },
        Init: {
          text: "Inicio"
        },
        Aabout: {
          text: "Acerca de"
        },
        Port: {
          text: "Portafolio"
        },
        Proyects: {
          text: "Proyectos"
        },
        Description: {
          text: "Descripcion"
        },
        Contacts: {
          text: "Contactos"
        },
      }
      return siteContent.textContent = Texts.siteContent.text, 
      staticContent.textContent = Texts.staticContent.text,
      NamePresentation.textContent = Texts.NamePresentation.text,
      ShortDescription.textContent = Texts.ShortDescription.text,
      ContactMe.textContent = Texts.ContactMe.text,
      about.textContent = Texts.about.text,
      PresentationTecnologies.textContent = Texts.PresentationTecnologies.text,
      Tecnologies.textContent = Texts.Tecnologies.text,
      CV.textContent = Texts.CV.text,
      WhatIDo.textContent = Texts.WhatIDo.text,
      DesignWeb.textContent = Texts.DesignWeb.text,
      DesktopApp.textContent = Texts.DesktopApp.text,
      API.textContent = Texts.API.text,
      TextDesign.textContent = Texts.TextDesign.text,
      TextDesktop.textContent = Texts.TextDesktop.text,
      TextAPI.textContent = Texts.TextAPI.text,
      DateEC.textContent = Texts.DateEC.text,
      TextEC.textContent = Texts.TextEC.text,
      DateAPI.textContent = Texts.DateAPI.text,
      TextAPI2.textContent = Texts.TextAPI2.text,
      DatePHP.textContent = Texts.DatePHP.text,
      TextPHP.textContent = Texts.TextPHP.text,
      WhyHire.textContent = Texts.WhyHire.text,
      SkillsHere.textContent = Texts.SkillsHere.text,
      HireMe.textContent = Texts.HireMe.text,
      infoContact.textContent = Texts.infoContact.text,
      SendMessage.textContent = Texts.SendMessage.text,
      MessageEmail.textContent = Texts.MessageEmail.text,
      SendNow.textContent = Texts.SendNow.text,
      Init.textContent = Texts.Init.text,
      Aabout.textContent = Texts.Aabout.text,
      Port.textContent = Texts.Port.text,
      Proyects.textContent = Texts.Proyects.text,
      Description.textContent = Texts.Description.text,
      Contacts.textContent = Texts.Contacts.text
    },
  },
  data() {
    return {
      images: true,
      all: true,
      design: true,
      inventory: true
    }
  },
  setup(){
    return {
      slider2: 50,

      items: [
        {
          img: "E-commerce.png"
        },
        {
          img: "E-Commerce-2.png"
        },
        {
          img: "E-Commerce-3.png"
        },
        {
          img: "E-Commerce-4.png"
        },
        {
          img: "API.png"
        },
        {
          img: "API-2.png"
        },
        {
          img: "API-3.png"
        },
        {
          img: "PHP-App.png"
        },
        {
          img: "PHP-App-2.png"
        },
        {
          img: "PHP-App-3.png"
        },
        {
          img: "Design.png"
        },
        {
          img: "Design-2.png"
        },
      ],

      items2: [
        {
          img: "E-commerce.png"
        },
        {
          img: "E-Commerce-2.png"
        },
        {
          img: "E-Commerce-3.png"
        },
        {
          img: "E-Commerce-4.png"
        }
      ],

      items3: [
        {
          img: "API.png"
        },
        {
          img: "API-2.png"
        },
        {
          img: "API-3.png"
        }
      ],

      items4: [
        {
          img: "PHP-App.png"
        },
        {
          img: "PHP-App-2.png"
        },
        {
          img: "PHP-App-3.png"
        }
      ],

      items5: [
        {
          img: "Design.png"
        },
        {
          img: "Design-2.png"
        }
      ],
    }
  },

  components: {
    // HelloWorld,
    Navbar,
    FooterView,
  },

  data: () => ({
    //
  }),
}
</script>
<style scoped>
  .v-container{
    padding: 16px 0;
  }
  .head{
    position: relative;
    text-align: center;
    padding: 12px;
    margin-bottom: 6px;
    height: 400px;
    width: 100%;
    color: rgb(112, 102, 102);
  }
  .head::before{
    content: " ";
    position: absolute;
    top: 0;
    left: 0;
    height: 90%;
    width: 50%;
    background-color: black;
    transform: skew(0deg, -6.5deg)
  }
  .head::after{
    content: " ";
    position: absolute;
    top: 0;
    right: 0;
    height: 90%;
    width: 50%;
    background-color: black;
    transform: skew(0deg, 6.5deg)
  }
  .egg{
    display: block;
    margin-left: 100px;
    margin-top: 50px;
    width: 356px;
    height: 340px;
    background-color:  rgb(255, 73, 73);
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
  }
  .first{
    width: 100%;
    height: 200px;
    text-align: center;
    padding: 2rem 2rem;
  }
  .child{
    display: inline-block;
    padding: 2rem 1rem;
    vertical-align: middle;
    text-align: center;
    margin-right: 8px;
  }
  .imgHover{
    padding: 0 200px;
  }
  .pre{
    width: 100%;
    height: 530px;
    text-align: center;
    padding: 0 200px;
    background-color: rgb(5, 51, 100);
  }
  .hire{
    width: 100%;
    height: 200px;
    padding: 0 100px;
    background-color: rgb(46, 105, 168);
    margin-top: -24px;
  }
  #TextDesign{
    width: 300px;
    /* height: 170px; */
  }
  #TextDesktop{
    width: 300px;
  }
  #TextAPI{
    width: 300px;
  }
</style>
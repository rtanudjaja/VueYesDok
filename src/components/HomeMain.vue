<template>
  <main>
    <!-- Book Modal -->
    <div
      class="modal fade"
      id="bookModal"
      tabindex="-1"
      role="dialog"
      aria-labelledby="bookModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="bookModalLabel">
              {{ bookModalTitle }}
            </h5>
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            {{ bookModalBody }}
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Carousel -->
    <div id="myCarousel" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
        <li data-target="#myCarousel" data-slide-to="1"></li>
        <li data-target="#myCarousel" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            class="first-slide"
            src="../assets/img/carousel-img1.png"
            style="width: 100%;"
            alt="First image slide"
          />
        </div>
        <div class="carousel-item">
          <img
            class="second-slide"
            src="../assets/img/carousel-img2.png"
            style="width: 100%;"
            alt="Second image slide"
          />
        </div>
        <div class="carousel-item">
          <img
            class="third-slide"
            src="../assets/img/carousel-img3.png"
            style="width: 100%;"
            alt="Third image slide"
          />
        </div>
      </div>
      <a
        class="carousel-control-prev"
        href="#myCarousel"
        role="button"
        data-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a
        class="carousel-control-next"
        href="#myCarousel"
        role="button"
        data-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>

    <!-- Consultation -->
    <div class="container-fluid py-3 consultation">
      <div class="text-center">
        <h2 class="align-middle d-inline-block my-0 py-0">
          {{ ConsultationTitle }}
        </h2>
        <!-- Button trigger modal -->
        <button
          type="button"
          class="btn btn-danger btn-lg active d-inline-block ml-3 mt-1"
          data-toggle="modal"
          data-target="#bookModal"
        >
          {{ ConsultationBody }}
        </button>
      </div>
    </div>

    <!-- CARDS -->
    <div class="container-fluid card-tokens pt-2 pb-5">
      <hr class="featurette-divider" />
      <div class="container">
        <div class="row">
          <div class="col-6 col-lg-3 d-flex align-items-stretch">
            <div class="card">
              <img
                class="card-img-top"
                src="../assets/img/guarantee.png"
                alt=""
              />
              <div class="card-body text-center">
                <h5 class="card-title">
                  {{ CardsGuaranteeTitle }}
                </h5>
                <p class="card-text">
                  {{ CardsGuaranteeBody }}
                </p>
              </div>
            </div>
          </div>
          <div class="col-6 col-lg-3 d-flex align-items-stretch">
            <div class="card">
              <img
                class="card-img-top"
                src="../assets/img/24_hour_EN.png"
                alt=""
              />
              <div class="card-body text-center">
                <h5 class="card-title">{{ Cards24HourTitle }}</h5>
                <p class="card-text">
                  {{ Cards24HourBody }}
                </p>
              </div>
            </div>
          </div>
          <div class="col-6 col-lg-3 d-flex align-items-stretch">
            <div class="card">
              <img
                class="card-img-top"
                src="../assets/img/registered_doctor.png"
                alt=""
              />
              <div class="card-body text-center">
                <h5 class="card-title">
                  {{ CardsDoctorTitle }}
                </h5>
                <p class="card-text">
                  {{ CardsDoctorBody }}
                </p>
              </div>
            </div>
          </div>
          <div class="col-6 col-lg-3 d-flex align-items-stretch">
            <div class="card">
              <img
                class="card-img-top"
                src="../assets/img/iso_certified.png"
                alt=""
              />
              <div class="card-body text-center">
                <h5 class="card-title">
                  {{ CardsISOTitle }}
                </h5>
                <p class="card-text">
                  {{ CardsISOBody }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- INTRO -->
    <a id="Company"></a>
    <div class="row col-md-12 my-5">
      <div class="col-md-7 order-md-2">
        <h2>{{ IntroTitle }}</h2>
        <p class="lead">
          {{ IntroBody }}
        </p>
      </div>
      <div class="col-md-5 order-md-1">
        <div class="embed-responsive embed-responsive-16by9">
          <iframe
            class="embed-responsive-item"
            src="https://www.youtube.com/embed/KrW0Ozk53BU"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>

    <!-- Articles -->
    <hr class="featurette-divider" />
    <a id="Articles"></a>
    <div class="container-fluid py-5">
      <h2>{{ ArticleTitle }}</h2>
      <div class="row pt-3">
        <div class="col-lg-6" v-for="post in posts" :key="post.id">
          <div class="row">
            <div class="col-4">
              <div
                class="mx-auto d-block img-thumbnail text-centre font-weight-bold"
                style="height: 200px;width: 200px;background-color: #555;color: white; padding: 100px 0px; text-align: center;"
              >
                SAMPLE
              </div>
            </div>
            <div class="col-8">
              <h4>{{ post.title }}</h4>
              <p>{{ post.body }}</p>
              <p>
                <a class="btn btn-primary disabled btn-sm" role="button"
                  >{{ ArticleBody }} &raquo;</a
                >
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- About Us -->
    <a id="AboutUs"></a>
    <div class="container-fluid text-center text-light bg py-5">
      <div class="container">
        <h1 class="pb-3">{{ AboutUsTitle }}</h1>
        <p>
          {{ AboutUsBodyP1 }}
        </p>
        <p>
          {{ AboutUsBodyP2 }}
        </p>
        <p>
          {{ AboutUsBodyP3 }}
        </p>
        <p>
          <strong>{{ AboutUsBodyP4 }}</strong>
        </p>
      </div>
    </div>

    <!-- Contact Us -->
    <a id="ContactUs"></a>
    <div class="container text-center my-5">
      <form class="mx-2">
        <h2>{{ ContactUsTitle }}</h2>
        <p>
          {{ ContactUsBody }}
        </p>
        <div class="row">
          <div class="col-12 col-sm-6 px-0 my-2">
            <input
              type="name"
              class="form-control"
              id="contactUsFullName"
              aria-describedby="nameHelp"
              placeholder="Fullname"
            />
          </div>
          <div class="col-12 col-sm-6 px-0 my-2">
            <input
              type="email"
              class="form-control"
              id="contactUsEmail"
              aria-describedby="emailHelp"
              placeholder="E-mail"
            />
          </div>
        </div>
        <div class="row my-2">
          <textarea
            class="form-control"
            id="contactUsMessage"
            rows="3"
            placeholder="Your message"
          ></textarea>
        </div>
        <div id="RecaptchaField2" class="row text-center">
          <iframe
            class="mr-2 my-2"
            src="https://www.google.com/recaptcha/api2/anchor?ar=2&amp;k=6LfPFDIUAAAAAAdU03WEoy4vq6oQEIUUvyx5JKFR&amp;co=aHR0cHM6Ly93d3cueWVzZG9rLmNvbTo0NDM.&amp;hl=en&amp;v=HYx6hBAtwYatsD8qzq7tXNTk&amp;size=normal&amp;cb=hkzrvuy5irou"
            width="304"
            height="78"
            role="presentation"
            name="a-w58dqmghxak1"
            frameborder="0"
            scrolling="no"
            sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-top-navigation allow-modals allow-popups-to-escape-sandbox"
          ></iframe>
          <button type="submit" class="btn btn-primary btn-lg my-2" disabled>
            {{ ContactUsButton }}
          </button>
        </div>
      </form>
      <br />
      <h2>{{ ContactUsDownload }}</h2>
      <br />
      <div class="row">
        <div class="col-sm-12 col-md-6 pb-2">
          <img src="../assets/img/google_play.png" width="200" />
        </div>
        <div class="col-sm-12 col-md-6 pb-2">
          <img src="../assets/img/app_store.png" width="200" />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import axios from "axios";

export default {
  name: "HomeMain",
  props: {
    isEnglish: Boolean
  },
  data() {
    return {
      posts: []
    };
  },
  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts?_limit=4")
      .then(response => (this.posts = response.data))
      .catch(err => console.log(err));
  },
  computed: {
    bookModalTitle: function() {
      if (this.isEnglish) {
        return "Book Consultation";
      } else {
        return "Daftar Konsultasi";
      }
    },
    bookModalBody: function() {
      if (this.isEnglish) {
        return "Please login to book a consultation.";
      } else {
        return "Haraf login/sign-up untuk mendaftar konsultasi";
      }
    },
    ConsultationTitle: function() {
      if (this.isEnglish) {
        return "Worried sick? Consult our doctor!";
      } else {
        return "BINGUNG? TANYA DOKTER!";
      }
    },
    ConsultationBody: function() {
      if (this.isEnglish) {
        return "BOOK ONLINE";
      } else {
        return "MULAI KONSULTASI";
      }
    },
    CardsGuaranteeTitle: function() {
      if (this.isEnglish) {
        return "GUARANTEE OF SERVICE";
      } else {
        return "JAMINAN LAYANAN";
      }
    },
    CardsGuaranteeBody: function() {
      if (this.isEnglish) {
        return "We provide guarantee that every call will be answered by a doctor, money back guarantee.";
      } else {
        return "Kami memberikan jaminan bahwa setiap panggilan akan terjawab oleh dokter atau uang Anda kembali.";
      }
    },
    Cards24HourTitle: function() {
      if (this.isEnglish) {
        return "24/7/365";
      } else {
        return "24/7/365";
      }
    },
    Cards24HourBody: function() {
      if (this.isEnglish) {
        return "We are ready to serve anytime 24-hour, 7 days a week, 365 days a year.";
      } else {
        return "24 jam, 7 hari seminggu, 365 setahun kami siap melayani Anda.";
      }
    },
    CardsDoctorTitle: function() {
      if (this.isEnglish) {
        return "REGISTERED DOCTOR";
      } else {
        return "DOKTER TERDAFTAR";
      }
    },
    CardsDoctorBody: function() {
      if (this.isEnglish) {
        return "Every doctor that practices in YesDok is registered and owns license to practice.";
      } else {
        return "Setiap dokter yang terdaftar di YesDok memiliki STR (Surat Tanda Registrasi) dan SIP (Surat Ijin Praktek).";
      }
    },
    CardsISOTitle: function() {
      if (this.isEnglish) {
        return "ISO CERTIFIED";
      } else {
        return "BERSERTIFIKAT ISO";
      }
    },
    CardsISOBody: function() {
      if (this.isEnglish) {
        return "We are ISO Certified TUV NORD 16 00 C 19034.";
      } else {
        return "Kami bersertifikat ISO TUV NORD 16 00 C 19034.";
      }
    },
    IntroTitle: function() {
      if (this.isEnglish) {
        return "YesDok Introduction";
      } else {
        return "Pengenalan YesDok";
      }
    },
    IntroBody: function() {
      if (this.isEnglish) {
        return "You can now reach professional doctors anywhere and anytime convenient to you! YesDok is designed for efﬁciency that will save your time and money for unnecessary doctor visits.";
      } else {
        return "Sekarang anda bisa berkonsultasi kesehatan dengan dokter 24 jam secara mudah dan cepat! YesDok dihadirkan agar mempermudah pasien untuk menanyakan penyakit yang dialami kepada dokter tanpa harus menempuh perjalanan ke rumah sakit, mendaftar dan menunggu antrian.";
      }
    },
    ArticleTitle: function() {
      if (this.isEnglish) {
        return "Latest Articles";
      } else {
        return "Artikel Terbaru";
      }
    },
    ArticleBody: function() {
      if (this.isEnglish) {
        return "More details";
      } else {
        return "Selengkapnya";
      }
    },
    AboutUsTitle: function() {
      if (this.isEnglish) {
        return "About Us";
      } else {
        return "Tentang Kami";
      }
    },
    AboutUsBodyP1: function() {
      if (this.isEnglish) {
        return "Our company culture was built by an individual who looks forward, is perfectionist and emphasizes on strong discipline. Making continuous improvements is in our company DNA.";
      } else {
        return "Budaya perusahaan kami dibentuk oleh individu yang memandang ke depan, perfeksionis dan fanatik dalam kedisiplinan. Peningkatan yang terus menerus mengalir dalam DNA perusahaan kami.";
      }
    },
    AboutUsBodyP2: function() {
      if (this.isEnglish) {
        return "YesDok is an ehealth service that is reachable through mobile platform which is very powerful and easy to use. Penetrating 17.504 islands and 260 million users in Indonesia.";
      } else {
        return "YesDok adalah layanan ehealth yang terjangkau dengan platform mobile yang mudah digunakan dan tangguh. Menembus 17.504 pulau dan 260 juta pengguna di Indonesia.";
      }
    },
    AboutUsBodyP3: function() {
      if (this.isEnglish) {
        return "YesDok doctor-partners are those that are registered on Indonesian Medical Council. They are committed in being preventive, promotive and delivering quality health information.";
      } else {
        return "Dokter Mitra YesDok adalah dokter yang terdaftar di Konsil Kedokteran Indonesia. Dokter Mitra YesDok berkomitmen dalam preventif, promotif dan edukasi informasi kesehatan yang berkualitas.";
      }
    },

    AboutUsBodyP4: function() {
      if (this.isEnglish) {
        return "Welcome and thank you for joining YesDok.";
      } else {
        return "Selamat datang dan terima kasih sudah bergabung di YesDok.";
      }
    },
    ContactUsTitle: function() {
      if (this.isEnglish) {
        return "CONTACT US";
      } else {
        return "HUBUNGI KAMI";
      }
    },
    ContactUsBody: function() {
      if (this.isEnglish) {
        return "We are always ready to answer your questions about YesDok. Please let us know your queries and how we can help you.";
      } else {
        return "Kami selalu siap untuk menjawab pertanyaan Anda mengenai YesDok. Beritahu kami lebih lanjut mengenai apa yang Anda cari dan bagaimana kami bisa membantu Anda";
      }
    },
    ContactUsButton: function() {
      if (this.isEnglish) {
        return "SEND MESSAGE";
      } else {
        return "KIRIM PESAN";
      }
    },
    ContactUsDownload: function() {
      if (this.isEnglish) {
        return "Download Yes Dok Application";
      } else {
        return "Unduh Aplikasi YesDok di";
      }
    }
  }
};
</script>

<style scoped>
.consultation {
  background: #60b9bd;
}

.card-tokens {
  background-color: #024668;
}

.card {
  color: white;
  border-color: white;
  background-color: #024668;
}

.card-body {
  padding: 0rem 1rem 1rem;
}

.card-img-top {
  object-fit: cover;
  padding: 0rem;
}

.bg {
  /* The image used */
  background-image: url("../assets/img/bg_biru_desktop.png");

  /* Full height */
  height: 100%;

  /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>

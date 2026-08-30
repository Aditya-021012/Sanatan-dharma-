<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sanatan Darshan | Hindu Gods & Goddesses</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Georgia, "Times New Roman", serif;
    background: #fff8ed;
    color: #3d1f00;
    line-height: 1.6;
}

header {
    background: linear-gradient(135deg, #7b1e00, #d35400, #f39c12);
    color: white;
    text-align: center;
    padding: 35px 15px;
}

header h1 {
    font-size: 42px;
}

header p {
    font-size: 18px;
    margin-top: 8px;
}

nav {
    background: #3d1600;
    padding: 12px;
    text-align: center;
    position: sticky;
    top: 0;
    z-index: 10;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 12px;
    font-weight: bold;
}

nav a:hover {
    color: #ffc107;
}

.hero {
    text-align: center;
    padding: 55px 20px;
    background: linear-gradient(rgba(255,248,237,.85), rgba(255,248,237,.95));
}

.hero h2 {
    font-size: 34px;
    color: #8b2500;
}

.hero p {
    max-width: 800px;
    margin: 15px auto;
    font-size: 18px;
}

.om {
    font-size: 70px;
    color: #c0392b;
    margin-bottom: 10px;
}

section {
    padding: 45px 7%;
}

.section-title {
    text-align: center;
    color: #8b2500;
    font-size: 30px;
    margin-bottom: 25px;
}

.search {
    display: block;
    width: 90%;
    max-width: 600px;
    margin: 0 auto 30px;
    padding: 14px;
    border: 2px solid #d35400;
    border-radius: 25px;
    font-size: 17px;
    outline: none;
}

.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 22px;
}

.card {
    background: white;
    border-radius: 15px;
    padding: 25px;
    text-align: center;
    box-shadow: 0 5px 15px rgba(80,40,0,.15);
    border-top: 5px solid #e67e22;
    transition: .3s;
}

.card:hover {
    transform: translateY(-7px);
    box-shadow: 0 10px 25px rgba(80,40,0,.25);
}

.card .symbol {
    font-size: 48px;
}

.card h3 {
    color: #9b2c00;
    margin: 8px 0;
}

.card button {
    margin-top: 12px;
    padding: 9px 18px;
    border: none;
    border-radius: 20px;
    background: #d35400;
    color: white;
    cursor: pointer;
    font-weight: bold;
}

.card button:hover {
    background: #8b2500;
}

.info-box {
    background: #fff0d5;
    border-left: 6px solid #d35400;
    padding: 25px;
    margin: 15px auto;
    max-width: 900px;
    border-radius: 8px;
}

.info-box h3 {
    color: #8b2500;
    margin-bottom: 8px;
}

footer {
    background: #3d1600;
    color: white;
    text-align: center;
    padding: 30px 15px;
}

footer p {
    margin: 5px;
}

/* Popup */
.modal {
    display: none;
    position: fixed;
    z-index: 100;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,.65);
    padding: 30px 15px;
    overflow-y: auto;
}

.modal-content {
    background: #fffaf2;
    max-width: 700px;
    margin: 30px auto;
    padding: 30px;
    border-radius: 18px;
    position: relative;
}

.close {
    position: absolute;
    right: 20px;
    top: 10px;
    font-size: 32px;
    cursor: pointer;
    color: #8b2500;
}

.modal-content h2 {
    color: #8b2500;
    margin-bottom: 15px;
}

@media(max-width:600px) {
    header h1 {
        font-size: 30px;
    }

    nav a {
        display: inline-block;
        margin: 5px;
        font-size: 14px;
    }

    .hero h2 {
        font-size: 27px;
    }
}
</style>
</head>

<body>

<header>
    <div class="om">ॐ</div>
    <h1>Sanatan Darshan</h1>
    <p>Hindu Gods, Goddesses, Scriptures, Festivals & Sacred Traditions</p>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#deities">Deities</a>
    <a href="#festivals">Festivals</a>
    <a href="#scriptures">Scriptures</a>
    <a href="#temples">Temples</a>
</nav>

<section class="hero" id="home">
    <h2>Welcome to Sanatan Darshan 🪷</h2>
    <p>
        Explore information about major Hindu deities, their traditional
        associations, important festivals, sacred texts and famous temples.
    </p>
    <p>
        Hindu traditions are diverse, and different communities may understand
        and worship deities in different ways.
    </p>
</section>

<section id="deities">
    <h2 class="section-title">🕉️ Major Hindu Deities</h2>

    <input
        type="text"
        id="search"
        class="search"
        placeholder="🔍 Search for a deity..."
        onkeyup="searchDeities()"
    >

    <div class="grid" id="deityGrid">

        <div class="card" data-name="shiva">
            <div class="symbol">🔱</div>
            <h3>Lord Shiva</h3>
            <p>Associated with transformation, asceticism and meditation.</p>
            <button onclick="showInfo('shiva')">Learn More</button>
        </div>

        <div class="card" data-name="vishnu">
            <div class="symbol">🪷</div>
            <h3>Lord Vishnu</h3>
            <p>Associated with preservation and protection in Hindu traditions.</p>
            <button onclick="showInfo('vishnu')">Learn More</button>
        </div>

        <div class="card" data-name="brahma">
            <div class="symbol">📜</div>
            <h3>Lord Brahma</h3>
            <p>Traditionally associated with creation.</p>
            <button onclick="showInfo('brahma')">Learn More</button>
        </div>

        <div class="card" data-name="ganesha ganapati">
            <div class="symbol">🐘</div>
            <h3>Lord Ganesha</h3>
            <p>Widely revered as the remover of obstacles and deity of beginnings.</p>
            <button onclick="showInfo('ganesha')">Learn More</button>
        </div>

        <div class="card" data-name="krishna">
            <div class="symbol">🦚</div>
            <h3>Lord Krishna</h3>
            <p>A major figure in Vaishnava traditions and the Bhagavad Gita.</p>
            <button onclick="showInfo('krishna')">Learn More</button>
        </div>

        <div class="card" data-name="rama ram">
            <div class="symbol">🏹</div>
            <h3>Lord Rama</h3>
            <p>Hero of the Ramayana and an important avatar of Vishnu.</p>
            <button onclick="showInfo('rama')">Learn More</button>
        </div>

        <div class="card" data-name="hanuman">
            <div class="symbol">🙏</div>
            <h3>Lord Hanuman</h3>
            <p>Revered for devotion, courage, strength and service.</p>
            <button onclick="showInfo('hanuman')">Learn More</button>
        </div>

        <div class="card" data-name="lakshmi">
            <div class="symbol">🪷</div>
            <h3>Goddess Lakshmi</h3>
            <p>Associated with prosperity, abundance and good fortune.</p>
            <button onclick="showInfo('lakshmi')">Learn More</button>
        </div>

        <div class="card" data-name="saraswati">
            <div class="symbol">📚</div>
            <h3>Goddess Saraswati</h3>
            <p>Associated with learning, knowledge, music and the arts.</p>
            <button onclick="showInfo('saraswati')">Learn More</button>
        </div>

        <div class="card" data-name="durga">
            <div class="symbol">🦁</div>
            <h3>Goddess Durga</h3>
            <p>Revered as a powerful divine mother and protector.</p>
            <button onclick="showInfo('durga')">Learn More</button>
        </div>

        <div class="card" data-name="kali">
            <div class="symbol">🌺</div>
            <h3>Goddess Kali</h3>
            <p>A powerful form of the Divine Mother in Shakta traditions.</p>
            <button onclick="showInfo('kali')">Learn More</button>
        </div>

        <div class="card" data-name="surya">
            <div class="symbol">☀️</div>
            <h3>Surya</h3>
            <p>The Hindu solar deity, associated with light and vitality.</p>
            <button onclick="showInfo('surya')">Learn More</button>
        </div>

        <div class="card" data-name="kartikeya skanda murugan">
            <div class="symbol">🦚</div>
            <h3>Kartikeya</h3>
            <p>Also known as Skanda, Murugan and Subrahmanya.</p>
            <button onclick="showInfo('kartikeya')">Learn More</button>
        </div>

        <div class="card" data-name="shani">
            <div class="symbol">🪐</div>
            <h3>Shani</h3>
            <p>A deity associated with the planet Saturn in Hindu astrology.</p>
            <button onclick="showInfo('shani')">Learn More</button>
        </div>

        <div class="card" data-name="vishwakarma">
            <div class="symbol">🔨</div>
            <h3>Vishwakarma</h3>
            <p>Traditionally regarded as a divine architect and craftsman.</p>
            <button onclick="showInfo('vishwakarma')">Learn More</button>
        </div>

        <div class="card" data-name="dhanvantari">
            <div class="symbol">🌿</div>
            <h3>Dhanvantari</h3>
            <p>Associated with Ayurveda and healing traditions.</p>
            <button onclick="showInfo('dhanvantari')">Learn More</button>
        </div>

    </div>
</section>

<section id="festivals">
    <h2 class="section-title">🎉 Important Hindu Festivals</h2>

    <div class="info-box">
        <h3>🪔 Diwali</h3>
        <p>
            A major festival celebrated in many Hindu communities, associated
            with light, renewal and different regional traditions.
        </p>
    </div>

    <div class="info-box">
        <h3>🌈 Holi</h3>
        <p>
            A festival widely known for colours, joy and the arrival of spring.
        </p>
    </div>

    <div class="info-box">
        <h3>🙏 Ganesh Chaturthi</h3>
        <p>
            A festival celebrating the birth or manifestation of Lord Ganesha,
            especially prominent in Maharashtra.
        </p>
    </div>

    <div class="info-box">
        <h3>🏹 Ram Navami</h3>
        <p>
            A festival associated with the birth of Lord Rama.
        </p>
    </div>

    <div class="info-box">
        <h3>🦚 Janmashtami</h3>
        <p>
            A festival celebrating the birth of Lord Krishna.
        </p>
    </div>

    <div class="info-box">
        <h3>🔱 Mahashivratri</h3>
        <p>
            A major festival dedicated to Lord Shiva.
        </p>
    </div>

    <div class="info-box">
        <h3>🌺 Navratri</h3>
        <p>
            A period of devotion to the Divine Mother, with traditions varying
            across different regions of India.
        </p>
    </div>
</section>

<section id="scriptures">
    <h2 class="section-title">📚 Important Hindu Scriptures</h2>

    <div class="grid">

        <div class="card">
            <h3>📖 Bhagavad Gita</h3>
            <p>
                A philosophical dialogue between Krishna and Arjuna,
                forming part of the Mahabharata.
            </p>
        </div>

        <div class="card">
            <h3>📜 Ramayana</h3>
            <p>
                The epic traditionally attributed to Valmiki, centered on
                Rama, Sita, Lakshmana and Hanuman.
            </p>
        </div>

        <div class="card">
            <h3>⚔️ Mahabharata</h3>
            <p>
                One of India's great Sanskrit epics, containing the Bhagavad Gita.
            </p>
        </div>

        <div class="card">
            <h3>🕉️ Upanishads</h3>
            <p>
                Philosophical texts exploring concepts such as Brahman,
                Atman and ultimate reality.
            </p>
        </div>

        <div class="card">
            <h3>🔥 Vedas</h3>
            <p>
                The Rigveda, Samaveda, Yajurveda and Atharvaveda are the four
                Vedas.
            </p>
        </div>

        <div class="card">
            <h3>🌺 Puranas</h3>
            <p>
                A large body of traditional literature containing mythology,
                cosmology, genealogies and religious teachings.
            </p>
        </div>

    </div>
</section>

<section id="temples">
    <h2 class="section-title">🛕 Famous Hindu Temples</h2>

    <div class="grid">

        <div class="card">
            <h3>🛕 Kedarnath</h3>
            <p>One of the important Shiva pilgrimage sites in the Himalayas.</p>
        </div>

        <div class="card">
            <h3>🛕 Tirupati</h3>
            <p>A major pilgrimage center associated with Lord Venkateswara.</p>
        </div>

        <div class="card">
            <h3>🛕 Somnath</h3>
            <p>One of the traditionally important Jyotirlinga shrines of Shiva.</p>
        </div>

        <div class="card">
            <h3>🛕 Kashi Vishwanath</h3>
            <p>A renowned Shiva temple in Varanasi.</p>
        </div>

        <div class="card">
            <h3>🛕 Jagannath Temple</h3>
            <p>A major Vaishnava pilgrimage center in Puri.</p>
        </div>

        <div class="card">
            <h3>🛕 Meenakshi Temple</h3>
            <p>A famous historic temple in Madurai dedicated to Meenakshi and Sundareshwarar.</p>
        </div>

    </div>
</section>

<footer>
    <h2>ॐ नमः शिवाय</h2>
    <p>Sanatan Darshan</p>
    <p>Created as an educational website about Hindu traditions.</p>
    <p>© 2026</p>
</footer>


<!-- POPUP -->
<div id="modal" class="modal">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <h2 id="modalTitle"></h2>
        <p id="modalText"></p>
    </div>
</div>


<script>

const information = {

    shiva: {
        title: "🔱 Lord Shiva",
        text: "Shiva is one of the principal deities of Hinduism and is especially central to Shaiva traditions. He is associated with transformation, meditation, asceticism and the cosmic dance known as Tandava. Common symbols associated with Shiva include the trident, damaru, crescent moon, serpent and Shiva Linga."
    },

    vishnu: {
        title: "🪷 Lord Vishnu",
        text: "Vishnu is a principal deity in Hinduism and is associated with preservation and protection. Vaishnava traditions regard Vishnu as the Supreme Being. His famous avatars include Rama and Krishna. He is traditionally depicted with a conch, discus, mace and lotus."
    },

    brahma: {
        title: "📜 Lord Brahma",
        text: "Brahma is traditionally associated with creation in Hindu cosmology. He is commonly depicted with four faces and four arms. Brahma should not be confused with Brahman, the philosophical concept of ultimate reality."
    },

    ganesha: {
        title: "🐘 Lord Ganesha",
        text: "Ganesha is one of the most widely worshipped Hindu deities. He is traditionally associated with beginnings, wisdom and the removal of obstacles. He is commonly depicted with an elephant head and is associated with the mouse as his vehicle."
    },

    krishna: {
        title: "🦚 Lord Krishna",
        text: "Krishna is a major Hindu deity and an important figure in Vaishnava traditions. He appears prominently in the Mahabharata and Bhagavad Gita. He is traditionally associated with devotion, wisdom, compassion and divine play."
    },

    rama: {
        title: "🏹 Lord Rama",
        text: "Rama is the central figure of the Ramayana and is traditionally regarded in many Hindu traditions as an avatar of Vishnu. He is associated with righteousness, duty, courage and ideal kingship."
    },

    hanuman: {
        title: "🙏 Lord Hanuman",
        text: "Hanuman is a central figure in the Ramayana and is celebrated for his devotion to Rama, courage, strength and service. He is widely worshipped across India and beyond."
    },

    lakshmi: {
        title: "🪷 Goddess Lakshmi",
        text: "Lakshmi is a major Hindu goddess associated with prosperity, abundance, fortune and beauty. She is traditionally regarded as the consort of Vishnu and is especially worshipped during Diwali."
    },

    saraswati: {
        title: "📚 Goddess Saraswati",
        text: "Saraswati is associated with knowledge, learning, music, speech and the arts. She is traditionally depicted with a veena and is associated with the swan or peacock in different traditions."
    },

    durga: {
        title: "🦁 Goddess Durga",
        text: "Durga is a powerful form of the Divine Mother and is widely revered as a protector. The Durga tradition is especially prominent during Navratri and Durga Puja."
    },

    kali: {
        title: "🌺 Goddess Kali",
        text: "Kali is a powerful form of the Divine Mother, particularly important in Shakta traditions. She is associated with time, transformation and the destruction of ignorance."
    },

    surya: {
        title: "☀️ Surya",
        text: "Surya is the Hindu solar deity. He is associated with light, vitality and the Sun. Surya worship has a long history in Hindu traditions."
    },

    kartikeya: {
        title: "🦚 Kartikeya",
        text: "Kartikeya is also known as Skanda, Murugan, Subrahmanya and other regional names. He is associated with courage and martial power and is especially important in South Indian Hindu traditions."
    },

    shani: {
        title: "🪐 Shani",
        text: "Shani is associated with the planet Saturn and has an important place in Hindu astrology and religious traditions. He is often associated with discipline, responsibility and the consequences of one's actions."
    },

    vishwakarma: {
        title: "🔨 Vishwakarma",
        text: "Vishwakarma is traditionally regarded as a divine architect and craftsman. He is associated with craftsmanship, construction and skilled work."
    },

    dhanvantari: {
        title: "🌿 Dhanvantari",
        text: "Dhanvantari is traditionally associated with Ayurveda and healing. In Hindu mythology, he is described as emerging during the churning of the ocean and is often depicted holding a vessel associated with amrita."
    }
};

function showInfo(deity) {
    document.getElementById("modalTitle").innerText =
        information[deity].title;

    document.getElementById("modalText").innerText =
        information[deity].text;

    document.getElementById("modal").style.display = "block";
}

function closeModal() {
    document.getElementById("modal").style.display = "none";
}

window.onclick = function(event) {
    if (event.target === document.getElementById("modal")) {
        closeModal();
    }
}

function searchDeities() {

    let input =
        document.getElementById("search").value.toLowerCase();

    let cards =
        document.querySelectorAll("#deityGrid .card");

    cards.forEach(card => {

        let name =
            card.getAttribute("data-name");

        if (name.includes(input)) {
            card.style.display = "";
        } else {
            card.style.display = "none";
        }

    });
}

</script>

</body>
</html>

<!-- Flashcard Button -->
<button id="flashcardButton" class="option" onclick="openFlashcardPopup()" style="background-color: #3498db; color: white; width: 90%; margin-top: 20px;">
    Social Profiles
</button>
<!-- Flashcard Popup -->
<div id="flashcardPopup" class="hidden" style="
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #1e1e1e;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(52, 152, 219, 0.5);
    z-index: 1000;
    width: 90%;
    max-width: 400px;
    text-align: center;
    display: none;
">
    <h2 style="color: #3498db;">Social Profiles </h2>

    <div class="card" onclick="flipCard(this)" style="
        background-color: #3498db; 
        color: white; 
        padding: 10px; 
        margin: 10px 0;
        border-radius: 5px;
        cursor: pointer;

     ">
        <div class="card-front">YouTube</div>
        <div class="card-back" style="display: none;"><p>Join our <a href="https://youtube.com/@academeforgepro?si=d6ZmWYKcaFYCrspI" target="_blank" style="color: #00e5ff;">YouTube Channel</a> for updates.</p></div>
    </div>

    <div class="card" onclick="flipCard(this)" style="
        background-color: #3498db; 
        color: white; 
        padding: 10px; 
        margin: 10px 0;
        border-radius: 5px;
        cursor: pointer;
    ">
        <div class="card-front">Instagram</div>
        <div class="card-back" style="display: none;"><p>Follow us on <a href="https://www.instagram.com/academeforgee?igsh=MWYzNjAwMDgxbWYyMQ==" target="_blank" style="color: #00e5ff;">Instagram</a> for updates.</p></div>
    </div>

    <button onclick="closeFlashcardPopup()" class="option" style="background-color: #3498db; color: white; margin-top: 10px;">Close</button>
</div>
<script>
    function openFlashcardPopup() {
        document.getElementById('flashcardPopup').style.display = 'block';
    }

    function closeFlashcardPopup() {
        document.getElementById('flashcardPopup').style.display = 'none';
    }

    function flipCard(card) {
        var front = card.querySelector(".card-front");
        var back = card.querySelector(".card-back");
        
        if (back.style.display === "none") {
            front.style.display = "none";
            back.style.display = "block";
        } else {
            front.style.display = "block";
            back.style.display = "none";
        }
    }

    function showPage(page) {
        document.getElementById(`${currentPage}Container`).classList.add('hidden');
        document.getElementById(`${page}Container`).classList.remove('hidden');
        document.getElementById('backButton').style.display = (page !== 'login') ? 'block' : 'none';

        // Show elements only on login view
        if (page === 'login') {
            document.getElementById('aboutUsContainer').classList.remove('hidden');
            document.getElementById('announcementContainer').classList.remove('hidden');
            document.getElementById('flashcardButton').style.display = 'block'; 
            document.getElementById('flashcardPopup').style.display = 'none';  
        } else {
            document.getElementById('aboutUsContainer').classList.add('hidden');
            document.getElementById('announcementContainer').classList.add('hidden');
            document.getElementById('flashcardButton').style.display = 'none';  
            document.getElementById('flashcardPopup').style.display = 'none';  
        }

        currentPage = page;
    }
</script>

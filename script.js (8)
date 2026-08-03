/*=====================================
THE WEDDING OF
WANDI RAHMAN & AI ARDIANI
=====================================*/

document.addEventListener("DOMContentLoaded", () => {
      
      const loader = document.getElementById("loader");
      const cover = document.getElementById("cover");
      const content = document.getElementById("content");
      const openBtn = document.getElementById("openInvitation");
      const music = document.getElementById("music");
      const musicBtn = document.getElementById("musicBtn");
      
      /*=====================================
      CONTENT
      =====================================*/
      
      content.style.display = "none";
      document.body.style.overflow = "hidden";
      
      /*=====================================
      LOADER
      =====================================*/
      
      window.addEventListener("load", () => {
        
        setTimeout(() => {
          
          loader.style.opacity = "0";
          
          loader.style.transition = ".8s";
          
          setTimeout(() => {
            
            loader.remove();
            
          }, 800);
          
        }, 1200);
        
      });
      
      /*=====================================
      OPEN INVITATION
      =====================================*/
      
      openBtn.addEventListener("click", () => {
        
        cover.style.opacity = "0";
        
        cover.style.transition = ".8s";
        
        setTimeout(() => {
          
          cover.style.display = "none";
          
          content.style.display = "block";
          
          document.body.style.overflowY = "auto";
          
          music.play().catch(() => {});
          
          window.scrollTo({
            
            top: 0,
            
            behavior: "smooth"
            
          });
          
        }, 800);
        
      });
      
      /*=====================================
      MUSIC
      =====================================*/
      
      let playing = true;
      
      musicBtn.addEventListener("click", () => {
        musicBtn.classList.toggle("playing");
        if (music.paused) {
          
          music.play();
          
          playing = true;
          
          musicBtn.innerHTML = "❚❚";
          
        } else {
          
          music.pause();
          
          playing = false;
          
          musicBtn.innerHTML = "♫";
          
        }
        
      });
      
      /*=====================================
      GUEST NAME
      =====================================*/
      
      const params = new URLSearchParams(window.location.search);
      
      const guest = params.get("to");
      
      if (guest) {
        
        document.getElementById("guestName").textContent = decodeURIComponent(guest);
        
      }
      
      /*=====================================
      COUNTDOWN
      =====================================*/
      
      const target = new Date("December 26, 2026 09:00:00").getTime();
      
      function countdown() {
        
        const now = new Date().getTime();
        
        const distance = target - now;
        
        if (distance < 0) {
          
          return;
          
        }
        
        document.getElementById("day").innerHTML = Math.floor(distance / (1000 * 60 * 60 * 24));
        
        document.getElementById("hour").innerHTML = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        
        document.getElementById("minute").innerHTML = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        
        document.getElementById("second").innerHTML = Math.floor((distance % (1000 * 60)) / 1000);
        
      }
      
      countdown();
      
      setInterval(countdown, 1000);
      
      
      /*=====================================
COPY REKENING
=====================================*/

document.querySelectorAll(".copy-btn").forEach((btn) => {
  
  btn.addEventListener("click", () => {
    
    navigator.clipboard.writeText(btn.dataset.copy);
    
    const text = btn.innerHTML;
    
    btn.innerHTML = "✓ Berhasil Disalin";
    
    setTimeout(() => {
      
      btn.innerHTML = text;
      
    }, 2000);
    
  });
  
});

/*=====================================
LIGHTBOX GALLERY
=====================================*/

const images = document.querySelectorAll(".gallery-grid img");

const lightbox = document.createElement("div");

lightbox.id = "lightbox";

lightbox.innerHTML = '<img id="lightbox-img">';

document.body.appendChild(lightbox);

const lightboxImg = document.getElementById("lightbox-img");

images.forEach(img => {
  
  img.addEventListener("click", () => {
    
    lightbox.style.display = "flex";
    
    lightboxImg.src = img.src;
    
  });
  
});

lightbox.addEventListener("click", () => {
  
  lightbox.style.display = "none";
  
});

/*=====================================
BACK TO TOP
=====================================*/

const topBtn = document.createElement("button");

topBtn.id = "topBtn";

topBtn.innerHTML = "↑";

document.body.appendChild(topBtn);

window.addEventListener("scroll", () => {
  
  if (window.scrollY > 500) {
    
    topBtn.classList.add("show");
    
  } else {
    
    topBtn.classList.remove("show");
    
  }
  
});

topBtn.onclick = () => {
  
  window.scrollTo({
    
    top: 0,
    
    behavior: "smooth"
    
  });
  
};

/*=====================================
ROSE PETALS
=====================================*/

function createPetal() {
  
  const petal = document.createElement("div");
  
  petal.className = "petal";
  
  petal.innerHTML = "🌹";
  
  petal.style.left = Math.random() * 100 + "vw";
  
  petal.style.animationDuration = (6 + Math.random() * 4) + "s";
  
  petal.style.fontSize = (16 + Math.random() * 10) + "px";
  
  document.body.appendChild(petal);
  
  setTimeout(() => {
    
    petal.remove();
    
  }, 10000);
  
}

setInterval(createPetal, 2500);

});
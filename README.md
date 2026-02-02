/* NO button runs away 😈 */
const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", () => {
  noBtn.style.left = Math.random() * 80 + "%";
  noBtn.style.top = Math.random() * 80 + "%";
});

/* YES button → secret page 🎁 */
function yesClick() {
  document.getElementById("surprisePage").classList.remove("hidden");
}

/* Typing Love Letter ⌨️ */
const text = `
Dear You ❤️

Every smile of yours
makes my heart a little softer.
Every moment with you
feels like magic ✨

Will you be my Valentine? 🌹

– sara
`;

let index = 0;
function openLetter() {
  const letter = document.querySelector(".letter");
  const typedText = document.getElementById("typedText");
  letter.style.display = "block";
  typedText.innerHTML = "";
  index = 0;

  const typing = setInterval(() => {
    typedText.innerHTML += text[index];
    index++;
    if (index === text.length) clearInterval(typing);
  }, 40);
}

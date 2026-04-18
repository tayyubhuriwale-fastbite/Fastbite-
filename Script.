const menuContainer = document.getElementById("menu");
const searchInput = document.getElementById("search");
const filter = document.getElementById("filter");

function displayItems(items) {
  menuContainer.innerHTML = "";
  
  items.forEach(item => {
    const div = document.createElement("div");
    div.className = "card";
    div.innerHTML = `
      <img src="${item.img}" width="100%">
      <h3>${item.name}</h3>
      <p>₹${item.price}</p>
      <button onclick="order('${item.name}')">Order</button>
    `;
    menuContainer.appendChild(div);
  });
}

function order(item) {
  window.open(`https://wa.me/919529785348?text=I want ${item}`);
}

searchInput.addEventListener("input", update);
filter.addEventListener("change", update);

function update() {
  let filtered = menu;

  const searchValue = searchInput.value.toLowerCase();
  const category = filter.value;

  if (searchValue) {
    filtered = filtered.filter(i => i.name.toLowerCase().includes(searchValue));
  }

  if (category !== "all") {
    filtered = filtered.filter(i => i.category === category);
  }

  displayItems(filtered);
}

displayItems(menu);

# TASK-5-
Fifth and  my last internship task at ApexPlanet 


````html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Intermediate HTML, CSS & JavaScript — Full Project</title>
<style>
  :root{
    --brand:#0f7f78; --muted:#6b7b7a; --bg:#f4f6f7; --card:#ffffff;
    --accent:#0b5e5a; --danger:#d9534f; --success:#2a9d6f; --radius:12px;
    --gap:18px; --text:#133; font-family:"Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  }
  *{box-sizing:border-box}
  body{margin:0; background:linear-gradient(180deg,var(--bg),#eef2f2); color:var(--text); line-height:1.45;}
  .container{max-width:1100px;margin:28px auto;padding:20px;}

  header.site-header{display:flex;align-items:center;justify-content:space-between;gap:12px;
    background:linear-gradient(90deg,var(--brand),var(--accent));color:white;padding:18px;border-radius:16px;}
  .brand{display:flex;align-items:center;gap:12px}
  .logo{width:56px;height:56px;border-radius:10px;background:rgba(255,255,255,0.12);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:20px;}
  nav.primary{display:flex;gap:12px;align-items:center}
  nav.primary a{color:white;text-decoration:none;padding:8px 12px;border-radius:8px;font-weight:600}
  a:focus, button:focus, input:focus, textarea:focus { outline: 3px solid rgba(11,94,90,0.18); outline-offset:2px; }

  .main-grid{display:grid;grid-template-columns:2fr 1fr;gap:var(--gap);margin-top:20px;}
  .card{background:var(--card);border-radius:var(--radius);box-shadow:0 6px 18px rgba(20,40,40,0.06);padding:18px;}
  .muted{color:var(--muted)} .small{font-size:13px}

  /* Product list */
  .product-controls{display:flex;gap:8px;flex-wrap:wrap;align-items:center;margin-bottom:12px}
  .product-controls select, .product-controls input[type="search"]{padding:8px;border-radius:8px;border:1px solid #d6e0df}
  .products-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
  .product{border-radius:10px;border:1px solid #eef2f2;padding:12px;background:linear-gradient(180deg,#fff,#fbfcfc);display:flex;flex-direction:column;gap:8px}
  .product img{width:100%;height:140px;object-fit:cover;border-radius:8px}
  .product .meta{display:flex;justify-content:space-between;align-items:center}
  .product .title{font-weight:700}
  .product .price{font-weight:800}
  .product .actions{display:flex;gap:8px;margin-top:auto}
  .btn{background:var(--brand);color:white;border:none;padding:8px 12px;border-radius:8px;cursor:pointer;font-weight:700}
  .btn.secondary{background:#eef6f5;color:var(--accent);border:1px solid #d2e7e6}
  .chip{padding:4px 8px;border-radius:999px;background:#f2f7f6;border:1px solid #e6efee;font-size:13px}

  @media (max-width:900px){
    .main-grid{grid-template-columns:1fr}
    nav.primary{display:none}
    .products-grid{grid-template-columns:repeat(2,1fr)}
  }
  @media (max-width:520px){
    .products-grid{grid-template-columns:1fr}
  }
</style>
</head>
<body>
  <div class="container">
    <header class="site-header" role="banner">
      <div class="brand">
        <div class="logo" aria-hidden="true">AP</div>
        <div>
          <div style="font-weight:800;font-size:18px">ApexPlanet — Practice Lab</div>
          <div style="font-size:13px;color:rgba(255,255,255,0.9)">Full Project Implementation</div>
        </div>
      </div>
      <nav class="primary" role="navigation" aria-label="Main navigation">
        <a href="#portfolio">Portfolio</a>
        <a href="#todo">To-Do</a>
        <a href="#products">Products</a>
      </nav>
    </header>

    <main>
      <div class="main-grid" role="main">

        <!-- Left: main content (portfolio + product list) -->
        <section class="card" aria-labelledby="aboutTitle">
          <h2 id="aboutTitle">Full Project Implementation</h2>
          <p class="muted">This page contains: a demo portfolio area, a to-do app (localStorage), and a product listing with filters & sorting.</p>

          <!-- Portfolio visual / placeholder -->
          <div style="margin:12px 0;padding:12px;border-radius:10px;background:#f9fffd;border:1px solid #e8f6f5">
  <strong>Portfolio — Apex Planet</strong>
  <div>
    <h3>About Me</h3>
     <h1>Hi, I'm Ritesh Kumar Yadav </h1>
    <p>Web Developer | Learner | Creator</p>

    <p>I’m an aspiring web developer currently learning HTML, CSS, and JavaScript through the ApexPlanet 45-Day Internship Program. I enjoy building creative and functional websites.</p>
    <p class="small muted">(Example placeholder image below.)</p>
  </div>
  <div style="margin-top:10px">
    <img src="/mnt/data/Screenshot 2025-11-17 145516.png" alt="Final Project slide — ApexPlanet" style="width:100%;border-radius:8px;display:block"/>
    <div style="margin-top:16px">
      <h3>My Projects</h3>
      <ul>
        <li><strong>Task -1:</strong> Basic Webpage using HTML, CSS, and JavaScript — a responsive landing page demonstrating layout, typography and simple interactivity.</li>
        <li><strong>Task -2:</strong> Contact form with validation & responsive layout — form fields, client-side validation, and mobile-friendly styling.</li>
        <li><strong>Task -3:</strong> Interactive Quiz App using JavaScript — timed quiz, score tracking, and dynamic feedback for users.</li>
      </ul>
    </div>
  </div>
</div>

          <!-- Product listing (Task 3: product listing page) -->
          <section id="products" aria-labelledby="productsTitle" style="margin-top:18px">
            <h3 id="productsTitle">Product Listing</h3>
            <div class="product-controls" role="region" aria-label="Product filters and sorting">
              <label class="small">Search:
                <input type="search" id="searchInput" placeholder="Search products..." aria-label="Search products">
              </label>

              <label class="small">Category:
                <select id="categorySelect" aria-label="Filter by category">
                  <option value="">All</option>
                </select>
              </label>

              <label class="small">Sort:
                <select id="sortSelect" aria-label="Sort products">
                  <option value="featured">Featured</option>
                  <option value="price-asc">Price: Low → High</option>
                  <option value="price-desc">Price: High → Low</option>
                  <option value="rating-desc">Rating: High → Low</option>
                </select>
              </label>

              <button id="clearFilters" class="btn secondary">Clear</button>
              <div style="margin-left:auto;display:flex;gap:8px;align-items:center">
                <div class="chip" id="resultCount">0 items</div>
                <button id="viewFavorites" class="btn">Favorites</button>
              </div>
            </div>

            <div id="productsGrid" class="products-grid" aria-live="polite"></div>
          </section>

          <!-- To-do list -->
          <aside class="card" id="todo" style="margin-top:18px">
            <div id="todoApp">
              <h3 id="todoTitle">To-Do List (dynamic)</h3>
              <form id="todoForm" class="todo-controls" aria-label="Add task">
                <input id="taskInput" placeholder="Add a new task..." aria-label="Task" required />
                <button class="btn" type="submit">Add</button>
              </form>
              <ul class="todo-list" id="tasks" aria-live="polite" style="margin-top:12px"></ul>
              <div style="margin-top:10px;display:flex;gap:8px;align-items:center">
                <button id="clearCompleted" class="btn secondary" type="button">Clear All</button>
                <div style="flex:1;color:var(--muted);font-size:13px;text-align:right" id="todoCount">0 tasks</div>
              </div>
            </div>
          </aside>
        </section>

        <!-- Right: sidebar -->
        <aside class="card" aria-labelledby="sidebarTitle">
          <h3 id="sidebarTitle">Quick Notes</h3>
          <p class="muted">Tips & reminders for the project:</p>
          <ul style="padding-left:18px;color:var(--muted)">
            <li>Portfolio: include About / Projects / Contact pages.</li>
            <li>To-Do: data persisted using <code>localStorage</code>.</li>
            <li>Products: filtering, sorting, and favorites persisted for the user.</li>
          </ul>
        </aside>
      </div>
    </main>

    <footer class="site-footer" style="text-align:center;color:var(--muted);margin-top:18px">
      <small>&copy; <span id="year"></span> ApexPlanet Software Pvt Ltd — Full Project demo</small>
    </footer>
  </div>

<script>
/* ---------------- Utilities ---------------- */
const $ = id => document.getElementById(id);
$('year').textContent = new Date().getFullYear();

/* ---------------- Sample product data ----------------
   Replace or extend this array with server data or fetched JSON.
*/
const sampleProducts = [
  { id: 'p1', title: 'Ocean T-Shirt', category: 'Clothing', price: 19.99, rating: 4.2, image: 'https://via.placeholder.com/400x300?text=Ocean+T-Shirt' },
  { id: 'p2', title: 'Mountain Hoodie', category: 'Clothing', price: 39.99, rating: 4.7, image: 'https://via.placeholder.com/400x300?text=Mountain+Hoodie' },
  { id: 'p3', title: 'Stellar Mug', category: 'Home', price: 12.50, rating: 4.0, image: 'https://via.placeholder.com/400x300?text=Stellar+Mug' },
  { id: 'p4', title: 'Comet Lamp', category: 'Home', price: 49.95, rating: 4.6, image: 'https://via.placeholder.com/400x300?text=Comet+Lamp' },
  { id: 'p5', title: 'Trail Sneakers', category: 'Footwear', price: 69.00, rating: 4.3, image: 'https://via.placeholder.com/400x300?text=Trail+Sneakers' },
  { id: 'p6', title: 'Cloud Socks (3-pack)', category: 'Footwear', price: 9.99, rating: 4.1, image: 'https://via.placeholder.com/400x300?text=Cloud+Socks' }
];

const STORAGE_FAVS = 'apx_favs_v1';
let products = structuredClone(sampleProducts); // working copy
let favorites = JSON.parse(localStorage.getItem(STORAGE_FAVS) || '[]') || [];

const productsGrid = $('productsGrid');
const categorySelect = $('categorySelect');
const sortSelect = $('sortSelect');
const searchInput = $('searchInput');
const resultCount = $('resultCount');
const clearFiltersBtn = $('clearFilters');
const viewFavoritesBtn = $('viewFavorites');

/* Populate category dropdown */
function populateCategories() {
  const cats = Array.from(new Set(products.map(p => p.category))).sort();
  categorySelect.innerHTML = '<option value="">All</option>' + cats.map(c => `<option value="${c}">${c}</option>`).join('');
}
populateCategories();

/* Render product grid */
function isFavorited(id) { return favorites.includes(id); }

function renderProducts(list) {
  productsGrid.innerHTML = '';
  if (!list.length) {
    productsGrid.innerHTML = `<div class="muted small">No products found — try adjusting filters.</div>`;
    resultCount.textContent = '0 items';
    return;
  }
  resultCount.textContent = `${list.length} item${list.length !== 1 ? 's' : ''}`;
  list.forEach(p => {
    const card = document.createElement('div');
    card.className = 'product';
    card.innerHTML = `
      <img src="${p.image}" alt="${p.title}">
      <div class="meta"><div class="title">${escapeHtml(p.title)}</div><div class="price">$${p.price.toFixed(2)}</div></div>
      <div class="small muted">${escapeHtml(p.category)} · ★${p.rating.toFixed(1)}</div>
      <div class="actions">
        <button class="btn add-btn" data-id="${p.id}">Add (demo)</button>
        <button class="btn secondary fav-btn" data-id="${p.id}" aria-pressed="${isFavorited(p.id)}">${ isFavorited(p.id) ? 'Favorited' : 'Favorite' }</button>
      </div>`;
    productsGrid.appendChild(card);
  });
}

/* Simple escaping (for inserted text) */
function escapeHtml(s){ return String(s).replace(/[&<>"']/g, c=>({ '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;' }[c])); }

/* Filtering & sorting */
function applyFilters() {
  const q = (searchInput.value || '').trim().toLowerCase();
  const cat = categorySelect.value;
  const sort = sortSelect.value;

  let out = products.filter(p => {
    const matchQ = !q || p.title.toLowerCase().includes(q) || p.category.toLowerCase().includes(q);
    const matchCat = !cat || p.category === cat;
    return matchQ && matchCat;
  });

  if (sort === 'price-asc') out.sort((a,b)=>a.price - b.price);
  else if (sort === 'price-desc') out.sort((a,b)=>b.price - a.price);
  else if (sort === 'rating-desc') out.sort((a,b)=>b.rating - a.rating);
  // featured: keep default order

  renderProducts(out);
}

/* Favorites persistence */
function saveFavorites(){
  localStorage.setItem(STORAGE_FAVS, JSON.stringify(favorites));
}

function toggleFavorite(id) {
  const idx = favorites.indexOf(id);
  if (idx === -1) favorites.push(id);
  else favorites.splice(idx, 1);
  saveFavorites();
  applyFilters();
}

/* Event listeners: controls */
searchInput.addEventListener('input', () => applyFilters());
categorySelect.addEventListener('change', () => applyFilters());
sortSelect.addEventListener('change', () => applyFilters());

clearFiltersBtn.addEventListener('click', () => {
  searchInput.value = '';
  categorySelect.value = '';
  sortSelect.value = 'featured';
  applyFilters();
});

/* Event delegation for product actions */
productsGrid.addEventListener('click', (e) => {
  // Favorite button
  const fav = e.target.closest('.fav-btn');
  if (fav) {
    const id = fav.dataset.id;
    toggleFavorite(id);
    return;
  }
  // Add button (demo)
  const add = e.target.closest('.add-btn');
  if (add) {
    const id = add.dataset.id;
    const p = products.find(x=>x.id===id);
    if (p) alert(`(Demo) Adding "${p.title}" — extend to add to cart or server call.`);
  }
});

/* Show favorites view (simple modal-like list via alert for demo) */
viewFavoritesBtn.addEventListener('click', () => {
  if (!favorites.length) { alert('No favorites yet. Click "Favorite" on items to save them.'); return; }
  const favItems = favorites.map(id => products.find(p=>p.id===id)).filter(Boolean).map(p => `${p.title} — $${p.price.toFixed(2)}`).join('\n');
  alert('Favorites:\n' + favItems);
});

/* Init render */
renderProducts(products);
applyFilters();

/* ---------------- To-Do app (localStorage) ---------------- */
const todoForm = document.getElementById('todoForm');
const taskInput = document.getElementById('taskInput');
const tasksEl = document.getElementById('tasks');
const clearAllBtn = document.getElementById('clearCompleted');
const todoCount = document.getElementById('todoCount');
const STORAGE_TODO = 'apx_todo_v1';

let tasks = loadTasks();

function loadTasks() {
  try { return JSON.parse(localStorage.getItem(STORAGE_TODO) || '[]'); }
  catch { return []; }
}
function saveTasksLocal() { localStorage.setItem(STORAGE_TODO, JSON.stringify(tasks)); }

function renderTasks() {
  tasksEl.innerHTML = '';
  if (!tasks.length) {
    const li=document.createElement('li'); li.className='todo-item'; li.textContent='No tasks yet. Add one above!'; tasksEl.appendChild(li);
  } else {
    tasks.forEach((t, idx)=> {
      const li=document.createElement('li'); li.className='todo-item'; li.dataset.index=idx;
      const left=document.createElement('div'); left.className='left';
      const chk=document.createElement('input'); chk.type='checkbox'; chk.checked=!!t.done;
      const span=document.createElement('span'); span.textContent=t.text; span.style.textDecoration = t.done ? 'line-through' : 'none';
      left.appendChild(chk); left.appendChild(span);
      const actions=document.createElement('div'); const del=document.createElement('button'); del.type='button'; del.textContent='Remove'; del.className='remove-btn';
      actions.appendChild(del); li.appendChild(left); li.appendChild(actions); tasksEl.appendChild(li);
      chk.addEventListener('change', ()=> { tasks[idx].done = chk.checked; saveTasksLocal(); renderTasks(); });
      del.addEventListener('click', ()=> { tasks.splice(idx,1); saveTasksLocal(); renderTasks(); });
    });
  }
  todoCount.textContent = `${tasks.length} task${tasks.length !== 1 ? 's' : ''}`;
}

todoForm.addEventListener('submit', (e)=> {
  e.preventDefault();
  const text = taskInput.value.trim();
  if (!text) return;
  tasks.unshift({ text, done:false, created:Date.now() });
  saveTasksLocal();
  taskInput.value=''; taskInput.focus(); renderTasks();
});

clearAllBtn.addEventListener('click', ()=> {
  if (!confirm('Clear all tasks?')) return;
  tasks = []; saveTasksLocal(); renderTasks();
});

renderTasks();

/* ---------------- Small utilities ---------------- */
function structuredClone(obj) { return JSON.parse(JSON.stringify(obj)); }

</script>
</body>
</html>

---
layout: default
title: "GitHub Page Tugas - Profil & Mata Kuliah"
---

<!-- Bro, ini page lo yang paling gyatt, langsung rizz doang! -->

<div class="container">
  <!-- Sidebar: Profil dan foto lo yang paling gigachad -->
  <div class="sidebar">
    <div class="profile">
      <img src="https://via.placeholder.com/150" alt="Foto Profil">
      <h2>Nama Lo, Bro</h2>
      <p>Profil si alpha gen yang skibidi & sigma. Lo ga mau jadi beta, kan?</p>
    </div>
  </div>
  <!-- Konten: List tabs mata kuliah dan nested tabs materi -->
  <div class="content">
    <div class="tabs">
      <div class="tab active" data-tab="subject1">Mata Kuliah 1</div>
      <div class="tab" data-tab="subject2">Mata Kuliah 2</div>
    </div>
    
    <div id="subject1" class="tab-content active">
      <!-- Nested tabs buat materi Mata Kuliah 1 -->
      <div class="nested-tabs">
        <div class="nested-tab active" data-nested="materi1-1">Materi 1.1</div>
        <div class="nested-tab" data-nested="materi1-2">Materi 1.2</div>
      </div>
      <div id="materi1-1" class="nested-content active">
        <p>Konten Materi 1.1, bro. Materi ini udah rizz banget, jadi jangan jadi impostor kalo mau pinter!</p>
      </div>
      <div id="materi1-2" class="nested-content">
        <p>Konten Materi 1.2, skibidi! Ini cuma contoh, jadi ga usah ribet, rizz lo biar ga jadi baby gronk!</p>
      </div>
    </div>
    
    <div id="subject2" class="tab-content">
      <!-- Nested tabs buat materi Mata Kuliah 2 -->
      <div class="nested-tabs">
        <div class="nested-tab active" data-nested="materi2-1">Materi 2.1</div>
        <div class="nested-tab" data-nested="materi2-2">Materi 2.2</div>
      </div>
      <div id="materi2-1" class="nested-content active">
        <p>Konten Materi 2.1, ini dia bro. Materi ini beneran sigma, jangan sampe lo jadi goon yang nyontek!</p>
      </div>
      <div id="materi2-2" class="nested-content">
        <p>Konten Materi 2.2, rizz lo dah, soalnya ini materi yang paling gyatt biar lo makin edge di dunia kuliah!</p>
      </div>
    </div>
  </div>
</div>

<style>
  /* Bro, ini style yang gyatt buat page lo, jangan jadi impostor ya! */
  body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
  }
  .container {
    display: flex;
    height: 100vh;
  }
  .sidebar {
    width: 25%;
    background-color: #333;
    color: #fff;
    padding: 20px;
    box-sizing: border-box;
  }
  .profile {
    text-align: center;
  }
  .profile img {
    border-radius: 50%;
    width: 150px;
    height: 150px;
  }
  .content {
    width: 75%;
    padding: 20px;
    box-sizing: border-box;
  }
  /* Tabs utama buat mata kuliah */
  .tabs {
    display: flex;
    border-bottom: 2px solid #ddd;
    margin-bottom: 20px;
  }
  .tab {
    padding: 10px 20px;
    cursor: pointer;
    background-color: #eee;
    margin-right: 5px;
  }
  .tab.active {
    background-color: #fff;
    border-top: 2px solid #333;
    border-left: 2px solid #333;
    border-right: 2px solid #333;
    border-bottom: none;
  }
  .tab-content {
    display: none;
    padding: 20px;
    background-color: #fff;
    border: 2px solid #333;
  }
  .tab-content.active {
    display: block;
  }
  /* Nested tabs buat materi, biar rizz makin mew */
  .nested-tabs {
    display: flex;
    border-bottom: 1px solid #ccc;
    margin-bottom: 10px;
  }
  .nested-tab {
    padding: 8px 16px;
    cursor: pointer;
    background-color: #ddd;
    margin-right: 5px;
  }
  .nested-tab.active {
    background-color: #bbb;
  }
  .nested-content {
    display: none;
    padding: 10px;
    background-color: #eee;
    border: 1px solid #ccc;
  }
  .nested-content.active {
    display: block;
  }
</style>

<script>
  // JavaScript buat kontrol tab utama, ga usah mumet, bro!
  const tabs = document.querySelectorAll('.tab');
  const tabContents = document.querySelectorAll('.tab-content');

  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      // Hapus kelas aktif dulu, jangan jadi impostor
      tabs.forEach(t => t.classList.remove('active'));
      tabContents.forEach(tc => tc.classList.remove('active'));

      // Tambahin kelas aktif buat tab dan konten yang dipilih
      tab.classList.add('active');
      document.getElementById(tab.getAttribute('data-tab')).classList.add('active');
    });
  });

  // JavaScript buat nested tabs materi, rizzin biar makin mew!
  const nestedTabs = document.querySelectorAll('.nested-tab');
  nestedTabs.forEach(nTab => {
    nTab.addEventListener('click', () => {
      const parent = nTab.closest('.tab-content');
      const allNestedTabs = parent.querySelectorAll('.nested-tab');
      const allNestedContents = parent.querySelectorAll('.nested-content');

      allNestedTabs.forEach(nt => nt.classList.remove('active'));
      allNestedContents.forEach(nc => nc.classList.remove('active'));

      nTab.classList.add('active');
      parent.querySelector('#' + nTab.getAttribute('data-nested')).classList.add('active');
    });
  });
</script>

<!--
  Catatan:
  - Kode ini udah sigma, bro. Lo bisa modifikasi sesuai kebutuhan.
  - Jangan lupa rizz kode lo, jangan sampe jadi baby gronk atau impostor!
  - Selamat belajar dan keep it gyatt, skibidi!
-->

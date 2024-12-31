<style>

@import url("https://fonts.googleapis.com/css?family=Roboto:400,400i,700");

* {
  margin: 0;
  padding: 0;
  font-family: Roboto, sans-serif;
  box-sizing: border-box;
}

main {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #ffffff;
  z-index: -2;
}

.tooltip {
  display: block;
  position: absolute;
  color: #b6b7b7;
  background: #18191c;
  padding: 0.4rem;
  border-radius: 3px;
  max-width: 150px;
  width: max-content;
  font-size: 0.8rem;
  transform: scale(0);
  transition: 0.055s ease-in-out transform;
  z-index: 10;
  box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.35);
  -webkit-box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.35);
}

.tooltip-up {
  bottom: 30px;
}

.tooltip-up::before {
  content: "";
  position: absolute;
  bottom: -5px;
  left: 50%;
  transform: translateX(-50%);
  width: 0;
  height: 0;
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-top: 6px solid #18191c;
}

.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  background-color: #535353;
  padding: 10px;
  border-radius: 3px;
  color: #fff;
  font-size: 0.85rem;
  transition: 0.2s ease-in-out;
  margin-top: 12px;
}

.btn:hover {
  background-color: #747474;
}

/* Card */
.card-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 1450px;
  z-index: 0;
}

.card {
  background: #292b2f;
  width: 345px;
  max-height: 95%;
  height: max-content;
  border-radius: 9px;
  box-shadow: 0px 0px 16px 3px rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 0px 0px 16px 3px rgba(0, 0, 0, 0.2);
  scrollbar-width: none;
}

.card::-webkit-scrollbar {
  display: none;
}

.card-header .banner {
  width: 100%;
  height: 60px;
  background: #ef5b0d;
  border-radius: 6px 6px 0 0;
  overflow: hidden;
}

.card-header .banner-img {
  width: 100%;
  height: 120px;
  background-position: center !important;
  background-size: 100% auto !important;
  border-radius: 6px 6px 0 0;
  overflow: hidden;
}

.card-body {
  padding: 15px;
  position: relative;
}

.card-body .profile-header {
  position: absolute;
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  justify-content: space-between;
  width: calc(100% - 30px);
  top: -50px;
}

.card-body .profile-header .profil-logo {
  position: relative;
  border: 6px solid #292b2f;
  border-radius: 50%;
}

.card-body .profile-header .profil-logo img {
  display: block;
  width: 80px;
  height: 80px;
  border-radius: 50%;
}

.card-body .profile-header .profil-logo::before {
  content: "VIEW PRPFILE";
  position: absolute;
  right: 0;
  top: 0;
  cursor: pointer;
  opacity: 0;
  width: 100%;
  height: 100%;
  color: #eeeeee;
  background: #000000;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  font-size: 0.6rem;
  font-weight: 600;
  text-transform: uppercase;
  transition-duration: 0.15s;
}

.card-body .profile-header .profil-logo:hover::before {
  opacity: 1;
}

.card-body .profile-header .badges-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  max-width: 220px;
  background: #18191c;
  border-radius: 7px;
  padding: 3px;
}

.card-body .profile-header .badges-container .badge-item {
  position: relative;
  margin: 5px;
  width: 15px;
  height: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.card-body .profile-header .badges-container .badge-item img {
  height: 110%;
}

.card-body .profile-header .badges-container .badge-item:hover > .tooltip {
  transform: scale(1);
}

.card-body .profile-body {
  background: #18191c;
  border-radius: 7px;
  padding: 13px;
  margin-top: 40px;
}

.card-body .profile-body .username {
  color: #eeeeee;
  font-weight: 600;
  font-size: 1.3rem;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.card-body .profile-body .username span {
  color: #b9bbbe;
}

.card-body .profile-body .username .badge {
  font-size: 0.65rem;
  background-color: #5865f2;
  text-transform: uppercase;
  font-weight: 300;
  width: max-content;
  padding: 2px 5px;
  margin-left: 5px;
  border-radius: 3px;
}

.card-body .profile-body hr {
  border: none;
  border-top: 0.5px solid #33353b;
}

.card-body .profile-body .category-title {
  color: #d6d6d6;
  font-weight: 700;
  text-transform: uppercase;
  font-size: 0.8rem;
  margin-bottom: 8px;
}

.card-body .profile-body .basic-infos {
  margin-bottom: 14px;
  margin-top: 12px;
}

.card-body .profile-body .basic-infos p {
  color: #bdbebf;
  font-size: 0.9rem;
}

.card-body .profile-body .basic-infos p a {
  color: #02a5e6;
  text-decoration: none;
}

.card-body .profile-body .basic-infos p a:hover {
  text-decoration: underline;
}

.card-body .profile-body .basic-infos p b {
  color: #ddd;
}

.card-body .profile-body .roles {
  margin-bottom: 14px;
}

.card-body .profile-body .roles .roles-list {
  display: flex;
  flex-wrap: wrap;
}

.card-body .profile-body .roles .roles-list .role {
  background: #292b2f;
  color: #c4c4c4;
  border-radius: 3px;
  font-size: 0.75rem;
  font-weight: 300;
  padding: 3px 6px;
  margin-right: 4px;
  margin-top: 4px;
  display: flex;
  align-items: center;
  flex-direction: row;
}

.card-body .profile-body .roles .roles-list .role .role-color {
  position: relative;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  margin-right: 5px;
}

.card-body .profile-body .roles .roles-list .role .role-color:hover::before {
  content: "✕";
  position: relative;
  top: -2px;
  right: 1px;
  font-size: 0.65rem;
  color: #f5f5f5;
  background: rgba(41, 43, 47, 0);
  border-radius: 50%;
  width: 15px;
  height: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.card-body .profile-body .roles .roles-list .role-add {
  cursor: pointer;
}

.card-body .profile-body .note textarea {
  border: none;
  outline: none;
  background: transparent;
  width: 100%;
  min-height: 30px;
  color: #e0e0e0;
  resize: none;
  font-size: 0.8rem;
  border-radius: 3px;
  padding: 5px;
  box-sizing: border-box;
  scrollbar-width: none;
}

.card-body .profile-body .note textarea::-webkit-scrollbar {
  display: none;
}

.card-body .profile-body .note textarea::placeholder {
  font-size: 0.8rem;
}

.card-body .profile-body .note textarea:focus::placeholder {
  opacity: 0;
}

.card-body .profile-body .message input {
  background: transparent;
  outline: none;
  border: 1.2px solid #cf5dca;
  padding: 13px;
  width: 100%;
  border-radius: 4px;
  color: #eeeeee;
  margin-top: 14px;
}
.nitro-card {
  position: relative;
  background-image: linear-gradient(0, #ff8cf9, #f37ff7);
  background-blend-mode: multiply;
  background-color: #0000006c;
}

.nitro-card:before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
  margin: -5px;
  border-radius: 12px;
  background: linear-gradient(0, #ff8cf9, #f37ff7);
}

.nitro-card .card-body .profile-body {
background: linear-gradient(0, #3e2a4488, #8a5b8791);
}

.nitro-card .card-body .profile-header .profil-logo {
  position: relative;
  border-color: transparent;
  z-index: 0;
}

.nitro-card .card-body .profile-header .profil-logo:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
  margin: -6px;
  border-radius: 50%;
  background-color: #cf5dca;
}

.nitro-card .card-body .profile-header .badges-container {
  background: #18191c77;
}

.nitro-card .card-body .profile-body .roles .roles-list .role {
  background: #f796e24d;
  border: 1px solid #fa45fa;
}


</style>
<main>
    <div class="card nitro-card">
        <div class="card-header">
          <div
            style="background: url('/imagenes/banner.gif')"
            class="banner-img">
        </div>
        </div>
        <div class="card-body">
          <div class="profile-header">
            <div class="profil-logo">
              <img src="imagenes/logo.jpg" />
            </div>
          </div>
          <div class="profile-body">
            <div class="username">
              <a> ReLoadX </a>
            </div>
            <p style="color: white;">_reloadx</p>
            <hr style="border-top: 1px solid #fa45fa;"/>
            <div class="basic-infos">
              <div class="category-title">Miembro Desde</div>
              <div style="display: flex; align-items: center;">
              <img src="https://i.ibb.co/HpbSK8B/icons8-discord-16.png" style="margin-right: 10px;">
                  <p style="margin: 0;">Dic 31, 2024</p>
            </div>
            </div>
             <div class="roles">
              <div class="category-title">Roles</div>
              <div class="roles-list">
                <div class="role">
                  <div class="role-color" style="background: lightyellow"></div>
                  <p>JavaScript</p>
                </div>
                <div class="role">
                  <div class="role-color" style="background: darkred"></div>
                  <p>HTML</p>
                </div>
                <div class="role">
                  <div class="role-color" style="background: darkgreen"></div>
                  <p>CSS</p>
                </div>
                <div class="role">
                  <div class="role-color" style="background: yellow"></div>
                  <p>Python</p>
                </div>
                <div class="role">
                  <div class="role-color" style="background: darkblue"></div>
                  <p>C#</p>
                </div>
                <div class="role">
                  <div class="role-color" style="background: orange"></div>
                  <p>Java</p>
                </div>
                <div class="role role-add">
                  <div class="role-add-text">+</div>
                </div>
              </div>
            </div>
            <div class="note">
              <div class="category-title">Notas</div>
               <textarea placeholder="Amo el algodon de azucar"></textarea>
            </div>
            <div class="message">
              <input id="content" type="text" placeholder="Envia Mensaje a @ReloadX"/>
            </div>
          </div>
        </div>
      </div>
</main>

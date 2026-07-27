<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>로그인 · 전력노조 집행부 업무포털</title>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-auth-compat.js"></script>
  <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --blue: #1a73e8;
      --blue-dk: #1557b0;
      --ink: #202124;
      --ink2: #5f6368;
      --line: #dadce0;
      --bg: #f1f3f4;
      --white: #ffffff;
      --red: #d93025;
    }
    body {
      font-family: 'Pretendard', 'Malgun Gothic', sans-serif;
      background: var(--bg);
      color: var(--ink);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }
    .card {
      background: var(--white);
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: 34px 28px;
      width: 100%;
      max-width: 380px;
      box-shadow: 0 8px 30px rgba(0,0,0,.08);
    }
    .logo-icon { width: 52px; height: 52px; border-radius: 14px; overflow: hidden; margin: 0 auto 16px; }
    .logo-icon img { width: 100%; height: 100%; object-fit: contain; }
    h1 { font-size: 18px; font-weight: 800; text-align: center; letter-spacing: -0.3px; }
    .sub { font-size: 13px; color: var(--ink2); text-align: center; margin-top: 6px; margin-bottom: 24px; line-height: 1.5; }
    label { display: block; font-size: 12.5px; font-weight: 700; color: var(--ink2); margin-bottom: 6px; }
    input[type=email], input[type=password] {
      width: 100%;
      padding: 13px 14px;
      font-size: 15px;
      font-family: inherit;
      border: 1px solid var(--line);
      border-radius: 10px;
      background: var(--white);
      color: var(--ink);
      margin-bottom: 14px;
    }
    input:focus { outline: none; border-color: var(--blue); box-shadow: 0 0 0 3px rgba(26,115,232,.15); }
    .btn {
      width: 100%;
      padding: 14px;
      font-size: 15px;
      font-weight: 700;
      font-family: inherit;
      background: var(--blue);
      color: #fff;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background .15s;
    }
    .btn:hover { background: var(--blue-dk); }
    .btn:disabled { background: #b7c8ea; cursor: default; }
    .err {
      color: var(--red);
      font-size: 13px;
      font-weight: 600;
      margin-top: 12px;
      text-align: center;
      min-height: 18px;
    }
    .foot { text-align: center; font-size: 11.5px; color: var(--ink2); margin-top: 20px; }
  </style>
</head>
<body>

  <div class="card">
    <div class="logo-icon"><img src="https://knewu.netlify.app/icon-192.png" alt="로고"></div>
    <h1>전국전력노동조합 <br> 집행부 업무포털</h1>
    <div class="sub">등록된 이메일과 비밀번호로 로그인하세요</div>

    <label for="email">이메일</label>
    <input type="email" id="email" placeholder="이름@회사도메인" autocomplete="username">

    <label for="pw">비밀번호</label>
    <input type="password" id="pw" placeholder="비밀번호" autocomplete="current-password">

    <button class="btn" id="loginBtn" onclick="doLogin()">로그인</button>
    <div class="err" id="errMsg"></div>

    <div class="foot">외부 공개 금지 · 집행부 내부 시스템</div>
  </div>

  <script>
    const firebaseConfig = {
        apiKey: "AIzaSyDUFwsNEBzTZxr8EJuY2BZkYTEBadQoMk8",
        authDomain: "knewu-64318.firebaseapp.com",
        databaseURL: "https://knewu-64318-default-rtdb.asia-southeast1.firebasedatabase.app",
        projectId: "knewu-64318",
        storageBucket: "knewu-64318.firebasestorage.app",
        messagingSenderId: "301755569133",
        appId: "1:301755569133:web:9bd85133d084c041368de4"
    };
    firebase.initializeApp(firebaseConfig);

    // 이미 로그인되어 있으면 원래 가려던 페이지(혹은 포털 첫 화면)로 바로 이동
    firebase.auth().onAuthStateChanged(function (user) {
      if (user) {
        goBack();
      }
    });

    function goBack() {
      let back = null;
      try { back = sessionStorage.getItem('knewu_redirect'); sessionStorage.removeItem('knewu_redirect'); } catch (e) {}
      window.location.href = back || 'index.html';
    }

    function doLogin() {
      const email = document.getElementById('email').value.trim();
      const pw = document.getElementById('pw').value;
      const btn = document.getElementById('loginBtn');
      const err = document.getElementById('errMsg');
      err.textContent = '';

      if (!email || !pw) {
        err.textContent = '이메일과 비밀번호를 입력해 주세요.';
        return;
      }

      btn.disabled = true;
      btn.textContent = '로그인 중…';

      firebase.auth().signInWithEmailAndPassword(email, pw)
        .then(() => { goBack(); })
        .catch((error) => {
          btn.disabled = false;
          btn.textContent = '로그인';
          if (error.code === 'auth/invalid-email') err.textContent = '이메일 형식이 올바르지 않습니다.';
          else if (error.code === 'auth/user-not-found' || error.code === 'auth/invalid-credential') err.textContent = '등록되지 않은 이메일이거나 비밀번호가 틀렸습니다.';
          else if (error.code === 'auth/wrong-password') err.textContent = '비밀번호가 틀렸습니다.';
          else if (error.code === 'auth/too-many-requests') err.textContent = '시도가 너무 많습니다. 잠시 후 다시 시도해 주세요.';
          else err.textContent = '로그인에 실패했습니다: ' + error.message;
        });
    }

    document.getElementById('pw').addEventListener('keydown', (e) => {
      if (e.key === 'Enter') doLogin();
    });
  </script>
</body>
</html>

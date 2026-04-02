<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>EduBuild — Eco Green by Modou Jaw</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,400;0,600;0,700;0,800;0,900;1,700&family=Lora:ital,wght@0,600;0,700;1,600&display=swap" rel="stylesheet" />
<style>
:root {
  --green: #1a9e5c;
  --green2: #25c270;
  --green3: #d4f5e2;
  --green4: #edfaf3;
  --amber: #f4a429;
  --indigo: #7c6ff7;
  --bg: #f5fbf7;
  --surface: #ffffff;
  --surface2: #f0faf5;
  --border: #d0ead9;
  --border2: #a8d8bc;
  --text: #1a3328;
  --text2: #3a6b52;
  --text3: #7aaa90;
  --shadow: 0 4px 24px rgba(26,158,92,0.10);
  --shadow2: 0 8px 40px rgba(26,158,92,0.16);
  --theme-transition: background 0.3s, color 0.3s, border-color 0.3s, box-shadow 0.3s;
}

[data-theme="dark"] {
  --green: #2ecc7a;
  --green2: #3de08a;
  --green3: #0d3324;
  --green4: #0a2a1d;
  --bg: #0e1812;
  --surface: #152218;
  --surface2: #111e15;
  --border: #1e3a28;
  --border2: #2a5238;
  --text: #d4f0e2;
  --text2: #8ecfaa;
  --text3: #4a8a66;
  --shadow: 0 4px 24px rgba(0,0,0,0.35);
  --shadow2: 0 8px 40px rgba(0,0,0,0.5);
}

*, *::before, *::after {
  transition: var(--theme-transition);
}

/* THEME TOGGLE */
.theme-toggle{width:42px;height:42px;border-radius:50%;border:1.5px solid var(--border2);background:var(--surface);color:var(--text2);font-size:18px;cursor:pointer;display:flex;align-items:center;justify-content:center;flex-shrink:0;box-shadow:var(--shadow);transition:all 0.2s;}
.theme-toggle:hover{border-color:var(--green);background:var(--green4);transform:rotate(20deg) scale(1.08);}
[data-theme="dark"] .theme-toggle{border-color:var(--border2);background:var(--surface2);}
*{box-sizing:border-box;margin:0;padding:0;}
/* Prevent transition flash on page load */
.no-transition, .no-transition *{transition:none!important;}
html{scroll-behavior:smooth;}
body{background:var(--bg);color:var(--text);font-family:'Nunito',sans-serif;overflow-x:hidden;min-height:100vh;}
::selection{background:#25c27044;color:var(--green);}
::-webkit-scrollbar{width:5px;}
::-webkit-scrollbar-track{background:var(--bg);}
::-webkit-scrollbar-thumb{background:var(--border2);border-radius:10px;}
::-webkit-scrollbar-thumb:hover{background:var(--green);}

/* NAV */
#navbar{position:fixed;top:0;left:0;right:0;z-index:1000;display:flex;align-items:center;justify-content:space-between;padding:0 36px;height:66px;background:rgba(245,251,247,0.93);backdrop-filter:blur(18px);border-bottom:1px solid var(--border);box-shadow:0 2px 16px rgba(26,158,92,0.07);}
[data-theme="dark"] #navbar{background:rgba(14,24,18,0.93);}
.nav-logo{display:flex;align-items:center;gap:10px;cursor:pointer;text-decoration:none;}
.nav-leaf{font-size:28px;animation:leafWiggle 3s ease-in-out infinite;display:inline-block;}
.nav-brand{font-family:'Lora',serif;font-size:20px;color:var(--green);font-weight:700;}
.nav-tagline{font-size:10px;color:var(--text3);letter-spacing:0.5px;font-weight:600;}
.nav-links{display:flex;gap:4px;}
.nav-btn{padding:8px 16px;border-radius:20px;border:1.5px solid transparent;background:transparent;color:var(--text2);font-family:'Nunito',sans-serif;font-size:13px;font-weight:700;cursor:pointer;transition:all 0.2s;}
.nav-btn:hover{background:var(--green4);color:var(--green);}
.nav-btn.active{border-color:var(--green);color:var(--green);background:var(--green4);}
.nav-cta{padding:10px 22px;border-radius:20px;border:none;background:var(--green);color:#fff;font-family:'Nunito',sans-serif;font-size:13px;font-weight:800;cursor:pointer;transition:all 0.2s;box-shadow:0 4px 16px #1a9e5c44;}
.nav-cta:hover{background:var(--green2);transform:translateY(-2px);box-shadow:0 8px 24px #25c27055;}

/* PAGES */
.page{display:none;padding-top:66px;}
.page.active{display:block;}

/* HERO */
#hero-page{padding-top:0;min-height:100vh;position:relative;overflow:hidden;}
.hero-shapes{position:absolute;inset:0;pointer-events:none;overflow:hidden;}
.shape{position:absolute;border-radius:50%;opacity:0.4;}
.s1{width:500px;height:500px;top:-160px;right:-100px;background:radial-gradient(circle,#c8f5de,transparent 70%);animation:shapeFloat 14s ease-in-out infinite;}
.s2{width:350px;height:350px;bottom:-80px;left:-80px;background:radial-gradient(circle,#d0eefc,transparent 70%);animation:shapeFloat 18s ease-in-out infinite reverse;}
.s3{width:220px;height:220px;top:55%;left:28%;background:radial-gradient(circle,#fef3d0,transparent 70%);animation:shapeFloat 22s ease-in-out infinite 3s;}
.dots{position:absolute;inset:0;opacity:0.2;background-image:radial-gradient(circle,#1a9e5c 1.5px,transparent 1.5px);background-size:38px 38px;}

.hero-content{position:relative;z-index:1;max-width:860px;margin:0 auto;padding:110px 36px 80px;text-align:center;}

.creator-badge{display:inline-flex;align-items:center;gap:8px;padding:9px 20px;border-radius:50px;background:var(--surface);border:1.5px solid var(--border2);font-size:13px;color:var(--text2);font-weight:700;margin-bottom:30px;animation:fadeUp 0.5s ease both;box-shadow:var(--shadow);}

.hero-emoji{font-size:72px;display:block;margin-bottom:18px;animation:floatBounce 4s ease-in-out infinite;filter:drop-shadow(0 8px 20px #1a9e5c33);}

.hero-headline{font-family:'Lora',serif;font-size:clamp(38px,7vw,74px);font-weight:700;line-height:1.1;margin-bottom:14px;animation:fadeUp 0.6s 0.1s ease both;color:var(--text);}
.eco-word{color:var(--green);font-style:italic;}

.hero-tagline{font-size:clamp(15px,2.2vw,19px);color:var(--text2);margin-bottom:14px;animation:fadeUp 0.6s 0.2s ease both;font-weight:700;line-height:1.6;}
.hero-mission{font-size:16px;color:var(--text3);max-width:510px;margin:0 auto 48px;line-height:1.9;animation:fadeUp 0.6s 0.3s ease both;font-weight:600;}

.hero-btns{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;animation:fadeUp 0.6s 0.4s ease both;margin-bottom:70px;}
.btn-big{padding:16px 34px;border-radius:50px;border:none;background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;font-family:'Nunito',sans-serif;font-size:15px;font-weight:800;cursor:pointer;box-shadow:0 6px 30px #1a9e5c44;transition:all 0.25s;}
.btn-big:hover{transform:translateY(-3px);box-shadow:0 12px 40px #25c27055;}
.btn-outline{padding:16px 34px;border-radius:50px;border:2px solid var(--border2);background:var(--surface);color:var(--text2);font-family:'Nunito',sans-serif;font-size:15px;font-weight:700;cursor:pointer;transition:all 0.25s;}
.btn-outline:hover{border-color:var(--green);color:var(--green);background:var(--green4);}

.hero-stats{display:flex;justify-content:center;gap:48px;flex-wrap:wrap;animation:fadeUp 0.6s 0.5s ease both;padding-bottom:80px;}
.stat{text-align:center;}
.stat-num{font-family:'Lora',serif;font-size:38px;color:var(--green);font-weight:700;line-height:1;}
.stat-lbl{font-size:12px;color:var(--text3);font-weight:700;margin-top:4px;}

/* HOW IT WORKS */
.how-section{padding:80px 36px;max-width:1080px;margin:0 auto;}
.sec-tag{display:inline-block;padding:5px 16px;border-radius:50px;background:var(--green3);color:var(--green);font-size:12px;font-weight:800;letter-spacing:0.5px;margin-bottom:14px;}
.sec-heading{font-family:'Lora',serif;font-size:clamp(26px,4vw,40px);font-weight:700;margin-bottom:44px;line-height:1.25;color:var(--text);}
.sec-heading em{color:var(--green);font-style:italic;}

.how-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:20px;}
.how-card{background:var(--surface);border:1.5px solid var(--border);border-radius:24px;padding:30px 24px;transition:all 0.28s;cursor:pointer;position:relative;overflow:hidden;}
.how-card::after{content:'';position:absolute;bottom:0;left:0;right:0;height:4px;background:var(--cc,var(--green));transform:scaleX(0);transform-origin:left;transition:transform 0.3s;border-radius:0 0 24px 24px;}
.how-card:hover{transform:translateY(-6px);box-shadow:var(--shadow2);border-color:var(--border2);}
.how-card:hover::after{transform:scaleX(1);}
.how-num{font-size:11px;font-weight:800;letter-spacing:2px;color:var(--text3);margin-bottom:18px;}
.how-emoji{font-size:38px;display:block;margin-bottom:12px;}
.how-title{font-family:'Lora',serif;font-size:19px;font-weight:700;margin-bottom:10px;color:var(--text);}
.how-desc{font-size:14px;color:var(--text2);line-height:1.85;font-weight:600;}

/* MANIFESTO */
.manifesto{padding:80px 36px;text-align:center;background:linear-gradient(135deg,#edfaf3,#f0faf5);border-top:1px solid var(--border);border-bottom:1px solid var(--border);}
.man-emoji{font-size:64px;display:block;margin-bottom:22px;animation:floatBounce 5s ease-in-out infinite;}
.man-title{font-family:'Lora',serif;font-size:clamp(20px,3.5vw,34px);font-weight:700;line-height:1.45;max-width:680px;margin:0 auto 18px;color:var(--text);}
.man-title em{color:var(--green);font-style:italic;}
.man-body{font-size:15px;color:var(--text2);max-width:470px;margin:0 auto 34px;line-height:1.9;font-weight:600;}
.pills{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;}
.pill{padding:9px 20px;border-radius:50px;background:var(--surface);border:1.5px solid var(--border2);font-size:13px;color:var(--text2);font-weight:700;transition:all 0.2s;cursor:default;}
.pill:hover{background:var(--green4);border-color:var(--green);color:var(--green);}

/* TEAM */
.team-section{padding:80px 36px;max-width:800px;margin:0 auto;text-align:center;}
.team-card{background:var(--surface);border:1.5px solid var(--border);border-radius:28px;padding:40px 36px;display:flex;flex-direction:column;align-items:center;gap:14px;box-shadow:var(--shadow);max-width:460px;margin:32px auto 0;transition:all 0.28s;}
.team-card:hover{box-shadow:var(--shadow2);transform:translateY(-4px);}
.team-ava{width:80px;height:80px;border-radius:50%;background:linear-gradient(135deg,var(--green),var(--green2));display:flex;align-items:center;justify-content:center;font-size:36px;box-shadow:0 6px 24px #1a9e5c44;}
.team-name{font-family:'Lora',serif;font-size:22px;font-weight:700;color:var(--text);}
.team-role{font-size:13px;color:var(--green);font-weight:800;background:var(--green3);padding:5px 16px;border-radius:50px;}
.team-bio{font-size:14px;color:var(--text2);line-height:1.85;font-weight:600;max-width:340px;}
.team-btns{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;}
.team-btn{padding:9px 18px;border-radius:20px;border:1.5px solid var(--border2);background:var(--surface);color:var(--text2);font-size:13px;font-weight:700;cursor:pointer;transition:all 0.2s;font-family:'Nunito',sans-serif;}
.team-btn:hover{border-color:var(--green);color:var(--green);background:var(--green4);}

/* FOOTER */
footer{border-top:1px solid var(--border);padding:44px 36px;text-align:center;background:var(--surface2);}
.foot-logo{font-family:'Lora',serif;font-size:22px;color:var(--green);margin-bottom:6px;font-weight:700;}
.foot-tag{font-size:14px;color:var(--text3);font-style:italic;margin-bottom:5px;font-weight:600;}
.foot-credit{font-size:13px;color:var(--text3);margin-bottom:22px;font-weight:700;}
.foot-credit span{color:var(--green);}
.foot-nav{display:flex;gap:24px;justify-content:center;margin-bottom:20px;flex-wrap:wrap;}
.foot-nav a{color:var(--text3);text-decoration:none;font-size:13px;font-weight:700;transition:color 0.2s;cursor:pointer;}
.foot-nav a:hover{color:var(--green);}
.foot-copy{font-size:12px;color:var(--text3);}

/* APP */
#app-section{padding-top:66px;min-height:100vh;background:var(--bg);}
.app-wrap{max-width:920px;margin:0 auto;padding:40px 24px;}
.app-title{font-family:'Lora',serif;font-size:28px;font-weight:700;color:var(--text);margin-bottom:6px;}
.app-sub{font-size:14px;color:var(--text3);margin-bottom:36px;font-weight:600;}

.step-row{display:flex;align-items:center;gap:10px;margin-bottom:18px;}
.step-bub{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:800;color:#fff;flex-shrink:0;}
.step-lbl{font-size:12px;font-weight:800;color:var(--text2);letter-spacing:0.5px;text-transform:uppercase;}

.field-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:14px;margin-bottom:32px;}
.field-card{background:var(--surface);border:2px solid var(--border);border-radius:20px;padding:22px 18px;cursor:pointer;transition:all 0.22s;}
.field-card:hover{border-color:var(--border2);transform:translateY(-2px);box-shadow:var(--shadow);}
.fi{font-size:32px;margin-bottom:10px;display:block;}
.fn{font-weight:800;font-size:14px;margin-bottom:4px;}
.ff{font-size:11px;color:var(--text3);line-height:1.6;font-weight:600;margin-top:8px;background:var(--bg);padding:8px 10px;border-radius:10px;}

.topics-wrap{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:28px;}
.topic-btn{padding:8px 16px;border-radius:20px;border:1.5px solid var(--border);background:var(--surface);color:var(--text2);font-size:13px;font-weight:700;cursor:pointer;transition:all 0.15s;font-family:'Nunito',sans-serif;}
.topic-btn:hover{border-color:var(--border2);background:var(--green4);color:var(--green);}
.topic-btn.sel{background:var(--green4);color:var(--green);}

.level-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;max-width:460px;margin-bottom:32px;}
.level-card{display:flex;align-items:center;gap:12px;padding:14px 16px;border-radius:16px;border:2px solid var(--border);background:var(--surface);cursor:pointer;transition:all 0.15s;}
.level-card:hover{border-color:var(--border2);background:var(--green4);}
.lname{font-weight:800;font-size:13px;}
.ldesc{font-size:11px;color:var(--text3);font-weight:600;}

.gen-btn{width:100%;max-width:460px;padding:17px;border-radius:16px;border:none;font-family:'Nunito',sans-serif;font-weight:800;font-size:15px;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:10px;transition:all 0.25s;margin-bottom:40px;background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;box-shadow:0 6px 28px #1a9e5c44;}
.gen-btn:hover:not(:disabled){transform:translateY(-2px);box-shadow:0 10px 36px #25c27055;}
.gen-btn:disabled{background:var(--border);color:var(--text3);cursor:not-allowed;box-shadow:none;}

.div-lbl{display:flex;align-items:center;gap:14px;margin-bottom:22px;}
.div-line{height:1px;flex:1;background:var(--border);}
.div-txt{font-size:11px;color:var(--text3);font-weight:800;letter-spacing:1px;}

.ideas-grid{display:grid;gap:18px;}
.idea-card{background:var(--surface);border-radius:20px;overflow:hidden;border:1.5px solid var(--border);transition:all 0.22s;}
.idea-card:hover{border-color:var(--border2);transform:translateY(-3px);box-shadow:var(--shadow2);}
.idea-bar{height:5px;}
.idea-body{padding:22px 24px;}
.idea-meta{font-size:11px;font-weight:800;margin-bottom:8px;letter-spacing:0.5px;}
.idea-title{font-family:'Lora',serif;font-size:20px;font-weight:700;color:var(--text);margin-bottom:10px;line-height:1.3;}
.idea-desc{color:var(--text2);font-size:14px;line-height:1.85;margin-bottom:16px;font-weight:600;}
.tech-tags{display:flex;flex-wrap:wrap;gap:7px;margin-bottom:16px;}
.tech-tag{padding:5px 14px;border-radius:20px;font-size:12px;font-weight:700;}
.idea-impact{background:var(--green4);border-radius:12px;padding:10px 14px;font-size:13px;color:var(--text2);margin-bottom:18px;font-weight:600;border:1px solid var(--green3);}
.idea-actions{display:flex;gap:10px;flex-wrap:wrap;}
.btn-eco{flex:1;min-width:180px;padding:12px;border-radius:12px;border:none;background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;font-family:'Nunito',sans-serif;font-weight:800;font-size:13px;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:7px;box-shadow:0 4px 16px #1a9e5c33;transition:all 0.2s;}
.btn-eco:hover{transform:translateY(-2px);box-shadow:0 8px 28px #25c27055;}
.btn-save{padding:12px 20px;border-radius:12px;font-family:'Nunito',sans-serif;font-size:13px;cursor:pointer;font-weight:700;transition:all 0.15s;}
.regen-btn{margin-top:16px;width:100%;padding:14px;border-radius:12px;border:2px solid var(--border);background:var(--surface);color:var(--text3);font-family:'Nunito',sans-serif;font-size:13px;font-weight:700;cursor:pointer;transition:all 0.2s;}
.regen-btn:hover{border-color:var(--green);color:var(--green);background:var(--green4);}

/* CHAT */
#chat-section{display:none;padding-top:66px;height:100vh;flex-direction:column;}
#chat-section.active{display:flex;}
.chat-wrap{flex:1;display:flex;flex-direction:column;max-width:720px;width:100%;margin:0 auto;padding:0 20px;overflow:hidden;}
.chat-head{display:flex;align-items:center;gap:14px;padding:18px 0 14px;border-bottom:1px solid var(--border);flex-shrink:0;}
.eco-ava{width:52px;height:52px;border-radius:50%;background:linear-gradient(135deg,var(--green),var(--green2));display:flex;align-items:center;justify-content:center;font-size:26px;flex-shrink:0;box-shadow:0 4px 20px #1a9e5c44;animation:ecoPulse 3s infinite;}
.eco-name{font-family:'Lora',serif;font-size:18px;font-weight:700;color:var(--green);}
.eco-status{font-size:12px;color:var(--text3);display:flex;align-items:center;gap:6px;font-weight:700;}
.sdot{width:7px;height:7px;border-radius:50%;background:var(--green2);animation:pulse 2s infinite;}
.build-chip{background:var(--green4);border:1.5px solid var(--green3);border-radius:12px;padding:8px 12px;font-size:11px;color:var(--green);max-width:160px;text-align:right;flex-shrink:0;margin-left:auto;line-height:1.6;font-weight:700;}

.qprompts{padding:12px 0 6px;display:flex;flex-wrap:wrap;gap:7px;flex-shrink:0;}
.qp{padding:8px 14px;border-radius:20px;border:1.5px solid var(--border);background:var(--surface);color:var(--text2);font-size:12px;font-weight:700;cursor:pointer;font-family:'Nunito',sans-serif;transition:all 0.15s;}
.qp:hover{border-color:var(--green);color:var(--green);background:var(--green4);}

.chat-msgs{flex:1;overflow-y:auto;padding:14px 0;display:flex;flex-direction:column;gap:14px;}
.msg-row{display:flex;gap:10px;animation:fadeUp 0.2s ease;}
.msg-row.user{flex-direction:row-reverse;}
.msg-ava{width:34px;height:34px;border-radius:50%;background:linear-gradient(135deg,var(--green),var(--green2));display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0;}
.bubble{max-width:76%;padding:13px 16px;font-size:14px;line-height:1.8;border-radius:18px;font-weight:600;}
.bubble.eco{background:var(--surface);border:1.5px solid var(--border);color:var(--text2);border-radius:4px 18px 18px 18px;box-shadow:0 2px 10px rgba(0,0,0,0.05);}
.bubble.user{background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;border-radius:18px 18px 4px 18px;box-shadow:0 4px 16px #1a9e5c33;}
.typing-bub{background:var(--surface);border:1.5px solid var(--border);border-radius:4px 18px 18px 18px;padding:14px 18px;box-shadow:0 2px 10px rgba(0,0,0,0.05);}
.typing-dots{display:inline-flex;gap:5px;align-items:center;}
.dot{width:8px;height:8px;border-radius:50%;background:var(--green2);}
.dot:nth-child(1){animation:dotBounce 1.2s 0s infinite ease-in-out;}
.dot:nth-child(2){animation:dotBounce 1.2s 0.2s infinite ease-in-out;}
.dot:nth-child(3){animation:dotBounce 1.2s 0.4s infinite ease-in-out;}

.chat-input-bar{padding:14px 0 22px;border-top:1px solid var(--border);display:flex;gap:10px;align-items:flex-end;flex-shrink:0;}
.chat-ta{flex:1;background:var(--surface);border:1.5px solid var(--border);border-radius:16px;padding:13px 17px;color:var(--text);font-family:'Nunito',sans-serif;font-size:14px;resize:none;outline:none;line-height:1.6;max-height:110px;overflow-y:auto;transition:border-color 0.2s;font-weight:600;}
.chat-ta:focus{border-color:var(--green);box-shadow:0 0 0 3px #1a9e5c18;}
.chat-ta::placeholder{color:var(--text3);}
.send-btn{width:48px;height:48px;border-radius:50%;border:none;font-size:18px;display:flex;align-items:center;justify-content:center;cursor:pointer;flex-shrink:0;transition:all 0.2s;}
.send-btn.ready{background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;box-shadow:0 4px 16px #1a9e5c44;}
.send-btn.ready:hover{transform:translateY(-2px);box-shadow:0 8px 24px #25c27055;}
.send-btn.off{background:var(--border);color:var(--text3);cursor:not-allowed;}

/* SAVED */
#saved-section{display:none;padding-top:66px;min-height:100vh;background:var(--bg);}
#saved-section.active{display:block;}
.saved-wrap{max-width:920px;margin:0 auto;padding:40px 24px;}
.saved-title{font-family:'Lora',serif;font-size:28px;font-weight:700;margin-bottom:6px;}
.saved-sub{font-size:14px;color:var(--text3);margin-bottom:32px;font-weight:600;}
.empty-box{text-align:center;padding:80px 0;}
.empty-icon{font-size:60px;margin-bottom:16px;display:block;}
.empty-txt{color:var(--text3);font-size:15px;margin-bottom:28px;font-weight:600;}
.saved-grid{display:grid;gap:16px;}
.saved-card{background:var(--surface);border:1.5px solid var(--border);border-radius:20px;overflow:hidden;transition:all 0.2s;}
.saved-card:hover{border-color:var(--border2);box-shadow:var(--shadow);}

/* CONFETTI */
#confetti-layer{position:fixed;inset:0;pointer-events:none;z-index:9999;}
.cp{position:absolute;animation:confettiFall 2s forwards;}

/* SPINNER */
.spinner{display:inline-block;width:18px;height:18px;border:2px solid rgba(255,255,255,0.3);border-top-color:#fff;border-radius:50%;animation:spin 0.8s linear infinite;}

@keyframes fadeUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
@keyframes floatBounce{0%,100%{transform:translateY(0)}50%{transform:translateY(-14px)}}
@keyframes leafWiggle{0%,100%{transform:rotate(-5deg)}50%{transform:rotate(5deg)}}
@keyframes shapeFloat{0%,100%{transform:translate(0,0)}33%{transform:translate(20px,-14px)}66%{transform:translate(-14px,20px)}}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.35}}
@keyframes ecoPulse{0%,100%{box-shadow:0 4px 20px #1a9e5c33}50%{box-shadow:0 4px 28px #1a9e5c77}}
@keyframes dotBounce{0%,80%,100%{transform:translateY(0)}40%{transform:translateY(-8px)}}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes confettiFall{0%{opacity:1;transform:translateY(0) rotate(0deg)}100%{opacity:0;transform:translateY(180px) rotate(720deg) scale(0.3)}}

@media(max-width:640px){
  #navbar{padding:0 16px;}
  .nav-links{display:none;}
  .hero-content{padding:90px 20px 60px;}
  .hero-stats{gap:28px;}
  .how-section,.manifesto,.team-section{padding:60px 20px;}
  .app-wrap,.saved-wrap{padding:28px 16px;}
}

/* API KEY OVERLAY */
#key-overlay{position:fixed;inset:0;z-index:99999;background:rgba(0,0,0,0.55);backdrop-filter:blur(6px);display:none;align-items:center;justify-content:center;padding:20px;}
.key-box{background:var(--surface);border:1.5px solid var(--border2);border-radius:24px;padding:36px 32px;max-width:420px;width:100%;box-shadow:var(--shadow2);text-align:center;}
.key-icon{font-size:44px;display:block;margin-bottom:14px;}
.key-title{font-family:'Lora',serif;font-size:22px;font-weight:700;color:var(--text);margin-bottom:8px;}
.key-sub{font-size:14px;color:var(--text3);margin-bottom:22px;line-height:1.7;font-weight:600;}
.key-input{width:100%;padding:13px 16px;border-radius:12px;border:1.5px solid var(--border2);background:var(--bg);color:var(--text);font-family:'Nunito',sans-serif;font-size:14px;outline:none;margin-bottom:14px;font-weight:600;}
.key-input:focus{border-color:var(--green);box-shadow:0 0 0 3px #1a9e5c18;}
.key-btns{display:flex;gap:10px;}
.key-save{flex:1;padding:13px;border-radius:12px;border:none;background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;font-family:'Nunito',sans-serif;font-weight:800;font-size:14px;cursor:pointer;}
.key-cancel{padding:13px 18px;border-radius:12px;border:1.5px solid var(--border2);background:var(--surface);color:var(--text3);font-family:'Nunito',sans-serif;font-weight:700;font-size:14px;cursor:pointer;}
.key-cancel:hover{border-color:var(--green);color:var(--green);}
.key-hint{font-size:11px;color:var(--text3);margin-top:14px;font-weight:600;}
.key-hint a{color:var(--green);text-decoration:none;}
/* Settings gear in navbar */
.key-btn{width:42px;height:42px;border-radius:50%;border:1.5px solid var(--border2);background:var(--surface);color:var(--text2);font-size:16px;cursor:pointer;display:flex;align-items:center;justify-content:center;flex-shrink:0;transition:all 0.2s;}
.key-btn:hover{border-color:var(--green);background:var(--green4);}
</style>
</head>
<body>

<div id="confetti-layer"></div>

<nav id="navbar">
  <a class="nav-logo" onclick="showPage('hero')">
    <span class="nav-leaf">🌿</span>
    <div>
      <div class="nav-brand">EduBuild</div>
      <div class="nav-tagline">Eco Green Engineering Hub</div>
    </div>
  </a>
  <div class="nav-links">
    <button class="nav-btn" id="nb-hero" onclick="showPage('hero')">Home</button>
    <button class="nav-btn" id="nb-app" onclick="showPage('app')">💡 Ideas</button>
    <button class="nav-btn" id="nb-chat" onclick="showPage('chat')">🌿 Eco Green</button>
    <button class="nav-btn" id="nb-saved" onclick="showPage('saved')">📌 Saved</button>
  </div>
  <div style="display:flex;align-items:center;gap:10px;">
    <button class="key-btn" onclick="promptForKey()" title="Set Gemini API Key">🔑</button>
    <button class="theme-toggle" id="theme-btn" onclick="toggleTheme()" title="Toggle dark/light mode">🌙</button>
    <button class="nav-cta" onclick="showPage('app')">Start Building ✨</button>
  </div>
</nav>

<!-- HERO -->
<section id="hero-page" class="page active">
  <div class="hero-shapes">
    <div class="dots"></div>
    <div class="shape s1"></div>
    <div class="shape s2"></div>
    <div class="shape s3"></div>
  </div>
  <div class="hero-content">
    <div class="creator-badge">
      👑 &nbsp;Created by <strong>Modou Jaw</strong> &nbsp;·&nbsp; Team Leader, Eco Green
    </div>
    <span class="hero-emoji">🌱</span>
    <h1 class="hero-headline">
      Your Engineering<br/>Ideas Start with<br/><span class="eco-word">Eco Green</span>
    </h1>
    <p class="hero-tagline">
      🌿 The energy that moves with you —<br/>let's save the world by saving energy.
    </p>
    <p class="hero-mission">
      Whether you're a first-year student or writing your thesis, Eco Green is your friendly AI engineering mentor. Get ideas, get guidance, and build something that truly matters. 🚀
    </p>
    <div class="hero-btns">
      <button class="btn-big" onclick="showPage('app')">✨ Generate Project Ideas</button>
      <button class="btn-outline" onclick="showPage('chat')">🌿 Chat with Eco Green</button>
    </div>
    <div class="hero-stats">
      <div class="stat"><div class="stat-num">3</div><div class="stat-lbl">Engineering Fields</div></div>
      <div class="stat"><div class="stat-num">24+</div><div class="stat-lbl">Speciality Topics</div></div>
      <div class="stat"><div class="stat-num">∞</div><div class="stat-lbl">Ideas Generated</div></div>
    </div>
  </div>

  <div class="how-section">
    <div class="sec-tag">✨ How it works</div>
    <h2 class="sec-heading">Three easy steps to<br/><em>your next great project</em></h2>
    <div class="how-grid">
      <div class="how-card" style="--cc:#f4a429" onclick="showPage('app')">
        <div class="how-num">STEP 01 ——</div>
        <span class="how-emoji">💡</span>
        <div class="how-title">Pick your field & level</div>
        <div class="how-desc">Choose Electrical, Civil, or Mechanical Engineering, tell us where you are in your studies, and we'll handle the rest!</div>
      </div>
      <div class="how-card" style="--cc:#1a9e5c" onclick="showPage('chat')">
        <div class="how-num">STEP 02 ——</div>
        <span class="how-emoji">🌿</span>
        <div class="how-title">Meet Eco Green, your mentor</div>
        <div class="how-desc">Your friendly AI mentor helps you understand, plan, and build any project — step by step, with tools, tips, and tons of encouragement.</div>
      </div>
      <div class="how-card" style="--cc:#7c6ff7" onclick="showPage('saved')">
        <div class="how-num">STEP 03 ——</div>
        <span class="how-emoji">📌</span>
        <div class="how-title">Save your favourites</div>
        <div class="how-desc">Found an idea you love? Bookmark it and jump back into building mode anytime — your ideas are always waiting for you.</div>
      </div>
    </div>
  </div>

  <div class="manifesto">
    <span class="man-emoji">🌍</span>
    <h2 class="man-title">"The energy that moves with you — <em>let's save the world</em> by saving energy, one project at a time."</h2>
    <p class="man-body">Every engineer has the power to make a real difference. Eco Green is here to help students like you turn great ideas into solutions that matter for our planet and future generations.</p>
    <div class="pills">
      <span class="pill">🔋 Energy Efficiency</span>
      <span class="pill">♻️ Sustainability</span>
      <span class="pill">🌍 Climate Action</span>
      <span class="pill">⚡ Clean Tech</span>
      <span class="pill">🌿 Green Engineering</span>
      <span class="pill">🔬 Innovation</span>
    </div>
  </div>

  <div class="team-section">
    <div class="sec-tag">👋 Behind Eco Green</div>
    <h2 class="sec-heading">Meet the person<br/><em>who started it all</em></h2>
    <div class="team-card">
      <div class="team-ava">👨‍💻</div>
      <div class="team-name">Modou Jaw</div>
      <div class="team-role">🌿 Team Leader · Eco Green</div>
      <p class="team-bio">Modou Jaw is the visionary team leader behind Eco Green — a platform built with heart, purpose, and a deep belief that students can engineer a better, greener world. His mission: make great engineering education accessible to everyone, everywhere.</p>
      <div class="team-btns">
        <button class="team-btn" onclick="showPage('app')">💡 Explore Ideas</button>
        <button class="team-btn" onclick="showPage('chat')">🌿 Chat with Eco Green</button>
      </div>
    </div>
  </div>

  <footer>
    <div class="foot-logo">🌿 EduBuild</div>
    <div class="foot-tag">"Eco Green — the energy that moves with you."</div>
    <div class="foot-credit">Created with 💚 by <span>Modou Jaw</span>, Team Leader of Eco Green</div>
    <div class="foot-nav">
      <a onclick="showPage('app')">Generate Ideas</a>
      <a onclick="showPage('chat')">Eco Green AI</a>
      <a onclick="showPage('saved')">Saved Projects</a>
    </div>
    <div class="foot-copy">© 2025 EduBuild · Eco Green Engineering Hub · Powered by Gemini AI</div>
  </footer>
</section>

<!-- APP -->
<section id="app-section" class="page">
  <div class="app-wrap">
    <h2 class="app-title">💡 Project Idea Generator</h2>
    <p class="app-sub">Tell us a little about yourself and we'll craft 4 project ideas just for you! 🎉</p>

    <div style="margin-bottom:30px">
      <div class="step-row">
        <div class="step-bub" id="s1b" style="background:var(--green)">1</div>
        <span class="step-lbl">Which engineering field are you in?</span>
      </div>
      <div class="field-grid" id="field-grid"></div>
    </div>

    <div id="step2" style="display:none;animation:fadeUp 0.3s ease;margin-bottom:28px">
      <div class="step-row">
        <div class="step-bub" id="s2b" style="background:var(--green)">2</div>
        <span class="step-lbl">Any specific topic? <span style="color:var(--text3);font-weight:600;text-transform:none">(totally optional 😊)</span></span>
      </div>
      <div class="topics-wrap" id="topics-wrap"></div>
    </div>

    <div id="step3" style="display:none;animation:fadeUp 0.4s ease;margin-bottom:32px">
      <div class="step-row">
        <div class="step-bub" id="s3b" style="background:var(--green)">3</div>
        <span class="step-lbl">Where are you in your studies?</span>
      </div>
      <div class="level-grid" id="level-grid"></div>
    </div>

    <div id="gen-wrap" style="display:none;animation:fadeUp 0.5s ease">
      <button class="gen-btn" id="gen-btn" onclick="generateIdeas()">✨ Generate My Project Ideas</button>
    </div>

    <div id="empty-prompt" style="text-align:center;padding:60px 0">
      <div style="font-size:52px;margin-bottom:14px">👆</div>
      <div style="color:var(--text3);font-size:15px;font-weight:600">Pick your engineering field above to get started!</div>
    </div>

    <div id="ideas-box" style="display:none;animation:fadeUp 0.4s ease">
      <div class="div-lbl"><div class="div-line"></div><span class="div-txt">🎉 YOUR IDEAS ARE READY!</span><div class="div-line"></div></div>
      <div class="ideas-grid" id="ideas-grid"></div>
      <button class="regen-btn" onclick="generateIdeas()">🔄 Give Me 4 Fresh Ideas</button>
    </div>
  </div>
</section>

<!-- CHAT -->
<section id="chat-section" class="page">
  <div class="chat-wrap">
    <div class="chat-head">
      <div class="eco-ava">🌿</div>
      <div style="flex:1">
        <div class="eco-name">Eco Green</div>
        <div class="eco-status"><span class="sdot"></span>Your AI Engineering Mentor · Always here for you 💚</div>
      </div>
      <div class="build-chip" id="build-chip" style="display:none"></div>
    </div>
    <div class="qprompts" id="qprompts">
      <button class="qp" onclick="sendQuick('How do I start a final year project? 🎓')">How do I start a final year project? 🎓</button>
      <button class="qp" onclick="sendQuick('What tools do I need for IoT? 🔌')">What tools do I need for IoT? 🔌</button>
      <button class="qp" onclick="sendQuick('Suggest a civil engineering project idea 🏗️')">Suggest a civil project idea 🏗️</button>
      <button class="qp" onclick="sendQuick('How do I write a project proposal? 📄')">How to write a proposal? 📄</button>
    </div>
    <div class="chat-msgs" id="chat-msgs"></div>
    <div class="chat-input-bar">
      <textarea class="chat-ta" id="chat-in" rows="1" placeholder="Ask Eco Green anything... (Enter to send, Shift+Enter for new line)" onkeydown="chatKey(event)" oninput="resizeTA(this)"></textarea>
      <button class="send-btn off" id="send-btn" onclick="sendChat()">↑</button>
    </div>
  </div>
</section>

<!-- SAVED -->
<section id="saved-section" class="page">
  <div class="saved-wrap">
    <h2 class="saved-title">📌 Saved Ideas</h2>
    <p class="saved-sub">Your bookmarked projects — ready to build whenever you are! 💪</p>
    <div id="saved-content"></div>
  </div>
</section>

<script>
const FIELDS={
  electrical:{label:"Electrical & Electronics",icon:"⚡",color:"#f4a429",topics:["IoT & Smart Devices","Embedded Systems","Power Electronics","Signal Processing","Robotics","Renewable Energy","Telecommunications","PCB Design"],fact:"Did you know? The first integrated circuit was invented in 1958! 🧠"},
  civil:{label:"Civil Engineering",icon:"🏗️",color:"#1a9e5c",topics:["Structural Design","Water Resources","Transportation","Geotechnical","Environmental","Construction Mgmt","Smart Infrastructure","Disaster Management"],fact:"Fun fact: The Great Wall of China used sticky rice as mortar! 🏯"},
  mechanical:{label:"Mechanical Engineering",icon:"⚙️",color:"#7c6ff7",topics:["Thermodynamics","Fluid Mechanics","Manufacturing","Robotics & Automation","HVAC","Automotive","Aerospace","Materials Science"],fact:"Cool fact: Steam engines sparked the Industrial Revolution in the 1760s! 🔥"},
};
const LEVELS=[
  {id:"Beginner",label:"Beginner 🌱",desc:"Year 1–2 student"},
  {id:"Intermediate",label:"Intermediate 🌿",desc:"Year 2–3 student"},
  {id:"Advanced",label:"Advanced 🌳",desc:"Final year student"},
  {id:"Research Level",label:"Research 🔬",desc:"Postgrad / thesis"},
];
const WELCOME=`Hey there! 👋 Welcome — I'm so glad you stopped by!\n\nI'm **Eco Green**, your personal AI engineering mentor, and I'm genuinely here to help you:\n\n💡 Understand any project idea deeply\n🛠️ Plan your build step by step\n📚 Find the right tools and resources\n⚡ Answer any engineering question you have\n\n*"The energy that moves with you — let's save the world by saving energy!"* 🌍\n\nSo, what are you working on? I can't wait to hear your ideas! 😊`;

let selField=null,selTopic='',selLevel='Intermediate';
let ideas=[],saved=[],chatHist=[],chatBusy=false,activeIdea=null;

function showPage(name){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b=>b.classList.remove('active'));
  const pm={hero:'hero-page',app:'app-section',chat:'chat-section',saved:'saved-section'};
  const nm={hero:'nb-hero',app:'nb-app',chat:'nb-chat',saved:'nb-saved'};
  document.getElementById(pm[name]).classList.add('active');
  const nb=document.getElementById(nm[name]);
  if(nb) nb.classList.add('active');
  if(name==='saved') renderSaved();
  if(name==='chat'){if(!chatHist.length)initChat();setTimeout(scrollDown,60);}
  window.scrollTo(0,0);
}

function renderFields(){
  const g=document.getElementById('field-grid');g.innerHTML='';
  Object.entries(FIELDS).forEach(([k,f])=>{
    const a=selField===k;
    const d=document.createElement('div');
    d.className='field-card';
    if(a)d.style.cssText=`border-color:${f.color};background:${f.color}12;box-shadow:0 4px 20px ${f.color}33`;
    d.innerHTML=`<span class="fi">${f.icon}</span><div class="fn" style="color:${a?f.color:'var(--text)'}">${f.label}</div>${a?`<div class="ff">${f.fact}</div>`:''}`;
    d.onclick=()=>{selField=k;selTopic='';ideas=[];document.getElementById('ideas-box').style.display='none';renderFields();renderSteps();};
    g.appendChild(d);
  });
}

function renderSteps(){
  const has=!!selField;
  ['step2','step3','gen-wrap'].forEach(id=>document.getElementById(id).style.display=has?'block':'none');
  document.getElementById('empty-prompt').style.display=has?'none':'block';
  if(!has)return;
  const f=FIELDS[selField];
  ['s1b','s2b','s3b'].forEach(id=>{const el=document.getElementById(id);if(el)el.style.background=f.color;});
  const tw=document.getElementById('topics-wrap');tw.innerHTML='';
  ['Any Topic',...f.topics].forEach(t=>{
    const val=t==='Any Topic'?'':t;
    const b=document.createElement('button');
    b.className='topic-btn'+(selTopic===val?' sel':'');
    if(selTopic===val)b.style.cssText=`border-color:${f.color};color:${f.color};background:${f.color}14`;
    b.textContent=(selTopic===val?'✓ ':'')+t;
    b.onclick=()=>{selTopic=val;renderSteps();};
    tw.appendChild(b);
  });
  const lg=document.getElementById('level-grid');lg.innerHTML='';
  LEVELS.forEach(l=>{
    const a=selLevel===l.id;
    const c=document.createElement('div');c.className='level-card';
    if(a)c.style.cssText=`border-color:${f.color};background:${f.color}12`;
    c.innerHTML=`<div><div class="lname" style="color:${a?f.color:'var(--text)'}">${l.label}</div><div class="ldesc">${l.desc}</div></div>`;
    c.onclick=()=>{selLevel=l.id;renderSteps();};
    lg.appendChild(c);
  });
}

async function generateIdeas(){
  if(!selField)return;
  const f=FIELDS[selField];
  const btn=document.getElementById('gen-btn');
  btn.disabled=true;
  btn.innerHTML='<span class="spinner"></span> Crafting your ideas...';
  const tc=selTopic?`specifically in the area of ${selTopic}`:'';
  const prompt=`Generate 4 creative, practical project ideas for a ${selLevel} student in ${f.label} ${tc}. For each idea return JSON: {"title":"...","description":"2 sentences","technologies":["t1","t2","t3","t4"],"impact":"1 sentence real-world impact","difficulty":1-5}. Return ONLY a valid JSON array of 4 objects, no markdown.`;
  try{
    const res=await callAPI([{role:'user',content:prompt}],"You are a friendly, encouraging engineering project advisor for university students. Be warm and practical.");
    let clean=res.trim().replace(/```json\n?/,'').replace(/```\n?$/,'');
    const arr=JSON.parse(clean);
    ideas=(Array.isArray(arr)?arr:[arr]).slice(0,4);
    renderIdeas();confetti();
  }catch(e){alert('Something went wrong — please try again! 😊 '+e.message);}
  finally{btn.disabled=false;btn.innerHTML='✨ Generate My Project Ideas';}
}

function renderIdeas(){
  const box=document.getElementById('ideas-box'),g=document.getElementById('ideas-grid');
  box.style.display='block';g.innerHTML='';
  const f=FIELDS[selField];
  ideas.forEach((idea,i)=>{
    const sv=!!saved.find(s=>s.title===idea.title);
    const d=document.createElement('div');d.className='idea-card';
    d.innerHTML=`
      <div class="idea-bar" style="background:linear-gradient(90deg,${f.color},${f.color}66)"></div>
      <div class="idea-body">
        <div class="idea-meta" style="color:${f.color}">IDEA ${i+1} &nbsp;·&nbsp; ${'⭐'.repeat(idea.difficulty)}${'☆'.repeat(5-idea.difficulty)}</div>
        <div class="idea-title">${idea.title}</div>
        <div class="idea-desc">${idea.description}</div>
        <div class="tech-tags">${idea.technologies.map(t=>`<span class="tech-tag" style="background:${f.color}15;border:1.5px solid ${f.color}44;color:${f.color}">${t}</span>`).join('')}</div>
        <div class="idea-impact">🌍 <strong>Why it matters:</strong> ${idea.impact}</div>
        <div class="idea-actions">
          <button class="btn-eco" onclick="ideaToChat(${i})">🌿 Build this with Eco Green</button>
          <button class="btn-save" id="sv${i}" onclick="toggleSave(${i})" style="border:2px solid ${sv?f.color:'var(--border2)'};background:${sv?f.color+'18':'var(--surface)'};color:${sv?f.color:'var(--text3)'}">${sv?'✓ Saved!':'📌 Save'}</button>
        </div>
      </div>`;
    g.appendChild(d);
  });
}

function toggleSave(i){
  const idea=ideas[i],idx=saved.findIndex(s=>s.title===idea.title);
  if(idx>=0)saved.splice(idx,1);else saved.push({...idea,field:selField});
  updateSavedNav();renderIdeas();
}
function updateSavedNav(){
  const nb=document.getElementById('nb-saved');
  if(nb)nb.textContent=saved.length?`📌 Saved (${saved.length})`:'📌 Saved';
}

function initChat(){chatHist=[{role:'assistant',content:WELCOME}];renderChat();}

function md(t){return t.replace(/\*\*(.*?)\*\*/g,'<strong>$1</strong>').replace(/\*(.*?)\*/g,'<em>$1</em>').replace(/\n/g,'<br/>');}

function renderChat(loading=false){
  const c=document.getElementById('chat-msgs');c.innerHTML='';
  chatHist.forEach(msg=>{
    const row=document.createElement('div');row.className='msg-row '+msg.role;
    if(msg.role==='assistant')row.innerHTML=`<div class="msg-ava">🌿</div><div class="bubble eco">${md(msg.content)}</div>`;
    else row.innerHTML=`<div class="bubble user">${md(msg.content)}</div>`;
    c.appendChild(row);
  });
  if(loading){
    const row=document.createElement('div');row.className='msg-row';
    row.innerHTML=`<div class="msg-ava">🌿</div><div class="typing-bub"><div class="typing-dots"><div class="dot"></div><div class="dot"></div><div class="dot"></div></div></div>`;
    c.appendChild(row);
  }
  scrollDown();
  document.getElementById('qprompts').style.display=chatHist.length<=1?'flex':'none';
}

function scrollDown(){const c=document.getElementById('chat-msgs');if(c)c.scrollTop=c.scrollHeight;}
function updateSendBtn(){const inp=document.getElementById('chat-in').value.trim(),btn=document.getElementById('send-btn');btn.className='send-btn '+(inp&&!chatBusy?'ready':'off');}
function chatKey(e){if(e.key==='Enter'&&!e.shiftKey){e.preventDefault();sendChat();}updateSendBtn();}
function resizeTA(el){el.style.height='auto';el.style.height=Math.min(el.scrollHeight,110)+'px';updateSendBtn();}

async function sendChat(){
  const inp=document.getElementById('chat-in'),msg=inp.value.trim();
  if(!msg||chatBusy)return;
  inp.value='';inp.style.height='auto';updateSendBtn();
  chatHist.push({role:'user',content:msg});chatBusy=true;renderChat(true);
  await doChat();
}
async function sendQuick(msg){
  if(chatBusy)return;
  if(!chatHist.length)chatHist=[{role:'assistant',content:WELCOME}];
  chatHist.push({role:'user',content:msg});chatBusy=true;renderChat(true);
  await doChat();
}
async function doChat(){
  const sys=`You are Eco Green — a warm, friendly, encouraging AI engineering mentor for university students, created by Modou Jaw as part of the Eco Green initiative. You speak like a supportive, knowledgeable older student who genuinely cares. Use simple, clear language. Avoid jargon unless you explain it. Use **bold** for key terms. Keep responses friendly and digestible. Add an emoji or two. Specialise in Electrical, Civil, and Mechanical Engineering. Believe in green engineering as a way to save the world.`;
  try{
    const msgs=chatHist.map(m=>({role:m.role,content:m.content}));
    const res=await callAPI(msgs,sys);
    chatHist.push({role:'assistant',content:res});
  }catch(e){
    chatHist.push({role:'assistant',content:"Oops, something went a bit wrong on my end! Could you try again? I'm still here for you! 😊"});
  }finally{chatBusy=false;renderChat(false);}
}

async function ideaToChat(i){
  const idea=ideas[i];activeIdea=idea;
  const msg=`Hi Eco Green! I'm really excited about this project: **${idea.title}**. ${idea.description} Can you help me plan how to build it step by step?`;
  chatHist=[{role:'assistant',content:WELCOME},{role:'user',content:msg}];
  chatBusy=true;showPage('chat');
  const chip=document.getElementById('build-chip');
  chip.style.display='block';chip.innerHTML=`🔨 Building:<br/><strong>${idea.title}</strong>`;
  renderChat(true);
  const sys=`You are Eco Green — a warm, friendly, encouraging AI engineering mentor, created by Modou Jaw. Help this student build their project step by step in a practical, friendly way. Use **bold** for key points. Be encouraging and clear! Add emojis to keep things warm.`;
  try{
    const res=await callAPI([{role:'user',content:msg}],sys);
    chatHist.push({role:'assistant',content:res});
  }catch(e){
    chatHist.push({role:'assistant',content:"Let's build something amazing together! Tell me a bit more about your goals and I'll put together a step-by-step plan for you. 🚀"});
  }finally{chatBusy=false;renderChat(false);}
}

function renderSaved(){
  const c=document.getElementById('saved-content');
  if(!saved.length){
    c.innerHTML=`<div class="empty-box"><span class="empty-icon">📭</span><div class="empty-txt">No saved ideas yet — go generate some! They'll all show up here 😊</div><button class="btn-big" onclick="showPage('app')">Go Generate Ideas ✨</button></div>`;
    return;
  }
  c.innerHTML='<div class="saved-grid" id="sg"></div>';
  const g=document.getElementById('sg');
  saved.forEach((idea,i)=>{
    const f=FIELDS[idea.field];
    const d=document.createElement('div');d.className='saved-card';
    d.innerHTML=`
      <div style="height:4px;background:linear-gradient(90deg,${f.color},${f.color}55)"></div>
      <div style="padding:20px 22px">
        <div style="display:flex;justify-content:space-between;align-items:flex-start;gap:12px;margin-bottom:12px">
          <div>
            <div style="font-size:11px;color:${f.color};font-weight:800">${f.icon} ${f.label}</div>
            <div style="font-family:'Lora',serif;font-size:18px;font-weight:700;color:var(--text);margin-top:4px;line-height:1.3">${idea.title}</div>
          </div>
          <button onclick="removeSaved(${i})" style="padding:6px 12px;border-radius:10px;border:1.5px solid #fca5a5;background:#fef2f2;color:#ef4444;cursor:pointer;font-size:12px;font-weight:700;font-family:'Nunito',sans-serif;flex-shrink:0">✕ Remove</button>
        </div>
        <p style="color:var(--text2);font-size:13px;line-height:1.8;margin:0 0 14px;font-weight:600">${idea.description}</p>
        <div style="display:flex;flex-wrap:wrap;gap:7px;margin-bottom:16px">
          ${idea.technologies.map(t=>`<span style="background:${f.color}15;border:1.5px solid ${f.color}44;color:${f.color};padding:4px 12px;border-radius:20px;font-size:12px;font-weight:700">${t}</span>`).join('')}
        </div>
        <button class="btn-eco" onclick="savedToChat(${i})" style="width:auto;padding:11px 22px">🌿 Build with Eco Green</button>
      </div>`;
    g.appendChild(d);
  });
}

function removeSaved(i){saved.splice(i,1);updateSavedNav();renderSaved();}
function savedToChat(i){ideas=[saved[i]];ideaToChat(0);}

// ── GEMINI API ─────────────────────────────────────────
let GEMINI_KEY = localStorage.getItem('edubuild-gemini-key') || '';

function promptForKey(){
  return new Promise(resolve=>{
    const overlay=document.getElementById('key-overlay');
    overlay.style.display='flex';
    document.getElementById('key-input').value=GEMINI_KEY||'';
    document.getElementById('key-save-btn').onclick=()=>{
      const val=document.getElementById('key-input').value.trim();
      if(!val)return;
      GEMINI_KEY=val;
      localStorage.setItem('edubuild-gemini-key',val);
      overlay.style.display='none';
      resolve(val);
    };
    document.getElementById('key-cancel-btn').onclick=()=>{
      overlay.style.display='none';
      resolve(null);
    };
  });
}

async function callAPI(msgs, sys){
  let key = GEMINI_KEY;
  if(!key){
    key = await promptForKey();
    if(!key) throw new Error('No API key provided.');
  }
  const contents = msgs.map(m=>({
    role: m.role === 'assistant' ? 'model' : 'user',
    parts:[{text: m.content}]
  }));
  const body = {contents, generationConfig:{maxOutputTokens:1000}};
  if(sys) body.system_instruction = {parts:[{text:sys}]};
  const res = await fetch(
    `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${key}`,
    {method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify(body)}
  );
  if(!res.ok){
    const e=await res.json();
    if(res.status===400||res.status===403){GEMINI_KEY='';localStorage.removeItem('edubuild-gemini-key');}
    throw new Error(e.error?.message||res.statusText);
  }
  const data=await res.json();
  return data.candidates?.[0]?.content?.parts?.map(p=>p.text||'').join('')||'';
}
// ──────────────────────────────────────────────────────

function confetti(){
  const layer=document.getElementById('confetti-layer');layer.innerHTML='';
  const colors=['#1a9e5c','#f4a429','#7c6ff7','#f0637a','#25c270','#60a5fa'];
  for(let i=0;i<30;i++){
    const p=document.createElement('div');p.className='cp';
    const sz=7+Math.random()*8;
    const isCircle=Math.random()>0.5;
    p.style.cssText=`left:${10+Math.random()*80}%;top:12%;width:${sz}px;height:${sz}px;background:${colors[Math.floor(Math.random()*colors.length)]};border-radius:${isCircle?'50%':'4px'};animation-delay:${Math.random()*0.5}s;animation-duration:${1.5+Math.random()*0.8}s`;
    layer.appendChild(p);
  }
  setTimeout(()=>layer.innerHTML='',2500);
}

// ── THEME ──────────────────────────────────────────────
function applyTheme(dark, animate){
  if(!animate){document.documentElement.classList.add('no-transition');}
  document.documentElement.setAttribute('data-theme', dark ? 'dark' : 'light');
  const btn = document.getElementById('theme-btn');
  if(btn) btn.textContent = dark ? '☀️' : '🌙';
  if(!animate){
    requestAnimationFrame(()=>{
      requestAnimationFrame(()=>{document.documentElement.classList.remove('no-transition');});
    });
  }
}
function toggleTheme(){
  const isDark = document.documentElement.getAttribute('data-theme') === 'dark';
  const next = !isDark;
  localStorage.setItem('edubuild-theme', next ? 'dark' : 'light');
  applyTheme(next, true);
}
// On load — apply saved preference without animation
(function(){
  const saved = localStorage.getItem('edubuild-theme');
  const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
  applyTheme(saved ? saved === 'dark' : prefersDark, false);
})();
// ──────────────────────────────────────────────────────

renderFields();
renderSteps();
document.getElementById('chat-in').addEventListener('input',updateSendBtn);
</script>

<!-- API KEY OVERLAY -->
<div id="key-overlay">
  <div class="key-box">
    <span class="key-icon">🔑</span>
    <div class="key-title">Enter your Gemini API Key</div>
    <p class="key-sub">Your key is stored locally in your browser and never sent anywhere except Google's API.</p>
    <input class="key-input" id="key-input" type="password" placeholder="AIza..." />
    <div class="key-btns">
      <button class="key-save" id="key-save-btn">Save & Continue ✨</button>
      <button class="key-cancel" id="key-cancel-btn">Cancel</button>
    </div>
    <p class="key-hint">Get a free key at <a href="https://aistudio.google.com/apikey" target="_blank">aistudio.google.com/apikey</a></p>
  </div>
</div>
</body>
</html>

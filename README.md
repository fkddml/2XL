<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>꿈의 핏 2XL</title>

<style>
/* 폰트 등록 */
@font-face {
    font-family: 'Paperozi';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/2408-3@1.0/Paperlogy-1Thin.woff2') format('woff2');
    font-weight: 100;
    font-display: swap;
}

/* [추가] 타이틀 전용 '서울관공서체 알림M' 폰트 등록 */
@font-face {
    font-family: 'SeoulNotice';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/2505-1@1.0/SeoulAlrimTTF-Medium.woff2') format('woff2');
    font-weight: 500;
    font-display: swap;
}

:root {
    --bg: #0a0a0a;
    --card: #141414;
    --accent: #00F0FF; /* 네온 블루 */
    --accent-dim: rgba(0, 240, 255, 0.15);
    --text-primary: #F0F8FF;
    --text-muted: #a0aec0;
    --border-color: #2d3748;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Paperozi', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
}

body {
    background: var(--bg);
    color: var(--text-primary);
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding: 20px;
}

.container {
    width: 100%;
    max-width: 1100px;
    background: var(--card);
    border-radius: 24px;
    padding: 32px;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5), 0 0 2px var(--accent);
    border: 1px solid rgba(255, 255, 255, 0.05);
}

.hidden {
    display: none !important;
}

h1 {
    text-align: center;
    margin-bottom: 24px;
    color: var(--text-primary);
    font-size: 2rem;
    letter-spacing: -0.05em;
}

/* [추가] '꿈의 핏 2XL' 부분에만 서울알림체 지정 */
.title-font, .title-font span {
    font-family: 'SeoulNotice', sans-serif !important;
}

h1 span {
    color: var(--accent);
    text-shadow: 0 0 10px rgba(0, 240, 255, 0.6);
}

.status {
    text-align: center;
    font-weight: bold;
    color: var(--accent);
    margin-bottom: 20px;
    font-size: 1.1rem;
    letter-spacing: 0.05em;
}

.login {
    display: flex;
    flex-direction: column;
    gap: 16px;
    max-width: 400px;
    margin: 60px auto;
}

input {
    padding: 16px;
    border-radius: 12px;
    border: 2px solid var(--border-color);
    background: #1e1e1e;
    color: #ffffff;
    font-size: 16px;
    transition: all 0.3s;
}

input:focus {
    outline: none;
    border-color: var(--accent);
    box-shadow: 0 0 10px rgba(0, 240, 255, 0.3);
}

button {
    background: var(--accent);
    color: #141414;
    border: none;
    padding: 16px;
    border-radius: 12px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    transition: all 0.2s;
    box-shadow: 0 4px 12px rgba(0, 240, 255, 0.3);
}

button:hover {
    background: #00c8d6;
    transform: translateY(-1px);
    box-shadow: 0 6px 20px rgba(0, 240, 255, 0.5);
}

.quiz-layout {
    display: grid;
    grid-template-columns: 360px 1fr;
    gap: 28px;
}

.selfie-box {
    background: #1a1a1a;
    padding: 16px;
    border-radius: 20px;
    border: 1px solid var(--border-color);
}

.selfie {
    width: 100%;
    height: 450px;
    object-fit: cover;
    border-radius: 14px;
    background: #2a2a2a;
}

.date {
    margin-top: 14px;
    font-weight: 600;
    text-align: center;
    color: var(--accent);
}

.bubble {
    margin-top: 12px;
    background: var(--accent-dim);
    border: 1px solid rgba(0, 240, 255, 0.3);
    padding: 14px;
    border-radius: 14px;
    text-align: center;
    font-weight: bold;
    color: #ffffff;
}

.right {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.category {
    background: #1a1a1a;
    padding: 16px;
    border-radius: 16px;
    border: 1px solid var(--border-color);
}

.category h3 {
    margin-bottom: 12px;
    color: #ffffff;
    font-size: 1rem;
    border-left: 4px solid var(--accent);
    padding-left: 8px;
}

.choice-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
}

.choice {
    width: 100px;
    height: 100px;
    object-fit: cover;
    border-radius: 12px;
    border: 3px solid transparent;
    cursor: pointer;
    transition: all 0.2s;
    background: #2a2a2a;
}

.choice:hover {
    transform: scale(1.05);
    border-color: rgba(255, 255, 255, 0.2);
}

.selected {
    border-color: var(--accent) !important;
    box-shadow: 0 0 12px rgba(0, 240, 255, 0.5);
}

.result {
    text-align: center;
}

.score {
    font-size: 64px;
    font-weight: 900;
    margin: 10px 0 30px 0;
    color: var(--accent);
    text-shadow: 0 0 20px rgba(0, 240, 255, 0.4);
}

.section-title {
    font-size: 1.3rem;
    margin: 40px 0 16px 0;
    color: #ffffff;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
}

.rank-list {
    list-style: none;
    max-width: 500px;
    margin: 0 auto;
}

.rank-list li {
    background: #1a1a1a;
    padding: 14px 20px;
    margin-bottom: 10px;
    border-radius: 12px;
    display: flex;
    justify-content: space-between;
    border: 1px solid var(--border-color);
}

.rank-list li.top-rank {
    background: var(--accent-dim);
    border-color: var(--accent);
    font-weight: bold;
}

.review-section {
    max-width: 800px;
    margin: 0 auto;
    text-align: left;
}

.review-card {
    background: #1a1a1a;
    border: 1px solid var(--border-color);
    border-radius: 16px;
    padding: 20px;
    margin-bottom: 20px;
}

.review-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #2d3748;
    padding-bottom: 10px;
    margin-bottom: 16px;
}

.review-q-num {
    font-weight: bold;
    font-size: 1.1rem;
}

.review-date {
    color: var(--text-muted);
    font-size: 0.9rem;
}

.review-body {
    display: grid;
    grid-template-columns: 120px 1fr;
    gap: 20px;
}

.review-selfie {
    width: 120px;
    height: 150px;
    object-fit: cover;
    border-radius: 8px;
    background: #2a2a2a;
}

.review-details {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.review-item {
    background: #222;
    padding: 10px 14px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 0.95rem;
}

.review-item.correct {
    border-left: 4px solid var(--accent);
}

.review-item.wrong {
    border-left: 4px solid #ff4a4a;
}

.part-name {
    font-weight: bold;
    color: #ffffff;
}

.answer-compare {
    display: flex;
    align-items: center;
    gap: 12px;
}

.badge {
    padding: 2px 8px;
    border-radius: 4px;
    font-size: 0.8rem;
    font-weight: bold;
}

.badge.bad-correct {
    background: rgba(0, 240, 255, 0.2);
    color: var(--accent);
}

.badge.bad-wrong {
    background: rgba(255, 74, 74, 0.2);
    color: #ff4a4a;
}

.thumb-preview {
    width: 32px;
    height: 32px;
    object-fit: cover;
    border-radius: 4px;
    border: 1px solid rgba(255,255,255,0.1);
    vertical-align: middle;
}

.vs-text {
    color: var(--text-muted);
    font-size: 0.85rem;
}

@media(max-width:900px){
    .quiz-layout {
        grid-template-columns: 1fr;
    }
    .selfie {
        height: 380px;
    }
    .choice {
        width: 80px;
        height: 80px;
    }
    .review-body {
        grid-template-columns: 1fr;
    }
    .review-selfie {
        width: 100%;
        height: 200px;
    }
}
</style>
</head>
<body>

<div class="container">
    <h1 class="title-font">꿈의 핏 <span>2XL</span></h1>

    <div id="loginScreen">
        <div class="login">
            <input id="nickname" placeholder="닉네임">
            <input id="password" type="password" maxlength="4" placeholder="비밀번호(4자리)">
            <button onclick="startGame()">START!</button>
        </div>
    </div>

    <div id="quizScreen" class="hidden">
        <div id="status" class="status">1 / 10</div>
        <div class="quiz-layout">
            <div class="selfie-box">
                <img id="selfie" class="selfie" alt="셀카 자리">
                <div id="date" class="date"></div>
                <div id="bubble" class="bubble">슬슬 두꺼운 옷을 꺼내야 할 때가 온 것 같다</div>
            </div>
            <div id="questionArea" class="right"></div>
        </div>
        <br>
        <button onclick="submitQuestion()" style="width:100%;">정답 제출</button>
    </div>

    <div id="resultScreen" class="hidden">
        <div class="result">
            <h2>YOUR FINAL SCORE</h2>
            <div id="finalScore" class="score">0점</div>
            
            <button onclick="location.reload()" style="max-width:300px; margin-bottom:40px;">다시 도전하기</button>

            <div class="section-title">🔍 내가 틀린 문제 & 정답 확인</div>
            <div id="reviewSection" class="review-section"></div>

            <div class="section-title">🏆 명예의 전당</div>
            <ul id="rankList" class="rank-list"></ul>
            <br>
        </div>
    </div>
</div>

<script>
const bubbleTexts = [
    "슬슬 두꺼운 옷을 꺼내야 할 때가 온 것 같다", "옷 따뜻하게 입어", "태어나줘서 고마워 🫶 오늘 하루 좋은 일만 있기를🙌", "미안해~ 매번 사랑한다고 하면 그 진심이 가벼워 보일까봐 그 말을 아껴두고 있어", 
    "엉 나도 많이 사랑해", "감기걸리지않도록", "저녁 아직 안먹었겠지 맛진저녁 되세요 😋💪", 
    "미리 잘자고나도잘잘게!!!!!!!!오늘고생많았다", "옷으로말하고있잖아 뭔말인지알지", "그니까 레고를 레고 레고레츠고레츠고레고레츠고레츠고레고레고레고레고레츠고레고레츠고레고 오케이?", "티라노 된다된다하면 진짜 되잖아요 어릴 때부터 티라노 된다 된다하니까 되더라고 진짜", "뭐해 /// @ ㅁ @ ///", "ㅋㅋㄹㅃㅃ ㅋㅋㄹ레뿅이라는뜻", "점심 마라마파두부덮밥 저녁 야채찜", "응원해줘서 고마워 ㅜ.ㅜ 항상 ㅎ.ㅎ", "다같이 6 7~~~~~~", "하하하 내 의도를 완벽히 파악했네~ 최고의 콤비 우리 둘은!", "- 앞으로만가의정석 정답과 해설 중 p. 915 -", "앞으로만가의정석 조금더 남아서 공부할 필요 있을거 같아.", "겉으로는 아닌 척해도 속으로는 위트 있는 성현이 멋있어보인다.", "???에 들어갈 지문을 완성", "개인적으로 햄버거는 치킨버거 혹은 불고기 버거라고 생각했습니다", "암튼 그나저나 이러쿵저러쿵 천방지축 이래저래 요리조리 제멋대로 내멋대로 찬란하게 찬란한 하루 보내", "(훗나좀똑똑명석해)", "나 왜이렇게 좋아해 😏 못말려 정말", "항상사랑합니다 아이러브유!", "우리모두열심히살아보자 파이팅", "love you30000"
];

const partTitles = {
    hat: "모자", top: "상의", bottom: "하의", accessory: "악세사리", shoes: "신발"
};

let nickname = "";
let currentQuestion = 0;
let totalScore = 0;
let selectedAnswers = {};
let questions = [];
let gameHistory = [];

const quizPool = [
    {
        date: "2026.06.01",
        selfie: "images/selfie1.jpg",
        hat: { answer: 0, choices: ["images/hat1.jpg", "images/hat2.jpg", "images/hat3.jpg"] },
        top: { answer: 1, choices: ["images/top1.jpg", "images/top2.jpg", "images/top3.jpg"] },
        bottom: { answer: 2, choices: ["images/bottom1.jpg", "images/bottom2.jpg", "images/bottom3.jpg"] },
        accessory: null,
        shoes: { answer: 0, choices: ["images/shoes1.jpg", "images/shoes2.jpg", "images/shoes3.jpg"] }
    },
    {
        date: "2026.06.02",
        selfie: "images/selfie2.jpg",
        hat: null,
        top: { answer: 0, choices: ["images/top4.jpg", "images/top5.jpg", "images/top6.jpg"] },
        bottom: { answer: 1, choices: ["images/bottom4.jpg", "images/bottom5.jpg", "images/bottom6.jpg"] },
        accessory: { answer: 2, choices: ["images/acc1.jpg", "images/acc2.jpg", "images/acc3.jpg"] },
        shoes: { answer: 1, choices: ["images/shoes4.jpg", "images/shoes5.jpg", "images/shoes6.jpg"] }
    }
];

function shuffle(array) {
    for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
    }
    return array;
}

function startGame() {
    nickname = document.getElementById("nickname").value.trim();
    const password = document.getElementById("password").value.trim();

    if (!nickname) { alert("닉네임을 입력해주세요!"); return; }
    if (password.length !== 4) { alert("비밀번호 4자리를 입력해주세요!"); return; }

    let poolCopy = JSON.parse(JSON.stringify(quizPool));
    questions = shuffle([...poolCopy]);

    while (questions.length < 10) {
        const randomItem = quizPool[Math.floor(Math.random() * quizPool.length)];
        questions.push(JSON.parse(JSON.stringify(randomItem)));
    }
    questions = shuffle(questions).slice(0, 10);

    document.getElementById("loginScreen").classList.add("hidden");
    document.getElementById("quizScreen").classList.remove("hidden");

    currentQuestion = 0;
    totalScore = 0;
    gameHistory = [];
    loadQuestion();
}

function loadQuestion() {
    selectedAnswers = {};
    const q = questions[currentQuestion];

    /* 3. 상단 퀴즈 진행 상태에서 'Q' 글자를 빼고 숫자만 노출 */
    document.getElementById("status").innerText = `${currentQuestion + 1} / 10`;
    document.getElementById("selfie").src = q.selfie;
    document.getElementById("date").innerText = q.date;
    document.getElementById("bubble").innerText = bubbleTexts[Math.floor(Math.random() * bubbleTexts.length)];

    const area = document.getElementById("questionArea");
    area.innerHTML = "";

    const keys = ["hat", "top", "bottom", "accessory", "shoes"];
    keys.forEach(key => {
        if (!q[key]) return;

        const box = document.createElement("div");
        box.className = "category";
        box.innerHTML = `<h3>${partTitles[key]}</h3>`;

        const row = document.createElement("div");
        row.className = "choice-row";

        q[key].choices.forEach((src, index) => {
            const img = document.createElement("img");
            img.src = src;
            img.className = "choice";

            img.onclick = () => {
                selectedAnswers[key] = index;
                row.querySelectorAll(".choice").forEach(el => el.classList.remove("selected"));
                img.classList.add("selected");
            };

            row.appendChild(img);
        });

        box.appendChild(row);
        area.appendChild(box);
    });
}

function submitQuestion() {
    const q = questions[currentQuestion];
    const activeParts = [];

    const keys = ["hat", "top", "bottom", "accessory", "shoes"];
    keys.forEach(key => { if (q[key]) activeParts.push(key); });

    for (let part of activeParts) {
        if (selectedAnswers[part] === undefined) {
            alert(`${partTitles[part]} 부위를 선택해주세요! 👀`);
            return;
        }
    }

    const pointPerPart = 10 / activeParts.length;
    let partResults = {};

    activeParts.forEach(part => {
        const userChoice = selectedAnswers[part];
        const correctAnswer = q[part].answer;
        const isCorrect = userChoice === correctAnswer;

        if (isCorrect) totalScore += pointPerPart;

        partResults[part] = {
            isCorrect: isCorrect,
            userChoiceImg: q[part].choices[userChoice],
            correctAnswerImg: q[part].choices[correctAnswer]
        };
    });

    gameHistory.push({
        qNum: currentQuestion + 1,
        date: q.date,
        selfie: q.selfie,
        partResults: partResults
    });

    currentQuestion++;

    if (currentQuestion >= 10) {
        finishGame();
    } else {
        loadQuestion();
    }
}

function finishGame() {
    document.getElementById("quizScreen").classList.add("hidden");
    document.getElementById("resultScreen").classList.remove("hidden");

    const final = Math.min(100, Math.round(totalScore));
    document.getElementById("finalScore").innerText = final + "점";

    let ranking = JSON.parse(localStorage.getItem("ootdRanking")) || [];
    ranking.push({ name: nickname, score: final });
    ranking.sort((a, b) => b.score - a.score);
    ranking = ranking.slice(0, 10);
    localStorage.setItem("ootdRanking", JSON.stringify(ranking));

    const rankList = document.getElementById("rankList");
    rankList.innerHTML = "";
    ranking.forEach((item, index) => {
        const li = document.createElement("li");
        if (index === 0) li.className = "top-rank";
        li.innerHTML = `<span>${index + 1}. ${item.name}</span> <span>${item.score}점</span>`;
        rankList.appendChild(li);
    });

    const reviewSection = document.getElementById("reviewSection");
    reviewSection.innerHTML = "";

    gameHistory.forEach(hist => {
        const card = document.createElement("div");
        card.className = "review-card";

        let detailsHtml = "";
        for (let part in hist.partResults) {
            const res = hist.partResults[part];
            if (res.isCorrect) {
                detailsHtml += `
                    <div class="review-item correct">
                        <span class="part-name">${partTitles[part]}</span>
                        <div class="answer-compare">
                            <span class="badge bad-correct">정답</span>
                            <img class="thumb-preview" src="${res.correctAnswerImg}">
                        </div>
                    </div>
                `;
            } else {
                detailsHtml += `
                    <div class="review-item wrong">
                        <span class="part-name">${partTitles[part]}</span>
                        <div class="answer-compare">
                            <span class="badge bad-wrong">오답</span>
                            <span class="vs-text">내 선택:</span>
                            <img class="thumb-preview" src="${res.userChoiceImg}">
                            <span class="vs-text">정답:</span>
                            <img class="thumb-preview" src="${res.correctAnswerImg}">
                        </div>
                    </div>
                `;
            }
        }

        card.innerHTML = `
            <div class="review-header">
                <span class="review-q-num">${hist.qNum}</span>
                <span class="review-date">${hist.date}</span>
            </div>
            <div class="review-body">
                <img class="review-selfie" src="${hist.selfie}">
                <div class="review-details">
                    ${detailsHtml}
                </div>
            </div>
        `;
        reviewSection.appendChild(card);
    });
}
</script>

</body>
</html>

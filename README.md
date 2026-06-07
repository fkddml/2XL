<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>꿈의 핏 2XL</title>

<style>
/* 새로운 전체 폰트 'OkDandan' 등록 */
@font-face {
    font-family: 'OkDandan';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/2508-2@1.0/OkDanDan-Bold.woff2') format('woff2');
    font-weight: normal;
    font-style: normal;
}

:root {
    --bg: #f8f9fa;            
    --card: #ffffff;          
    --accent: #00b4d8;        
    --accent-dim: rgba(0, 180, 216, 0.1);
    --text-primary: #1a1a1a;  
    --text-muted: #4a5568;    
    --border-color: #cbd5e1;  
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'OkDandan', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
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
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05), 0 0 1px rgba(0, 0, 0, 0.1);
    border: 1px solid rgba(0, 0, 0, 0.05);
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

.title-font, .title-font span {
    font-family: 'OkDandan', sans-serif !important;
}

h1 span {
    color: var(--accent);
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
    margin: 40px auto 20px auto;
}

input {
    padding: 16px;
    border-radius: 12px;
    border: 2px solid var(--border-color);
    background: #ffffff;
    color: #1a1a1a;
    font-size: 16px;
    transition: all 0.3s;
}

input:focus {
    outline: none;
    border-color: var(--accent);
    box-shadow: 0 0 10px rgba(0, 180, 216, 0.2);
}

button {
    background: var(--accent);
    color: #ffffff;
    border: none;
    padding: 16px;
    border-radius: 12px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    transition: all 0.2s;
    box-shadow: 0 4px 12px rgba(0, 180, 216, 0.2);
}

button:hover {
    background: #0077b6;
    transform: translateY(-1px);
    box-shadow: 0 6px 20px rgba(0, 180, 216, 0.3);
}

.loading-text {
    font-size: 1rem;
    color: var(--text-muted);
    margin: 15px 0;
    font-style: italic;
}

.quiz-layout {
    display: grid;
    grid-template-columns: 360px 1fr;
    gap: 28px;
}

.selfie-box {
    background: #f1f5f9;
    padding: 16px;
    border-radius: 20px;
    border: 1px solid var(--border-color);
}

.selfie {
    width: 100%;
    height: 450px;
    object-fit: cover;
    border-radius: 14px;
    background: #e2e8f0;
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
    border: 1px solid rgba(0, 180, 216, 0.2);
    padding: 14px;
    border-radius: 14px;
    text-align: center;
    font-weight: bold;
    color: var(--text-primary);
}

.right {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.category {
    background: #f1f5f9;
    padding: 16px;
    border-radius: 16px;
    border: 1px solid var(--border-color);
}

.category h3 {
    margin-bottom: 12px;
    color: var(--text-primary);
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
    background: #e2e8f0;
}

.choice:hover {
    transform: scale(1.05);
    border-color: rgba(0, 0, 0, 0.1);
}

.selected {
    border-color: var(--accent) !important;
    box-shadow: 0 0 12px rgba(0, 180, 216, 0.4);
}

.result {
    text-align: center;
}

.score {
    font-size: 64px;
    font-weight: 900;
    margin: 10px 0 30px 0;
    color: var(--accent);
}

.section-title {
    font-size: 1.3rem;
    margin: 30px 0 16px 0;
    color: var(--text-primary);
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
    background: #f1f5f9;
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
    background: #f1f5f9;
    border: 1px solid var(--border-color);
    border-radius: 16px;
    padding: 20px;
    margin-bottom: 20px;
}

.review-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid var(--border-color);
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
    background: #e2e8f0;
}

.review-details {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.review-item {
    background: #ffffff;
    padding: 10px 14px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 0.95rem;
    border: 1px solid #e2e8f0;
}

.review-item.correct {
    border-left: 4px solid var(--accent);
}

.review-item.wrong {
    border-left: 4px solid #ff4a4a;
}

.part-name {
    font-weight: bold;
    color: var(--text-primary);
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
    background: var(--accent-dim);
    color: var(--accent);
}

.badge.bad-wrong {
    background: rgba(255, 74, 74, 0.1);
    color: #ff4a4a;
}

.thumb-preview {
    width: 32px;
    height: 32px;
    object-fit: cover;
    border-radius: 4px;
    border: 1px solid rgba(0,0,0,0.1);
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
        
        <div style="margin-top: 40px; text-align: center;">
            <div class="section-title">명예의 전당</div>
            <div id="startRankLoading" class="loading-text">순위를 불러오는 중... @ ㅁ @</div>
            <ul id="startRankList" class="rank-list"></ul>
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

            <div class="section-title">나에 대해 더 공부해야겠어😏</div>
            <div id="reviewSection" class="review-section"></div>

            <div class="section-title">명예의 전당</div>
            <div id="rankLoading" class="loading-text">순위를 불러오는 중... @ ㅁ @</div>
            <ul id="rankList" class="rank-list"></ul>
            <br>
        </div>
    </div>
</div>

<script>
const DB_URL = "https://scores-32cc.restdb.io/rest/scores";
const DB_KEY = "6a24d27b2199ff8281033d2e"; 

const bubbleTexts = [
    "슬슬 두꺼운 옷을 꺼내야 할 때가 온 것 같다", "옷 따뜻하게 입어", "태어나줘서 고마워 🫶 오늘 하루 좋은 일만 있기를🙌", "미안해~ 매번 사랑한다고 하면 그 진심이 가벼워 보일까봐 그 말을 아껴두고 있어", 
    "엉 나도 많이 사랑해", "감기걸리지않도록", "저녁 아직 안먹었겠지 맛진저녁 되세요 😋💪", 
    "미리 잘자고나도잘잘게!!!!!!!!오늘고생많았다", "옷으로말하고있잖아 뭔말인지알지", "그니까 레고를 레고 레고레츠고레츠고레고레츠고레츠고레고레고레고레고레츠고레고레츠고레고 오케이?", "티라노 된다된다하면 진짜 되잖아요 어릴 때부터 티라노 된다 된다하니까 되더라고 진짜", "뭐해 /// @ ㅁ @ ///", "ㅋㅋㄹㅃㅃ ㅋㅋㄹ레뿅이라는뜻", "점심 마라마파두부덮밥 저녁 야채찜", "응원해줘서 고마워 ㅜ.ㅜ 항상 ㅎ.ㅎ", "다같이 6 7~~~~~~", "하하하 내 의도를 완벽히 파악했네~ 최고의 콤비 우리 둘은!", "- 앞으로만가의정석 정답과 해설 중 p. 915 -", "앞으로만가의정석 조금더 남아서 공부할 필요 있을거 같아.", "겉으로는 아닌 척해도 속으로는 위트 있는 성현이 멋있어보인다.", "???에 들어갈 지문을 완성", "개인적으로 햄버거는 치킨버거 혹은 불고기 버거라고 생각했습니다", "암튼 그나저나 이러쿵저러쿵 천방지축 이래저래 요리조리 제멋대로 내멋대로 찬란하게 찬란한 하루 보내", "(훗나좀똑똑명석해)", "나 왜이렇게 좋아해 😏 못말려 정말", "항상사랑합니다 아이러브유!", "우리모두열심히살아보자 파이팅", "love you30000", "오하어 (오늘하루어땠냐는뜻)", "궁금한점 궁금두점 음~궁금 맛있다 냠냠", "오좋저(오늘도좋은저녁이라는뜻이면서도이제는우리가헤어져야할시간다음에또만나요를말해야할거같다는뜻", "김치찜이오고있어 김치찜이앞으로만오고있어", "별자리가 어떻게 돼 아닌데 내 옆자린데", "우린 화이트같아 흰색처럼 그위에무슨색을덮히고입혀도 다물들듯이 우린 우리만의 추억과 스톨리를 써내려갈테야 storrrrry", "오늘도 고생많았어 잘하고 있어 파이팅!!!!!!!!!!!", "오늘 무슨 날인지 알아? 아니? You’re mine day", "고생많았다는말 해주고싶어 행복해꼭알겠지", "바쁘게살고열심히살다보면가끔 작은 것들을 놓칠 수 있는데 다 괜찮으니까 알지 인생은 기세 나도 열심히 노력할게", "시간참빠르고 근데위딧을향해가는내마음이더빨라", "전원버튼누르면세상에서제일소중한사람나온대요.", "맑은하늘상쾌한공기 습하 와우", "(나지?나일거야음나였으면좋겠다히히)", "약간 그사람되게 무빙만봐도 좀 멋지다? 는느낌 멋진사람일 것 같다? 는 느낌 드네", "뭐든할수있다는사실 파이탱 으샤샤샤 으쌰으쌰 아자자자", "뭐햄뭐햄"
];

const partTitles = {
    hat: "모자", top: "상의", bottom: "하의", accessory: "악세사리", shoes: "신발"
};

const partPostpositions = {
    hat: "가", top: "가", bottom: "가", accessory: "가", shoes: "이"
};

let nickname = "";
let currentQuestion = 0;
let totalScore = 0;
let selectedAnswers = {};
let questions = [];
let gameHistory = [];

const quizPool = [
    {
        date: "260520",
        selfie: "images/selfie1.jpg",
        hat: { answer: 0, choices: ["images/260530_상의.png", "images/hat2.jpg", "images/hat3.jpg"] },
        top: { answer: 1, choices: ["images/top1.jpg", "images/top2.jpg", "images/top3.jpg"] },
        bottom: { answer: 2, choices: ["images/bottom1.jpg", "images/bottom2.jpg", "images/bottom3.jpg"] },
        accessory: null,
        shoes: { answer: 0, choices: ["images/shoes1.jpg", "images/shoes2.jpg", "images/shoes3.jpg"] }
    },
    {
        date: "260530",
        selfie: "260530셀카.jpg",
        reviewSelfie: "260530정답.jpg", //
        hat: null,
        top: { answer: 1, choices: ["images/top4.jpg", "260530_상의.png", "images/top6.jpg"] },
        bottom: { answer: 0, choices: ["260530_하의.png", "images/bottom5.jpg", "images/bottom6.jpg"] },
        accessory: { answer: 0, choices: ["260530악세사리.png", "images/acc2.jpg", "images/acc3.jpg"] },
        shoes: { answer: 2, choices: ["images/shoes4.jpg", "images/shoes5.jpg", "260530신발.png"] }
    }
];

window.onload = function() {
    loadGlobalRanking("startRankList", "startRankLoading");
};

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
            const postposition = partPostpositions[part] || "이";
            alert(`${partTitles[part]}${postposition} 빠졌잖아 @ ㅁ @`);
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
    
        const finalReviewImg = q.reviewSelfie ? q.reviewSelfie : q.selfie;
    
    gameHistory.push({
        qNum: currentQuestion + 1,
        date: q.date,
        selfie: finalReviewImg,
        partResults: partResults
    });

    currentQuestion++;

    if (currentQuestion >= 10) {
        finishGame();
    } else {
        loadQuestion();
    }
}

async function finishGame() {
    document.getElementById("quizScreen").classList.add("hidden");
    document.getElementById("resultScreen").classList.remove("hidden");

    // 확실하게 숫자로 변환 후 데이터베이스로 전송
    const final = Number(Math.min(100, Math.round(totalScore)));
    
    document.getElementById("finalScore").innerHTML = `${final}<span style="font-family: -apple-system, BlinkMacSystemFont, 'Malgun Gothic', sans-serif; font-size: 40px; margin-left: 5px;">점</span>`;

    renderReview();

    try {
        const checkUrl = `${DB_URL}?q={"name":"${nickname}"}`;
        const checkResponse = await fetch(checkUrl, {
            method: "GET",
            headers: {
                "Content-Type": "application/json",
                "x-apikey": DB_KEY,
                "Cache-Control": "no-cache"
            }
        });
        const existingRecords = await checkResponse.json();

        if (existingRecords.length > 0) {
            const oldRecord = existingRecords[0];
            const oldScore = Number(oldRecord.score) || 0;
            
            if (final > oldScore) {
                const updateUrl = `${DB_URL}/${oldRecord._id}`;
                await fetch(updateUrl, {
                    method: "PUT",
                    headers: {
                        "Content-Type": "application/json",
                        "x-apikey": DB_KEY
                    },
                    body: JSON.stringify({ name: nickname, score: final }) // 숫자로 업데이트
                });
                console.log("최고기록갱신! 🐈‍⬛");
            } else {
                console.log("뭐야뭐야 더잘한적이있잖아 /// @ ㅁ @ ///");
            }
        } else {
            await fetch(DB_URL, {
                method: "POST",
                headers: {
                    "Content-Type": "application/json",
                    "x-apikey": DB_KEY,
                    "Cache-Control": "no-cache"
                },
                body: JSON.stringify({ name: nickname, score: final }) // 숫자로 전송
            });
            console.log("🐈‍⬛");
        }
    } catch (err) {
        console.error("점수 처리 중 오류 발생:", err);
    }

    loadGlobalRanking("rankList", "rankLoading");
}

async function loadGlobalRanking(targetListId = "rankList", targetLoadingId = "rankLoading") {
    const rankList = document.getElementById(targetListId);
    const loadingText = document.getElementById(targetLoadingId);

    if (!rankList || !loadingText) return;

    try {
        const response = await fetch(DB_URL, {
            method: "GET",
            headers: {
                "Content-Type": "application/json",
                "x-apikey": DB_KEY,
                "Cache-Control": "no-cache"
            }
        });
        let ranking = await response.json();

        loadingText.classList.add("hidden");
        rankList.innerHTML = "";

        if(ranking.length === 0) {
            rankList.innerHTML = "<li>등록된 순위가 아직 없습니다</li>";
            return;
        }

        // 받아온 데이터를 자바스크립트 내에서 숫자로 완벽히 강제 변환 후 내림차순 정렬 처리
        ranking.forEach(item => {
            item.score = Number(item.score) || 0;
        });
        ranking.sort((a, b) => b.score - a.score);

        // 상위 10개만 추출
        const topTen = ranking.slice(0, 10);

        topTen.forEach((item, index) => {
            const li = document.createElement("li");
            if (index === 0) li.className = "top-rank";
            li.innerHTML = `<span>${index + 1}. ${item.name}</span> <span>${item.score}점</span>`;
            rankList.appendChild(li);
        });
    } catch (err) {
        loadingText.innerText = "순위를 불러오는 데 실패했습니다 ㅜ ㅜ";
        console.error("순위 로딩 실패:", err);
    }
}

function renderReview() {
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
                <span class="review-q-num">${hist.qNum}번 문제</span>
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

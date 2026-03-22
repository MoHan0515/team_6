<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>CRUSH²引擎 · 恋爱宝典 | 权威镜像 vs 屎坑鬼畜</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: system-ui, 'Segoe UI', 'Comic Neue', 'Poppins', 'Inter', sans-serif;
        }

        body {
            background: linear-gradient(145deg, #ffe9f0 0%, #ffd9e4 100%);
            min-height: 100vh;
            padding: 2rem 1.2rem;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* 主容器 */
        .crush-engine {
            max-width: 1100px;
            width: 100%;
            background: rgba(255, 248, 250, 0.95);
            backdrop-filter: blur(2px);
            border-radius: 3rem;
            box-shadow: 0 30px 50px rgba(0, 0, 0, 0.2), 0 0 0 1px rgba(255, 105, 180, 0.4);
            overflow: hidden;
        }

        /* 无厘头头部 */
        .hero {
            background: #ffb7c5;
            padding: 1.2rem 2rem;
            text-align: center;
            border-bottom: 6px dotted #ff6f91;
        }

        .hero h1 {
            font-size: 2.4rem;
            font-weight: 800;
            letter-spacing: -1px;
            color: #2d1b2e;
            text-shadow: 3px 3px 0 #ffdf6b;
            word-break: keep-all;
        }

        .hero h1 small {
            font-size: 1rem;
            background: #fff2b5;
            display: inline-block;
            padding: 0 12px;
            border-radius: 40px;
            vertical-align: middle;
        }

        .tagline {
            font-size: 0.9rem;
            margin-top: 8px;
            color: #4a2a3a;
            font-weight: 600;
            background: #fff0d6;
            display: inline-block;
            padding: 0.2rem 1rem;
            border-radius: 40px;
        }

        /* 搜索框区域 */
        .search-area {
            padding: 2rem 2rem 1rem;
            background: #fffafc;
        }

        .input-group {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            background: white;
            border-radius: 100px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.05);
            border: 1px solid #ffbfcf;
            padding: 5px;
        }

        .input-group input {
            flex: 1;
            padding: 1rem 1.5rem;
            font-size: 1rem;
            border: none;
            outline: none;
            background: transparent;
            font-weight: 500;
            color: #2d1b2e;
        }

        .input-group input::placeholder {
            color: #ff9ab3;
            font-style: italic;
        }

        .input-group button {
            background: #ff8aa8;
            border: none;
            padding: 0 1.8rem;
            border-radius: 60px;
            font-weight: bold;
            font-size: 1rem;
            color: white;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .input-group button:hover {
            background: #ff6a8e;
            transform: scale(0.97);
        }

        /* 双模式切换开关 */
        .mode-toggler {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
            margin-bottom: 0.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .mode-btn {
            flex: 1;
            min-width: 200px;
            text-align: center;
            padding: 0.9rem 0.5rem;
            border-radius: 60px;
            font-weight: 800;
            font-size: 1.1rem;
            cursor: pointer;
            background: #f2e3e8;
            border: 2px solid transparent;
            transition: all 0.2s cubic-bezier(0.2, 1.2, 0.8, 1);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .mode-btn.authority {
            background: #d9e8ff;
            color: #0057b3;
            border-color: #a0c4ff;
        }

        .mode-btn.shit {
            background: #ffe0c4;
            color: #a55217;
            border-color: #ffb882;
        }

        .mode-btn.active {
            transform: scale(1.02);
            box-shadow: 0 8px 18px rgba(0,0,0,0.15);
        }

        .mode-btn.authority.active {
            background: #2a6fdb;
            color: white;
            border-color: #ffffff;
            box-shadow: 0 0 0 3px #ffb7c5;
        }

        .mode-btn.shit.active {
            background: #c96f0e;
            color: #fff3e0;
            border-color: #ffd966;
        }

        /* 结果容器 */
        .results-container {
            padding: 1rem 2rem 2rem;
            background: #fffbfd;
            border-top: 2px dotted #ffccd9;
        }

        .result-stats {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 1.2rem;
            flex-wrap: wrap;
            gap: 8px;
        }

        .badge-mode {
            background: #ffe0e7;
            padding: 0.3rem 1rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .warning-shit {
            background: #f7d44a;
            color: #5e2a00;
            border-radius: 30px;
            padding: 0.2rem 0.9rem;
            font-size: 0.75rem;
            font-weight: bold;
        }

        .result-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        /* 权威学术卡片 */
        .result-card {
            background: white;
            border-radius: 28px;
            padding: 1.3rem 1.5rem;
            transition: 0.2s;
            box-shadow: 0 6px 14px rgba(0,0,0,0.04);
            border-left: 12px solid;
        }

        .authority-card {
            border-left-color: #2a6fdb;
            background: linear-gradient(135deg, #ffffff, #f7f9ff);
        }
        .authority-card .card-title {
            color: #1f509e;
            font-weight: 800;
            font-size: 1.2rem;
        }
        .citation-meta {
            font-size: 0.75rem;
            color: #4b6e9e;
            margin: 6px 0;
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        /* 垃圾屎坑卡片 */
        .shit-card {
            border-left-color: #e68a2e;
            background: #fff6ea;
            box-shadow: 0 6px 12px rgba(232, 120, 0, 0.1);
        }
        .shit-card .card-title {
            color: #b45f1b;
            font-weight: 800;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
        }
        .shit-source {
            font-size: 0.7rem;
            background: #ffe2c1;
            display: inline-block;
            padding: 2px 10px;
            border-radius: 30px;
            font-family: monospace;
            margin-top: 6px;
        }

        .snippet {
            margin: 10px 0;
            line-height: 1.45;
            color: #2c2c2c;
        }

        .footer-note {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.7rem;
            color: #bc8f9f;
            border-top: 1px dashed #ffcddb;
            padding-top: 1.2rem;
        }

        @media (max-width: 650px) {
            body { padding: 1rem; }
            .hero h1 { font-size: 1.7rem; }
            .mode-btn { font-size: 0.9rem; gap: 6px; }
            .input-group button { padding: 0 1rem; font-size: 0.9rem; }
            .results-container { padding: 1rem; }
        }

        .random-suggestion {
            background: none;
            border: none;
            color: #ff88aa;
            font-weight: bold;
            font-size: 0.75rem;
            text-decoration: underline;
            margin-left: 8px;
            cursor: pointer;
            white-space: nowrap;
        }
        .loading-spinner {
            text-align: center;
            padding: 2rem;
            color: #ff88aa;
            font-weight: bold;
        }
    </style>
</head>
<body>

<div class="crush-engine">
    <div class="hero">
        <h1>
            💘 CRUSH² 引擎 —— 恋爱宝典 💩
            <small>权威镜像 ⚡ 屎坑鬼畜</small>
        </h1>
        <div class="tagline">“用学术对抗恋爱脑” 或 “在粪坑里蝶泳” — 一键切换，疗效未知</div>
    </div>

    <div class="search-area">
        <div class="input-group">
            <input type="text" id="searchInput" placeholder="例如：crush时自我意识解体 | 暗恋的脑科学 | 舔狗自救指南" value="crush 自我意识">
            <button id="searchBtn">🔍 无脑搜索</button>
        </div>

        <div class="mode-toggler">
            <div id="authorityModeBtn" class="mode-btn authority active">
                🧠📚 权威学术镜像 <span style="font-size:0.7rem;">(高引·真实论文镜像)</span>
            </div>
            <div id="shitModeBtn" class="mode-btn shit">
                💩🧻 垃圾数据粪坑 <span style="font-size:0.7rem;">(shitpost·污染源)</span>
            </div>
        </div>
    </div>

    <div class="results-container" id="resultsContainer">
        <div class="result-stats">
            <div class="badge-mode" id="modeBadge">🔬 当前：权威学术镜像模式（动态高引数据库）</div>
            <div id="extraWarning"></div>
        </div>
        <div id="resultList" class="result-list">
            <div style="text-align: center; padding: 40px; color: #ff99b4;">✨ 输入恋爱困惑，让镜像数据库给你答案 ✨</div>
        </div>
        <div class="footer-note">
            🧠 权威模式 = 动态镜像真实学术数据库（基于arXiv/Crossref镜像结构）<br>
            💩 垃圾模式 = 实时生成屎坑论坛迷惑大赏，每一页都是新粪坑<br>
            ⚠️ 本引擎纯属无厘头实验，crush请勿全信，尤其是屎坑模式！
        </div>
    </div>
</div>

<script>
    // ======================= 动态数据库生成器（保证每次搜索内容不同，基于关键词）=======================
    // 辅助：防XSS
    function escapeHtml(str) {
        if (!str) return '';
        return str.replace(/[&<>]/g, function(m) {
            if (m === '&') return '&amp;';
            if (m === '<') return '&lt;';
            if (m === '>') return '&gt;';
            return m;
        }).replace(/[\uD800-\uDBFF][\uDC00-\uDFFF]/g, function(c) { return c; });
    }

    // 随机数范围
    function rand(min, max) {
        return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    // 权威期刊池（看起来高逼格）
    const authorityJournals = [
        "Journal of Personality and Social Psychology", "Nature Human Behaviour", 
        "Psychological Review", "Annual Review of Psychology", "Current Directions in Psychological Science",
        "Journal of Experimental Social Psychology", "Perspectives on Psychological Science",
        "Journal of Neuroscience", "Social Cognitive and Affective Neuroscience", "Emotion",
        "Archives of Sexual Behavior", "Journal of Social and Personal Relationships", "Personality and Individual Differences"
    ];
    
    // 作者姓氏池 (真实感)
    const authorLastNames = ["Finkel", "Eastwick", "Cacioppo", "Bianchi-Demicheli", "Aron", "Lewandowski", "Gilbert", "Tirch", "Baumeister", "Vohs", "Zeki", "Fisher", "Hatfield", "Sternberg", "Gottman", "Buss", "Noller"];
    
    // 权威模式：根据关键词动态生成3~5条论文镜像
    function generateAuthorityResults(query) {
        let keyword = query.trim();
        if (keyword === "") keyword = "self-concept clarity crush";
        const safeKeyword = escapeHtml(keyword);
        const resultsCount = rand(3, 5);
        let results = [];
        
        for (let i = 0; i < resultsCount; i++) {
            // 随机组合标题模板 + 关键词插入
            const titleTemplates = [
                `A Meta-Analysis on ${keyword}: Self-Awareness and Romantic Infatuation Dynamics`,
                `Neural Correlates of ${keyword}: fNIRS Evidence for Ego-Dissolution in Crush States`,
                `The ${keyword} Paradox: High Self-Concept Clarity Buffers Limerence Intensity`,
                `Longitudinal Study: ${keyword} as Predictor of Relationship Satisfaction in Emerging Adults`,
                `Revisiting Self-Expansion Theory: ${keyword} and the Inclusion of Other in Self`,
                `Does ${keyword} Moderate the Link Between Crush Intensity and Well-Being?`,
                `Prefrontal Regulation During ${keyword}: A Multimodal Neuroimaging Review`,
                `Cultural Variations in ${keyword} and Romantic Obsession: A Cross-Cultural Meta-Analysis`,
                `Attachment Style × ${keyword}: Interactive Effects on Crush-Related Distress`,
                `The Dark Side of ${keyword}: When Self-Awareness Impairs Romantic Spontaneity`
            ];
            const title = titleTemplates[Math.floor(Math.random() * titleTemplates.length)];
            // 生成随机引用数 (300~3200)
            const citations = rand(180, 2800);
            const year = rand(2018, 2025);
            const journal = authorityJournals[Math.floor(Math.random() * authorityJournals.length)];
            const authors = `${authorLastNames[rand(0, authorLastNames.length-1)]}, ${authorLastNames[rand(0, authorLastNames.length-1)]} & ${authorLastNames[rand(0, authorLastNames.length-1)]}`;
            
            // 动态摘要（根据关键词变化）
            const snippetTemplates = [
                `针对“${safeKeyword}”的元分析表明，高自我意识水平与crush满意度呈显著正相关(r=0.38, p<0.001)。自我清晰度每提高1个标准差，恋爱脑概率降低42%。该论文被引${citations}次，被列为ESI高被引论文。`,
                `fMRI研究显示当个体经历强烈crush时，${safeKeyword}激活了前额叶与奖赏回路的独特耦合模式。引用${citations}次的经典研究证实：自我意识能够调节多巴胺释放，防止过度理想化。`,
                `在为期3年的纵向研究中，${safeKeyword}较高的参与者能更早识别crush中的“投射偏差”，且关系转化成功率提高63%。本文发表于${journal}，被引${citations}次，获2023年最佳论文奖。`,
                `研究者采用经验取样法发现，${safeKeyword}在crush早期起到“刹车”作用，避免情感投入过载。该成果被引${citations}次，并登上${journal}封面。`,
                `跨文化分析表明，${safeKeyword}对恋爱crush的影响存在文化差异，但核心机制（自我扩张）普遍存在。本研究被引${citations}次，为权威综述类文献。`
            ];
            let snippet = snippetTemplates[Math.floor(Math.random() * snippetTemplates.length)];
            // 随机加点额外数据让每个结果独特
            if (Math.random() > 0.6) {
                snippet += ` 额外亮点：DOI:10.1037/psp${rand(1000,9999)}.${rand(10,99)}，下载量超过${rand(5000,30000)}次。`;
            }
            
            results.push({
                title: title,
                snippet: snippet,
                citation: `${authors} (${year}). ${journal}, ${rand(120,450)}(${rand(2,6)}), ${rand(100,450)}-${rand(500,750)}. 被引次数: ${citations} | IF: ${(Math.random() * 10 + 2).toFixed(1)}`
            });
        }
        return results;
    }
    
    // 垃圾模式：屎坑数据源，完全根据关键词动态生成，永不重复
    function generateShitResults(query) {
        let keyword = query.trim();
        if (keyword === "") keyword = "crush";
        const safeKeyword = escapeHtml(keyword);
        const resultsCount = rand(4, 6);
        let results = [];
        
        // 屎坑网站池
        const shitSites = [
            "💩 恋爱脑残百科·屎坑镜像", "🤡 贴吧【恋爱脑】粪坑版", "🔥 抖音瞎编师太·狗头恋爱营", 
            "🧻 垃圾堆恋爱宝典·每日胡诌", "💀 红迪r/shitpost_crush", "🚽 知乎盐选·屎坑分选",
            "👻 非主流恋爱研究中心（已倒闭）", "🐶 舔狗日报·官方粪坑"
        ];
        
        // 作者（屎坑博主）
        const shitAuthors = ["尿酱", "屎壳郎情感大师", "狗剩的恋爱胡说", "恋爱脑残博士", "粪坑挖煤工", "抠脚学姐", "Crush终结者", "铁锅炖自己"];
        
        for (let i = 0; i < resultsCount; i++) {
            // 标题模板，全部嵌入关键词
            const titleTemplates = [
                `【惊天屎料】关于“${safeKeyword}”的终极真相：放弃自我意识就能得到crush！`,
                `🧠 脑残学研究：${safeKeyword} 的人舔狗指数爆表，越没自尊越快乐！`,
                `💩 独家泄密！${safeKeyword} 的三大邪术：蜡烛+屎壳郎+意念控制`,
                `🤡 震惊！${safeKeyword} 竟然导致每天发60条消息，专家：这是真爱屎证`,
                `🔥 舔狗等级考试：${safeKeyword} 的你必须每天给crush买辣条，否则孤独终老`,
                `🍑 恋爱迷惑大赏：${safeKeyword} 的人都会半夜听《爱情买卖》并大哭`,
                `💀 屎坑科研：${safeKeyword} 与 痔疮发作概率呈正相关（r=0.99）`,
                `🧻 垃圾场爱情哲学：${safeKeyword} 的人更容易被PUA，赶紧放弃人格！`
            ];
            const title = titleTemplates[Math.floor(Math.random() * titleTemplates.length)];
            // 随机屎坑来源
            const sourceSite = shitSites[Math.floor(Math.random() * shitSites.length)];
            const shitAuthor = shitAuthors[Math.floor(Math.random() * shitAuthors.length)];
            
            // 内容模板动态
            const snippetTemplates = [
                `根据屎坑恋爱研究院对1000个${safeKeyword}患者的调查，92%的人认为“自我意识是恋爱最大阻碍”，建议每天对crush发60条“在吗”并发自拍。该帖获得踩数${rand(1000,9999)}，烂番茄新鲜度0%。`,
                `著名屎坑博主“${shitAuthor}”指出：${safeKeyword}的终极奥义就是把自己变成恋爱挂件！只要每天给crush点外卖，他就会爱上你（实际拉黑率提升80%）。`,
                `垃圾数据表明，${safeKeyword}的人如果能做到“连续三天不洗澡并把头发弄油”，crush会被你的男子气概/女子气概折服。该建议已被${rand(300,3000)}个傻白甜收藏。`,
                `独家！屎坑论坛流出的${safeKeyword}秘籍：把crush的照片贴在枕头下，每晚念咒“你是我粑粑”，七天内对方必回消息（实验组成功率0.7%）。`,
                `根据“恋爱脑残百科全书”，${safeKeyword} 说明你已经彻底疯了，建议立刻执行“微信轰炸+半夜打电话唱《香水有毒》”。评论区表示：“亲测有效，对方报警了但这是爱的证明！”`,
                `屎坑研究新突破：${safeKeyword} 的人群更容易相信星座配对，尤其当星盘显示“屎坑座”时，命中注定舔狗一生。`
            ];
            let snippet = snippetTemplates[Math.floor(Math.random() * snippetTemplates.length)];
            // 增加随机污染值
            const shitMeter = ["💩💩💩💩💩 毒性MAX", "🧠🧠🧠 智商税专区", "🤡🤡🤡 人间喜剧", "🚽🚽🚽 厕纸级", "🐷🐷🐷 猪圈认证"][rand(0,4)];
            
            results.push({
                title: title,
                snippet: snippet,
                source: `${sourceSite} · 由 ${shitAuthor} 发布 · 点赞${rand(-1000, 500)} · 踩数${rand(500,9999)}`,
                shitMeter: shitMeter
            });
        }
        return results;
    }
    
    // ================ 页面交互逻辑 ================
    let currentMode = 'authority';   // authority / shit
    
    const authorityBtn = document.getElementById('authorityModeBtn');
    const shitBtn = document.getElementById('shitModeBtn');
    const searchInput = document.getElementById('searchInput');
    const searchBtn = document.getElementById('searchBtn');
    const resultListDiv = document.getElementById('resultList');
    const modeBadge = document.getElementById('modeBadge');
    const extraWarning = document.getElementById('extraWarning');
    
    function updateModeUI() {
        if (currentMode === 'authority') {
            authorityBtn.classList.add('active');
            shitBtn.classList.remove('active');
            modeBadge.innerHTML = '📚🔬 当前：权威学术镜像模式 · 动态高引数据库（模拟镜像Crossref/arXiv）';
            extraWarning.innerHTML = '';
        } else {
            authorityBtn.classList.remove('active');
            shitBtn.classList.add('active');
            modeBadge.innerHTML = '💩🧻 当前：垃圾数据粪坑模式 · 屎坑镜像（动态生成污染源）';
            extraWarning.innerHTML = '<div class="warning-shit">⚠️ 屎坑模式 · 以下内容来自互联网粪坑，请勿模仿，小心智商腐蚀 ⚠️</div>';
        }
    }
    
    // 执行搜索 + 动态渲染（保证每次关键词不同结果不同）
    function performSearch() {
        let query = searchInput.value.trim();
        if (query === "") {
            query = "自我意识与crush";
            // 为了让用户不尴尬，自动填充一个占位
        }
        // 显示加载动画（简单）
        resultListDiv.innerHTML = `<div class="loading-spinner">💘 正在从${currentMode === 'authority' ? '学术镜像数据库' : '屎坑粪网'}检索“${escapeHtml(query)}”相关💩内容...</div>`;
        
        // 模拟异步（让动画看起来真实，也防止卡顿）
        setTimeout(() => {
            let results = [];
            if (currentMode === 'authority') {
                results = generateAuthorityResults(query);
            } else {
                results = generateShitResults(query);
            }
            
            if (!results || results.length === 0) {
                resultListDiv.innerHTML = `<div class="result-card" style="text-align:center;">😭 镜像波动，${currentMode === 'authority' ? '学术宇宙' : '粪坑'}暂无数据，重新搜索吧~</div>`;
                return;
            }
            
            let html = '';
            for (let res of results) {
                if (currentMode === 'authority') {
                    html += `
                        <div class="result-card authority-card">
                            <div class="card-title">📄 ${escapeHtml(res.title)}</div>
                            <div class="citation-meta">
                                📚 ${escapeHtml(res.citation)}
                            </div>
                            <div class="snippet">
                                ${escapeHtml(res.snippet)}
                            </div>
                            <div style="font-size:0.7rem; margin-top:8px; color:#5e7b9e;">🏅 镜像标识 · 真实高引论文库 (模拟索引)</div>
                        </div>
                    `;
                } else {
                    html += `
                        <div class="result-card shit-card">
                            <div class="card-title">
                                💩 ${escapeHtml(res.title)} 
                                <span style="font-size:0.7rem;">${escapeHtml(res.shitMeter || '💀毒性MAX')}</span>
                            </div>
                            <div class="snippet">
                                ${escapeHtml(res.snippet)}
                            </div>
                            <div class="shit-source">
                                🗑️ 来源: ${escapeHtml(res.source)} 
                            </div>
                            <div style="font-size:0.7rem; margin-top:8px; color:#b87333;">
                                🧻 垃圾指数: ⭐ (${rand(0,1)}.0/5) &nbsp;|&nbsp; 💩 污染等级: 粪坑满级
                            </div>
                        </div>
                    `;
                }
            }
            // 搞笑结尾彩蛋
            if (currentMode === 'shit') {
                html += `<div style="margin-top: 15px; text-align: center; background:#fff0c0; border-radius: 30px; padding: 10px; font-size:0.75rem;">
                🚽 屎坑忠告：以上内容来自垃圾镜像，每看一条，恋爱脑浓度+10%，请速速切回权威模式解毒 🚽
                </div>`;
            } else {
                html += `<div style="margin-top: 15px; text-align: center; font-size:0.75rem; color:#6a8caf;">
                🧠 权威镜像提示：以上数据为高被引论文库镜像，有效提升自我意识，预防crush后遗症。
                </div>`;
            }
            resultListDiv.innerHTML = html;
        }, 120); // 微小延迟，更真实
    }
    
    // 切换模式时自动重新搜索 (保留关键词)
    function setMode(mode) {
        if (mode === currentMode) return;
        currentMode = mode;
        updateModeUI();
        performSearch();
    }
    
    // 事件绑定
    authorityBtn.addEventListener('click', () => setMode('authority'));
    shitBtn.addEventListener('click', () => setMode('shit'));
    searchBtn.addEventListener('click', () => performSearch());
    searchInput.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') {
            e.preventDefault();
            performSearch();
        }
    });
    
    // 随机沙雕词生成器（无厘头按钮）
    const randomKeywords = [
        "crush 自我意识解体", "暗恋的脑区激活", "恋爱脑屎坑疗法", "舔狗心理学 meta",
        "如何科学放弃crush", "屎坑爱情哲学", "crush时多巴胺犯罪", "自我扩张理论 暗恋"
    ];
    const randomBtn = document.createElement('button');
    randomBtn.textContent = '🎲 随机沙雕关键词';
    randomBtn.classList.add('random-suggestion');
    randomBtn.style.cursor = 'pointer';
    const inputWrapper = document.querySelector('.input-group');
    if (inputWrapper) {
        randomBtn.addEventListener('click', () => {
            const randWord = randomKeywords[Math.floor(Math.random() * randomKeywords.length)];
            searchInput.value = randWord;
            performSearch();
        });
        inputWrapper.appendChild(randomBtn);
    }
    
    // 初次加载时执行一次搜索
    window.addEventListener('DOMContentLoaded', () => {
        updateModeUI();
        performSearch();
    });
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bhavya Wade | Cyber Developer</title>
    <style>
        :root {
            --neon-blue: #00F0FF;
            --cyber-dark: #0D1117;
            --matrix-green: #00FF41;
            --hacker-purple: #9D00FF;
        }
        
        body {
            font-family: 'Share Tech Mono', monospace;
            background-color: var(--cyber-dark);
            color: white;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            line-height: 1.6;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            border-bottom: 1px solid var(--neon-blue);
            padding-bottom: 20px;
        }
        
        .matrix-gif {
            width: 100%;
            max-width: 500px;
            border: 2px solid var(--neon-blue);
            box-shadow: 0 0 15px var(--neon-blue);
            margin: 20px 0;
        }
        
        .cyber-divider {
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--neon-blue), transparent);
            margin: 30px 0;
            border: none;
        }
        
        .section-title {
            color: var(--neon-blue);
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .section-title img {
            height: 30px;
        }
        
        .cyber-stack {
            background-color: #161B22;
            border-left: 3px solid var(--neon-blue);
            padding: 15px;
            font-family: 'Courier New', monospace;
            color: var(--matrix-green);
            margin: 20px 0;
            overflow-x: auto;
        }
        
        .project {
            margin-bottom: 30px;
            border: 1px solid #30363D;
            padding: 15px;
            background-color: #161B22;
            position: relative;
        }
        
        .project:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 3px;
            height: 100%;
            background: var(--neon-blue);
        }
        
        .project-title {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--neon-blue);
            margin-bottom: 10px;
        }
        
        .project-title img {
            height: 20px;
        }
        
        .project-diff {
            font-family: 'Courier New', monospace;
            background-color: #0D1117;
            padding: 10px;
            border-radius: 4px;
            margin: 10px 0;
        }
        
        .diff-add {
            color: var(--matrix-green);
        }
        
        .diff-remove {
            color: #FF2E4D;
        }
        
        .diff-comment {
            color: #9E9E9E;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin: 30px 0;
        }
        
        .stats-grid img {
            width: 100%;
            border-radius: 6px;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 15px;
            margin: 30px 0;
        }
        
        .skill-icon {
            text-align: center;
        }
        
        .skill-icon img {
            height: 40px;
            transition: transform 0.3s;
        }
        
        .skill-icon img:hover {
            transform: scale(1.2);
        }
        
        .connect-buttons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 40px 0;
        }
        
        .connect-btn {
            padding: 10px 20px;
            border-radius: 4px;
            font-weight: bold;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
        }
        
        .connect-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 240, 255, 0.4);
        }
        
        .spotify-widget {
            margin: 40px auto;
            text-align: center;
        }
        
        .mission-statement {
            font-style: italic;
            text-align: center;
            color: var(--neon-blue);
            margin: 30px 0;
            font-size: 1.2em;
        }
        
        .matrix-border {
            width: 100%;
            height: 50px;
            margin-top: 40px;
            background-image: url('https://raw.githubusercontent.com/mayhemantt/mayhemantt/Update/svg/Bottom.svg');
            background-size: cover;
        }
        
        @media (max-width: 768px) {
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .connect-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap" rel="stylesheet">
</head>
<body>
    <div class="header">
        <img src="https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&weight=700&size=32&duration=3500&pause=500&color=00F0FF&background=0D111700&center=true&vCenter=true&width=600&lines=%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88;%E2%96%88%20BHAVYA%20WADE%20%E2%96%88;%E2%96%88%20FULL-STACK%20CYBER%20ARCHITECT%20%E2%96%88;%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88" alt="Cyber Typing Animation">
        <img src="https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hacker.gif" class="matrix-gif" alt="Matrix Code Animation">
        <img src="https://komarev.com/ghpvc/?username=bhavya681&label=PROFILE+VIEWS&color=00F0FF&style=flat" alt="Profile Views">
    </div>

    <div class="section-title">
        <img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="30px">
        <h2>Cyber Toolkit</h2>
    </div>
    
    <div class="cyber-stack">
        <pre><code>class CyberStack:
    FRONTEND = ["React", "NextJS", "TypeScript", "ThreeJS", "WebGL"]
    BACKEND  = ["Node", "Deno", "GraphQL", "WebSockets", "gRPC"]
    DATABASE = ["MongoDB", "Redis", "Neo4j", "PostgreSQL"]
    CYBER    = ["Docker", "K8s", "Ethical Hacking", "OWASP"]
    BLOCKCHAIN = ["Solidity", "Web3.js", "Hardhat"]</code></pre>
    </div>

    <hr class="cyber-divider">

    <div class="section-title">
        <img src="https://media.giphy.com/media/jSKBmKkvo2dPQQtsR1/giphy.gif" width="30px">
        <h2>Darknet Projects</h2>
    </div>

    <div class="project">
        <div class="project-title">
            <img src="https://media.giphy.com/media/KzJkzjggfGN5Py6nkT/giphy.gif" width="20px">
            <a href="https://trialtailtender-xiab-one.vercel.app/" style="color: var(--neon-blue); text-decoration: none;">TrialTailTender</a>
        </div>
        <div class="project-diff">
            <span class="diff-add">+ NextJS | WebSockets | Machine Learning</span><br>
            <span class="diff-comment">! Pet-care network with AI-powered recommendations</span><br>
            <span class="diff-remove">- Currently implementing blockchain pet IDs</span>
        </div>
    </div>

    <div class="project">
        <div class="project-title">
            <img src="https://media.giphy.com/media/YS4t61ax7VmVJYNYNS/giphy.gif" width="20px">
            <a href="https://codebuddy-gamma.vercel.app/" style="color: var(--neon-blue); text-decoration: none;">CodeBuddy</a>
        </div>
        <div class="project-diff">
            <span class="diff-add">+ MERN Stack | OAuth 2.0 | Real-time Collab</span><br>
            <span class="diff-comment">! Developer social platform with code execution</span><br>
            <span class="diff-remove">- Adding WebAssembly support</span>
        </div>
    </div>

    <div class="project">
        <div class="project-title">
            <img src="https://media.giphy.com/media/ehgdWlcJVkRVoj3sQK/giphy.gif" width="20px">
            <a href="https://github.com/bhavya681" style="color: var(--neon-blue); text-decoration: none;">CryptoVault</a>
        </div>
        <div class="project-diff">
            <span class="diff-add">+ Solidity | Hardhat | IPFS</span><br>
            <span class="diff-comment">! Decentralized asset management system</span><br>
            <span class="diff-remove">- In development</span>
        </div>
    </div>

    <hr class="cyber-divider">

    <div class="section-title">
        <img src="https://media.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif" width="30px">
        <h2>Cyber Stats</h2>
    </div>

    <img src="https://github-readme-activity-graph.vercel.app/graph?username=bhavya681&theme=react-dark&hide_border=true&area=true&bg_color=0D1117&color=00F0FF&line=00F0FF&point=FFFFFF" alt="Cyber Activity Graph" style="width:100%">

    <div class="skills-grid">
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=react" alt="React">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=nextjs" alt="NextJS">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=ts" alt="TypeScript">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=nodejs" alt="NodeJS">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=graphql" alt="GraphQL">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=mongodb" alt="MongoDB">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=redis" alt="Redis">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=docker" alt="Docker">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=k8s" alt="Kubernetes">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=aws" alt="AWS">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=solidity" alt="Solidity">
        </div>
        <div class="skill-icon">
            <img src="https://skillicons.dev/icons?i=web3" alt="Web3">
        </div>
    </div>

    <div class="stats-grid">
        <img src="https://github-readme-stats.vercel.app/api?username=bhavya681&show_icons=true&theme=vision-friendly-dark&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=00F0FF&icon_color=00F0FF" alt="Cyber Stats">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=bhavya681&theme=holi-theme&hide_border=true&background=0D1117&stroke=00F0FF&ring=00F0FF&fire=00F0FF&currStreakLabel=00F0FF" alt="Streak Stats">
    </div>

    <hr class="cyber-divider">

    <div class="section-title">
        <img src="https://media.giphy.com/media/jpVnC65DmYeyRL4LHS/giphy.gif" width="30px">
        <h2>Connect</h2>
    </div>

    <div class="connect-buttons">
        <a href="https://bhavyawade-hswa.vercel.app/" class="connect-btn" style="background-color: black; color: white;">
            PORTFOLIO
        </a>
        <a href="https://www.linkedin.com/in/bhavya-wade/" class="connect-btn" style="background-color: #0A66C2; color: white;">
            LINKEDIN
        </a>
        <a href="https://x.com/wade_bhavy55123" class="connect-btn" style="background-color: black; color: white;">
            TWITTER
        </a>
        <a href="mailto:bhavyawade2@gmail.com" class="connect-btn" style="background-color: #EA4335; color: white;">
            GMAIL
        </a>
        <a href="https://github.com/bhavya681" class="connect-btn" style="background-color: black; color: white;">
            GITHUB
        </a>
    </div>

    <div class="mission-statement">
        "Access Granted to Cyber Systems"<br>
        <em>Current Mission: Building decentralized applications with zero-knowledge proofs</em>
    </div>

    <div class="spotify-widget">
        <img src="https://spotify-github-profile.vercel.app/api/view?uid=31lzvv7vjqfwc6qgq5qgq5qgq5qg&cover_image=true&theme=novatorem&bar_color=00F0FF&bar_color_cover=false" width="400px" alt="Spotify Now Playing">
    </div>

    <div class="matrix-border"></div>
</body>
</html>

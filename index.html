<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>藍田循道衞理小學 校本打譜網站</title>
    <script src="https://cdn.jsdelivr.net/npm/vexflow@4.2.2/build/cjs/vexflow.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.49/Tone.js"></script>
    
    <style id="print-style">
        @page { size: portrait; margin: 0; }
    </style>

    <style>
        :root {
            --primary: #4f46e5; --primary-dark: #3730a3; --primary-light: #e0e7ff;
            --success: #10b981; --success-dark: #059669;
            --danger: #ef4444; --danger-dark: #dc2626;
            --warning: #f59e0b; --warning-dark: #d97706;
            --surface: #ffffff;
            --border: #e5e7eb; --text-main: #111827; --text-muted: #4b5563;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            color: var(--text-main); margin: 0; padding: 20px 15px;
            display: flex; flex-direction: column; align-items: center;
            min-height: 100vh;
        }
        
        h2 { margin: 0 0 20px 0; font-size: 28px; font-weight: 800; color: var(--primary-dark); text-shadow: 1px 1px 2px rgba(0,0,0,0.05); text-align: center; }

        .toolbar-container { width: 100%; max-width: 1200px; display: flex; flex-direction: column; gap: 12px; margin-bottom: 20px; }

        .toolbar-row {
            background-color: rgba(255, 255, 255, 0.9); padding: 12px 18px; border-radius: 12px;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05), 0 2px 4px -1px rgba(0,0,0,0.03);
            border: 1px solid rgba(255, 255, 255, 0.5); backdrop-filter: blur(5px);
            display: flex; flex-wrap: wrap; align-items: center; gap: 15px;
            transition: box-shadow 0.3s ease;
        }
        .toolbar-row:hover { box-shadow: 0 8px 15px -3px rgba(0,0,0,0.08); }

        .tool-group { display: flex; align-items: center; gap: 8px; border-right: 1px solid var(--border); padding-right: 15px; flex-wrap: wrap; }
        .tool-group:last-child { border-right: none; padding-right: 0; }
        
        .tool-label { font-size: 13px; font-weight: 700; color: var(--text-muted); }

        select, button, input[type="text"], input[type="number"] {
            padding: 8px 12px; font-size: 14px; font-weight: 600; cursor: pointer;
            border: 1px solid var(--border); border-radius: 8px; 
            background-color: var(--surface); color: var(--text-main);
            transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1); touch-action: manipulation; 
        }
        
        select:hover, input:hover { border-color: var(--primary); }
        button:hover:not(:disabled) { transform: translateY(-2px); box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1); }
        button:active:not(:disabled) { transform: translateY(1px); box-shadow: none; }
        select:focus, input:focus { outline: none; border-color: var(--primary); box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.2); }
        input[type="text"], input[type="number"] { cursor: text; background-color: #f9fafb; }

        .toggle-btn { min-width: 48px; background-color: #f1f5f9; }
        .toggle-btn.active { background-color: var(--primary); color: white; border-color: var(--primary); box-shadow: 0 4px 6px rgba(79, 70, 229, 0.3); transform: translateY(-1px); }
        .acc-btn { font-size: 16px; font-family: serif; padding: 6px 12px; background-color: #f1f5f9;}
        .acc-btn.active { background-color: var(--danger); color: white; border-color: var(--danger); box-shadow: 0 4px 6px rgba(239, 68, 68, 0.3); }

        .btn-action-rest { background-color: #e2e8f0; color: #334155; border-color: #cbd5e1; font-weight: 700; margin-left: 5px; }
        .btn-action-rest:hover:not(:disabled) { background-color: #cbd5e1; color: #0f172a; }
        .btn-edit { background-color: #fffbeb; color: #b45309; border-color: #fde68a; }
        .btn-edit:hover:not(:disabled) { background-color: #fef3c7; color: #92400e; }

        button:disabled, .toggle-btn:disabled { opacity: 0.4; cursor: not-allowed; transform: none !important; box-shadow: none !important; background-color: #f3f4f6; color: #9ca3af; }

        .btn-play { background-color: var(--success); color: white; border: none; transition: background-color 0.3s; }
        .btn-play:hover { filter: brightness(0.9); transform: translateY(-2px); }
        .btn-export { background-color: var(--primary); color: white; border: none; }
        .btn-danger { color: var(--danger); border-color: var(--danger); background-color: #fff0f2; }
        .btn-reset { background-color: var(--warning); color: white; border: none; }
        .btn-shortcut { background-color: var(--primary-light); color: var(--primary-dark); border: none; font-weight: 700; padding: 12px 20px; }

        .solfege-container { display: flex; flex-direction: column; gap: 6px; width: 100%; margin-top: 5px; }
        .solfege-row { display: flex; gap: 6px; flex-wrap: wrap; }
        .solfege-btn { font-weight: 800; padding: 10px 8px; flex: 1; min-width: 45px; border-radius: 8px; border: 1px solid rgba(0,0,0,0.05); }
        
        .c-red { background-color: #fee2e2; color: #b91c1c; }     
        .c-orange { background-color: #ffedd5; color: #c2410c; }  
        .c-yellow { background-color: #fef9c3; color: #a16207; }  
        .c-green { background-color: #dcfce7; color: #15803d; }   
        .c-teal { background-color: #ccfbf1; color: #0f766e; }    
        .c-blue { background-color: #dbeafe; color: #1d4ed8; }    
        .c-purple { background-color: #f3e8ff; color: #7e22ce; }  

        .extended-row { display: none; }
        .show-extended .extended-row { display: flex; }
        .annotation-container { display: none; margin-top: 5px; }
        .annotation-container.show-annotation { display: flex; gap: 6px; flex-wrap: wrap; }
        
        #tempo-input { width: 60px; text-align: center; font-weight: 800; color: var(--primary-dark); }
        #note-text-input { width: 130px; }

        .top-header-row { display: flex; justify-content: space-between; align-items: flex-start; gap: 15px; width: 100%; }
        .info-details {
            flex: 1; background-color: rgba(255, 255, 255, 0.9); border-radius: 12px;
            border: 1px solid var(--border); overflow: hidden; box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05);
            backdrop-filter: blur(5px);
        }
        .info-details summary {
            padding: 12px 20px; font-weight: 700; color: var(--primary-dark); cursor: pointer; user-select: none; outline: none;
            display: flex; align-items: center; justify-content: space-between;
        }
        .info-details summary::-webkit-details-marker { display: none; }
        .info-panel-content {
            padding: 15px 20px; border-top: 1px solid var(--border); background-color: #f8fafc;
            display: flex; flex-wrap: wrap; gap: 15px; font-size: 13px; align-items: center;
        }
        .student-input-group { display: flex; align-items: center; gap: 6px; }
        .student-input-group label { font-weight: bold; color: var(--text-main); }
        .student-input-group input[type="text"], .student-input-group input[type="number"] { padding: 6px 10px; }

        .modal-overlay {
            display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.5); z-index: 9999; align-items: center; justify-content: center; backdrop-filter: blur(4px);
        }
        .modal-overlay.active { display: flex; }
        .modal-content {
            background: var(--surface); padding: 30px; border-radius: 16px; width: 90%; max-width: 500px;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25); position: relative; border: 1px solid var(--border);
        }
        .modal-close { position: absolute; top: 15px; right: 20px; font-size: 28px; font-weight: bold; cursor: pointer; color: var(--text-muted); }
        .modal-close:hover { color: var(--danger); }
        .shortcut-panel-inner { display: flex; flex-wrap: wrap; gap: 15px; font-size: 14px; color: var(--primary-dark); margin-top: 15px; line-height: 2; }
        .kbd { background-color: #fff; border: 1px solid #c7d2fe; border-radius: 6px; padding: 4px 10px; font-family: monospace; font-weight: 800; box-shadow: 0 2px 4px rgba(0,0,0,0.05); color: #3730a3; }

        /* 樂譜工作區：排版與滾輪設定 */
        #score-wrapper {
            width: 100%; max-width: 1200px; background-color: #ffffff; 
            border-radius: 16px; box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1), 0 10px 10px -5px rgba(0,0,0,0.04); 
            padding: 30px 40px; box-sizing: border-box; border: 1px solid var(--border);
            display: flex; flex-direction: column;
            user-select: none; -webkit-user-select: none; -webkit-touch-callout: none; flex-grow: 1;
        }
        
        #score-header { display: flex; justify-content: center; position: relative; margin-bottom: 20px; min-height: 50px; width: 100%; flex-shrink: 0; }
        .score-title-display { font-size: 32px; font-weight: 900; color: var(--text-main); text-align: center; max-width: 60%; letter-spacing: 1px;}
        .score-student-info { position: absolute; right: 10px; top: 0; text-align: right; font-size: 16px; font-weight: 600; color: var(--text-main); white-space: pre; }
        
        /* 鎖定兩行高度並加入滾輪 */
        #score-container { 
            cursor: crosshair; position: relative; width: 100%; 
            height: 380px; /* 約兩行高度 */
            overflow-y: auto; overflow-x: hidden;
            border-top: 1px solid #f1f5f9; padding-top: 10px;
        }

        /* 自訂滾輪樣式以符合整體 UI */
        #score-container::-webkit-scrollbar { width: 8px; }
        #score-container::-webkit-scrollbar-track { background: #f8fafc; border-radius: 4px; }
        #score-container::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        #score-container::-webkit-scrollbar-thumb:hover { background: #94a3b8; }

        #svg-playback-cursor { transition: x 0.05s linear, width 0.05s linear; }

        @media (max-width: 950px) {
            .top-header-row { flex-direction: column; }
            .btn-shortcut { width: 100%; }
            #score-wrapper { padding: 15px; }
            .score-student-info { font-size: 14px; right: 0; }
        }

        /* 完美無痕列印排版 */
        @media print {
            @page { margin: 0; size: auto; } 
            body { background: white; padding: 10mm 15mm !important; margin: 0 !important; } 
            .toolbar-container, h2, .modal-overlay { display: none !important; } 
            #score-wrapper { 
                box-shadow: none !important; border: none !important; padding: 0 !important; 
                max-width: 100% !important; height: auto !important; max-height: none !important; 
                overflow: visible !important; margin: 0 !important; display: block !important;
            }
            #score-container { height: auto !important; overflow: visible !important; border: none !important; padding: 0 !important; }
            #score-container svg { width: 100% !important; height: auto !important; display: block; margin: 0 auto; }
        }
    </style>
</head>
<body>

    <h2>🎼 藍田循道衞理小學 校本打譜網站</h2>

    <!-- 快捷鍵視窗 -->
    <div id="shortcut-modal" class="modal-overlay" onclick="closeShortcuts(event)">
        <div class="modal-content" onclick="event.stopPropagation()">
            <span class="modal-close" onclick="closeShortcuts(event)">&times;</span>
            <h3 style="margin-top: 0; color: var(--text-main); font-weight: 800;">⌨️ 鍵盤快捷鍵指南</h3>
            <p style="font-size: 13px; color: var(--text-muted); margin-bottom: 5px; font-weight: bold;">(提示：於文字輸入框打字時，快捷鍵將自動停用以防干擾)</p>
            <div class="shortcut-panel-inner">
                <span><span class="kbd">1</span>~<span class="kbd">7</span> = do~ti</span>
                <span><span class="kbd">8</span> = do'</span>
                <span><span class="kbd">g</span> = 全音符</span>
                <span><span class="kbd">h</span> = 二分</span>
                <span><span class="kbd">j</span> = 四分</span>
                <span><span class="kbd">k</span> = 八分</span>
                <span><span class="kbd">l</span> = 十六分</span>
                <span><span class="kbd">.</span> = 附點</span>
                <span><span class="kbd">+</span> = ♯ 升號</span>
                <span><span class="kbd">-</span> = ♭ 降號</span>
                <span><span class="kbd">=</span> = ♮ 還原</span>
                <span><span class="kbd">Backspace</span> = 刪除一個音</span>
                <span><span class="kbd">Ctrl+Z</span> = 還原上一步</span>
            </div>
        </div>
    </div>

    <div class="toolbar-container">
        
        <div class="top-header-row">
            <details class="info-details" open>
                <summary><span>📝 填寫樂曲資料與學生資訊</span> <span>▼</span></summary>
                <div class="info-panel-content">
                    <div class="student-input-group">
                        <label>樂曲標題：</label>
                        <input type="text" id="input-song-title" oninput="updateScoreHeader()" placeholder="例如：小星星" style="width: 180px;">
                    </div>
                    <div class="student-input-group">
                        <label>班別：</label>
                        <input type="text" id="input-class" oninput="updateScoreHeader()" placeholder="例如：1A" style="width: 60px;">
                    </div>
                    <div class="student-input-group">
                        <label>姓名：</label>
                        <input type="text" id="input-name" oninput="updateScoreHeader()" placeholder="陳小明" style="width: 100px;">
                    </div>
                    <div class="student-input-group">
                        <label>學號：</label>
                        <input type="number" id="input-num" oninput="updateScoreHeader()" placeholder="1" style="width: 60px;">
                    </div>
                    <div class="student-input-group" style="margin-left: auto; background: #fff; padding: 4px 10px; border-radius: 6px; border: 1px solid var(--border);">
                        <label style="cursor: pointer; font-weight: normal; font-size: 13px;"><input type="checkbox" id="chk-show-title" onchange="updateScoreHeader()"> 顯示標題</label>
                        <label style="cursor: pointer; font-weight: normal; font-size: 13px; margin-left: 10px;"><input type="checkbox" id="chk-show-info" onchange="updateScoreHeader()"> 顯示資料</label>
                    </div>
                </div>
            </details>
            <button class="btn-shortcut" onclick="document.getElementById('shortcut-modal').classList.add('active')">⌨️ 快捷鍵清單</button>
        </div>

        <div class="toolbar-row">
            <div class="tool-group">
                <span class="tool-label">系統與版面</span>
                <select id="key-sig-select" onchange="changeKeySig(this.value)">
                    <option value="C" selected>C 大調</option><option value="G">G 大調 (1♯)</option><option value="D">D 大調 (2♯)</option>
                    <option value="F">F 大調 (1♭)</option><option value="Bb">B♭ 大調 (2♭)</option>
                    <option value="Rhythm" style="font-weight: bold; color: var(--primary);">🥁 節奏模式</option>
                </select>
                <select id="time-sig-select" onchange="changeTimeSig(this.value)">
                    <option value="4/4" selected>4/4 拍</option><option value="3/4">3/4 拍</option>
                    <option value="2/4">2/4 拍</option><option value="6/8">6/8 拍</option>
                </select>
                <button class="btn-reset" onclick="resetScore()">🔄 重設</button>
                <label style="font-size:13px; font-weight:bold; color:var(--primary); cursor:pointer; margin-left:5px;">
                    <input type="checkbox" id="chk-color-notes" onchange="renderScore()"> 彩色音符
                </label>
            </div>
            
            <div class="tool-group">
                <span class="tool-label">小節編輯</span>
                <button onclick="changeActiveMeasure(-1)">◀</button>
                <span id="measure-indicator" style="font-weight:900; color:var(--primary-dark); min-width: 50px; text-align: center;">第 1 節</span>
                <button onclick="changeActiveMeasure(1)">▶</button>
                <button onclick="addMeasure()">➕ 新增</button>
                <button class="btn-danger" onclick="clearCurrentMeasure()">清空</button>
                <button class="btn-danger" onclick="deleteCurrentMeasure()">🗑️ 刪除小節</button>
            </div>

            <div class="tool-group" style="margin-left: auto; border: none;">
                <span class="tool-label">播放與輸出</span>
                <span style="font-size: 13px; font-weight: 800; color: var(--text-main);">BPM:</span>
                <input type="number" id="tempo-input" min="40" max="200" value="100">
                <button class="btn-play" id="btn-play" onclick="togglePlay()">▶ 播放</button>
                <button class="btn-export" id="export-btn" onclick="exportWav()">⬇️ .wav</button>
                <button onclick="window.print()">🖨️ 列印 / PDF</button>
            </div>
        </div>

        <div class="toolbar-row">
            <div class="tool-group">
                <span class="tool-label">音符時值</span>
                <button class="toggle-btn" id="btn-w" onclick="setDuration('w', this)">全音符</button>
                <button class="toggle-btn" id="btn-h" onclick="setDuration('h', this)">二分</button>
                <button class="toggle-btn active" id="btn-q" onclick="setDuration('q', this)">♩ 四分</button>
                <button class="toggle-btn" id="btn-8" onclick="setDuration('8', this)">♪ 八分</button>
                <button class="toggle-btn" id="btn-16" onclick="setDuration('16', this)">♬ 十六分</button>
                <button class="toggle-btn" id="btn-dot" onclick="toggleDot()">附點(.)</button>
                <button class="btn-action-rest" id="btn-rest" onclick="addRest()">⏸️ 休止符</button>
            </div>
            
            <div class="tool-group">
                <span class="tool-label">修正操作</span>
                <button class="btn-edit" onclick="undo()">↩️ 還原上一步</button>
                <button class="btn-edit" onclick="deleteLastNote()">⌫ 刪除一個音</button>
            </div>

            <div class="tool-group" style="border: none; flex: 1;">
                <div style="display:flex; justify-content:space-between; width: 100%; margin-bottom: 2px;">
                    <span class="tool-label">附加標記</span>
                    <button onclick="document.getElementById('annotation-panel').classList.toggle('show-annotation')" style="padding: 2px 8px; font-size:12px; height: 20px;">↕️ 展開/收合</button>
                </div>
                <div id="annotation-panel" class="annotation-container">
                    <input type="text" id="note-text-input" placeholder="自訂文字(如指法)">
                    <select id="auto-annotate-select">
                        <option value="none" selected>無自動標記</option>
                        <option value="solfege">自動唱名 (d, r, m)</option>
                        <option value="note">自動音名 (C, D, E)</option>
                    </select>
                    <select id="note-text-pos">
                        <option value="top">放上方</option>
                        <option value="bottom">放下方</option>
                    </select>
                </div>
            </div>
        </div>

        <div class="toolbar-row" style="flex-direction: column; align-items: stretch;">
            <div style="display:flex; flex-wrap:wrap; gap:15px; align-items:center;">
                <div class="tool-group" style="border: none; padding: 0;">
                    <span class="tool-label">輸入模式</span>
                    <select id="input-mode-select" onchange="updateInputLabels()" style="padding: 6px 10px; font-size: 13px;">
                        <option value="solfege" selected>唱名</option>
                        <option value="notename">音名</option>
                    </select>
                </div>
                
                <div class="tool-group" id="accidental-panel-wrapper" style="border-left: 1px solid var(--border); padding-left: 15px;">
                    <span class="tool-label">臨時記號</span>
                    <button class="toggle-btn acc-btn" id="btn-flat" onclick="toggleAccidental('b', this)">♭</button>
                    <button class="toggle-btn acc-btn" id="btn-nat" onclick="toggleAccidental('n', this)">♮</button>
                    <button class="toggle-btn acc-btn" id="btn-sharp" onclick="toggleAccidental('#', this)">♯</button>
                </div>
                
                <button onclick="toggleExtendedSolfege()" style="margin-left: auto; padding: 6px 15px; font-size:13px; background-color: #f8fafc;">↕️ 展開/收合八度</button>
            </div>
            
            <div id="solfege-panel-wrapper" style="width: 100%;">
                <div id="solfege-panel" class="solfege-container">
                    <div class="solfege-row extended-row">
                        <button class="solfege-btn c-red" data-deg="0" data-oct="1" onclick="addSolfegeNote(0, 1)">do'</button>
                        <button class="solfege-btn c-orange" data-deg="1" data-oct="1" onclick="addSolfegeNote(1, 1)">re'</button>
                        <button class="solfege-btn c-yellow" data-deg="2" data-oct="1" onclick="addSolfegeNote(2, 1)">mi'</button>
                        <button class="solfege-btn c-green" data-deg="3" data-oct="1" onclick="addSolfegeNote(3, 1)">fa'</button>
                        <button class="solfege-btn c-teal" data-deg="4" data-oct="1" onclick="addSolfegeNote(4, 1)">so'</button>
                        <button class="solfege-btn c-blue" data-deg="5" data-oct="1" onclick="addSolfegeNote(5, 1)">la'</button>
                        <button class="solfege-btn c-purple" data-deg="6" data-oct="1" onclick="addSolfegeNote(6, 1)">ti'</button>
                        <button class="solfege-btn c-red" data-deg="0" data-oct="2" onclick="addSolfegeNote(0, 2)">do''</button>
                    </div>
                    <div class="solfege-row">
                        <button class="solfege-btn c-red" id="btn-do" data-deg="0" data-oct="0" onclick="addSolfegeNote(0, 0)">do</button>
                        <button class="solfege-btn c-orange" id="btn-re" data-deg="1" data-oct="0" onclick="addSolfegeNote(1, 0)">re</button>
                        <button class="solfege-btn c-yellow" id="btn-mi" data-deg="2" data-oct="0" onclick="addSolfegeNote(2, 0)">mi</button>
                        <button class="solfege-btn c-green" id="btn-fa" data-deg="3" data-oct="0" onclick="addSolfegeNote(3, 0)">fa</button>
                        <button class="solfege-btn c-teal" id="btn-so" data-deg="4" data-oct="0" onclick="addSolfegeNote(4, 0)">so</button>
                        <button class="solfege-btn c-blue" id="btn-la" data-deg="5" data-oct="0" onclick="addSolfegeNote(5, 0)">la</button>
                        <button class="solfege-btn c-purple" id="btn-ti" data-deg="6" data-oct="0" onclick="addSolfegeNote(6, 0)">ti</button>
                        <button class="solfege-btn c-red" id="btn-do-high" data-deg="0" data-oct="1" onclick="addSolfegeNote(0, 1)">do'</button>
                    </div>
                    <div class="solfege-row extended-row">
                        <button class="solfege-btn c-red" data-deg="0" data-oct="-1" onclick="addSolfegeNote(0, -1)">do,</button>
                        <button class="solfege-btn c-orange" data-deg="1" data-oct="-1" onclick="addSolfegeNote(1, -1)">re,</button>
                        <button class="solfege-btn c-yellow" data-deg="2" data-oct="-1" onclick="addSolfegeNote(2, -1)">mi,</button>
                        <button class="solfege-btn c-green" data-deg="3" data-oct="-1" onclick="addSolfegeNote(3, -1)">fa,</button>
                        <button class="solfege-btn c-teal" data-deg="4" data-oct="-1" onclick="addSolfegeNote(4, -1)">so,</button>
                        <button class="solfege-btn c-blue" data-deg="5" data-oct="-1" onclick="addSolfegeNote(5, -1)">la,</button>
                        <button class="solfege-btn c-purple" data-deg="6" data-oct="-1" onclick="addSolfegeNote(6, -1)">ti,</button>
                        <button class="solfege-btn c-red" data-deg="0" data-oct="0" onclick="addSolfegeNote(0, 0)">do</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 樂譜工作區 -->
    <div id="score-wrapper">
        <div id="score-header">
            <div class="score-title-display" id="display-song-title">未命名樂曲</div>
            <div class="score-student-info" id="display-student-info">姓名：_____________     班別：____(   )</div>
        </div>
        <div id="score-container"></div>
    </div>
    
    <script>
        const { Renderer, Stave, StaveNote, Voice, Formatter, Dot, Beam, Accidental, Fraction, Barline } = Vex.Flow;
        
        let measures = [ [] ]; 
        let activeMeasureIndex = 0; 
        let renderedStavesInfo = []; 

        let currentDuration = 'q'; let isDotted = false;      
        let currentTimeSig = '4/4'; let currentKeySig = 'C';
        let activeAccidental = null; let maxQuarterBeats = 4; 
        let isPrinting = false; 

        let isPlaying = false;
        let historyStack = [];
        let vexNotesCache = []; 

        const keySignatureMap = { 'C': {}, 'G': { 'f': '#' }, 'D': { 'f': '#', 'c': '#' }, 'F': { 'b': 'b' }, 'Bb': { 'b': 'b', 'e': 'b' } };
        const diatonicMaps = {
            'C':  [ {l:'c', o:4}, {l:'d', o:4}, {l:'e', o:4}, {l:'f', o:4}, {l:'g', o:4}, {l:'a', o:4}, {l:'b', o:4} ],
            'G':  [ {l:'g', o:4}, {l:'a', o:4}, {l:'b', o:4}, {l:'c', o:5}, {l:'d', o:5}, {l:'e', o:5}, {l:'f', o:5} ],
            'D':  [ {l:'d', o:4}, {l:'e', o:4}, {l:'f', o:4}, {l:'g', o:4}, {l:'a', o:4}, {l:'b', o:4}, {l:'c', o:5} ],
            'F':  [ {l:'f', o:4}, {l:'g', o:4}, {l:'a', o:4}, {l:'b', o:4}, {l:'c', o:5}, {l:'d', o:5}, {l:'e', o:5} ],
            'Bb': [ {l:'b', o:3}, {l:'c', o:4}, {l:'d', o:4}, {l:'e', o:4}, {l:'f', o:4}, {l:'g', o:4}, {l:'a', o:4} ]
        };
        const noteColors = ["#dc2626", "#ea580c", "#d97706", "#16a34a", "#0d9488", "#2563eb", "#9333ea"];

        const previewSynth = new Tone.PolySynth(Tone.Synth, { oscillator: { type: "sine" }, envelope: { attack: 0.02, decay: 0.1, sustain: 0.2, release: 1.0 } }).toDestination();

        function saveState() {
            historyStack.push(JSON.stringify({ m: measures, a: activeMeasureIndex }));
            if (historyStack.length > 50) historyStack.shift(); 
        }

        function undo() {
            if (historyStack.length > 0) {
                let state = JSON.parse(historyStack.pop());
                measures = state.m; activeMeasureIndex = state.a;
                updateMeasureIndicator(); renderScore();
            } else { alert("已經是最初狀態了！"); }
        }

        function deleteLastNote() {
            saveState();
            if (measures[activeMeasureIndex].length > 0) {
                measures[activeMeasureIndex].pop();
            } else if (activeMeasureIndex > 0) {
                activeMeasureIndex--; measures.pop(); 
                if(measures[activeMeasureIndex] && measures[activeMeasureIndex].length > 0) {
                    measures[activeMeasureIndex].pop();
                }
                updateMeasureIndicator();
            }
            renderScore();
        }

        // --- 新增的重設樂譜功能 ---
        function resetScore() {
            if (confirm("確定要清空整份樂譜嗎？此動作無法還原。")) {
                measures = [ [] ];
                activeMeasureIndex = 0;
                historyStack = [];
                updateMeasureIndicator();
                renderScore();
            }
        }

        function closeShortcuts(e) { document.getElementById('shortcut-modal').classList.remove('active'); }
        
        function updateScoreHeader() {
            let title = document.getElementById('input-song-title').value.trim() || "未命名樂曲";
            let cls = document.getElementById('input-class').value.trim() || "____";
            let name = document.getElementById('input-name').value.trim() || "__________";
            let num = document.getElementById('input-num').value.trim() || "   ";
            
            document.getElementById('display-song-title').innerText = title;
            document.getElementById('display-student-info').innerText = `姓名：${name}     班別：${cls} ( ${num} )`;

            let showTitle = document.getElementById('chk-show-title').checked;
            let showInfo = document.getElementById('chk-show-info').checked;
            document.getElementById('display-song-title').style.display = showTitle ? 'block' : 'none';
            document.querySelector('.score-student-info').style.display = showInfo ? 'block' : 'none';
            document.getElementById('score-header').style.display = (!showTitle && !showInfo) ? 'none' : 'flex';
        }

        function updateInputLabels() {
            let mode = document.getElementById('input-mode-select').value;
            let map = diatonicMaps[currentKeySig];
            if(!map) return;
            document.querySelectorAll('.solfege-btn').forEach(btn => {
                let deg = parseInt(btn.getAttribute('data-deg'));
                let oct = parseInt(btn.getAttribute('data-oct'));
                if (mode === 'solfege') {
                    let name = ['do', 're', 'mi', 'fa', 'so', 'la', 'ti'][deg];
                    if(oct === 1) name += "'"; if(oct === 2) name += "''"; if(oct === -1) name += ",";
                    btn.innerText = name;
                } else {
                    let baseNote = map[deg];
                    let absoluteOctave = baseNote.o + oct;
                    let noteLetter = baseNote.l.toUpperCase();
                    let acc = keySignatureMap[currentKeySig][noteLetter.toLowerCase()] || "";
                    let name = noteLetter + acc;
                    
                    if (absoluteOctave === 5) name += "'";
                    else if (absoluteOctave === 6) name += "''";
                    else if (absoluteOctave === 7) name += "'''";
                    else if (absoluteOctave === 3) name += ",";
                    else if (absoluteOctave === 2) name += ",,";
                    
                    btn.innerText = name;
                }
            });
        }

        window.addEventListener('beforeprint', () => { isPrinting = true; renderScore(); });
        window.addEventListener('afterprint', () => { isPrinting = false; renderScore(); });

        document.addEventListener('keydown', function(event) {
            if (event.target.tagName === 'INPUT' || event.target.tagName === 'SELECT') return;
            
            if (event.ctrlKey && event.key.toLowerCase() === 'z') { event.preventDefault(); undo(); return; }
            const key = event.key.toLowerCase();
            if (key === 'backspace') { event.preventDefault(); deleteLastNote(); return; }

            switch(key) {
                case '1': document.getElementById('btn-do').click(); break;
                case '2': document.getElementById('btn-re').click(); break;
                case '3': document.getElementById('btn-mi').click(); break;
                case '4': document.getElementById('btn-fa').click(); break;
                case '5': document.getElementById('btn-so').click(); break;
                case '6': document.getElementById('btn-la').click(); break;
                case '7': document.getElementById('btn-ti').click(); break;
                case '8': document.getElementById('btn-do-high').click(); break;
                case 'g': document.getElementById('btn-w').click(); break;
                case 'h': document.getElementById('btn-h').click(); break;
                case 'j': document.getElementById('btn-q').click(); break;
                case 'k': document.getElementById('btn-8').click(); break;
                case 'l': document.getElementById('btn-16').click(); break;
                case '.': document.getElementById('btn-dot').click(); break;
                case '+': document.getElementById('btn-sharp').click(); break;
                case '-': document.getElementById('btn-flat').click(); break;
                case '=': document.getElementById('btn-nat').click(); break;
            }
        });

        let pressTimer; let isLongPress = false; let startX, startY;
        const scoreContainer = document.getElementById('score-container');

        scoreContainer.addEventListener('contextmenu', e => e.preventDefault());
        scoreContainer.addEventListener('mousedown', handlePointerDown);
        scoreContainer.addEventListener('touchstart', handlePointerDown, {passive: false});
        scoreContainer.addEventListener('mouseup', handlePointerUp);
        scoreContainer.addEventListener('touchend', handlePointerUp);
        scoreContainer.addEventListener('mouseleave', handlePointerCancel);
        scoreContainer.addEventListener('touchcancel', handlePointerCancel);

        function handlePointerDown(event) {
            if(event.type === 'touchstart') { startX = event.touches[0].clientX; startY = event.touches[0].clientY; } 
            else { startX = event.clientX; startY = event.clientY; }
            isLongPress = false;
            pressTimer = setTimeout(() => { isLongPress = true; processClickOrPress(event, true); }, 800);
        }

        function handlePointerUp(event) {
            clearTimeout(pressTimer);
            if (!isLongPress) {
                let endX = event.type === 'touchend' ? event.changedTouches[0].clientX : event.clientX;
                let endY = event.type === 'touchend' ? event.changedTouches[0].clientY : event.clientY;
                if (Math.abs(endX - startX) < 10 && Math.abs(endY - startY) < 10) processClickOrPress(event, false);
            }
        }
        function handlePointerCancel() { clearTimeout(pressTimer); }

        function processClickOrPress(event, isLong) {
            const svg = scoreContainer.querySelector("svg"); if (!svg) return;
            let pt = svg.createSVGPoint(); 
            let clientX, clientY;
            if (event.type.startsWith('touch')) {
                let touch = event.touches[0] || event.changedTouches[0];
                clientX = touch.clientX; clientY = touch.clientY;
            } else { clientX = event.clientX; clientY = event.clientY; }
            
            pt.x = clientX; pt.y = clientY;
            let svgP = pt.matrixTransform(svg.getScreenCTM().inverse());
            
            let targetStaveInfo = renderedStavesInfo.find(s => svgP.x >= s.x && svgP.x <= s.x + s.width && svgP.y >= s.y - 40 && svgP.y <= s.y + 120);
            if (targetStaveInfo) {
                if (activeMeasureIndex !== targetStaveInfo.index) { activeMeasureIndex = targetStaveInfo.index; updateMeasureIndicator(); renderScore(); }
            } else { targetStaveInfo = renderedStavesInfo[activeMeasureIndex]; }

            if (!isLong) {
                let pitchIndex = Math.round((svgP.y - targetStaveInfo.stave.getYForLine(0)) / 5);
                const pitches = [
                    { letter: 'a', o: '5' }, { letter: 'g', o: '5' }, { letter: 'f', o: '5' }, { letter: 'e', o: '5' }, { letter: 'd', o: '5' }, { letter: 'c', o: '5' },
                    { letter: 'b', o: '4' }, { letter: 'a', o: '4' }, { letter: 'g', o: '4' }, { letter: 'f', o: '4' }, { letter: 'e', o: '4' }, { letter: 'd', o: '4' },
                    { letter: 'c', o: '4' }, { letter: 'b', o: '3' }, { letter: 'a', o: '3' }
                ];
                let arrayIndex = Math.max(0, Math.min(pitches.length - 1, pitchIndex + 2));
                addNote(pitches[arrayIndex].letter, pitches[arrayIndex].o);
            } else {
                if(navigator.vibrate) navigator.vibrate(50);
            }
        }

        function toggleExtendedSolfege() { document.getElementById('solfege-panel').classList.toggle('show-extended'); }
        function addSolfegeNote(degreeIndex, octaveOffset) {
            let baseNote = diatonicMaps[currentKeySig][degreeIndex];
            addNote(baseNote.l, (baseNote.o + octaveOffset).toString(), degreeIndex);
        }

        function updateMeasureIndicator() { document.getElementById('measure-indicator').innerText = `第 ${activeMeasureIndex + 1} 節`; }
        function changeActiveMeasure(delta) {
            let newIndex = activeMeasureIndex + delta;
            if (newIndex >= 0 && newIndex < measures.length) { activeMeasureIndex = newIndex; updateMeasureIndicator(); renderScore(); }
        }
        function addMeasure() { saveState(); measures.splice(activeMeasureIndex + 1, 0, []); activeMeasureIndex++; updateMeasureIndicator(); renderScore(); }
        function clearCurrentMeasure() { saveState(); measures[activeMeasureIndex] = []; renderScore(); }
        function deleteCurrentMeasure() {
            saveState();
            if (measures.length <= 1) measures[0] = [];
            else { measures.splice(activeMeasureIndex, 1); if (activeMeasureIndex >= measures.length) activeMeasureIndex = measures.length - 1; }
            updateMeasureIndicator(); renderScore();
        }

        function getNoteBeats(duration, dotted) {
            let b = duration === 'w' ? 4 : duration === 'h' ? 2 : duration === 'q' ? 1 : duration === '8' ? 0.5 : 0.25;
            return dotted ? b * 1.5 : b;
        }
        function getCurrentMeasureBeats() { return measures[activeMeasureIndex].reduce((sum, n) => sum + getNoteBeats(n.duration, n.isDotted), 0); }

        function updateRhythmButtonsState() {
            let remaining = maxQuarterBeats - getCurrentMeasureBeats();
            if (remaining === 0) remaining = maxQuarterBeats; 
            const durs = ['w', 'h', 'q', '8', '16'];
            let currentStillValid = false;

            durs.forEach(dur => {
                let btn = document.getElementById('btn-' + dur);
                if (getNoteBeats(dur, false) > remaining + 0.01) {
                    btn.disabled = true; btn.classList.remove('active');
                } else {
                    btn.disabled = false; if (currentDuration === dur) currentStillValid = true;
                }
            });

            let dotBtn = document.getElementById('btn-dot');
            if (getNoteBeats(currentDuration, true) > remaining + 0.01) {
                dotBtn.disabled = true; if (isDotted) { isDotted = false; dotBtn.classList.remove('active'); }
            } else { dotBtn.disabled = false; }
            
            let restBtn = document.getElementById('btn-rest');
            restBtn.disabled = (getNoteBeats(currentDuration, isDotted) > remaining + 0.01);

            if (!currentStillValid) {
                for (let i = 0; i < durs.length; i++) {
                    if (getNoteBeats(durs[i], false) <= remaining + 0.01) { setDuration(durs[i], document.getElementById('btn-' + durs[i])); break; }
                }
            }
        }

        function setDuration(dur, btn) {
            if (btn.disabled) return;
            currentDuration = dur;
            document.querySelectorAll('.toggle-btn:not(#btn-dot):not(.acc-btn)').forEach(b => b.classList.remove('active'));
            btn.classList.add('active'); updateRhythmButtonsState(); 
        }

        function toggleDot() { 
            let btn = document.getElementById('btn-dot'); if (btn.disabled) return;
            isDotted = !isDotted; btn.classList.toggle('active', isDotted); updateRhythmButtonsState();
        }

        function changeTimeSig(sig) {
            saveState();
            currentTimeSig = sig; maxQuarterBeats = sig === '2/4' ? 2 : sig === '3/4' ? 3 : sig === '4/4' ? 4 : 3; 
            measures = [ [] ]; activeMeasureIndex = 0; updateMeasureIndicator(); renderScore();
        }
        
        function changeKeySig(sig) { 
            saveState();
            currentKeySig = sig; let isRhythmMode = (sig === 'Rhythm');
            document.getElementById('solfege-panel-wrapper').style.display = isRhythmMode ? 'none' : 'block';
            document.getElementById('accidental-panel-wrapper').style.opacity = isRhythmMode ? '0.3' : '1';
            document.getElementById('accidental-panel-wrapper').style.pointerEvents = isRhythmMode ? 'none' : 'auto';
            updateInputLabels(); renderScore(); 
        }

        function toggleAccidental(acc, btn) {
            if (activeAccidental === acc) { activeAccidental = null; btn.classList.remove('active'); } 
            else { activeAccidental = acc; document.querySelectorAll('.acc-btn').forEach(b => b.classList.remove('active')); btn.classList.add('active'); }
        }

        async function addRest() {
            let neededBeats = getNoteBeats(currentDuration, isDotted);
            let currentBeats = getCurrentMeasureBeats();
            if (currentBeats + neededBeats > maxQuarterBeats + 0.01) { alert(`⚠️ 第 ${activeMeasureIndex + 1} 節空間不足！`); return; }

            saveState();
            measures[activeMeasureIndex].push({ isRest: true, duration: currentDuration, isDotted: isDotted });

            if (Math.abs((currentBeats + neededBeats) - maxQuarterBeats) < 0.01) {
                if (activeMeasureIndex === measures.length - 1) measures.push([]);
                activeMeasureIndex++; updateMeasureIndicator();
            }
            renderScore();
        }

        async function addNote(baseLetter, octave, providedDegree = -1) {
            let neededBeats = getNoteBeats(currentDuration, isDotted);
            let currentBeats = getCurrentMeasureBeats();
            if (currentBeats + neededBeats > maxQuarterBeats + 0.01) { alert(`⚠️ 第 ${activeMeasureIndex + 1} 節空間不足！`); return; }

            saveState(); 

            let textInput = document.getElementById('note-text-input');
            let customText = textInput.value.trim();
            let autoAnnType = document.getElementById('auto-annotate-select').value;
            let noteTextPos = document.getElementById('note-text-pos').value;

            let isRhythmMode = (currentKeySig === 'Rhythm');
            let finalToneKey, vexKey, generatedText = "";
            let toneAccidental = "";
            let degreeIndex = providedDegree;
            
            if (isRhythmMode) {
                vexKey = "b/4"; finalToneKey = "F4"; activeAccidental = null; 
            } else {
                if (activeAccidental && activeAccidental !== 'n') toneAccidental = activeAccidental;
                else if (!activeAccidental) toneAccidental = keySignatureMap[currentKeySig][baseLetter.toLowerCase()] || "";
                finalToneKey = baseLetter.toUpperCase() + toneAccidental + octave;
                vexKey = baseLetter.toLowerCase() + "/" + octave;

                if (degreeIndex === -1) {
                    degreeIndex = diatonicMaps[currentKeySig].findIndex(n => n.l === baseLetter.toLowerCase());
                }

                if (autoAnnType === 'solfege') {
                    if (degreeIndex !== -1) {
                        generatedText = ['d', 'r', 'm', 'f', 's', 'l', 't'][degreeIndex];
                        if (activeAccidental && activeAccidental !== 'n') generatedText += activeAccidental;
                        let octDiff = parseInt(octave) - diatonicMaps[currentKeySig][degreeIndex].o;
                        if (octDiff > 0) generatedText += "'".repeat(octDiff);
                        if (octDiff < 0) generatedText += ",".repeat(Math.abs(octDiff));
                    }
                } else if (autoAnnType === 'note') {
                    let absoluteOctave = parseInt(octave);
                    generatedText = baseLetter.toUpperCase() + (toneAccidental || "");
                    if (absoluteOctave === 5) generatedText += "'";
                    else if (absoluteOctave === 6) generatedText += "''";
                    else if (absoluteOctave === 7) generatedText += "'''";
                    else if (absoluteOctave === 3) generatedText += ",";
                    else if (absoluteOctave === 2) generatedText += ",,";
                }
            }

            let finalText = customText !== "" ? customText : generatedText;

            measures[activeMeasureIndex].push({ 
                isRest: false, baseKey: vexKey, toneKey: finalToneKey, duration: currentDuration, 
                isDotted: isDotted, explicitAccidental: activeAccidental, 
                text: finalText, textPos: noteTextPos, deg: degreeIndex
            });
            
            textInput.value = ""; 
            await Tone.start(); previewSynth.triggerAttackRelease(finalToneKey, "8n");
            activeAccidental = null; document.querySelectorAll('.acc-btn').forEach(b => b.classList.remove('active'));

            if (Math.abs((currentBeats + neededBeats) - maxQuarterBeats) < 0.01) {
                if (activeMeasureIndex === measures.length - 1) measures.push([]);
                activeMeasureIndex++; updateMeasureIndicator();
            }
            renderScore();
        }

        function createPerfectBeams(notesData, vexNotes, timeSig) {
            let beams = [], currentBeamNotes = [], accumulatedBeats = 0;
            let beatThreshold = timeSig === '6/8' ? 1.5 : 1.0; 
            let currentBoundary = beatThreshold;

            notesData.forEach((n, idx) => {
                let noteBeats = getNoteBeats(n.duration, n.isDotted);
                let isBeamable = ['8', '16', '32'].includes(n.duration) && !n.isRest;
                if (isBeamable) currentBeamNotes.push(vexNotes[idx]);
                accumulatedBeats += noteBeats;

                if (accumulatedBeats >= currentBoundary - 0.01 || !isBeamable) {
                    if (currentBeamNotes.length > 1) beams.push(new Beam(currentBeamNotes));
                    currentBeamNotes = [];
                    while(accumulatedBeats >= currentBoundary - 0.01) currentBoundary += beatThreshold;
                }
            });
            if (currentBeamNotes.length > 1) beams.push(new Beam(currentBeamNotes));
            return beams;
        }

        // --- 核心繪圖渲染 (支援響應式與置中) ---
        function renderScore() {
            const container = document.getElementById("score-container");
            
            // 【修復跳動】儲存目前的滾動位置
            let savedScrollTop = container.scrollTop; 
            
            container.innerHTML = ""; renderedStavesInfo = []; vexNotesCache = [];
            
            let wrapperWidth = document.getElementById("score-wrapper").clientWidth - 40; 
            let PAGE_WIDTH = 800; // 一般縱向預設寬度
            
            if (isPrinting) {
                PAGE_WIDTH = 800; // 強制固定縱向寬度
            } else {
                // 平板自適應
                PAGE_WIDTH = Math.max(800, wrapperWidth);
            }

            const MARGIN = 15; 
            const MAX_X = PAGE_WIDTH - 25; // 縮小邊界以確保最後小節線列印成功
            
            let isRhythmMode = (currentKeySig === 'Rhythm');
            let useColor = document.getElementById('chk-color-notes').checked && !isRhythmMode;
            let measureLayouts = [];
            
            measures.forEach((measureNotes, index) => {
                let requiredMinWidth = 0, voice = null, vexNotes = [];
                if (measureNotes.length > 0) {
                    vexNotes = measureNotes.map((n, idx) => {
                        let note = new StaveNote({ keys: [n.isRest ? "b/4" : n.baseKey], duration: n.isRest ? n.duration + "r" : n.duration });
                        if (n.explicitAccidental && !isRhythmMode && !n.isRest) note.addModifier(new Accidental(n.explicitAccidental), 0);
                        if (n.isDotted) Dot.buildAndAttach([note], { all: true });
                        if (useColor && !n.isRest && n.deg !== undefined && n.deg >= 0 && n.deg <= 6) {
                            note.setStyle({ fillStyle: noteColors[n.deg], strokeStyle: noteColors[n.deg] });
                        }
                        return note;
                    });
                    
                    let [numBeats, beatValue] = currentTimeSig.split('/').map(Number);
                    voice = new Voice({ num_beats: numBeats, beat_value: beatValue }).setMode(Voice.Mode.SOFT);
                    voice.addTickables(vexNotes);
                    requiredMinWidth = new Formatter().joinVoices([voice]).preCalculateMinTotalWidth([voice]);
                }
                measureLayouts.push({ index, notes: measureNotes, vexNotes, voice, minRequiredWidth: requiredMinWidth });
            });

            let lines = [], currentLine = [], currentX = MARGIN;
            measureLayouts.forEach((ml, i) => {
                let isFirstOnLine = currentLine.length === 0;
                let needsClefInfo = isFirstOnLine || i === 0;
                let clefWidth = needsClefInfo ? (isRhythmMode ? 60 : 120) : 30; 
                let calculatedWidth = Math.max(clefWidth + ml.minRequiredWidth + 40, needsClefInfo ? 200 : 150); 

                if (currentX + calculatedWidth > MAX_X && !isFirstOnLine) {
                    lines.push(currentLine); currentLine = [ml];
                    ml.needsClefInfo = true; ml.clefWidth = (isRhythmMode ? 60 : 120);
                    ml.calculatedWidth = Math.max(ml.clefWidth + ml.minRequiredWidth + 40, 200);
                    currentX = MARGIN + ml.calculatedWidth;
                } else {
                    ml.needsClefInfo = needsClefInfo; ml.clefWidth = clefWidth;
                    ml.calculatedWidth = calculatedWidth; currentLine.push(ml); currentX += calculatedWidth;
                }
            });
            if (currentLine.length > 0) lines.push(currentLine);

            const renderer = new Renderer(container, Renderer.Backends.SVG);
            const context = renderer.getContext();
            let currentY = 50, maxCanvasHeight = 150;

            lines.forEach((line, lineIndex) => {
                let totalLineWidth = line.reduce((sum, ml) => sum + ml.calculatedWidth, 0);
                let extraPerMeasure = (!((lineIndex === lines.length - 1) && totalLineWidth <= (MAX_X - MARGIN) * 0.6)) 
                    ? (MAX_X - MARGIN - totalLineWidth) / line.length : 0;
                
                let lineX = MARGIN;
                let lineMinY = currentY + 40; let lineMaxY = currentY + 60; 

                line.forEach(ml => {
                    let finalWidth = ml.calculatedWidth + extraPerMeasure;
                    let stave = new Stave(lineX, currentY, finalWidth);
                    
                    if (isRhythmMode) stave.getConfigForLines().forEach(cfg => cfg.visible = false);
                    if (ml.needsClefInfo) {
                        if (!isRhythmMode) stave.addClef("treble").addKeySignature(currentKeySig);
                        if (ml.index === 0) stave.addTimeSignature(currentTimeSig);
                    }
                    if (ml.index === measures.length - 1) stave.setEndBarType(Barline.type.END);
                    
                    if (!isPrinting && ml.index === activeMeasureIndex) {
                        context.setFillStyle("rgba(79, 70, 229, 0.08)");
                        context.fillRect(lineX, currentY - 20, finalWidth, 120);
                        context.setFillStyle("#000000"); 
                    }

                    stave.setContext(context).draw();
                    renderedStavesInfo.push({ index: ml.index, stave, x: lineX, y: currentY, width: finalWidth });

                    if (ml.voice && ml.vexNotes.length > 0) {
                        let beams = createPerfectBeams(ml.notes, ml.vexNotes, currentTimeSig);
                        new Formatter().joinVoices([ml.voice]).formatToStave([ml.voice], stave);
                        ml.voice.draw(context, stave);
                        beams.forEach(b => b.setContext(context).draw());
                        
                        ml.vexNotes.forEach(note => {
                            vexNotesCache.push(note); 
                            let yHead = note.getYs()[0];
                            if (yHead - 35 < lineMinY) lineMinY = yHead - 35; 
                            if (yHead + 45 > lineMaxY) lineMaxY = yHead + 45;
                        });
                    }
                    lineX += finalWidth;
                });

                const svg = container.querySelector("svg");
                let topTextY = Math.min(currentY - 10, lineMinY);
                let bottomTextY = Math.max(currentY + 110, lineMaxY);

                line.forEach(ml => {
                    ml.notes.forEach((data, idx) => {
                        if (data.text && data.text !== "") {
                            let note = ml.vexNotes[idx];
                            let x = note.getAbsoluteX() + (note.getGlyphWidth() ? note.getGlyphWidth()/2 : 8); 
                            let y = data.textPos === 'top' ? topTextY : bottomTextY;

                            let textNode = document.createElementNS("http://www.w3.org/2000/svg", "text");
                            textNode.setAttribute("x", x); textNode.setAttribute("y", y);
                            textNode.setAttribute("text-anchor", "middle");
                            textNode.setAttribute("font-family", "'Segoe UI', Arial, sans-serif");
                            textNode.setAttribute("font-size", "15px"); textNode.setAttribute("font-weight", "800");
                            textNode.setAttribute("fill", (useColor && !data.isRest && data.deg >= 0) ? noteColors[data.deg] : "#1e3a8a"); 
                            textNode.textContent = data.text;
                            svg.appendChild(textNode);
                        }
                    });
                });

                currentY += 160; 
            });

            const svg = container.querySelector("svg");
            if (svg && !isPrinting) {
                let cursorRect = document.createElementNS("http://www.w3.org/2000/svg", "rect");
                cursorRect.setAttribute("id", "svg-playback-cursor");
                cursorRect.setAttribute("fill", "rgba(245, 158, 11, 0.4)");
                cursorRect.setAttribute("rx", "6"); cursorRect.setAttribute("ry", "6");
                cursorRect.setAttribute("display", "none");
                cursorRect.style.pointerEvents = "none";
                svg.appendChild(cursorRect);
            }

            renderer.resize(PAGE_WIDTH, currentY + 20);

            if (svg) {
                // 自動響應式縮放設定 (完美解決平板版面)
                svg.setAttribute("viewBox", `0 0 ${PAGE_WIDTH} ${currentY + 20}`);
                svg.style.width = "100%"; svg.style.height = "auto";
                svg.removeAttribute("width"); svg.removeAttribute("height");
            }

            // 【修復跳動】還原滾動位置，如果新輸入的音符超出範圍，則自動平滑捲動到當前行
            if (!isPrinting) {
                let activeStaveInfo = renderedStavesInfo.find(s => s.index === activeMeasureIndex);
                if (activeStaveInfo) {
                    let staveY = activeStaveInfo.y;
                    // 如果正在編輯的樂譜行已經被擠到畫面外，則自動捲動跟隨
                    if (staveY < savedScrollTop || staveY > savedScrollTop + container.clientHeight - 140) {
                        container.scrollTop = Math.max(0, staveY - 50);
                    } else {
                        // 否則保持不動，確保畫面平穩
                        container.scrollTop = savedScrollTop;
                    }
                } else {
                    container.scrollTop = savedScrollTop;
                }
            }

            updateRhythmButtonsState(); 
        }

        async function togglePlay() {
            if (isPlaying) stopPlayback(); 
            else await playScore(); 
        }

        function stopPlayback() {
            Tone.Transport.stop(); Tone.Transport.cancel();
            isPlaying = false;
            let btn = document.getElementById('btn-play');
            btn.innerHTML = "▶ 播放"; btn.style.backgroundColor = "var(--success)";
            let cursor = document.getElementById("svg-playback-cursor");
            if (cursor) cursor.setAttribute("display", "none");
        }

        async function playScore() {
            let allNotesCount = measures.flat().length;
            if (allNotesCount === 0) return alert("樂譜是空的！");
            
            await Tone.start(); 
            isPlaying = true;
            let playBtn = document.getElementById('btn-play');
            playBtn.innerHTML = "⏹ 停止"; playBtn.style.backgroundColor = "var(--danger)";
            
            let bpm = parseInt(document.getElementById('tempo-input').value) || 100;
            Tone.Transport.cancel(); Tone.Transport.stop(); Tone.Transport.bpm.value = bpm;
            
            const synth = new Tone.PolySynth(Tone.Synth, { oscillator: { type: "sine" }, envelope: { attack: 0.05, decay: 0.1, sustain: 0.3, release: 1.5 } }).toDestination();
            
            let timeOffset = 0.1; 
            let secondsPerQuarter = 60 / bpm;
            let flatNoteIndex = 0; 
            
            measures.forEach((measureNotes, mIdx) => {
                let stave = renderedStavesInfo.find(s => s.index === mIdx).stave;
                let staveY = stave.getYForLine(0) - 20; 
                
                measureNotes.forEach((note, nIdx) => {
                    let durationSeconds = getNoteBeats(note.duration, note.isDotted) * secondsPerQuarter;
                    let vNote = vexNotesCache[flatNoteIndex];
                    
                    if (!note.isRest) {
                        Tone.Transport.schedule((time) => {
                            synth.triggerAttackRelease(note.toneKey, durationSeconds * 0.95, time);
                        }, timeOffset);
                    }

                    if (vNote) {
                        Tone.Transport.schedule((time) => {
                            Tone.Draw.schedule(() => {
                                let cursor = document.getElementById("svg-playback-cursor");
                                if (cursor) {
                                    let noteX = vNote.getAbsoluteX();
                                    cursor.setAttribute("x", noteX - 10); cursor.setAttribute("y", staveY);
                                    cursor.setAttribute("width", 30); cursor.setAttribute("height", 90);
                                    cursor.setAttribute("display", "block");
                                    
                                    // 播放時畫面也能自動捲動跟隨
                                    const container = document.getElementById("score-container");
                                    if (staveY > container.scrollTop + container.clientHeight - 120 || staveY < container.scrollTop) {
                                        container.scrollTop = Math.max(0, staveY - 50);
                                    }
                                }
                            }, time);
                        }, timeOffset);
                    }

                    timeOffset += durationSeconds;
                    flatNoteIndex++;
                });
            });

            Tone.Transport.schedule((time) => { Tone.Draw.schedule(() => { stopPlayback(); }, time); }, timeOffset);
            Tone.Transport.start();
        }

        async function exportWav() {
            try {
                let allNotes = measures.flat(); 
                if (allNotes.length === 0) return alert("樂譜是空的，無法匯出！");
                
                const btn = document.getElementById('export-btn'); 
                btn.innerText = "⏳ 運算中..."; 
                btn.disabled = true;

                // 讓出線程，讓瀏覽器更新 UI
                await new Promise(resolve => setTimeout(resolve, 50));

                let bpm = parseInt(document.getElementById('tempo-input').value) || 100;
                let secondsPerQuarter = 60 / bpm;
                let totalSeconds = 0;
                allNotes.forEach(n => { totalSeconds += getNoteBeats(n.duration, n.isDotted) * secondsPerQuarter; });

                const buffer = await Tone.Offline(() => {
                    const offlineSynth = new Tone.PolySynth(Tone.Synth, { 
                        oscillator: { type: "sine" }, 
                        envelope: { attack: 0.05, decay: 0.1, sustain: 0.3, release: 1.5 } 
                    }).toDestination();
                    
                    let timeOffset = 0;
                    allNotes.forEach((note) => {
                        let durationSeconds = getNoteBeats(note.duration, note.isDotted) * secondsPerQuarter;
                        if (!note.isRest) {
                            offlineSynth.triggerAttackRelease(note.toneKey, durationSeconds * 0.95, timeOffset);
                        }
                        timeOffset += durationSeconds;
                    });
                }, totalSeconds + 2); 

                const wavData = audioBufferToWav(buffer.get());
                const blob = new Blob([new DataView(wavData)], { type: 'audio/wav' });
                const url = URL.createObjectURL(blob);
                
                const anchor = document.createElement("a"); 
                anchor.style.display = "none";
                anchor.href = url; 
                anchor.download = "Score_Export.wav"; 
                document.body.appendChild(anchor);
                anchor.click();
                
                setTimeout(() => { document.body.removeChild(anchor); URL.revokeObjectURL(url); }, 100);

                btn.innerText = "⬇️ .wav"; btn.disabled = false;
            } catch(e) {
                console.error("WAV Export Error:", e);
                alert("匯出發生錯誤，請稍後再試。");
                const btn = document.getElementById('export-btn'); 
                btn.innerText = "⬇️ .wav"; btn.disabled = false;
            }
        }

        function audioBufferToWav(buffer) {
            let numChannels = buffer.numberOfChannels, sampleRate = buffer.sampleRate, format = 1, bitDepth = 16;
            let result = numChannels === 2 ? interleave(buffer.getChannelData(0), buffer.getChannelData(1)) : buffer.getChannelData(0);
            return encodeWAV(result, format, sampleRate, numChannels, bitDepth);
        }
        function interleave(inputL, inputR) {
            let length = inputL.length + inputR.length, result = new Float32Array(length), index = 0, inputIndex = 0;
            while (index < length) { result[index++] = inputL[inputIndex]; result[index++] = inputR[inputIndex]; inputIndex++; }
            return result;
        }
        function writeString(view, offset, string) { for (let i = 0; i < string.length; i++) view.setUint8(offset + i, string.charCodeAt(i)); }
        function encodeWAV(samples, format, sampleRate, numChannels, bitDepth) {
            let bytesPerSample = bitDepth / 8, blockAlign = numChannels * bytesPerSample;
            let buffer = new ArrayBuffer(44 + samples.length * bytesPerSample), view = new DataView(buffer);
            writeString(view, 0, 'RIFF'); view.setUint32(4, 36 + samples.length * bytesPerSample, true);
            writeString(view, 8, 'WAVE'); writeString(view, 12, 'fmt '); view.setUint32(16, 16, true);
            view.setUint16(20, format, true); view.setUint16(22, numChannels, true); view.setUint32(24, sampleRate, true);
            view.setUint32(28, sampleRate * blockAlign, true); view.setUint16(32, blockAlign, true); view.setUint16(34, bitDepth, true);
            writeString(view, 36, 'data'); view.setUint32(40, samples.length * bytesPerSample, true);
            let offset = 44;
            for (let i = 0; i < samples.length; i++, offset += 2) {
                let s = Math.max(-1, Math.min(1, samples[i])); view.setInt16(offset, s < 0 ? s * 0x8000 : s * 0x7FFF, true);
            }
            return buffer;
        }

        window.addEventListener('resize', () => { if(measures.length > 0) renderScore(); });

        updateScoreHeader(); updateInputLabels(); renderScore();
    </script>
</body>
</html>

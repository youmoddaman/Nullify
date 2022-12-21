// Use with a bookmark. Remove javascript: if using in the console or else it will not work. Code is obfuscated.

javascript:function fixLesson(){var csid = html5Iframe.src.split("?csid=")[1].split("&type")[0];
fetch(`https://login.i-ready.com/student/v2/web/lesson_component/${csid}/markprogress/${csid}`, {
  "headers": {
    "accept": "application/json, text/plain, */*",
    "accept-language": "en-US,en;q=0.9",
    "content-type": "application/json;charset=UTF-8",
    "sec-fetch-dest": "empty",
    "sec-fetch-mode": "cors",
    "sec-fetch-site": "same-origin",
    "sec-gpc": "1",
  },
  "referrer": "https://login.i-ready.com/student/dashboard/home",
  "referrerPolicy": "strict-origin-when-cross-origin",
  "body": `{\"value\":\"a",\"bucket\":\"short_term_unsecured\",\"datatype\":\"json\"}`,
  "method": "POST",
  "mode": "cors",
  "credentials": "include"
});
alert("Lesson fixed successfully! You may reload the lesson now.");}function getFrameSrc(){open(html5Iframe.src)}function toggleMenu(){'{"showMenu":true}'!==html5Iframe.contentWindow.localStorage.cheats?(html5Iframe.contentWindow.localStorage.cheats='{"showMenu":true}',html5Iframe.contentWindow.document.getElementById("settings-gear").click(),html5Iframe.contentWindow.document.getElementById("cancelBtn").click(),document.getElementById("tm").innerHTML="Disable"):(html5Iframe.contentWindow.localStorage.cheats='{"showMenu":false}',html5Iframe.contentWindow.document.getElementById("settings-gear").click(),html5Iframe.contentWindow.document.getElementById("cancelBtn").click(),setTimeout(function(){html5Iframe.contentWindow.localStorage.clear(),html5Iframe.contentWindow.document.getElementById("settings-gear").click(),html5Iframe.contentWindow.document.getElementById("cancelBtn").click(),document.getElementById("tm").innerHTML="Enable"},1e3))}function dragElement(e){var t=0,n=0,o=0,r=0;function s(e){(e=e||window.event).preventDefault(),o=e.clientX,r=e.clientY,document.onmouseup=i,document.onmousemove=c}function c(s){(s=s||window.event).preventDefault(),t=o-s.clientX,n=r-s.clientY,o=s.clientX,r=s.clientY,e.style.top=e.offsetTop-n+"px",e.style.left=e.offsetLeft-t+"px"}function i(){document.onmouseup=null,document.onmousemove=null}document.getElementById(e.id+"header")?document.getElementById(e.id+"header").onmousedown=s:e.onmousedown=s}const _api={};_api.dev={csidToAnswer(e){console.log(`https://cdn.i-ready.com/instruction/content/reading-comp/lessons/${e}/${e}.json`),html5Iframe.contentWindow.fetch(`https://cdn.i-ready.com/instruction/content/reading-comp/lessons/${e}/${e}.json`,{referrerPolicy:"strict-origin-when-cross-origin",body:null,method:"GET",mode:"no-cors",credentials:"include"}).then(e=>e.json()).then(e=>{if(""===String(_api.dataToAnswers(e,1),_api.dataToAnswers(e,2))){alert("This lesson isnt supported! No answers found >:");return}let t="No answers found! Please report this on the github or on discord",n=String(_api.dataToAnswers(e,1),_api.dataToAnswers(e,2)).split(",");for(let o=0;o<n.length;o++)n[o].split(":")[0]===html5Iframe.contentWindow.com.cainc.ifabric.lessonReport.collectReportData().lessonNavigationData.currentStep?t=n[o].split(":")[1]:console.log(n[o]);alert(t)})}},_api.dataToAnswers=(e,t)=>{function n(e){if("string"!=typeof e)return!1;try{let t=JSON.parse(e),n=Object.prototype.toString.call(t);return"[object Object]"===n||"[object Array]"===n}catch(o){return!1}}let o=[];for(let r in e.screens)for(let s in e.screens[r])if(s.includes("correct")&&!s.includes("incorrect")&&1==t)for(let c in e.screens[r][s])n(JSON.stringify(e.screens[r][s][c]))&&o.push(r+":"+e.screens[r][s][c].answer_text.value);else if(s.includes("part2_stem")&&2==t)for(let i=0;i<e.screens[r][s].part2_answer.length;i++)!0==e.screens[r][s].part2_answer[i].part2_is_correct&&e.screens[r][s].part2_answer[i].tp_t1_part2_answer_text&&o.push(r+":"+e.screens[r][s].part2_answer[i].tp_t1_part2_answer_text.part2_answer_text.value);return o},_api.getAnswers=()=>{_api.dev.csidToAnswer(html5Iframe.src.split("lesson/")[1])};const createElement=e=>document.body.appendChild(document.createElement(e));var UI=createElement("div");UI.innerHTML=`
	<div style="width:240px; left: 1px; top: 1px; background-color: #282828EB; color: white; outline: transparent 1px; position:absolute; z-index: 99999;">
		<div class="image">
        	<img src="https://res.cloudinary.com/dodofguiy/image/upload/v1671055312/icon_e4jrbs1_xzbsp8.png">
      		</div> <h1 style="font-size: 26px;">Nullify</h1>
		<br>
                <h3 style="font-size: 19px; font-style: normal !important; color: white !important;">Teacher Menu</h3>
		<button id='tm' onclick="toggleMenu()">Toggle</button>
		<br>
		<br>
		<h3 style="font-size: 19px; font-style: normal !important; color: white !important;">Get i-frame src</h3>
		<button onclick="getFrameSrc()">Get i-frame src</button>
		<br>
		<br>
	<h3 style="font-size: 19px; font-style: normal !important; color: white !important;">Get Answers (beta)</h3>
		<button onclick="_api.getAnswers();">Get</button>
                <br>
                <br>
        <h3 style="font-size: 19px; font-style: normal !important; color: white !important;">Lesson Fixer</h3>
		<button onclick="fixLesson()">Fix</button>
                <br>
                <br>
        <h3 style="font-size: 19px; font-style: normal !important; color: white !important;">Free i-Ready Games</h3>
		<button onclick="window.open('https://docs.google.com/document/d/1w-uay3y5pwOm45sG9JqiSopKH9DO3pejABpUPBL-uiw/edit?usp=sharing', '_blank');">Go to site</button>
        <h3 style="font-size: 19px; font-style: normal !important; color: white !important;">____________________________</h3>
		<button onclick="window.open('https://discord.gg/aAVVuVVVcm', '_blank');">Join the Nullify Discord</button>
	        <br>
                <br>
        <h1 style="font-size: 12px; font-style: normal !important; color: white !important;">Created by TonicGaro, notplu, wang, and H</h1>
        </div>`,dragElement(UI.firstElementChild);


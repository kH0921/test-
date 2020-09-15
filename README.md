<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <script>
      const name = 'litegames' //여기에 자기 엔트리아이디를 입력하세요
      const userid = '5f45980a3057be03b993738b' //여기에 자기 유저아이디를 입력하세요 (엔트리콘솔창에 user._id를 치면 자신의 유저아이디를 볼수있어요)
      const gitname = 'kH0921' //여기에 자기 깃허브아이디를 입력하세요 (깃허브계정이 없으면 그냥 avocad5를 입력하세요<ㅍ)
      const nickname = '라이트' //여기에 자기 별명을 입력하세요 
      const myment = '참신하고 재미있는 콘텐츠' //여기에 상태메시지를 입력하세요 
      const mywork = 'DISCORD' //여기에 자신의 대표작품을 입력하세요
      const career = '1년' //여기에 자신의 경력을 입력하세요
      const explanation = '지나가던 평범한 사람' //여기에 자기소개를 입력하세요
      const maincolor = '#0000FF' //여기에 메인컬러를 입력하세요 #87FFB7
      const subcolor = '#00FFFF' //여기에 서브컬러를 입력하세요
      const projectname = ['DISCORD','SECRE','[문답챌린지]영자의 22문답']; //여기에 자기 엔트리작품 이름을 입력하세요 (저는 3개만 했지만 여러분은 엄청 많이 하셔도 되요)
      const projectment = ['서버 생성이 가능한 채팅 프로그램!','스스로 배우는 똑똑한 AI!','영자님의 22문답!'] //여기에 자기 엔트리작품 소개를 입력하세요 
      const projectid = ['5f461c11aa40150402ba5840','5f49819fcef69d00612f8b4b','5f58994e21437402794fbb1a'] //여기에 자기 엔트리작품 id를 입력하세요
      const theme = 'dark' //light또는 dark를 입력하세요
      
      
      function load(){
        for(var i = 0; i<projectname.length; i++){
          document.getElementsByClassName('project')[0].innerHTML += `<a href="https://playentry.org/${name}/${projectid[i]}"><img class="pimg" src="https://playentry.org/uploads/thumb/${projectid[i].substring(0,4)}/${projectid[i]}.png"><div class="pdiv"><p class="pname"><strong>${projectname[i]}</strong></p><p class="pment">${projectment[i]}</p></div></a>`
        }
        var avatar = `https://playentry.org/uploads/profile/${userid.substring(0,2)}/${userid.substring(2,4)}/avatar_${userid}.png`
        document.title = `${nickname}의 공식사이트`
        document.querySelector("body > div.name").innerHTML = name
        document.querySelector("body > div.ment").innerHTML = myment
        document.querySelector("body > div.container > svg > path").style.fill = maincolor
        document.querySelector("body > div.profile > a").href = `https://playentry.org/${name}`
        document.querySelector("body > div.profile > a").innerHTML = `<img src="${avatar}">`
        document.querySelector("body > div.profile > div").innerHTML = `<p>이름 : ${name}</p><p>별명 : ${nickname}</p><p>대표작 : ${mywork}</p><p>경력 : ${career}</p><p>소개 : ${explanation}</p>`
        document.querySelector("body > div.footer").innerHTML = `<a href="https://github.com/${gitname}"><span>Github</span></a><a href="https://playentry.org/${name}#!/"><span>Entry</span></a>`
        var css = `.project a div:hover{background-color: ${maincolor};}`
        var style = document.createElement('style');
        if (style.styleSheet) {
            style.styleSheet.cssText = css;
        } else {
            style.appendChild(document.createTextNode(css));
        }
        document.getElementsByTagName('head')[0].appendChild(style);
      }
      function darkmode(){
        var p = document.getElementsByTagName('p')
        for(var i = 0; i<p.length; i++){
          p[i].style.color = 'white'
        }
        var pdiv = document.getElementsByClassName('pdiv')
        var pimg = document.getElementsByClassName('pimg')
        for(var i = 0; i<pdiv.length; i++){
          pdiv[i].style.backgroundColor = '#505050'
          pdiv[i].style.boxShadow = '0 0 30px -15px #111111'
          pimg[i].style.boxShadow = '0 0 30px -15px #111111'
        }
        document.querySelector("body").style.backgroundColor = '#1E1E1E'
        document.querySelector("body > div.projecttext").style.color = 'white'
        document.querySelector("body > div.profile > a > img").style.boxShadow = '0 0 30px -15px #111111'
      }
    </script>
    <title>자기소개</title>
    <style>
      @font-face { font-family: 'GmarketSansBold'; src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2001@1.1/GmarketSansBold.woff') format('woff'); font-weight: normal; font-style: normal; }
      body{
        margin: 0;
        background-color : #FcFcFc;
      }
      .container {
        z-index:-1;
        display: inline-block;
        position: relative;
        width: 100%;
        padding-bottom: 100%;
        vertical-align: middle;
        overflow: hidden;
      }
      .head {
        display: inline-block;
        position: absolute;
        top: 0;
        left: 0;
      }
      .svgpath{
        stroke: none;
        fill:#87FFB7;
      }
      .name{
        margin-top:-95%;
        display: flex;
        justify-content: center;
        font-family: "GmarketSansBold";
        font-size: 570%;
      }
      .ment{
        display: flex;
        justify-content: center;
        color: #404040;
        font-size: 20px;
      }
      .profile{
        display: flex;
        justify-content: center;
        margin-top: 20%;
      }
      .profile a{
        margin-right: 10%;
      }
      .profile a img{
        width: 400px;
        height: 400px;
        box-shadow: 0 0 30px -10px #A0A0A0;
        border-radius: 30px;
        border: 2px solid black;
      }
      .profile p{
        font-size: 25px;
      }
      .projecttext{
        font-size: 50px;
        text-align: center;
        margin-top: 10%;
        font-family: "GmarketSansBold";
      }
      .project{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin-top: -2%;
        margin-bottom: 10%;
      }
      .project a{
        margin-top: 100px;
        width: 450px;
        height: 300px;
        margin-left: 50px;
        margin-right: 50px;
        text-align: center;
        text-decoration:none;
      }
      .project a img{
        width: 400px;
        border-radius: 30px;
        box-shadow: 0 0 30px -15px #A0A0A0;
        border: 2px solid black;
      }
      .project a div{
        height: 170px;
        border-radius: 30px;
        box-shadow: 0 0 30px -15px #A0A0A0;
        margin-top: -80px;
        background-color: white;
        transition: background-color 0.5s;
      }
      .project a div .pname{
        color: black;
        padding-top: 70px;
        font-size: 20px;
      }
      .project a div .pment{
        color: black;
        margin-top: -10px;
      }
      .foot{
        position: relative;
        -moz-transform: scaleY(-1);
        -o-transform: scaleY(-1);
        -webkit-transform: scaleY(-1);
        transform: scaleY(-1);
        filter: FlipV;
        -ms-filter: "FlipV";
        fill: #BFFFC3;
        margin-top: -1900px;
        z-index: -10;
      }
      .footer{
        display: flex;
        justify-content: center;
        height: 100px;
        background-color: #BFFFC3;
        margin-top: -100px;
      }
      .footer a{
        border: 2px solid black;
        border-radius: 5px;
        width: 100px;
        height: 50px;
        text-align: center;
        font-size: 20px;
        padding-top: 15px;
        margin-left: 5px;
        margin-right: 5px;
        transition: 0.5s;
        color: black;
        text-decoration:none;
      }
      .footer a:hover{
        background-color: black;
        border-color: black;
        color: white;
        transition: 0.5s;
      }
    </style>
    <head>
</head>
  </head>
  <body>
    <div class="container">
      <svg class="head" viewBox="0 0 500 500" preserveAspectRatio="xMinYMin meet">
        <path d="M0,100 C150,200 350,0 500,100 L500,00 L0,0 Z" class="svgpath"></path>
      </svg>
    </div>
    <div class="name">
      avocad5
    </div>
    <div class="ment">
      참신하고 재미있는 콘텐츠
    </div>
    <div class="profile">
      <a href="https://playentry.org/avocad5" class="proimg"></a>
      <div class="about">
        <p>이름 : litegames</p>
        <p>별명 : 라이트</p>
        <p>엔트리 경력 : 1년</p>
        <p>웹개발 경력 : 1일</p>
        <p>소개 : 지나가던 평범한 사람</p>
      </div>
    </div>
    <div class="projecttext">my projects</div>
    <div class="project">

    </div>
    <svg class="foot" viewBox="0 0 500 500" preserveAspectRatio="xMinYMin meet">
      <path d="M0,100 C150,200 350,0 500,100 L500,00 L0,0 Z"></path>
      <div class="footer">
      </div>
    </svg>
  </body>
  <script>load();if(theme=='dark'){darkmode();}</script>
</html>

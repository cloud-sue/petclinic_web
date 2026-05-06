<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pet Clinic</title>
<style>
body {
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
height: 100vh;
margin: 0;
font-family: sans-serif;
background-color: #f9f9f9;
}
img {
width: 300px;
border-radius: 15px;
margin-bottom: 20px;
box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}
h2 {
color: #333;
margin-bottom: 20px;
}
/* 서버 정보를 보여줄 박스 디자인 추가 */
.server-info {
margin-bottom: 20px;
padding: 15px 30px;
background-color: #e3f2fd;
border: 1px solid #90caf9;
border-radius: 8px;
color: #1565c0;
text-align: center;
line-height: 1.6;
}
button {
padding: 12px 24px;
font-size: 16px;
color: white;
background-color: #4CAF50;
border: none;
border-radius: 5px;
cursor: pointer;
transition: background-color 0.3s;
}
button:hover {
background-color: #45a049;
}
</style>
</head>
<body>

<img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yuumi_0.jpg" alt="귀여운 유미 사진">

<h2>petclinic으로 들어가시겠습니까</h2>

<!-- AWS **********************************************************************************************************************************************    -->
<div class="server-info">
    <?php
    // 1. 호스트명(가상머신 이름) 가져오기
    $hostname = gethostname();

    // 2. AWS IMDSv2 토큰 발급 (보안 강화 버전)
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, "http://169.254.169.254/latest/api/token");
    curl_setopt($ch, CURLOPT_CUSTOMREQUEST, "PUT");
    curl_setopt($ch, CURLOPT_HTTPHEADER, array('X-aws-ec2-metadata-token-ttl-seconds: 21600'));
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
    curl_setopt($ch, CURLOPT_TIMEOUT, 2);
    $token = curl_exec($ch);
    curl_close($ch);

    $zone = "확인 불가 (비 AWS 환경 또는 에러)";

    // 토큰 발급에 성공했을 경우에만 Zone 정보 요청
    if ($token) {
        $ch = curl_init();
        curl_setopt($ch, CURLOPT_URL, "http://169.254.169.254/latest/meta-data/placement/availability-zone");
        curl_setopt($ch, CURLOPT_HTTPHEADER, array("X-aws-ec2-metadata-token: $token"));
        curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
        curl_setopt($ch, CURLOPT_TIMEOUT, 2);
        $zone_response = curl_exec($ch);
        curl_close($ch);

        if ($zone_response) {
            $zone = $zone_response;
        }
    }

    echo "<strong>접속된 서버(EC2):</strong> " . $hostname . "<br>";
    echo "<strong>가용 영역(Availability Zone):</strong> " . $zone;
    ?>
</div>

<!-- Azure **********************************************************************************************************************************************    -->    
<!--

<div class="server-info">
    <?php
    // 1. 호스트명(가상머신 이름) 가져오기
    $hostname = gethostname();

    // 2. 클라우드 메타데이터 서비스(IMDS)에서 Zone 정보 가져오기 (Azure 기준)
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, "http://169.254.169.254/metadata/instance/compute/zone?api-version=2021-02-01&format=text");
    curl_setopt($ch, CURLOPT_HTTPHEADER, array('Metadata:true'));
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
    curl_setopt($ch, CURLOPT_TIMEOUT, 2); // 응답 지연 방지
    $zone = curl_exec($ch);
    curl_close($ch);

    if(!$zone) {
        $zone = "확인 불가 (해당 클라우드 환경 아님)";
    }

    echo "<strong>접속된 서버(VM):</strong> " . $hostname . "<br>";
    echo "<strong>가용 영역(Zone):</strong> " . $zone;
    ?>
</div>
    -->

<button onclick="window.location.href='/petclinic/'">입장하기</button>

</body>
</html>

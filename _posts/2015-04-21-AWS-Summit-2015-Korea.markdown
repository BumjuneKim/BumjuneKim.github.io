---
title:  "AWS Summit 2015 Korea"
---
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>AWS Summit 2015 Korea</title>
    <link rel="stylesheet" href="/css/reveal.css">
    <link rel="stylesheet" href="/css/theme/simple.css" id="theme">
    <!--[i?f lt IE 9]>
    <script src="lib/js/html5shiv.js"></script>
    <![endif]-->
</head>
<body>
<div class="reveal">
    <div class="slides">
        <section>
            <section>
                <img src="/images/AWSSummit/title.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/1-1.jpg" style="border: none;height:100%">
            </section>
            <section>
                <img src="/images/AWSSummit/1-2.jpg" style="border: none;height:100%">
            </section>
            <section>
                <img src="/images/AWSSummit/1-3.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/1-4.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/1-5.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/1-6.jpg" style="border: none;height:100%">
            </section>
        </section>
        <section>
            <h2>목차</h2>
            <ol>
                <li>Keynote</li>
                <li>IoT - 컴퓨팅의 진화 </li>
                <li>AWS소개</li>
                <li>CloudFront와 Route53기반 콘텐츠 배포 전략 </li>
                <li>AWS를 활용한 실시간 빅데이터 및 스트리밍 분석 </li>
                <li>국민내비 김기사, AWS 하이브리드 클라우드 성공사례 </li>
                <li>모바일 및 IoT환경을 위한 AWS클라우드 플랫폼의 진화 </li>
                <li>EBS성능향상 및 EC2비용 최적화기법</li>
            </ol>
        </section>
        <section>
            <section>
                <h1>Keynote</h1>
            </section>
            <section>
                <img src="/images/AWSSummit/2-1.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/2-3.jpg" style="border: none;">
            </section>
            <section>
                <div style="text-align: left;">
                    <ul>
                        <li style="list-style-type: none;">1. AWS현황</li>
                        <li>Retail, B2B, Infrastructure</li>
                        <li>2013 Q4 ~ 2014 Q4 : S3(102%), EC2(93%)</li>
                        <li>go with partners and customers</li>
                        <li>점점 cloud는 대안이 아닌 대세가 되어가고 있다.</li>
                        <br /> 
                        <li style="list-style-type: none;">2. AWS장점</li>
                        <li>Mobility, Agility, Speed, Cost....</li>
                        <li>이용사례 : 3D렌더링, SM엔터, 삼성전자프린터사업</li>
                        <br /> 
                        <li style="list-style-type: none;">3. 목표</li>
                        <li>9년간 비지니스하여 혁명을 이뤘다</li>
                        <li>고객지향, 개척자정신, 장기적투자</li>
                    </ul>
                </div>
            </section>
            <section>
                <img src="/images/AWSSummit/2-2.jpg" style="border: none;">
            </section>
        </section>
        <section>
            <section>
                <h2>IoT - 컴퓨팅의 진화(intel)</h2>
            </section>
            <section>
                <div style="text-align: left;">
                    <ul>
                        <li>2020년 500억개 디바이스 연결 예상</li>
                        <li>Peer to Peer -> Things to Things </li>
                        <li>End to End Solution 제공</li>
                        <li>Cloud is the best solution for IoT</li>
                        <li>Edison flatform</li>
                    </ul>
                </div>
            </section>
            <section>
                <img src="/images/AWSSummit/3-1.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/3-2.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/3-3.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/3-4.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/3-5.jpg" style="border: none;">
            </section>
        </section>
        <section>
            <section>
                <h1>AWS소개</h1>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">1. AWS장점</li>
                    <li>선 투자금 없음(가변비용)</li>
                    <li>규모의경제(48번의 가격인하)</li>
                    <li>탄력적인 처리용량(예측이 불필요)</li>
                    <li>Agility - 분단위 provisioning</li>
                    <li>비지니스에 집중</li>
                    <li>수 분내에 글로벌 고객에게 진출가능</li>
                </ul>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">2. AWS구성(위치)</li>
                    <li>11 Regions</li>
                    <li>29 Availability zones - 전력, 인터넷 독립</li>
                    <li>Region > AZ >= Datacenter</li>
                    <li>53 Edge Location(CDN) - Seoul 2Edge</li>
                </ul>
            </section>
            <section>
                <h2>Compute Service</h2>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">1) Amazon EC2(Elastic Compute Cloud)</li>
                    <li>Virtual Machine - 쉽게 확장, 축소</li>
                    <li>37개의 instance type - 동일타입내 사이즈별 구분</li>
                    <li>되도록이면 최신에 나온 타입 사용권장</li>
                    <li>사이즈가 2배가 되면 가격도 두배</li>
                    <li>작은 사이즈에서 테스트 하며 적합 인스턴스 타입 탐색</li>
                    <li>2xlarge = 2 * xlarge = 4 * large</li>
                    <li>c4.large --> 숫자는 버전 large는 사이즈</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/4-1.jpg" style="border: none;">
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">2) Auto Scailing</li>
                    <li>EC2와 ELB등에서 사용할 수 있는 서비스</li>
                    <li>수동으로도 가능</li>
                    <li>쿠키런이 Auto Scailing을 사용한 좋은 사례(in Korea)</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/4-2.jpg" style="border: none;">
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">3) ELB(Elastic Load Balancing)</li>
                    <li>트래픽을 자동으로 분산 </li>
                    <li>자동으로 용량 확장/축소(Auto Scailing)</li>
                    <li>물리적으로 스위치가 여러개 있는것처럼 동작</li>
                    <li>외부에 둘수도 WAS안에 둘수도 있다.</li>
                </ul>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">4) 구매옵션</li>
                    <li>On-Demand : 시간당과금</li>
                    <li>Reserved : 정액제(항상 켜져있는 서비스)</li>
                    <li>Spot : 경매방식으로 저렴하게 공급</li>
                    <li>Dedicated : 제한적인 인원만을 위한 물리적서버</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/4-3.jpg" style="border: none;">
            </section>
            <section>
                <h2>Storage</h2>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">1) S3(Simple Storage Service)</li>
                    <li>내구성, 안정성 최고 99.999999999%</li>
                    <li>원하는만큼 사용이가능(무제한)</li>
                    <li>저장하는 만큼 과금</li>
                    <li>static 리소스에 관한 매니징(webserver로 동작)</li>
                    <li>Auto Scailing이 되어 서비스가 안되는 경우는 없다.</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/4-4.jpg" style="border: none;">
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">2) Amazon Glacier</li>
                    <li>백업용도의 Cold데이터 저장</li>
                    <li>S3의 1/3 가격</li>
                    <li>retrieval시 3~5시간 정도 걸리는 단점</li>
                    <li>오래된 자료 또는 열람이 잘 안되는 자료 보관용도로 적합</li>
                    <li>라이프사이클 정책 지정가능</li>
                    <li>S3 -> 30days -> Glacier -> 1year drop</li>
                </ul>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">3) EBS(Elastic Block Store)</li>
                    <li>EC2에 마운트된 하드디스크의 개념</li>
                    <li>필요할때 얼마든지 system in & out가능</li>
                    <li>EC2상태에 상관없이 독립적</li>
                    <li>1GB ~ 16TB (per 1 Volume)</li>
                    <li>Magnetic, General Purpose, Provisioned IOPS</li>
                    <br />
                    <li style="list-style-type: none;">4) Elastic File Service</li> 
                    <li>Petabyte Scale, Beta서비스중, NAS대체할수 있다.</li>
                </ul>
            </section>
            <section>
                <h2>Database</h2>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">1) RDS(Relational Database Service)</li>
                    <li>MySQL, Oracle, MS SQL, PostgreSQL</li>
                    <li>Fully Managed / low admin</li>
                    <li>라이센스 포함되어 걱정없이 사용하시라.</li>
                    <li>자동 스냅샷(1일1회 자동생성, 35일 보관)</li>
                    <li>스냅샷을 다른 region으로 복제 및 생성가능</li>
                    <li>Read-replica복제 (read>write) 가까운 region으로</li>
                </ul>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">2) DynamoDB</li>
                    <li>NoSQL</li>
                    <li>Fully Managed / low admin</li>
                    <li>몇 개의 클라이언트가 붙던간에 같은성능제공</li>
                    <li>SSD기반</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/4-5.jpg" style="border: none;">
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">3) Elastic Cache</li>
                    <li>In-Memory Cache</li>
                    <li>탄력적이고 안정적</li>
                    <li>Cache층의 관리포인트 줄어듬</li>
                    <li>Memcached or Redis</li>
                    <li>작은용량에 잦은접근을 하는 데이터에 적합</li>
                    <li>AirBnB 핫포인트 발생하는 경우 AEC사용</li>
                    <li style="list-style-type: none;">4) New DB Service:Aurora</li> 
                    <li>beta지만 곧 상용예정</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/4-7.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/4-8.jpg" style="border: none;">
            </section>
        </section>
        <section>
            <section>
                <h3>CloudFront,Route53기반</h3>
                <h3>     콘텐츠배포전략       </h3>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">1. CloudFront</li>
                    <li>AWS의 CDN서비스</li>
                    <li>가장 가까운 서버로부터 컨텐츠 전송받기</li>
                    <li>사용자의 경험성, 편의성 증가</li>
                    <li>편의점이 가장 현실적인 비유</li>
                    <li>서울에 2개 Edge존재 -> AWS의 Korea생각!</li>
                </ul>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">2. Route53</li>
                    <li>Cloud DNS웹 시스템</li>
                    <li>GSLB서비스의 일종</li>
                    <li>장비들의 상태, 성능 파악하여 최적경로제공</li>
                    <li>latency, 가중치, region등으로 결정</li>
                    <li>1억건 질의해도 한달10만원</li>
                    <li>전송최적화, SSL적용, Signed Url, cookie등 추가기능제공</li>
                </ul>
            </section>
        </section>
        <section>
            <section>
                <h3>AWS를 활용한 실시간 빅데이터 및 스트리밍 분석 </h3>
            </section>
            <section>
                <ul>
                    <li>Batch Processing EMR(Elastic MapReduce)</li>
                    <li>Hue -> Web Management System(system oper)</li>
                    <li>flexible</li>
                    <li>Easy to add and remove compute capacity on your cluster.</li>
                </ul>
            </section>
        </section>
        <section>
            <section>
                <h3>      국민내비 김기사 </h3>
                <h3>AWS 하이브리드 클라우드 성공사례 </h3>
            </section>
            <section>
                <ul>
                    <li>Cloud dosen't matter</li>
                    <li>1년 트래픽분석 -> 명절때 트래픽 상승</li>
                    <li>김기사는 private환경으로 먼저 구성</li>
                    <li>HOSTWAY에서 Hybrid제안</li>
                    <li>Managed Service (AWS <-> 고객)</li>
                    <li>개,꼬리 역전</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/5-1.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/5-2.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/5-3.jpg" style="border: none;">
            </section>
        </section>
        <section>
            <section>
                <h3>모바일 및 IoT환경을 위한</h3>
                <h3>   AWS 플랫폼의 진화 </h3>
            </section>
            <section>
                <ul>
                    <li>서비스 큰 이슈 : 속도</li>
                    <li>개발집중 환경 중요</li>
                    <li>레고 조립 -> 요구사항을 정확히 파악</li>
                    <li>AWS Kinesis(streaming), Cognito(auth)</li>
                    <li>*AWS Lambda : Event Driven하여 개발자 코드실행</li>
                    <li>이벤트 발생하여 사용되는 만큼만 과금</li>
                    <li>Rules based on Automatic server : serverless</li>
                    <li><a href="https://youtu.be/iz8ke9ROq0A" target="_blank">Demo</a> (AWS Lambda) </li>
                    <li><a href="http://youtu.be/COKgKBvAjx0" target="_blank">Demo</a> (AWS IoT - Arduino) </li>
                    <li><a href="https://github.com/awslabs/aws-sdk-arduino">Github-SDK</a></li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/6-1.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/6-2.jpg" style="border: none;">
            </section>
        </section>
        <section>
            <section>
                <h2>EBS성능향상 및 EC2비용 최적화기법</h2>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">1. EBS Volume type</li>
                    <li>General Purpose, Provisioned IOPS, Magnetic</li>
                    <li>IOPS (Input Output Per Second)</li>
                    <li>volume limit 1TB -> 16TB (2015.3.19)</li>
                    <li>pre-warming / RAID / queue depth조정</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/7-1.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/7-2.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/7-3.jpg" style="border: none;">
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">2. AWS Cost</li>
                    <li>cost줄이길 원한다면 아무것도 하지마라.</li>
                    <li>규모의 경제를 만들어 선순환하자</li>
                    <li>2006년부터 48번의 가격하락</li>
                    <li>AWS Trusted Advisor에서 권고하는사항</li>
                    <li>Optimization != Lower cost</li>
                </ul>
            </section>
            <section>
                <ul>
                    <li style="list-style-type: none;">3. Cost Optimization Tip 7</li>
                    <li>Turn off unused instances</li>
                    <li>Use Auto Scailing(진입장벽 높지만 운영 편해짐)</li>
                    <li>Use reserved instance(런칭 후 통계보고 결정)</li>
                    <li>Use spot instance(최근 인스턴스 terminated 2분전 알림)</li>
                    <li>Decide S3 class  99.999999999% -> 99.99%<br />
                         Reduced Redundancy Storage / Glacier</li>
                    <li>Optimize Amazon DynamoDB capacity units</li>
                    <li>Offload your architecture</li>
                </ul>
            </section>
            <section>
                <img src="/images/AWSSummit/7-4.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/7-5.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/7-6.jpg" style="border: none;">
            </section>
            <section>
                <img src="/images/AWSSummit/7-7.jpg" style="border: none;">
            </section>
        </section>
        <section style="text-align: left;">
            <h1>Thank you</h1>
        </section>
    </div>
</div>
<script src="/js/jquery-1.11.1.min.js"></script>
<script src="/lib/js/head.min.js"></script>
<script src="/js/reveal.js"></script>
<script>
    Reveal.initialize({
        controls: true,
        progress: true,
        slideNumber: true,
        fragments: true,
        top: 0
    });
</script>
</body>

</html>

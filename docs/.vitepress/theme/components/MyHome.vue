<template>
  <main>
    <div class="banner">
      <h1>BFChain开发者社区</h1>
      <p>为开发者提供全方位服务和工具，帮助构建区块链生态体系。</p>
    </div>
    <section class="forest">
      <div class="content">
        <div class="title">什么是生物链林?</div>
        <div class="description">信用而生，缔造人人可信的信用时代</div>
        <div class="detail">
          <div class="detail-item">
            <div class="img feature-1"></div>
            <div class="detail-des">
              全球首款移动公有链
            </div>
          </div>
          <div class="detail-item">
            <div class="img feature-2"></div>
            <div class="detail-des">
              移动区块链底层协议
            </div>
          </div>
          <div class="detail-item">
            <div class="img feature-3"></div>
            <div class="detail-des">
              构建移动端底层公链BFChain、社交链FINChain、联盟链数据版
            </div>
          </div>
          <div class="detail-item">
            <div class="img feature-4"></div>
            <div class="detail-des">
              自成体系，跨链特性互有关联
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="developer-group">
      <div class="content">
        <div class="developer-group-left">
          <div class="title">BFChain开发者社区是?</div>
          <div class="description">
            BFChain开发者社区是一个在BFChain上开发和构建应用程序所需工具的地方,包含开发者所需相关资源的汇集地。
          </div>
        </div>
        <div class="developer-group-right">
          <div class="img">
            <img src="/dev-community.png" />
          </div>
        </div>
      </div>
    </section>
    <section class="developer-tool">
      <div class="content">
        <div class="title">开发者工具</div>
        <div class="description">DEVELOPER TOOL</div>
        <div class="tool">
          <div class="tool-item">
            <div class="img bfs">
              <!-- <img src="/assets/1BFS.png" alt=""> -->
            </div>
            <div class="tool-item-name">
              BFS
            </div>
            <div class="tool-des">
              Bioforest Chain System
            </div>
          </div>
          <div class="tool-item">
            <div class="img five-click">
              <!-- <img src="/assets/2五敲.png" alt=""> -->
            </div>
            <div class="tool-item-name">
              五敲
            </div>
            <div class="tool-des">
              分布式协作工具
            </div>
          </div>
          <div class="tool-item">
            <div class="img sdk">
              <!-- <img src="/assets/3开发者SDK.png" alt=""> -->
            </div>
            <div class="tool-item-name">
              开发者SDK
            </div>
            <div class="tool-des">
              区块链编程的软件开发工具包
            </div>
          </div>
          <div class="tool-item">
            <div class="img terminal">
              <!-- <img src="/assets/4超级终端.png" alt=""> -->
            </div>
            <div class="tool-item-name">
              超级终端
            </div>
            <div class="tool-des">
              区块链跨平台集成开发环境
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="recommend">
      <div class="content">
        <div class="title">推荐</div>
        <div class="description">RECOMMEND</div>
        <div class="recommend-articles">
          <a class="recommend-item" href="/blog/03">
            <div class="img-container"><img src="./imgs/re_03.jpg" /></div>
            <div class="recommend-item-name">
              生物链林BFChain的共识机制有什么独到之处？
            </div>
            <div class="recommend-item-des">
              共识（Consensus），即达成一致的意见。自人类协作关系产生起，共识就已诞生。一个正常运转的...
            </div>
          </a>
          <a class="recommend-item" href="/blog/04">
            <div class="img-container"><img src="./imgs/re_04.jpg" /></div>
            <div class="recommend-item-name">
              生物链林的技术特性和优势
            </div>
            <div class="recommend-item-des">
              两大特性及优势：“完全自主化研发的区块链底层基础设施” 和
              “移动区块链赋能实体企业数字化转型”...
            </div>
          </a>
          <a class="recommend-item" href="/blog/05">
            <div class="img-container"><img src="./imgs/re_05.jpg" /></div>
            <div class="recommend-item-name">
              BFChain首创的移动端点对点通信方案，到底厉害在哪？
            </div>
            <div class="recommend-item-des">
              区块链技术打破传统互联网的诸多限制，其中一点，是P2P（peer to
              peer，即点对点）的通信方式...
            </div>
          </a>
          <a class="recommend-item" href="/blog/06">
            <div class="img-container"><img src="./imgs/re_06.jpg" /></div>
            <div class="recommend-item-name">
              揭秘BFChain如何破解移动端区块链三大技术难题？
            </div>
            <div class="recommend-item-des">
              BFChain作为全球第一条基于移动端的公有链，真正实现了移动端直连区块链并参与链上治理...
            </div>
          </a>
        </div>
        <a class="more" href="/blog/">了解更多 ></a>
      </div>
    </section>
  </main>
  <footer>
    <div class="content footer-content">
      <div class="footer-copyright">
        <span>版权所有 © BFChain开发者社区</span>
      </div>
      <div class="footer-law">
        <!-- <span><a href="#">隐私政策</a></span> -->
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts"></script>

<style global>
:root {
  --c-brand: #4a78f7;
  --c-brand-light: #5688ff;
  --docsearch-primary-color: #4a78f7;
}
.nav-bar-title {
  text-indent: -9999px;
  width: 175px;
  height: 37px;
  background: url(/logo.png);
  background-size: cover;
}
.DocSearch {
  --docsearch-primary-color: var(--docsearch-primary-color) !important;
  --docsearch-highlight-color: var(--docsearch-primary-color) !important;
}
p > img {
  display: block;
  margin: 0 auto;
  width: 100%;
}
.content p {
  text-indent: 2em;
}
.content li p {
  text-indent: 0;
  margin: 0;
}
</style>
<style scoped>
.home {
  padding-top: var(--header-height);
}
.banner {
  height: 480px;
  text-align: center;
  background: url(/banner.jpg) no-repeat top left;
  background-size: cover;
  display: flex;
  flex-direction: column;
  color: #fff;
  justify-content: space-around;
  padding: 180px 0;
}
* {
  margin: 0;
  padding: 0;
}
html {
  width: 100%;
  /* fontsize: 6.94444444vw; */
}
body {
  width: 100%;
  font-size: 14px;
  background-color: rgba(255, 255, 255, 1);
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* -----main global begin------- */
main {
  width: 100%;
}
header,
section,
footer {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
}
section {
  height: 480px;
  max-height: 480px;
  background-color: rgb(250, 250, 250);
}
/* -----main global end------- */
.content {
  width: 1024px;
  max-width: 1366px;
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.title {
  font-weight: bold;
}
/*----- global 全局 end------*/

/* -----banner&developer-group begin------ */
.developer-group .content,
.banner .content {
  display: flex;
}
.developer-group-left,
.developer-group-right,
.banner-left,
.banner-right {
  width: 50%;
}

.developer-group-left,
.banner-left {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.developer-group-left div,
.banner-left div {
  margin-left: 100px;
}
.developer-group-left .title,
.banner-left .title {
  line-height: 50px;
  font-family: PingFangSC-Semibold;
  font-size: 36px;
  color: #131313;
  letter-spacing: 0;
}
.developer-group-left .title {
  line-height: 33px;
  font-size: 28px;
}
.developer-group-left .description,
.banner-left .description {
  margin-top: 8px;
  padding-left: 2px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #131313;
}
.developer-group-left .description {
  width: 320px;
}

.developer-group-right .img,
.banner-right .img {
  width: 400px;
  height: 300px;
  margin: 70px 90px 110px auto;
}

.developer-group-right .img {
  margin: 90px 90px 90px auto;
}
/* -----banner&developer-group end------ */

/* -----forest begin----- */
.forest {
  background-color: #fff;
}
.forest .content {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}
.forest .title {
  line-height: 40px;
  margin-top: 74px;
  margin-bottom: 8px;
  font-family: PingFangSC-Semibold;
  font-size: 28px;
  color: #131313;
  letter-spacing: 0;
  text-align: center;
}

.forest .description {
  height: 26px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #131313;
  text-align: center;
}

.forest .detail {
  display: flex;
  justify-content: space-around;
}

.detail .detail-item {
  width: 25%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 55px;
}

.detail-item .img {
  width: 120px;
  height: 120px;
  margin-bottom: 34px;
  /* background: #D8D8D8; */
  background: url(/assets/forest/1.png) no-repeat;
  background-size: cover;
  border-radius: 50%;
}

.detail-item .feature-2 {
  background-image: url(/assets/forest/2.png);
}

.detail-item .feature-3 {
  background-image: url(/assets/forest/3.png);
}

.detail-item .feature-4 {
  background-image: url(/assets/forest/4.png);
}

.detail-item .detail-des {
  width: 205px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #131313;
  text-align: center;
}

/* -----forest end----- */

/* -----developer-tool begin----- */

.developer-tool {
  background-color: #fff;
}
.developer-tool .content {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}
.developer-tool .title {
  height: 33px;
  margin-top: 60px;
  margin-bottom: 4px;
  font-family: PingFangSC-Semibold;
  font-size: 24px;
  color: #131313;
  letter-spacing: 0;
  text-align: center;
}

.developer-tool .description {
  height: 26px;
  font-family: PingFangSC-Medium;
  font-size: 14px;
  color: #666666;
  text-align: center;
}

.developer-tool .tool {
  display: flex;
  justify-content: space-around;
}

.tool .tool-item {
  width: 25%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 40px;
}

.tool-item .img {
  width: 120px;
  height: 120px;
  margin-bottom: 17px;
  /* background: #D8D8D8; */
  background: url(/assets/tools/1.png) no-repeat;
  background-size: cover;
}

.tool-item .five-click {
  background-image: url(/assets/tools/2.png);
}

.tool-item .sdk {
  background-image: url(/assets/tools/3.png);
}

.tool-item .terminal {
  background-image: url(/assets/tools/4.png);
}

.img img {
  width: 100%;
}

.tool-item .tool-item-name {
  line-height: 22px;
  margin-bottom: 5px;
  font-family: PingFangSC-Semibold;
  font-size: 16px;
  font-weight: bold;
  color: #131313;
  text-align: center;
}

.tool-item .tool-des {
  width: 205px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #131313;
  text-align: center;
}

/* -----developer-tool end----- */

/* -----recommend begin----- */

.recommend {
}
.recommend .content {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
.recommend .title {
  height: 33px;
  margin-top: 60px;
  margin-bottom: 4px;
  font-family: PingFangSC-Semibold;
  font-size: 24px;
  color: #131313;
  letter-spacing: 0;
  text-align: center;
}

.recommend .description {
  height: 26px;
  font-family: PingFangSC-Medium;
  font-size: 14px;
  color: #666666;
  text-align: center;
}

.recommend .recommend-articles {
  width: 934px;
  display: flex;
  justify-content: space-between;
}

.recommend-articles .recommend-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 40px;
  cursor: pointer;
  text-decoration: none;
}

.recommend-item .img-container {
  width: 216px;
  height: 130px;
  overflow: hidden;
  margin-bottom: 20px;
  background: #d8d8d8;
}

.recommend-item .img-container img {
  cursor: pointer;
  transition: all 0.5s; /* 所有的属性变化在0.5s的时间段内完成 */
}
.recommend-item:hover .img-container img {
  transform: scale(1.2);
}

.recommend-item .recommend-item-name {
  width: 216px;
  line-height: 22px;
  margin-bottom: 6px;
  font-family: PingFangSC-Semibold;
  font-size: 16px;
  font-weight: bold;
  color: #131313;
  text-align: left;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  transition: all 60ms;
}

.recommend-item .recommend-item-des {
  width: 216px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #131313;
  text-align: left;
  overflow: hidden;
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}

.recommend .more {
  margin-top: 35px;
  font-family: PingFangSC-Regular;
  font-size: 14px;
  color: #4a78f7;
  text-decoration: none;
}
/* -----recommend end----- */

footer {
  height: 80px;
  margin-top: 60px;
}
.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-copyright {
  font-family: PingFangSC-Regular;
  font-size: 16px;
  color: #131313;
}

.footer-law a {
  font-family: PingFangSC-Regular;
  font-size: 16px;
  color: #131313;
  text-align: right;
  text-decoration: none;
}
</style>

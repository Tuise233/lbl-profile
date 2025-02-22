<script setup lang="ts">

function scrollTo(section: string) {
    const element = document.getElementById(section);
    if(element) {
        element.scrollIntoView({ behavior: 'smooth' });
    }
}

function openLink(url: string) {
    window.open(url, '_blank');
}

function toggleTheme() {
    const theme = document.documentElement.getAttribute('data-theme');
    document.documentElement.setAttribute('data-theme', theme === 'dark' ? 'light' : 'dark');
}

</script>

<template>
    <div class="app-home">
        <div class="app-header">
            <h1>{{ '<Racoon419. />' }}</h1>
            <div class="app-container">
                <a @click="scrollTo('about')">关于</a>
                <a @click="scrollTo('skill')">技术栈</a>
                <a @click="scrollTo('experience')">项目经历</a>
                <a @click="scrollTo('contact')">联系我</a>
                <div class="app-split"></div>
                <font-awesome-icon :icon="['fas', 'moon']" @click="toggleTheme" />
            </div>
        </div>

        <div class="app-desc">
            <div class="app-text">
                <h1>Hi, I'm Racoon419.👋</h1>
                <p>大四软件工程在读，全栈偏前端个人开发者(Node.js与NestJS)，专注于WebApp、微信小程序等响应式界面开发。丰富的前端项目经验，在干中学习与思考，热爱编程如生命。</p>
                <div class="app-location">
                    <font-awesome-icon :icon="['fas', 'location-dot']" />
                    <span>ShangHai, China</span>
                </div>
                <div class="app-brands">
                    <font-awesome-icon @click="openLink('https://github.com/tuise233')" :icon="['fab', 'github']" />
                </div>
            </div>

            <div class="app-avatar">
                <img src="../../assets/avatar.jpg" />
                <div class="app-background"></div>
            </div>
        </div>

        <div class="app-about" id="about" ref="about">
            <span>About Me</span>
            <div class="app-container">
                <div class="app-avatar">
                    <img src="../../assets/avatar.jpg" />
                    <div class="app-background"></div>
                </div>

                <div class="app-col">
                    <span>对我好奇吗？这里有我的介绍：</span>
                    <p>我是一个充满激情的个人开发者，致力于从事全栈开发（Node.js与NestJS）。我非常热衷于WebApp的构建，用户体验、像素完美的设计以及编写清晰、可读、高性能的代码对我来说是非常重要的。</p>
                    <p>我于2020年正式开始我的前端开发之旅，从那时起，我作为一名大一学生不断成长与发展，接受新的挑战，并在干中学习与思考，学习最新的技术。现在，在我23岁时，开始我的WebApp构建之旅5年后，我正在使用NestJS、TypeScript、NestJS、Vue3、Pinia、Sass等现代技术构建Web应用程序。</p>
                    <p>我是一个设计与编程并肩热爱的人，源于我的大学专业建筑设计与软件工程。我会在构建Web项目的过程中不断思考并融入属于我自己的独立思想。</p>
                    <p>在最后，简要的介绍一下我自己：</p>
                    <div class="app-tip">
                        <span>• 丰富的项目经验</span>
                        <span>• 熟练掌握TypeScript、具备Java、C#、MySQL的基本知识</span>
                        <span>• 熟悉Vue、Sass、Pinia等前端框架与工具</span>
                        <span>• 熟悉NestJS、Express、TypeORM等后端框架与工具</span>
                        <span>• 熟悉Git版本控制，掌握团队协作开发流程</span>
                        <span>• 优秀的学习能力，热衷于新技术探索，能够快速适应并掌握新技能</span>
                    </div>
                    <p>如果你对于我感兴趣，请通过以下信息联系我！</p>
                </div>
            </div>
        </div>

        <div class="app-skill" id="skill" ref="skill">
            <span>Skills</span>
            <p>我擅长的技能、工具与技术：</p>

            <div class="app-wrapper">
                <div class="app-item">
                    <img src="../../assets/icon-javascript.png" />
                    <span>Javascript</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-typescript.png" />
                    <span>Typescript</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-nodejs.png" />
                    <span>Node.js</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-express.png" style="background-color: var(--color-500);" />
                    <span>Epress.js</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-nest.png" />
                    <span>Nest.js</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-sass.png" />
                    <span>Sass/Scss</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-git.png" />
                    <span>Git</span>
                </div>
                <div class="app-item">
                    <img src="../../assets/icon-figma.png" />
                    <span>Figma</span>
                </div>
            </div>
        </div>

        <div class="app-experience" id="experience" ref="experience">
            <span>Experience</span>
            <p>以下是我最近项目经历的总结：</p>

            <div class="app-wrapper">
                <div class="app-item">
                    <div class="app-row">
                        <span>alt:V服务器脚本开发</span>
                        <span>2020.12 ~ 至今</span>
                    </div>
                    <span>项目概述</span>
                    <p>该项目是基于某单机游戏的玩家社区，利用多人联机模组SDK开发了游戏服务器脚本，设计多个模块的构建，包括游戏客户端脚本、服务端脚本、管理后台以及客户端启动器。此外，我还主导了社区的宣传和推广工作，以提升项目用户覆盖与活跃度。</p>
                    <span>工作内容</span>
                    <p>• 游戏客户端脚本与服务端脚本开发：负责使用Node.js、Vue和TypeScript进行游戏客户端脚本和服务端脚本的开发，确保游戏功能稳定运行并优化性能。</p>
                    <p>• 管理后台开发：使用NestJS框架进行后端开发，前端采用Vue构建，设计并实现了高效的后台管理系统，支持实时数据监控与操作。</p>
                    <p>• 游戏启动器开发：基于Electron框架开发的游戏启动器，提供简洁的启动界面和流畅的用户体验。</p>
                    <p>• 社区推广：主导游戏的宣发工作，设计并实施了有效的宣传策略，推动社区用户增长与活跃度提升。</p>
                </div>
                
                <div class="app-item">
                    <div class="app-row">
                        <span>基于NestJS的冻存医疗信息管理系统</span>
                        <span>2024.10 ~ 2024.12</span>
                    </div>
                    <span>项目概述</span>
                    <p>本项目旨在为村医提供一套统一的医疗信息管理平台，用于记录和管理患者健康信息，便于村医在走访和治疗时快速获取患者病史，提高诊断效率，减少误诊和不必要的检查，从而提升农村医疗服务的质量与便利性。</p>
                    <span>工作内容</span>
                    <p>• 前端开发：使用Vue 3 + Sass构建用户友好的医疗信息管理界面，优化交互体验，提高村医的信息查询效率。</p>
                    <p>• 后端开发：基于NestJS + TypeORM开发高效的后端系统，实现患者数据的存储、查询及权限管理。</p>
                    <p>• 数据库设计：使用MySQL进行数据建模，设计合理的数据存储结构，确保医疗信息的安全性与可扩展性。</p>
                </div>

                <div class="app-item">
                    <div class="app-row">
                        <span>个人微信小程序</span>
                        <span>2023.10 ~ 2023.12</span>
                    </div>
                    <span>项目概述</span>
                    <p>该项目是一款原生微信小程序，集成个人记事本、TODO List、每日打卡等功能，旨在提供简洁高效的个人事务管理工具，方便用户记录日常任务与习惯养成。</p>
                    <span>工作内容</span>
                    <p>• 前端开发：使用原生微信小程序构建页面与交互，优化用户体验，实现高效便捷的任务管理功能。</p>
                    <p>• 后端开发：基于微信小程序云开发搭建后端，无需额外服务器，实现数据存储、用户身份管理及业务逻辑处理，提高开发效率与系统稳定性。</p>
                </div>
            </div>
        </div>

        <div class="app-contact" id="contact" ref="contact">
            <span>Contact Me</span>
            <p>最重要的是，如果您正在寻找开发人员、有疑问或只是单纯想联系我，欢迎打扰。</p>
            
            <div class="app-row">
                <font-awesome-icon :icon="['fas', 'envelope']" />
                <span>2039203690@qq.com</span>
            </div>

            <div class="app-row">
                <font-awesome-icon :icon="['fab', 'weixin']" />
                <span>tuise233</span>
            </div>

            <p>你同样可以通过以下方式联系到我！</p>

            <div class="app-brands">
                <font-awesome-icon @click="openLink('https://github.com/tuise233')" :icon="['fab', 'github']" />
            </div>
        </div>

        <div class="app-footer">
            <font-awesome-icon :icon="['fas', 'copyright']" />
            <span>2025 | Designed and coded with ❤ by Racoon419.</span>
        </div>
    </div>
</template>

<style src="./style.scss" scoped />
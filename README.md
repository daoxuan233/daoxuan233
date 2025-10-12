<!-- Neumorphism & Frosted Glass Design System -->
<style>
:root {
  /* 主色调配色体系 */
  --primary-klein-blue: #002FA7;
  --primary-green-glaze: #517B4D;
  --secondary-light-blue: #4A90E2;
  --secondary-sage-green: #7BA05B;
  --accent-gold: #FFD700;
  --accent-silver: #C0C0C0;

  /* Neumorphism 配色 */
  --neuro-bg: #f0f0f3;
  --neuro-shadow-dark: #d1d1d4;
  --neuro-shadow-light: #ffffff;
  --neuro-inset-dark: #cbcbce;
  --neuro-inset-light: #ffffff;

  /* Frosted Glass 配色 */
  --glass-bg: rgba(255, 255, 255, 0.25);
  --glass-border: rgba(255, 255, 255, 0.18);
  --glass-backdrop: blur(20px);
}

.neuro-card {
  background: var(--neuro-bg);
  border-radius: 20px;
  box-shadow: 
    8px 8px 16px var(--neuro-shadow-dark),
    -8px -8px 16px var(--neuro-shadow-light);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.neuro-card:hover {
  box-shadow: 
    12px 12px 24px var(--neuro-shadow-dark),
    -12px -12px 24px var(--neuro-shadow-light);
  transform: translateY(-2px);
}

.neuro-inset {
  background: var(--neuro-bg);
  border-radius: 15px;
  box-shadow: 
    inset 4px 4px 8px var(--neuro-inset-dark),
    inset -4px -4px 8px var(--neuro-inset-light);
}

.glass-card {
  background: var(--glass-bg);
  backdrop-filter: var(--glass-backdrop);
  -webkit-backdrop-filter: var(--glass-backdrop);
  border: 1px solid var(--glass-border);
  border-radius: 20px;
  box-shadow: 0 8px 32px rgba(0, 47, 167, 0.15);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.glass-card:hover {
  background: rgba(255, 255, 255, 0.35);
  box-shadow: 0 12px 48px rgba(0, 47, 167, 0.25);
  transform: translateY(-4px) scale(1.02);
}

.gradient-text {
  background: linear-gradient(135deg, var(--primary-klein-blue), var(--primary-green-glaze));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.floating-animation {
  animation: floating 3s ease-in-out infinite;
}

@keyframes floating {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.pulse-glow {
  animation: pulse-glow 2s ease-in-out infinite alternate;
}

@keyframes pulse-glow {
  from { box-shadow: 0 0 20px rgba(0, 47, 167, 0.3); }
  to { box-shadow: 0 0 30px rgba(81, 123, 77, 0.5); }
}

/* 响应式设计 */
@media (max-width: 768px) {
  .neuro-card, .glass-card {
    margin: 10px;
    padding: 15px;
  }
}

@media (max-width: 480px) {
  .neuro-card, .glass-card {
    margin: 5px;
    padding: 12px;
    border-radius: 15px;
  }
}
</style>

<div align="center" style="background: linear-gradient(135deg, #f0f0f3 0%, #e8e8eb 100%); min-height: 100vh; padding: 20px 0;">

<!-- 主标题区域 - Neumorphism风格 -->
<div class="neuro-card floating-animation" style="max-width: 800px; margin: 40px auto; padding: 40px;">
  <h1 class="gradient-text" style="font-size: 3.5em; margin: 0; font-weight: 700; letter-spacing: -2px;">
    👋 Hey there! I'm daoxuan233
  </h1>

  <div class="neuro-inset" style="margin: 30px 0; padding: 25px;">
    <h3 style="color: var(--primary-klein-blue); margin: 0; font-size: 1.4em; font-weight: 500;">
      🚀 Full Stack Developer | 💡 Tech Enthusiast | 🌟 Open Source Contributor
    </h3>
  </div>

  <!-- 统计徽章 - Frosted Glass风格 -->
  <div style="display: flex; justify-content: center; align-items: center; gap: 20px; margin: 35px 0; flex-wrap: wrap;">
    <div class="glass-card pulse-glow" style="padding: 15px 25px;">
      <img src="https://profile-counter.glitch.me/daoxuan233/count.svg" alt="访客计数" style="border-radius: 8px;"/>
    </div>
    <div class="glass-card pulse-glow" style="padding: 10px;">
      <img src="https://img.shields.io/github/followers/daoxuan233?style=for-the-badge&logo=github&logoColor=white&color=002FA7" alt="GitHub followers"/>
    </div>
    <div class="glass-card pulse-glow" style="padding: 10px;">
      <img src="https://img.shields.io/github/stars/daoxuan233?style=for-the-badge&logo=github&logoColor=white&color=517B4D" alt="GitHub stars"/>
    </div>
  </div>
</div>

<!-- GitHub 统计数据 - 混合风格 -->
<div style="max-width: 1200px; margin: 60px auto;">
  <h2 class="gradient-text" style="font-size: 2.5em; margin-bottom: 40px; text-align: center;">📊 GitHub 统计数据</h2>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(450px, 1fr)); gap: 30px; padding: 0 20px;">

    <!-- GitHub Stats Card -->
    <div class="neuro-card" style="padding: 30px; position: relative; overflow: hidden;">
      <div style="position: absolute; top: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, var(--primary-klein-blue), var(--primary-green-glaze));"></div>
      <a href="https://github.com/daoxuan233" style="text-decoration: none;">
        <img src="https://github-readme-stats-ouuan.vercel.app/api?username=daoxuan233&theme=default&show_icons=true&hide_border=true&bg_color=f0f0f3&title_color=002FA7&text_color=517B4D&icon_color=FFD700" alt="GitHub Stats" style="width: 100%; border-radius: 15px;"/>
      </a>
    </div>
    
    <!-- Top Languages Card -->
    <div class="neuro-card" style="padding: 30px; position: relative; overflow: hidden;">
      <div style="position: absolute; top: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, var(--primary-green-glaze), var(--primary-klein-blue));"></div>
      <a href="https://github.com/daoxuan233" style="text-decoration: none;">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=daoxuan233&layout=compact&theme=default&hide_border=true&bg_color=f0f0f3&title_color=002FA7&text_color=517B4D&langs_count=8&hide=smali" alt="Top Languages" style="width: 100%; border-radius: 15px;"/>
      </a>
    </div>

  </div>
</div>

<!-- 精选项目 - Frosted Glass风格 -->
<div style="max-width: 1200px; margin: 80px auto;">
  <h2 class="gradient-text" style="font-size: 2.5em; margin-bottom: 50px; text-align: center;">🌟 精选项目</h2>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(400px, 1fr)); gap: 35px; padding: 0 20px;">

    <!-- 惠农商城项目 -->
    <div class="glass-card" style="padding: 35px; background: linear-gradient(135deg, rgba(0, 47, 167, 0.1), rgba(81, 123, 77, 0.1));">
      <div style="display: flex; align-items: center; margin-bottom: 20px;">
        <span style="font-size: 2em; margin-right: 15px;">🛒</span>
        <h4 style="color: var(--primary-klein-blue); margin: 0; font-size: 1.4em; font-weight: 600;">惠农商城练习</h4>
      </div>
      <a href="https://github.com/daoxuan233/shopping_mall" style="text-decoration: none;">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=daoxuan233&repo=shopping_mall&theme=default&hide_border=true&bg_color=f0f0f3&title_color=002FA7&text_color=517B4D&icon_color=FFD700" alt="Shopping Mall" style="width: 100%; border-radius: 15px; transition: transform 0.3s ease;"/>
      </a>
    </div>
    
    <!-- FutureBack_end项目 -->
    <div class="glass-card" style="padding: 35px; background: linear-gradient(135deg, rgba(81, 123, 77, 0.1), rgba(0, 47, 167, 0.1));">
      <div style="display: flex; align-items: center; margin-bottom: 20px;">
        <span style="font-size: 2em; margin-right: 15px;">🚀</span>
        <h4 style="color: var(--primary-green-glaze); margin: 0; font-size: 1.4em; font-weight: 600;">FutureBack_end</h4>
      </div>
      <a href="https://github.com/Futureluxe/FutureBack_end" style="text-decoration: none;">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=Futureluxe&repo=FutureBack_end&theme=default&hide_border=true&bg_color=f0f0f3&title_color=002FA7&text_color=517B4D&icon_color=FFD700" alt="FutureBack_end" style="width: 100%; border-radius: 15px; transition: transform 0.3s ease;"/>
      </a>
    </div>

  </div>
</div>

<!-- GitHub 贡献动态 - Neumorphism风格 -->
<div style="max-width: 1000px; margin: 80px auto;">
  <h2 class="gradient-text" style="font-size: 2.5em; margin-bottom: 40px; text-align: center;">🐍 GitHub 贡献动态</h2>

  <div class="neuro-card" style="padding: 40px; background: linear-gradient(135deg, #f0f0f3 0%, #e8e8eb 100%);">
    <div class="neuro-inset" style="padding: 30px; text-align: center;">
      <h3 style="color: var(--primary-klein-blue); margin-bottom: 25px; font-size: 1.3em;">📈 我的 GitHub 活动轨迹</h3>
      <img src="https://raw.githubusercontent.com/daoxuan233/daoxuan233/main/assets/github-contribution-grid-snake.gif" alt="GitHub Snake Animation" style="width: 100%; max-width: 800px; border-radius: 20px; box-shadow: 0 8px 32px rgba(0, 47, 167, 0.2);"/>
    </div>
  </div>
</div>

<!-- 3D 贡献图表 - Frosted Glass风格 -->
<div style="max-width: 1000px; margin: 80px auto;">
  <h2 class="gradient-text" style="font-size: 2.5em; margin-bottom: 40px; text-align: center;">🎨 3D 贡献图表</h2>

  <div class="glass-card" style="padding: 40px; background: linear-gradient(135deg, rgba(81, 123, 77, 0.15), rgba(0, 47, 167, 0.15));">
    <h3 style="color: var(--primary-green-glaze); margin-bottom: 25px; text-align: center; font-size: 1.3em;">🌟 3D 贡献可视化</h3>
    <div style="text-align: center;">
      <img src="./profile-3d-contrib/profile-green-animate.svg" alt="3D Contribution Graph" style="width: 100%; max-width: 900px; border-radius: 20px; box-shadow: 0 8px 32px rgba(81, 123, 77, 0.3);"/>
    </div>
  </div>
</div>

<!-- 联系方式 - 混合风格 -->
<div style="max-width: 800px; margin: 80px auto 40px;">
  <h2 class="gradient-text" style="font-size: 2.5em; margin-bottom: 40px; text-align: center;">🤝 联系我</h2>

  <div class="neuro-card" style="padding: 40px; background: linear-gradient(135deg, #f0f0f3 0%, #e8e8eb 100%);">
    <h3 style="color: var(--primary-klein-blue); margin-bottom: 30px; text-align: center; font-size: 1.4em;">💬 让我们一起创造精彩！</h3>

    <div style="display: flex; justify-content: center; gap: 25px; flex-wrap: wrap;">
      <a href="https://github.com/daoxuan233" style="text-decoration: none;" class="glass-card" style="padding: 15px 25px; display: inline-block;">
        <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white&color=002FA7" alt="GitHub" style="border-radius: 8px;"/>
      </a>
      <div class="glass-card" style="padding: 15px 25px; display: inline-block;">
        <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge&color=517B4D" alt="Status" style="border-radius: 8px;"/>
      </div>
      <div class="glass-card" style="padding: 15px 25px; display: inline-block;">
        <img src="https://img.shields.io/badge/Focus-Full%20Stack-blue?style=for-the-badge&color=002FA7" alt="Focus" style="border-radius: 8px;"/>
      </div>
    </div>
  </div>
</div>

<!-- 页脚波浪 -->
<div style="text-align: center; margin-top: 60px;">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,2,5,30&height=120&section=footer&text=Thanks%20for%20visiting!&fontSize=18&fontColor=002FA7&animation=fadeIn" alt="Footer Wave"/>
</div>

</div>
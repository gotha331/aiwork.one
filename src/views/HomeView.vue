<template>
  <main class="home-page">
    <section class="hero">
      <p class="eyebrow">Vue 3 Starter</p>
      <h1>AI Work 项目首页</h1>
      <p class="intro">
        一个保留路由、状态管理和测试基础设施的轻量前端起点，适合继续扩展真实业务页面。
      </p>
      <div class="actions">
        <RouterLink class="primary-action" to="/about">查看项目说明</RouterLink>
        <a href="https://vite.dev/guide/" target="_blank" rel="noopener">Vite 文档</a>
      </div>
    </section>

    <section class="highlights" aria-label="项目能力">
      <article>
        <h2>清晰结构</h2>
        <p>页面、组件、路由和状态管理已分层，后续功能可以按目录自然扩展。</p>
      </article>
      <article>
        <h2>现代工具链</h2>
        <p>基于 Vite、TypeScript、Vitest 和 Playwright，覆盖开发、构建和验证流程。</p>
      </article>
      <article>
        <h2>低风险起步</h2>
        <p>当前改动范围集中在展示层，没有引入额外依赖，也没有改变项目架构。</p>
      </article>
    </section>
  </main>
</template>

<style scoped>
.home-page {
  padding: 4rem 0 5rem;
}

.hero {
  max-width: 760px;
}

.eyebrow {
  margin-bottom: 0.75rem;
  color: #0f766e;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0;
  text-transform: uppercase;
}

h1 {
  max-width: 720px;
  color: var(--color-heading);
  font-size: clamp(2.4rem, 6vw, 4.25rem);
  font-weight: 800;
  line-height: 1.05;
}

.intro {
  max-width: 640px;
  margin-top: 1.25rem;
  color: var(--color-text);
  font-size: 1.15rem;
}

.actions {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.85rem;
  margin-top: 2rem;
}

.actions a {
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: 0.75rem 1rem;
  color: var(--color-heading);
  font-weight: 700;
}

.actions .primary-action {
  border-color: #0f766e;
  background: #0f766e;
  color: white;
}

.actions a:hover {
  background: var(--color-background-soft);
}

.actions .primary-action:hover {
  background: #115e59;
}

.highlights {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 1rem;
  margin-top: 4rem;
}

article {
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: 1.25rem;
  background: var(--color-background-soft);
}

h2 {
  color: var(--color-heading);
  font-size: 1.05rem;
  font-weight: 700;
}

article p {
  margin-top: 0.6rem;
}

@media (max-width: 760px) {
  .home-page {
    padding: 2.75rem 0 4rem;
  }

  .highlights {
    grid-template-columns: 1fr;
  }
}
</style>

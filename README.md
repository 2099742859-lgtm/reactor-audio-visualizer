# Reactor Audio Visualizer

以切尔诺贝利反应堆堆芯的控制棒阵列为视觉原型的实时音频可视化实验。

网页使用 Web Audio API 在浏览器本机分析音频，将不同频段的能量映射为 709 根控制棒的升降运动。支持演示信号、本地音频文件、麦克风输入、视角拖动与缩放，以及灵敏度、平滑度和音量调节。

## Run locally

```bash
python3 -m http.server 4173 --directory dist
```

Then open <http://localhost:4173>.

## Deploy (GitHub Pages)

站点是纯静态的（`dist/` 目录），已附带 GitHub Actions 工作流自动部署。

1. 推送 `main` 分支到 GitHub。
2. 打开仓库 **Settings → Pages**。
3. 把 **Source** 设为 **GitHub Actions**。
4. 推送后工作流会自动运行，站点发布在
   `https://<用户名>.github.io/reactor-audio-visualizer/`。

工作流定义见 [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)。

## Notes

This is an audiovisual interaction experiment. It is not a physical simulation of a reactor, and audio is processed locally in the browser.

## License

MIT. See [LICENSE](LICENSE).

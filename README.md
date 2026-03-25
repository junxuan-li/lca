# Large-scale Codec Avatars — Project Page

Project page for the CVPR 2026 paper:

**Large-scale Codec Avatars: The Unreasonable Effectiveness of Large-scale Avatar Pretraining**

Junxuan Li*, Rawal Khirodkar*, Egor Zakharov, Jihyun Lee, Zhaoen Su, Yuan Dong, Julieta Martinez, Kai Li, Qingyang Tan, Takaaki Shiratori, Matthew Hu, Peihong Guo, Xuhua Huang, Zhongshi Jiang, Lingchen Yang, Ariyan Zarei, Marco Pesavento, Yichen Xu, Chengan He, He Wen, Giljoo Nam, Teng Deng, Wyatt Borsos, Anjali Thakrar, Jean-Charles Bazin, Rinat Abdrashitov, Carsten Stoll, Ginés Hidalgo, James Booth, Lucy Wang, Xiaowen Ma, Yu Rong, Sairanjith Thalanki, Chen Cao, Christian Häne, Abhishek Kar, Sofien Bouaziz, Jason Saragih, Yaser Sheikh, Shunsuke Saito†

*Core contributors  †Project lead

Codec Avatars Lab, Meta

## Local Preview

Open `index.html` in a browser, or run a local server:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Structure

```
index.html              Main page (single-file, no build step)
video.mp4               Supplementary video
static/
  css/style.css         Stylesheet
  images/               Figure PNGs (converted from paper PDFs at 200 DPI)
  videos/               Avatar result video clips (01-15.mp4)
```

## Deployment

Before deploying, replace the symlinks in `static/videos/` with actual files:

```bash
# Convert symlinks to real files
cd static/videos
for f in *.mp4; do
  cp --remove-destination "$(readlink -f "$f")" "$f"
done
```

Update the placeholder `href="#"` links in `index.html` for Paper and arXiv buttons once URLs are available.

## Acknowledgments

Website template inspired by [Nerfies](https://nerfies.github.io).

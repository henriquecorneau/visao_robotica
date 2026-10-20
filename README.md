# visao_robotica
Repositório utilizado na disciplina da pós graduação em Mecatrônica, visão robótica, em que envolve o estudo aprofundado do opencv.

## Curso de Visão Computacional (em inglês)

O conteúdo deste repositório, junto com os TPs de *Traitement d'Images* do INSA Rouen, foi
reorganizado em um curso completo de visão computacional, com teoria, implementações do zero
comparadas ao OpenCV e um script executável por lição:

**https://henriquecorneau.github.io/my-portfolio/course/**

| Material deste repositório | Lição do curso |
|---|---|
| aula 01 | [01 – Images are arrays](https://henriquecorneau.github.io/my-portfolio/course/01-images-as-arrays.html) |
| atividade 01 | [02 – Sampling, quantization and interpolation](https://henriquecorneau.github.io/my-portfolio/course/02-sampling-quantization.html) |
| aulas 03, 04, 06, 07 | [03 – Geometric transforms](https://henriquecorneau.github.io/my-portfolio/course/03-geometric-transforms.html) |
| aula 06 | [04 – Histograms, point operations and LUTs](https://henriquecorneau.github.io/my-portfolio/course/04-histograms-lut.html) |
| aulas 02, 07, atividade 03 | [05 – Noise and spatial filtering](https://henriquecorneau.github.io/my-portfolio/course/05-noise-filtering.html) |
| aula 08 | [06 – Edge detection](https://henriquecorneau.github.io/my-portfolio/course/06-edges.html) |
| aula 09, atividade 04 | [07 – The Canny edge detector](https://henriquecorneau.github.io/my-portfolio/course/07-canny.html) |
| aula 10, atividade 04 | [08 – The Hough transform](https://henriquecorneau.github.io/my-portfolio/course/08-hough.html) |
| aula 06 | [10 – Colour spaces](https://henriquecorneau.github.io/my-portfolio/course/10-color.html) |
| atividade 05 | [11 – Corners and tracking](https://henriquecorneau.github.io/my-portfolio/course/11-corners-tracking.html) |
| atividade 06 | [12 – FAST, ORB and SIFT](https://henriquecorneau.github.io/my-portfolio/course/12-keypoints-orb-sift.html), [13 – Homography and RANSAC](https://henriquecorneau.github.io/my-portfolio/course/13-homography-ransac.html) |
| atividade 02 | [14 – Camera model and calibration](https://henriquecorneau.github.io/my-portfolio/course/14-camera-calibration.html) |
| atividades 08, 09 | [15 – Stereo vision](https://henriquecorneau.github.io/my-portfolio/course/15-stereo-vision.html) |
| atividade 07 | [16 – Structure from Motion](https://henriquecorneau.github.io/my-portfolio/course/16-structure-from-motion.html) |

Algumas correções feitas no curso em relação às atividades originais:

- **Atividade 07 (SfM):** o `intrinsics.yml` usado é a calibração das imagens de exemplo do OpenCV
  (f = 535), não a do KITTI (f = 718,9); `decomposeEssentialMat` sozinho não escolhe a solução
  física (use `recoverPose`); e o pareamento 2D–3D do PnP precisa de rastreamento explícito dos pontos.
- **Atividades 08/09 (estéreo):** a nuvem de pontos deve ser reprojetada a partir da disparidade em
  float, não do mapa de disparidade colorido.
- **Atividade 04 (Canny):** os argumentos do `arctan2` estavam invertidos e a histerese precisa
  propagar as bordas fortes até convergir.

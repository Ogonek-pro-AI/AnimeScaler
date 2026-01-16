<!DOCTYPE html>
<html>
<body>
    <div align="center">    
        <img src="https://github.com/Djdefrag/AnimeScaler/blob/main/Assets/logo.png" width="175"> 
        <br><br> AnimeScaler - image/video AI upscaler app <br><br>
        <a href="https://jangystudio.itch.io/qualityscaler">
            <button>
                <img src="https://static.itch.io/images/badge-color.svg" width="225" height="70">
            </button>     
        </a>
        <a href="https://store.steampowered.com/app/2463110/AnimeScaler/">
            <button>
                 <img src="https://images.squarespace-cdn.com/content/v1/5b45fae8b98a78d9d80b9c5c/1531959264455-E7B8MJ3VMPX0593VGCZG/button-steam-available-fixed-2.png" width="250" height="70">
            </button>                 
        </a>
    </div>
    <br>
    <div align="center">
      <img src="Assets/logo.png" alt="AnimeScaler logo" width="160" />
    </div>

    # AnimeScaler — AI image & video upscaler

    AnimeScaler — лёгкий в использовании инструмент на Python для повышения разрешения, подавления шумов и улучшения качества изображений и видеороликов с помощью ONNX-моделей. README подготовлен на русском; проект совместим с Windows и может запускаться локально без доступа в интернет.

    **ому подходит:** продвинутые пользователи и разработчики, которым нужна автономная утилита для пакетного или интерактивного улучшения контента.

    **лючевые моменты:** автономная работа, поддержка ONNX-моделей (папка `AI-onnx/`), локальное ускорение через DirectML/CPU, простая GUI-оболочка.

    **раткий план:** установка → подготовка моделей → запуск `AnimeScaler.py`.

    **ыстрый старт**

    - Скопируйте репозиторий на машину и поместите модели в папку `AI-onnx/`.
    - оместите `ffmpeg.exe` (если планируется работа с видео) в папку `Assets/`.
    - становите зависимости и запустите скрипт:

    ```powershell
    python -m pip install -r requirements.txt
    python AnimeScaler.py
    ```

    сли вы используете PowerShell, команды идентичны; для других оболочек замените `python` на соответствующий интерпретатор.

    то важно: в этом репозитории уже есть несколько предобученных ONNX-моделей в `AI-onnx/`. ти файлы используются как движок масштабирования — см. раздел «одели».

    ## становка и подготовка

    1. бедитесь, что на компьютере установлен Python 3.10–3.11 (в примерах использовался Python 3.11).
    2. лонируйте или скачайте репозиторий и откройте папку проекта.
    3. становите зависимости:

    ```bash
    python -m pip install -r requirements.txt
    ```

    4. Скачайте ONNX-модели и поместите их в `AI-onnx/` (в репозитории уже лежат несколько моделей — проверьте содержимое).
    5. ля работы с видео положите `ffmpeg.exe` в `Assets/` (или убедитесь, что ffmpeg доступен в PATH).

    ## апуск

    GUI

    ```bash
    python AnimeScaler.py
    ```

    омандный режим (если доступен в будущем) — следите за подсказками в интерфейсе или в обновлённых инструкциях.

    ##  моделях (папка `AI-onnx/`)

     каталоге `AI-onnx/` находятся файлы моделей ONNX. римеры из репозитория:

    - `BSRGANx2_fp16.onnx` — BSRGAN x2
    - `BSRGANx4_fp16.onnx` — BSRGAN x4
    - `RealESR_Animex4_fp16.onnx` — Real-ESRGAN (аниме-ориентированный)
    - `RealESR_Gx4_fp16.onnx` — ещё одна конфигурация Real-ESRGAN
    - `RealESRGANx4_fp16.onnx` — Real-ESRGAN x4

    аменяйте или добавляйте модели по мере необходимости — интерфейс позволяет выбирать модель для обработки.

    ## Требования

    - перационная система: Windows 10/11 (проект ориентирован на Windows GUI)
    - Python 3.10–3.11
    - : рекомендуемые >= 8 
    - ля аппаратного ускорения: DirectX12-совместимая видеокарта (если используется DirectML)

    оддерживаемые форматы (взято из текущего кода):

    - зображения: jpg, png, tif, bmp, webp, heic
    - идео: mp4, webm, mkv, flv, gif, avi, mov, mpg, qt, 3gp

    ## Содержание репозитория

    - `AnimeScaler.py` — основной исполняемый скрипт (GUI и/или запуск)
    - `requirements.txt` — зависимости Python
    - `AI-onnx/` — папка с ONNX-моделями
    - `Assets/` — логотип и вспомогательные файлы (разместите `ffmpeg.exe` сюда при необходимости)

    ## римеры использования

    1) ыстрый запуск GUI (Windows):

    ```powershell
    python AnimeScaler.py
    ```

    2) одготовка: убедитесь, что нужная модель находится в `AI-onnx/`, исходный файл в удобной папке — выбирайте в интерфейсе и нажимайте «Start».

    ## ицензия

    ицензия и правовой статус проекта сохранены в файлах `LICENSE` и `LICENSE.txt`. ставляем текущую лицензию без изменений.

    ## онтакты

    сли нужно добавить информацию об авторе или способ связи — пришлите желаемый текст, добавлю в README.

    ---

#### Videos

![original](https://user-images.githubusercontent.com/32263112/209139620-bdd028f8-d5fc-40de-8f3d-6b80a14f8aab.gif)

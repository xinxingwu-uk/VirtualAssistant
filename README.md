# Talking Slide Avatars for Class Lectures  
**OpenVoice + Ditto-TalkingHead Pipeline**

This project demonstrates how to create **AI-generated talking images** for course slides by combining **OpenVoice** (speech generation) and **Ditto-TalkingHead** (audio-driven facial animation).  
The final outputs are short speaking images or videos that can be embedded directly into **lecture slides** in class - <button onclick="window.open('https://xinxingwu-uk.github.io/projects/demo3/slides.html', '_blank')">
  Demo
</button>


<button onclick="openDemo()">Demo</button>



---

## ✨ Project Overview

This workflow allows instructors to turn **static images** into **speaking avatars** that narrate slide content such as weekly goals, assignment explanations, and key concepts.  
It is especially useful for **online, hybrid, and asynchronous teaching**.

---

## 🧠 Workflow

Text Script  
→ OpenVoice (Text → Speech)  
→ Audio (.wav)  
→ Ditto-TalkingHead (Audio + Image)  
→ Talking Image / Video  
→ Lecture Slides (PPT / PDF / HTML)

---

## 🛠 Tools Used

### OpenVoice (Speech Generation)
- Converts lecture text into natural-sounding speech
- Output format: `.wav`

### Ditto-TalkingHead (Talking Image Generation)
- Animates a static image using speech audio
- Produces a lip-synced talking image or video

---

## 📂 Recommended Project Structure

```
project/
├── scripts/
│   └── lecture_text.txt
├── audio/
│   └── lecture.wav
├── images/
│   └── avatar.jpg
├── output/
│   └── talking_avatar.mp4
├── slides/
│   └── week1_slides.pptx
└── README.md
```

---

## ▶️ Step-by-Step Usage

### Step 1: Write the Lecture Script

Example:
```
This week, we have four assignments.
Assignment one is an introduction of yourself.
Assignment two is a one-page proposal.
Assignment three focuses on contracts.
Assignment four includes hourly logs and a journal entry.
```

---

### Step 2: Generate Audio with OpenVoice

```
python openvoice_infer.py --text scripts/lecture_text.txt --output audio/lecture.wav
```

---

### Step 3: Generate Talking Image with Ditto-TalkingHead

```
python inference.py --audio audio/lecture.wav --image images/avatar.jpg --output output/talking_avatar.mp4
```

---

### Step 4: Use in Slides

Insert the generated video into:
- PowerPoint
- Google Slides
- PDF
- HTML course pages

---

## 🎓 Educational Benefits

- Improves student engagement
- Makes slides more interactive
- Reduces repetitive narration work
- Reusable across semesters

---

## ⚠️ Best Practices

- Keep audio clips short (10–30 seconds)
- Use clear, front-facing images
- Speak at a moderate pace

---

## 📜 License & Usage Notes

This project is for **educational use**.  
Please follow the licenses of OpenVoice and Ditto-TalkingHead.  
Do not use real people’s images without permission.

---

## 🙌 Acknowledgements

- OpenVoice — Text-to-speech
- Ditto-TalkingHead — Talking head animation

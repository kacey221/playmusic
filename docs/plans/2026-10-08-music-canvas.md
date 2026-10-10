# 音乐画布 Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Build a browser-only music canvas where photo pixels, hand-drawn lines, and tap points can each become playable music.

**Architecture:** A single canvas stores background photo, strokes, and beat points. Web Audio API synthesizes notes and percussion from normalized canvas events; an animation loop scans left-to-right during playback.

**Tech Stack:** HTML, CSS, vanilla JavaScript, Canvas 2D, Web Audio API.

---

### Task 1: Build the visual shell
- Create `index.html` with sidebar controls, canvas workspace, and transport bar.
- Create `styles.css` with warm dark studio styling, responsive layout, and visible state chips.

### Task 2: Implement canvas authoring
- Create `app.js` state for photo, strokes, and beats.
- Handle pointer drawing, tap placement, resize, photo upload, clear, and redraw.
- Render photo, strokes, beats, scan line, and helper grid.

### Task 3: Implement photo-to-music and audio playback
- Analyze uploaded photo strips into melody notes and percussion events.
- Map strokes to notes and beat points to drum hits.
- Use Web Audio oscillators and noise bursts for synthesized playback with play/pause/reset.

### Task 4: Verify
- Run a local static server and exercise upload, draw, tap, play/pause, redraw, and clear flows in browser.

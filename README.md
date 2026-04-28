<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="English Pro">
<meta name="theme-color" content="#0F172A">
<title>English Pro - Master English</title>
<link rel="apple-touch-icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 180 180'%3E%3Cdefs%3E%3ClinearGradient id='g' x1='0%25' y1='0%25' x2='100%25' y2='100%25'%3E%3Cstop offset='0%25' stop-color='%236366F1'/%3E%3Cstop offset='100%25' stop-color='%23EC4899'/%3E%3C/linearGradient%3E%3C/defs%3E%3Crect width='180' height='180' rx='40' fill='url(%23g)'/%3E%3Ctext x='50%25' y='50%25' text-anchor='middle' dy='.35em' font-family='-apple-system' font-weight='800' font-size='100' fill='white'%3EE%3C/text%3E%3C/svg%3E">
<style>
* { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

:root {
  --bg-primary: #0F172A;
  --bg-secondary: #1E293B;
  --bg-card: #1E293B;
  --bg-elevated: #334155;
  --text-primary: #F8FAFC;
  --text-secondary: #94A3B8;
  --text-tertiary: #64748B;
  --accent-primary: #6366F1;
  --accent-secondary: #EC4899;
  --accent-success: #10B981;
  --accent-warning: #F59E0B;
  --accent-danger: #EF4444;
  --gradient-primary: linear-gradient(135deg, #6366F1 0%, #EC4899 100%);
  --gradient-success: linear-gradient(135deg, #10B981 0%, #34D399 100%);
  --gradient-warning: linear-gradient(135deg, #F59E0B 0%, #FB923C 100%);
  --gradient-danger: linear-gradient(135deg, #EF4444 0%, #F87171 100%);
  --gradient-cool: linear-gradient(135deg, #3B82F6 0%, #06B6D4 100%);
  --border: rgba(255, 255, 255, 0.08);
  --shadow: 0 10px 40px rgba(0, 0, 0, 0.4);
  --safe-top: env(safe-area-inset-top);
  --safe-bottom: env(safe-area-inset-bottom);
}

@media (prefers-color-scheme: light) {
  :root {
    --bg-primary: #F8FAFC;
    --bg-secondary: #FFFFFF;
    --bg-card: #FFFFFF;
    --bg-elevated: #F1F5F9;
    --text-primary: #0F172A;
    --text-secondary: #475569;
    --text-tertiary: #94A3B8;
    --border: rgba(0, 0, 0, 0.08);
    --shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
  }
}

html, body {
  font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'SF Pro Text', sans-serif;
  background: var(--bg-primary);
  color: var(--text-primary);
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
  overscroll-behavior-y: none;
  user-select: none;
  -webkit-user-select: none;
  font-size: 16px;
  line-height: 1.5;
}

input, textarea {
  user-select: text;
  -webkit-user-select: text;
  font-family: inherit;
}

button {
  font-family: inherit;
  border: none;
  cursor: pointer;
  background: none;
  color: inherit;
}

/* App Container */
.app {
  min-height: 100vh;
  padding-top: var(--safe-top);
  padding-bottom: calc(var(--safe-bottom) + 80px);
  position: relative;
  max-width: 500px;
  margin: 0 auto;
}

/* Top Bar */
.top-bar {
  position: sticky;
  top: 0;
  background: var(--bg-primary);
  z-index: 100;
  padding: 12px 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  background: rgba(15, 23, 42, 0.85);
  border-bottom: 1px solid var(--border);
}

@media (prefers-color-scheme: light) {
  .top-bar { background: rgba(248, 250, 252, 0.85); }
}

.app-logo {
  display: flex;
  align-items: center;
  gap: 10px;
}

.app-logo-icon {
  width: 36px;
  height: 36px;
  border-radius: 10px;
  background: var(--gradient-primary);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 18px;
  color: white;
  box-shadow: 0 4px 12px rgba(99, 102, 241, 0.4);
}

.app-logo-text {
  font-weight: 700;
  font-size: 17px;
}

.top-stats {
  display: flex;
  gap: 8px;
}

.top-stat {
  background: var(--bg-elevated);
  padding: 6px 12px;
  border-radius: 100px;
  font-size: 13px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 4px;
}

.top-stat.streak { color: #FB923C; }
.top-stat.xp { color: #6366F1; }

/* Main Content */
.main-content {
  padding: 16px 20px;
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Hero Card */
.hero-card {
  background: var(--gradient-primary);
  border-radius: 24px;
  padding: 24px;
  color: white;
  position: relative;
  overflow: hidden;
  margin-bottom: 20px;
}

.hero-card::before {
  content: '';
  position: absolute;
  top: -100px;
  right: -100px;
  width: 250px;
  height: 250px;
  background: rgba(255,255,255,0.1);
  border-radius: 50%;
  pointer-events: none;
}

.hero-greeting {
  font-size: 14px;
  opacity: 0.9;
  margin-bottom: 4px;
  position: relative;
}

.hero-title {
  font-size: 24px;
  font-weight: 800;
  margin-bottom: 16px;
  position: relative;
}

.hero-progress {
  background: rgba(255,255,255,0.2);
  border-radius: 100px;
  height: 8px;
  overflow: hidden;
  margin-bottom: 8px;
  position: relative;
}

.hero-progress-fill {
  height: 100%;
  background: white;
  border-radius: 100px;
  transition: width 0.5s ease;
}

.hero-progress-text {
  font-size: 13px;
  opacity: 0.95;
  position: relative;
}

/* Section */
.section {
  margin-bottom: 24px;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 12px;
  padding: 0 4px;
}

.section-title {
  font-size: 18px;
  font-weight: 700;
}

.section-action {
  font-size: 13px;
  color: var(--accent-primary);
  font-weight: 600;
}

/* Quick Actions Grid */
.quick-actions {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  margin-bottom: 20px;
}

.quick-action {
  background: var(--bg-card);
  border-radius: 18px;
  padding: 16px;
  border: 1px solid var(--border);
  transition: transform 0.2s;
  text-align: left;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 8px;
  position: relative;
  overflow: hidden;
}

.quick-action:active { transform: scale(0.97); }

.quick-action-icon {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  margin-bottom: 4px;
}

.quick-action-title {
  font-weight: 700;
  font-size: 15px;
  color: var(--text-primary);
}

.quick-action-desc {
  font-size: 12px;
  color: var(--text-secondary);
}

/* Stats Cards */
.stats-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
  margin-bottom: 20px;
}

.stat-mini {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 12px;
  text-align: center;
}

.stat-mini-value {
  font-size: 20px;
  font-weight: 800;
  margin-bottom: 2px;
}

.stat-mini-label {
  font-size: 11px;
  color: var(--text-secondary);
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

/* Lesson Card */
.lesson-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 16px;
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  gap: 14px;
  transition: transform 0.2s;
  position: relative;
  overflow: hidden;
}

.lesson-card:active { transform: scale(0.98); }

.lesson-card.locked { opacity: 0.5; }
.lesson-card.completed { border-color: var(--accent-success); }

.lesson-icon {
  width: 50px;
  height: 50px;
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  flex-shrink: 0;
  background: var(--bg-elevated);
}

.lesson-icon.completed {
  background: var(--gradient-success);
  color: white;
}

.lesson-content {
  flex: 1;
  min-width: 0;
}

.lesson-level-tag {
  font-size: 10px;
  font-weight: 700;
  color: var(--accent-primary);
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 2px;
}

.lesson-title {
  font-weight: 700;
  font-size: 15px;
  margin-bottom: 2px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.lesson-meta {
  font-size: 12px;
  color: var(--text-secondary);
  display: flex;
  gap: 8px;
}

.lesson-arrow {
  color: var(--text-tertiary);
  font-size: 18px;
}

/* Bottom Navigation */
.bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: var(--bg-secondary);
  border-top: 1px solid var(--border);
  padding: 8px 0;
  padding-bottom: calc(8px + var(--safe-bottom));
  display: flex;
  justify-content: space-around;
  z-index: 100;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  background: rgba(30, 41, 59, 0.95);
  max-width: 500px;
  margin: 0 auto;
}

@media (prefers-color-scheme: light) {
  .bottom-nav { background: rgba(255, 255, 255, 0.95); }
}

.nav-item {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  padding: 8px;
  color: var(--text-tertiary);
  font-size: 11px;
  font-weight: 600;
  transition: color 0.2s;
}

.nav-item.active { color: var(--accent-primary); }

.nav-icon { font-size: 22px; }

/* Pages */
.page { display: none; }
.page.active { display: block; }

/* Lesson Player */
.lesson-player {
  background: var(--bg-primary);
  position: fixed;
  inset: 0;
  z-index: 200;
  display: none;
  flex-direction: column;
  padding-top: var(--safe-top);
  padding-bottom: var(--safe-bottom);
  overflow-y: auto;
}

.lesson-player.active { display: flex; }

.lesson-header {
  padding: 16px 20px;
  display: flex;
  align-items: center;
  gap: 16px;
  border-bottom: 1px solid var(--border);
  background: var(--bg-primary);
  position: sticky;
  top: 0;
  z-index: 10;
}

.close-btn {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: var(--bg-elevated);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
  flex-shrink: 0;
}

.lesson-progress-bar {
  flex: 1;
  height: 8px;
  background: var(--bg-elevated);
  border-radius: 100px;
  overflow: hidden;
}

.lesson-progress-bar-fill {
  height: 100%;
  background: var(--gradient-primary);
  border-radius: 100px;
  transition: width 0.4s ease;
}

.lesson-body {
  flex: 1;
  padding: 24px 20px;
  display: flex;
  flex-direction: column;
}

/* Exercise types */
.exercise-prompt {
  font-size: 14px;
  color: var(--text-secondary);
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 600;
  margin-bottom: 8px;
}

.exercise-question {
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 24px;
  line-height: 1.3;
}

.exercise-sentence {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 20px;
  margin-bottom: 20px;
  font-size: 18px;
  font-weight: 600;
  text-align: center;
}

.options {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}

.option {
  background: var(--bg-card);
  border: 2px solid var(--border);
  border-radius: 14px;
  padding: 16px;
  display: flex;
  align-items: center;
  gap: 12px;
  text-align: left;
  font-size: 15px;
  font-weight: 500;
  color: var(--text-primary);
  transition: all 0.2s;
}

.option:active { transform: scale(0.98); }
.option.selected { border-color: var(--accent-primary); background: rgba(99, 102, 241, 0.1); }
.option.correct { border-color: var(--accent-success); background: rgba(16, 185, 129, 0.1); }
.option.incorrect { border-color: var(--accent-danger); background: rgba(239, 68, 68, 0.1); }
.option.disabled { pointer-events: none; opacity: 0.5; }

.option-letter {
  width: 28px;
  height: 28px;
  border-radius: 8px;
  background: var(--bg-elevated);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 13px;
  flex-shrink: 0;
}

.option.correct .option-letter { background: var(--accent-success); color: white; }
.option.incorrect .option-letter { background: var(--accent-danger); color: white; }

/* Input */
.text-input {
  width: 100%;
  background: var(--bg-card);
  border: 2px solid var(--border);
  border-radius: 14px;
  padding: 16px;
  font-size: 16px;
  color: var(--text-primary);
  margin-bottom: 16px;
  outline: none;
  transition: border-color 0.2s;
}

.text-input:focus { border-color: var(--accent-primary); }

textarea.text-input {
  min-height: 100px;
  resize: vertical;
}

/* Voice Button */
.voice-button {
  background: var(--gradient-primary);
  border-radius: 100px;
  padding: 16px 24px;
  color: white;
  font-weight: 700;
  font-size: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  width: 100%;
  margin-bottom: 16px;
  transition: transform 0.2s;
  box-shadow: 0 8px 20px rgba(99, 102, 241, 0.4);
}

.voice-button:active { transform: scale(0.97); }

.voice-button.recording {
  background: var(--gradient-danger);
  animation: pulse 1.5s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { box-shadow: 0 8px 20px rgba(239, 68, 68, 0.4); }
  50% { box-shadow: 0 8px 30px rgba(239, 68, 68, 0.7); }
}

.voice-status {
  text-align: center;
  font-size: 14px;
  color: var(--text-secondary);
  margin-bottom: 16px;
  min-height: 20px;
}

.voice-result {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 16px;
  margin-bottom: 16px;
  font-size: 15px;
  min-height: 60px;
}

.speak-button {
  background: var(--bg-elevated);
  border-radius: 12px;
  padding: 10px 16px;
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  font-weight: 600;
  margin-bottom: 16px;
}

/* Vocab card */
.vocab-card {
  background: var(--gradient-primary);
  border-radius: 20px;
  padding: 24px;
  color: white;
  margin-bottom: 16px;
  position: relative;
}

.vocab-word-en {
  font-size: 32px;
  font-weight: 800;
  margin-bottom: 6px;
}

.vocab-word-fr {
  font-size: 17px;
  opacity: 0.9;
  margin-bottom: 12px;
}

.vocab-example {
  background: rgba(255,255,255,0.2);
  border-radius: 12px;
  padding: 12px;
  font-size: 14px;
  font-style: italic;
}

.vocab-controls {
  display: flex;
  gap: 8px;
  margin-top: 16px;
}

.vocab-control-btn {
  flex: 1;
  background: rgba(255,255,255,0.2);
  border-radius: 12px;
  padding: 12px;
  color: white;
  font-weight: 600;
  font-size: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}

/* Continue Button */
.continue-btn {
  background: var(--gradient-primary);
  color: white;
  border-radius: 14px;
  padding: 16px;
  font-weight: 700;
  font-size: 16px;
  width: 100%;
  margin-top: auto;
  transition: transform 0.2s;
  box-shadow: 0 8px 20px rgba(99, 102, 241, 0.3);
}

.continue-btn:disabled {
  opacity: 0.5;
  box-shadow: none;
}

.continue-btn:active:not(:disabled) { transform: scale(0.98); }

/* Feedback */
.feedback {
  border-radius: 16px;
  padding: 16px;
  margin-bottom: 16px;
  border: 2px solid;
  animation: slideUp 0.3s ease;
}

@keyframes slideUp {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

.feedback.correct {
  background: rgba(16, 185, 129, 0.1);
  border-color: var(--accent-success);
}

.feedback.incorrect {
  background: rgba(239, 68, 68, 0.1);
  border-color: var(--accent-danger);
}

.feedback-title {
  font-weight: 800;
  font-size: 17px;
  margin-bottom: 6px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.feedback.correct .feedback-title { color: var(--accent-success); }
.feedback.incorrect .feedback-title { color: var(--accent-danger); }

.feedback-text {
  font-size: 14px;
  color: var(--text-secondary);
  line-height: 1.5;
}

.feedback-correction {
  background: var(--bg-card);
  border-radius: 10px;
  padding: 10px;
  margin-top: 8px;
  font-size: 14px;
  font-weight: 600;
}

/* Hint */
.hint {
  background: rgba(245, 158, 11, 0.1);
  border-left: 3px solid var(--accent-warning);
  padding: 10px 14px;
  border-radius: 8px;
  font-size: 13px;
  color: var(--text-secondary);
  margin-bottom: 12px;
}

/* Badge */
.badge {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  padding: 4px 10px;
  border-radius: 100px;
  font-size: 11px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.badge.primary { background: rgba(99, 102, 241, 0.15); color: var(--accent-primary); }
.badge.success { background: rgba(16, 185, 129, 0.15); color: var(--accent-success); }
.badge.warning { background: rgba(245, 158, 11, 0.15); color: var(--accent-warning); }

/* Achievement */
.achievement {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 14px;
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 8px;
}

.achievement.unlocked { border-color: var(--accent-warning); }
.achievement.locked { opacity: 0.5; }

.achievement-icon {
  width: 44px;
  height: 44px;
  border-radius: 12px;
  background: var(--bg-elevated);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  flex-shrink: 0;
}

.achievement.unlocked .achievement-icon {
  background: var(--gradient-warning);
}

.achievement-content { flex: 1; }
.achievement-title { font-weight: 700; font-size: 14px; margin-bottom: 2px; }
.achievement-desc { font-size: 12px; color: var(--text-secondary); }

/* Modal */
.modal {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.7);
  z-index: 300;
  align-items: flex-end;
  justify-content: center;
  padding: 0;
}

.modal.active { display: flex; }

.modal-content {
  background: var(--bg-secondary);
  width: 100%;
  max-width: 500px;
  border-radius: 24px 24px 0 0;
  padding: 24px;
  padding-bottom: calc(24px + var(--safe-bottom));
  max-height: 85vh;
  overflow-y: auto;
  animation: slideUp 0.3s ease;
}

.modal-handle {
  width: 36px;
  height: 4px;
  background: var(--text-tertiary);
  border-radius: 2px;
  margin: 0 auto 16px;
}

/* Toast */
.toast {
  position: fixed;
  top: calc(var(--safe-top) + 20px);
  left: 20px;
  right: 20px;
  background: var(--bg-elevated);
  border-radius: 14px;
  padding: 14px 18px;
  z-index: 400;
  box-shadow: var(--shadow);
  display: flex;
  align-items: center;
  gap: 12px;
  transform: translateY(-200%);
  transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
  max-width: 460px;
  margin: 0 auto;
}

.toast.show { transform: translateY(0); }
.toast-icon { font-size: 24px; }
.toast-text { flex: 1; font-weight: 600; font-size: 14px; }

/* Confetti */
.confetti-container {
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 500;
  overflow: hidden;
}

.confetti {
  position: absolute;
  width: 10px;
  height: 10px;
  animation: confetti-fall 3s linear forwards;
}

@keyframes confetti-fall {
  0% { transform: translateY(-100vh) rotate(0deg); opacity: 1; }
  100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
}

/* Urgency Mode */
.urgency-card {
  background: var(--gradient-warning);
  border-radius: 20px;
  padding: 20px;
  color: white;
  margin-bottom: 16px;
  position: relative;
  overflow: hidden;
}

.urgency-title {
  font-size: 18px;
  font-weight: 800;
  margin-bottom: 6px;
}

.urgency-desc {
  font-size: 13px;
  opacity: 0.95;
  margin-bottom: 12px;
}

.urgency-btn {
  background: white;
  color: #F59E0B;
  border-radius: 12px;
  padding: 10px 20px;
  font-weight: 700;
  font-size: 14px;
}

/* Install banner */
.install-banner {
  background: var(--gradient-cool);
  border-radius: 16px;
  padding: 16px;
  color: white;
  margin-bottom: 16px;
  display: none;
}

.install-banner.show { display: block; }

.install-banner-title { font-weight: 700; margin-bottom: 4px; }
.install-banner-text { font-size: 13px; opacity: 0.9; margin-bottom: 12px; }

.install-banner-btn {
  background: white;
  color: #3B82F6;
  border-radius: 10px;
  padding: 8px 14px;
  font-weight: 700;
  font-size: 13px;
}

/* Empty state */
.empty {
  text-align: center;
  padding: 40px 20px;
}

.empty-icon { font-size: 48px; margin-bottom: 12px; }
.empty-title { font-weight: 700; font-size: 18px; margin-bottom: 6px; }
.empty-text { color: var(--text-secondary); font-size: 14px; }

/* Skill bar */
.skill-row {
  margin-bottom: 14px;
}

.skill-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 6px;
  font-size: 13px;
}

.skill-name { font-weight: 600; }
.skill-percent { color: var(--text-secondary); }

.skill-bar {
  height: 8px;
  background: var(--bg-elevated);
  border-radius: 100px;
  overflow: hidden;
}

.skill-bar-fill {
  height: 100%;
  border-radius: 100px;
  transition: width 0.6s ease;
}

/* Dialogue */
.dialogue-line {
  padding: 12px 14px;
  border-radius: 14px;
  margin-bottom: 8px;
  background: var(--bg-card);
  border: 1px solid var(--border);
}

.dialogue-line.you {
  background: rgba(99, 102, 241, 0.1);
  border-color: var(--accent-primary);
}

.dialogue-speaker {
  font-size: 11px;
  font-weight: 700;
  color: var(--accent-primary);
  text-transform: uppercase;
  margin-bottom: 4px;
  letter-spacing: 0.5px;
}

.dialogue-text {
  font-weight: 600;
  margin-bottom: 4px;
  font-size: 15px;
}

.dialogue-fr {
  font-size: 13px;
  color: var(--text-secondary);
  font-style: italic;
}

.dialogue-controls {
  display: flex;
  gap: 6px;
  margin-top: 8px;
}

.mini-btn {
  background: var(--bg-elevated);
  padding: 6px 10px;
  border-radius: 8px;
  font-size: 12px;
  font-weight: 600;
  display: inline-flex;
  align-items: center;
  gap: 4px;
}

/* Grammar */
.grammar-card {
  background: rgba(245, 158, 11, 0.1);
  border: 1px solid rgba(245, 158, 11, 0.3);
  border-radius: 16px;
  padding: 16px;
  margin-bottom: 16px;
}

.grammar-title {
  font-weight: 700;
  font-size: 16px;
  margin-bottom: 8px;
  color: var(--accent-warning);
}

.grammar-rule {
  background: var(--bg-card);
  border-radius: 10px;
  padding: 10px 12px;
  margin-bottom: 6px;
  font-size: 14px;
}

/* Level cards */
.level-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
  margin-bottom: 20px;
}

.level-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 14px;
  text-align: center;
}

.level-card.active {
  background: var(--gradient-primary);
  color: white;
  border: none;
}

.level-card-name { font-size: 24px; font-weight: 800; margin-bottom: 2px; }
.level-card-label { font-size: 11px; font-weight: 600; opacity: 0.8; }
.level-card-progress { font-size: 12px; margin-top: 4px; opacity: 0.9; }

/* Word list */
.word-item {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 12px;
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.word-item-content { flex: 1; }
.word-item-en { font-weight: 700; font-size: 15px; }
.word-item-fr { font-size: 13px; color: var(--text-secondary); }

.word-play {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: var(--accent-primary);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  flex-shrink: 0;
}

/* Profession picker */
.profession-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}

.profession-item {
  background: var(--bg-card);
  border: 2px solid var(--border);
  border-radius: 14px;
  padding: 16px;
  text-align: center;
  font-weight: 600;
  font-size: 14px;
}

.profession-item.selected {
  border-color: var(--accent-primary);
  background: rgba(99, 102, 241, 0.1);
}

.profession-icon { font-size: 28px; margin-bottom: 6px; }

/* Loading */
.spinner {
  width: 24px;
  height: 24px;
  border: 3px solid var(--bg-elevated);
  border-top-color: var(--accent-primary);
  border-radius: 50%;
  animation: spin 0.8s linear infinite;
  display: inline-block;
}

@keyframes spin { to { transform: rotate(360deg); } }
</style>
</head>
<body>

<!-- Toast -->
<div class="toast" id="toast">
  <div class="toast-icon" id="toastIcon">✨</div>
  <div class="toast-text" id="toastText">Bienvenue !</div>
</div>

<!-- Confetti container -->
<div class="confetti-container" id="confettiContainer"></div>

<div class="app">
  <!-- Top Bar -->
  <div class="top-bar">
    <div class="app-logo">
      <div class="app-logo-icon">E</div>
      <div class="app-logo-text">English Pro</div>
    </div>
    <div class="top-stats">
      <div class="top-stat streak">🔥 <span id="streakCount">0</span></div>
      <div class="top-stat xp">⚡ <span id="xpCount">0</span></div>
    </div>
  </div>

  <!-- HOME PAGE -->
  <div class="page active" id="page-home">
    <div class="main-content">
      <!-- Install banner (PWA) -->
      <div class="install-banner" id="installBanner">
        <div class="install-banner-title">📲 Installe l'app sur ton iPhone</div>
        <div class="install-banner-text">Appuie sur Partager ⬆️ puis "Sur l'écran d'accueil"</div>
        <button class="install-banner-btn" onclick="document.getElementById('installBanner').classList.remove('show')">Compris</button>
      </div>

      <!-- Hero -->
      <div class="hero-card">
        <div class="hero-greeting" id="greeting">Bonjour 👋</div>
        <div class="hero-title">Continue ton parcours</div>
        <div class="hero-progress">
          <div class="hero-progress-fill" id="heroProgress" style="width: 0%"></div>
        </div>
        <div class="hero-progress-text"><span id="heroLessonsDone">0</span> leçons complétées · Niveau <span id="heroLevel">A1</span></div>
      </div>

      <!-- Stats -->
      <div class="stats-row">
        <div class="stat-mini">
          <div class="stat-mini-value" style="color: var(--accent-primary)" id="statXP">0</div>
          <div class="stat-mini-label">XP</div>
        </div>
        <div class="stat-mini">
          <div class="stat-mini-value" style="color: var(--accent-success)" id="statAccuracy">0%</div>
          <div class="stat-mini-label">Précision</div>
        </div>
        <div class="stat-mini">
          <div class="stat-mini-value" style="color: var(--accent-warning)" id="statWords">0</div>
          <div class="stat-mini-label">Mots</div>
        </div>
      </div>

      <!-- Quick Actions -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Actions rapides</div>
        </div>
        <div class="quick-actions">
          <button class="quick-action" onclick="openUrgencyMode()">
            <div class="quick-action-icon" style="background: var(--gradient-warning)">⚡</div>
            <div class="quick-action-title">Mode Urgence</div>
            <div class="quick-action-desc">Réunion ou call dans peu de temps</div>
          </button>
          <button class="quick-action" onclick="startQuickPractice('vocabulary')">
            <div class="quick-action-icon" style="background: var(--gradient-cool)">📚</div>
            <div class="quick-action-title">Vocabulaire</div>
            <div class="quick-action-desc">Réviser les mots</div>
          </button>
          <button class="quick-action" onclick="startQuickPractice('listening')">
            <div class="quick-action-icon" style="background: var(--gradient-primary)">🎧</div>
            <div class="quick-action-title">Écoute</div>
            <div class="quick-action-desc">Compréhension orale</div>
          </button>
          <button class="quick-action" onclick="startQuickPractice('speaking')">
            <div class="quick-action-icon" style="background: var(--gradient-success)">🎙️</div>
            <div class="quick-action-title">Prononciation</div>
            <div class="quick-action-desc">Parle en anglais</div>
          </button>
        </div>
      </div>

      <!-- Continue lessons -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Continuer la leçon</div>
        </div>
        <div id="recommendedLessons"></div>
      </div>
    </div>
  </div>

  <!-- LESSONS PAGE -->
  <div class="page" id="page-lessons">
    <div class="main-content">
      <div class="section">
        <div class="section-header">
          <div class="section-title">Niveaux</div>
        </div>
        <div class="level-grid" id="levelGrid"></div>
      </div>

      <div class="section">
        <div class="section-header">
          <div class="section-title">Toutes les leçons - <span id="currentLevelTitle">A1</span></div>
        </div>
        <div id="allLessons"></div>
      </div>
    </div>
  </div>

  <!-- VOCABULARY PAGE -->
  <div class="page" id="page-vocab">
    <div class="main-content">
      <div class="section">
        <div class="section-header">
          <div class="section-title">📖 Mon vocabulaire</div>
          <div class="section-action" onclick="reviewWeakWords()">Réviser faibles</div>
        </div>
        <div id="vocabList"></div>
      </div>
    </div>
  </div>

  <!-- PROFILE PAGE -->
  <div class="page" id="page-profile">
    <div class="main-content">
      <!-- Profession setup -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">💼 Mon métier</div>
        </div>
        <div class="profession-grid" id="professionGrid"></div>
      </div>

      <!-- Skills -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">🎯 Mes compétences</div>
        </div>
        <div id="skillsList"></div>
      </div>

      <!-- Achievements -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">🏆 Mes badges</div>
        </div>
        <div id="achievementsList"></div>
      </div>

      <!-- Reset -->
      <div class="section">
        <button class="continue-btn" style="background: var(--bg-elevated); color: var(--text-secondary)" onclick="resetProgress()">Réinitialiser ma progression</button>
      </div>
    </div>
  </div>

  <!-- LESSON PLAYER -->
  <div class="lesson-player" id="lessonPlayer">
    <div class="lesson-header">
      <button class="close-btn" onclick="closeLesson()">✕</button>
      <div class="lesson-progress-bar">
        <div class="lesson-progress-bar-fill" id="lessonProgressFill"></div>
      </div>
      <div style="font-weight: 700; font-size: 14px;" id="lessonHearts">❤️ 5</div>
    </div>
    <div class="lesson-body" id="lessonBody"></div>
  </div>

  <!-- Bottom Nav -->
  <div class="bottom-nav">
    <button class="nav-item active" onclick="switchPage('home', this)">
      <div class="nav-icon">🏠</div>
      <div>Accueil</div>
    </button>
    <button class="nav-item" onclick="switchPage('lessons', this)">
      <div class="nav-icon">📚</div>
      <div>Leçons</div>
    </button>
    <button class="nav-item" onclick="switchPage('vocab', this)">
      <div class="nav-icon">📖</div>
      <div>Mots</div>
    </button>
    <button class="nav-item" onclick="switchPage('profile', this)">
      <div class="nav-icon">👤</div>
      <div>Profil</div>
    </button>
  </div>
</div>

<!-- Modal -->
<div class="modal" id="modal">
  <div class="modal-content" id="modalContent">
    <div class="modal-handle"></div>
    <div id="modalBody"></div>
  </div>
</div>

<script>
// ==========================================
// DATA: COMPLETE CURRICULUM
// ==========================================

const LEVELS = {
  A1: { name: 'Beginner', label: 'Débutant', color: '#10B981', target: 200 },
  A2: { name: 'Elementary', label: 'Élémentaire', color: '#3B82F6', target: 250 },
  B1: { name: 'Intermediate', label: 'Intermédiaire', color: '#8B5CF6', target: 300 },
  B2: { name: 'Upper Int.', label: 'Avancé', color: '#F59E0B', target: 350 },
  C1: { name: 'Advanced', label: 'Expert', color: '#EF4444', target: 400 },
  C2: { name: 'Mastery', label: 'Maîtrise', color: '#DC2626', target: 500 }
};

const PROFESSIONS = [
  { id: 'general', icon: '🌐', name: 'Général' },
  { id: 'business', icon: '💼', name: 'Business' },
  { id: 'tech', icon: '💻', name: 'Tech/IT' },
  { id: 'sales', icon: '🛍️', name: 'Commerce' },
  { id: 'finance', icon: '💰', name: 'Finance' },
  { id: 'medical', icon: '🏥', name: 'Médical' },
  { id: 'hr', icon: '👥', name: 'RH' },
  { id: 'marketing', icon: '📢', name: 'Marketing' }
];

const ACHIEVEMENTS = [
  { id: 'first_lesson', icon: '🎯', title: 'Premier pas', desc: 'Compléter ta 1ère leçon', condition: p => p.lessonsCompleted >= 1 },
  { id: 'streak_3', icon: '🔥', title: 'Sur ma lancée', desc: '3 jours de suite', condition: p => p.streak >= 3 },
  { id: 'streak_7', icon: '🌟', title: 'Une semaine !', desc: '7 jours de suite', condition: p => p.streak >= 7 },
  { id: 'streak_30', icon: '👑', title: 'Inarrêtable', desc: '30 jours de suite', condition: p => p.streak >= 30 },
  { id: 'words_50', icon: '📚', title: 'Vocabulaire +', desc: 'Apprendre 50 mots', condition: p => p.wordsLearned >= 50 },
  { id: 'words_200', icon: '🧠', title: 'Mémoire d\'éléphant', desc: 'Apprendre 200 mots', condition: p => p.wordsLearned >= 200 },
  { id: 'words_500', icon: '🎓', title: 'Polyglotte', desc: 'Apprendre 500 mots', condition: p => p.wordsLearned >= 500 },
  { id: 'perfect_lesson', icon: '💯', title: 'Sans faute', desc: 'Leçon parfaite', condition: p => p.perfectLessons >= 1 },
  { id: 'lessons_10', icon: '🏅', title: 'Studieux', desc: '10 leçons complétées', condition: p => p.lessonsCompleted >= 10 },
  { id: 'lessons_50', icon: '🥇', title: 'Champion', desc: '50 leçons complétées', condition: p => p.lessonsCompleted >= 50 },
  { id: 'voice_first', icon: '🎙️', title: 'Premier mot', desc: 'Première reconnaissance vocale', condition: p => p.voiceCount >= 1 },
  { id: 'voice_50', icon: '🗣️', title: 'Orateur', desc: '50 phrases parlées', condition: p => p.voiceCount >= 50 },
  { id: 'level_a2', icon: '🚀', title: 'Vers A2', desc: 'Atteindre le niveau A2', condition: p => p.currentLevel === 'A2' || levelOrder.indexOf(p.currentLevel) > 0 },
  { id: 'level_b1', icon: '⭐', title: 'Vers B1', desc: 'Atteindre le niveau B1', condition: p => levelOrder.indexOf(p.currentLevel) >= 2 },
  { id: 'xp_1000', icon: '💎', title: '1000 XP', desc: 'Gagner 1000 XP', condition: p => p.xp >= 1000 }
];

const levelOrder = ['A1','A2','B1','B2','C1','C2'];

// COMPREHENSIVE LESSONS DATABASE
const LESSONS = [
  // ====== A1 LEVEL ======
  {
    id: 'a1_01', level: 'A1', module: 'Foundations',
    title: 'Saluer & se présenter',
    icon: '👋', skill: 'social',
    vocabulary: [
      { en: 'Hello', fr: 'Bonjour', ex: 'Hello, how are you?' },
      { en: 'Good morning', fr: 'Bonjour (matin)', ex: 'Good morning, team!' },
      { en: 'Good afternoon', fr: 'Bon après-midi', ex: 'Good afternoon, sir.' },
      { en: 'Good evening', fr: 'Bonsoir', ex: 'Good evening, everyone.' },
      { en: 'Nice to meet you', fr: 'Enchanté(e)', ex: 'Nice to meet you, Sarah.' },
      { en: 'My name is', fr: 'Je m\'appelle', ex: 'My name is John.' },
      { en: 'How are you?', fr: 'Comment allez-vous?', ex: 'How are you today?' },
      { en: 'I\'m fine, thanks', fr: 'Je vais bien, merci', ex: 'I\'m fine, thanks. And you?' },
      { en: 'Thank you', fr: 'Merci', ex: 'Thank you very much.' },
      { en: 'Goodbye', fr: 'Au revoir', ex: 'Goodbye, see you tomorrow.' }
    ],
    grammar: {
      title: 'Verbe TO BE (être)',
      rules: ['I am (I\'m) → Je suis', 'You are (You\'re) → Tu es / Vous êtes', 'He/She/It is → Il/Elle est', 'We are (We\'re) → Nous sommes', 'They are → Ils/Elles sont']
    },
    exercises: [
      { type: 'mcq', q: 'Comment dit-on "Bonjour" le matin ?', options: ['Good night', 'Good morning', 'Good evening', 'Good afternoon'], correct: 1 },
      { type: 'mcq', q: 'Complète : "Hello, ___ John."', options: ['I am', 'I is', 'I be', 'I are'], correct: 0, exp: 'Avec "I" on utilise "am"' },
      { type: 'speak', text: 'Hello, my name is...', hint: 'Présente-toi' },
      { type: 'fill', sentence: 'Nice to ___ you', correct: 'meet', hint: 'Enchanté' },
      { type: 'translate', fr: 'Je vais bien, merci', correct: "i'm fine thanks", keywords: ['fine', 'thanks'] },
      { type: 'mcq', q: 'Qu\'est-ce qui veut dire "Au revoir" ?', options: ['Hello', 'Welcome', 'Goodbye', 'Thanks'], correct: 2 },
      { type: 'listen', text: 'How are you today?', q: 'Qu\'as-tu entendu ?', options: ['How old are you?', 'How are you today?', 'Where are you today?', 'Who are you?'], correct: 1 },
      { type: 'fill', sentence: 'My name ___ Marie', correct: 'is', hint: 'She/He/It → ?' }
    ],
    dialogue: {
      title: 'Premier jour au bureau',
      lines: [
        { speaker: 'You', text: 'Good morning! I\'m new here.', fr: 'Bonjour! Je suis nouveau ici.' },
        { speaker: 'Sarah', text: 'Good morning! Welcome. I\'m Sarah.', fr: 'Bonjour! Bienvenue. Je suis Sarah.' },
        { speaker: 'You', text: 'Nice to meet you, Sarah.', fr: 'Enchanté, Sarah.' },
        { speaker: 'Sarah', text: 'Nice to meet you too. What\'s your name?', fr: 'Enchantée aussi. Quel est votre nom ?' }
      ]
    }
  },
  {
    id: 'a1_02', level: 'A1', module: 'Foundations',
    title: 'Mon métier & moi',
    icon: '💼', skill: 'professional',
    vocabulary: [
      { en: 'I work as', fr: 'Je travaille comme', ex: 'I work as an engineer.' },
      { en: 'I am a', fr: 'Je suis un(e)', ex: 'I am a teacher.' },
      { en: 'Job', fr: 'Métier', ex: 'What\'s your job?' },
      { en: 'Company', fr: 'Entreprise', ex: 'I work for a tech company.' },
      { en: 'Colleague', fr: 'Collègue', ex: 'She\'s my colleague.' },
      { en: 'Boss', fr: 'Patron(ne)', ex: 'My boss is nice.' },
      { en: 'Office', fr: 'Bureau (lieu)', ex: 'I go to the office.' },
      { en: 'Where are you from?', fr: 'D\'où venez-vous ?', ex: 'Where are you from?' },
      { en: 'I\'m from', fr: 'Je viens de', ex: 'I\'m from France.' },
      { en: 'What do you do?', fr: 'Que faites-vous ?', ex: 'What do you do for work?' }
    ],
    grammar: {
      title: 'Articles a / an',
      rules: ['"a" devant consonne : a manager, a job', '"an" devant voyelle : an engineer, an office', 'Voyelles : a, e, i, o, u', 'Exemple : a doctor, an architect']
    },
    exercises: [
      { type: 'mcq', q: 'I work as ___ engineer', options: ['a', 'an', 'the', '—'], correct: 1, exp: '"engineer" commence par une voyelle → an' },
      { type: 'mcq', q: 'She is ___ teacher', options: ['a', 'an', 'the', '—'], correct: 0, exp: '"teacher" commence par une consonne → a' },
      { type: 'fill', sentence: 'I\'m ___ Paris', correct: 'from', hint: 'Je viens de...' },
      { type: 'translate', fr: 'Je travaille comme designer', correct: 'i work as a designer', keywords: ['work', 'designer'] },
      { type: 'speak', text: 'I work as a manager', hint: 'Dis ton métier' },
      { type: 'mcq', q: 'Que veut dire "colleague" ?', options: ['Patron', 'Collègue', 'Client', 'Stagiaire'], correct: 1 },
      { type: 'listen', text: 'What do you do for work?', q: 'Qu\'as-tu entendu ?', options: ['What do you do for work?', 'Where do you work?', 'When do you work?', 'Who do you work with?'], correct: 0 },
      { type: 'fill', sentence: 'I work ___ a tech company', correct: 'for', hint: 'Préposition' }
    ],
    dialogue: {
      title: 'Networking event',
      lines: [
        { speaker: 'John', text: 'Hi! What do you do?', fr: 'Salut! Que faites-vous ?' },
        { speaker: 'You', text: 'I\'m a developer. And you?', fr: 'Je suis développeur. Et vous ?' },
        { speaker: 'John', text: 'I work as a designer for a startup.', fr: 'Je travaille comme designer pour une startup.' },
        { speaker: 'You', text: 'Interesting! Where are you from?', fr: 'Intéressant ! D\'où venez-vous ?' }
      ]
    }
  },
  {
    id: 'a1_03', level: 'A1', module: 'Office',
    title: 'Le bureau & les objets',
    icon: '🏢', skill: 'professional',
    vocabulary: [
      { en: 'Desk', fr: 'Bureau (meuble)', ex: 'This is my desk.' },
      { en: 'Computer', fr: 'Ordinateur', ex: 'I use a computer.' },
      { en: 'Phone', fr: 'Téléphone', ex: 'My phone is broken.' },
      { en: 'Email', fr: 'Email', ex: 'Send me an email.' },
      { en: 'Meeting', fr: 'Réunion', ex: 'I have a meeting at 10.' },
      { en: 'Document', fr: 'Document', ex: 'Sign this document.' },
      { en: 'File', fr: 'Fichier', ex: 'Save the file.' },
      { en: 'Printer', fr: 'Imprimante', ex: 'The printer is broken.' },
      { en: 'Coffee', fr: 'Café', ex: 'I need a coffee.' },
      { en: 'Break', fr: 'Pause', ex: 'Let\'s take a break.' }
    ],
    grammar: {
      title: 'Présent simple - I/You/We/They',
      rules: ['I work / You work / We work / They work', 'Pour les actions habituelles', 'Pour les faits et routines', 'Question : Do you work?']
    },
    exercises: [
      { type: 'mcq', q: 'Comment dit-on "réunion" ?', options: ['Meeting', 'Greeting', 'Building', 'Reading'], correct: 0 },
      { type: 'mcq', q: 'I ___ in an office', options: ['works', 'work', 'working', 'to work'], correct: 1, exp: 'Avec I on utilise verbe sans s' },
      { type: 'fill', sentence: 'Send me an ___', correct: 'email', hint: 'Communication digitale' },
      { type: 'translate', fr: 'J\'ai une réunion à 10h', correct: 'i have a meeting at 10', keywords: ['have', 'meeting'] },
      { type: 'speak', text: 'Let\'s take a break', hint: 'Faisons une pause' },
      { type: 'listen', text: 'The printer is broken', q: 'Qu\'est-ce qui ne marche pas ?', options: ['Computer', 'Printer', 'Phone', 'Desk'], correct: 1 },
      { type: 'fill', sentence: 'I need ___ coffee', correct: 'a', hint: 'Article' },
      { type: 'mcq', q: 'Que veut dire "file" ?', options: ['Bureau', 'Fichier', 'Pause', 'Café'], correct: 1 }
    ]
  },
  {
    id: 'a1_04', level: 'A1', module: 'Time',
    title: 'L\'heure & les jours',
    icon: '🕐', skill: 'time',
    vocabulary: [
      { en: 'What time is it?', fr: 'Quelle heure est-il ?', ex: 'What time is it now?' },
      { en: 'It\'s 9 o\'clock', fr: 'Il est 9 heures', ex: 'It\'s 9 o\'clock sharp.' },
      { en: 'Half past', fr: 'Et demie', ex: 'It\'s half past two.' },
      { en: 'Quarter past', fr: 'Et quart', ex: 'It\'s quarter past three.' },
      { en: 'Quarter to', fr: 'Moins le quart', ex: 'It\'s quarter to five.' },
      { en: 'Monday', fr: 'Lundi', ex: 'See you Monday.' },
      { en: 'Tuesday', fr: 'Mardi', ex: 'Meeting on Tuesday.' },
      { en: 'Today', fr: 'Aujourd\'hui', ex: 'Today is Monday.' },
      { en: 'Tomorrow', fr: 'Demain', ex: 'See you tomorrow.' },
      { en: 'Yesterday', fr: 'Hier', ex: 'I worked yesterday.' }
    ],
    grammar: {
      title: 'Prépositions AT / IN / ON',
      rules: ['AT pour les heures : at 9 AM', 'IN pour les parties du jour : in the morning', 'ON pour les jours : on Monday', 'IN pour les mois : in May']
    },
    exercises: [
      { type: 'mcq', q: 'The meeting is ___ 3 PM', options: ['at', 'in', 'on', 'to'], correct: 0 },
      { type: 'mcq', q: 'I work ___ Monday', options: ['at', 'in', 'on', 'to'], correct: 2 },
      { type: 'fill', sentence: 'See you ___', correct: 'tomorrow', hint: 'Demain' },
      { type: 'translate', fr: 'Quelle heure est-il ?', correct: 'what time is it', keywords: ['what', 'time'] },
      { type: 'speak', text: 'It\'s half past three', hint: '3h30' },
      { type: 'listen', text: 'The meeting is on Tuesday', q: 'Quand est la réunion ?', options: ['Monday', 'Tuesday', 'Wednesday', 'Thursday'], correct: 1 },
      { type: 'mcq', q: 'I work ___ the morning', options: ['at', 'in', 'on', '—'], correct: 1 }
    ]
  },
  {
    id: 'a1_05', level: 'A1', module: 'Numbers',
    title: 'Les chiffres & les nombres',
    icon: '🔢', skill: 'numbers',
    vocabulary: [
      { en: 'Zero', fr: 'Zéro', ex: 'Score is zero.' },
      { en: 'Ten', fr: 'Dix', ex: 'I have ten emails.' },
      { en: 'Twenty', fr: 'Vingt', ex: 'Twenty euros.' },
      { en: 'Hundred', fr: 'Cent', ex: 'One hundred dollars.' },
      { en: 'Thousand', fr: 'Mille', ex: 'Two thousand people.' },
      { en: 'Million', fr: 'Million', ex: 'A million users.' },
      { en: 'First', fr: 'Premier', ex: 'My first day.' },
      { en: 'Second', fr: 'Deuxième', ex: 'Second floor.' },
      { en: 'Last', fr: 'Dernier', ex: 'Last meeting.' },
      { en: 'How many?', fr: 'Combien ? (comptable)', ex: 'How many people?' }
    ],
    grammar: {
      title: 'How much / How many',
      rules: ['How MANY pour comptable : How many emails?', 'How MUCH pour incomptable : How much coffee?', 'Comptable : objets, personnes', 'Incomptable : eau, argent, temps']
    },
    exercises: [
      { type: 'mcq', q: '___ people are in the meeting?', options: ['How much', 'How many', 'How', 'What'], correct: 1 },
      { type: 'mcq', q: '___ time do we have?', options: ['How much', 'How many', 'How', 'What'], correct: 0 },
      { type: 'fill', sentence: 'My ___ day at work was great', correct: 'first', hint: '1er' },
      { type: 'translate', fr: 'Cent dollars', correct: 'one hundred dollars', keywords: ['hundred', 'dollars'] },
      { type: 'speak', text: 'Two thousand and twenty-five', hint: '2025' },
      { type: 'listen', text: 'I have twenty emails', q: 'Combien d\'emails ?', options: ['Ten', 'Twenty', 'Thirty', 'Forty'], correct: 1 }
    ]
  },
  {
    id: 'a1_06', level: 'A1', module: 'Email',
    title: 'Email basique',
    icon: '📧', skill: 'writing',
    vocabulary: [
      { en: 'Dear', fr: 'Cher/Chère (formel)', ex: 'Dear Mr. Smith,' },
      { en: 'Hi', fr: 'Salut (informel)', ex: 'Hi John,' },
      { en: 'Best regards', fr: 'Cordialement', ex: 'Best regards, Marie' },
      { en: 'Sincerely', fr: 'Sincèrement', ex: 'Sincerely yours,' },
      { en: 'Subject', fr: 'Objet', ex: 'Subject: Meeting tomorrow' },
      { en: 'Attachment', fr: 'Pièce jointe', ex: 'Please see the attachment.' },
      { en: 'Reply', fr: 'Répondre', ex: 'Please reply soon.' },
      { en: 'Forward', fr: 'Transférer', ex: 'Can you forward this?' },
      { en: 'Thank you for', fr: 'Merci pour', ex: 'Thank you for your email.' },
      { en: 'Looking forward to', fr: 'Dans l\'attente de', ex: 'Looking forward to your reply.' }
    ],
    grammar: {
      title: 'Formules email',
      rules: ['Formel : Dear Mr./Ms. + nom', 'Informel : Hi + prénom', 'Fin formelle : Best regards / Sincerely', 'Fin informelle : Best / Cheers']
    },
    exercises: [
      { type: 'mcq', q: 'Plus formel pour commencer un email :', options: ['Hi', 'Hey', 'Dear Mr. Smith', 'What\'s up'], correct: 2 },
      { type: 'mcq', q: 'Bonne fermeture professionnelle :', options: ['Bye', 'See ya', 'Best regards', 'Cheerio'], correct: 2 },
      { type: 'fill', sentence: '___ forward to your reply', correct: 'Looking', hint: 'Dans l\'attente' },
      { type: 'translate', fr: 'Merci pour votre email', correct: 'thank you for your email', keywords: ['thank', 'email'] },
      { type: 'speak', text: 'Looking forward to your reply', hint: 'Formule de fin' },
      { type: 'mcq', q: 'Que veut dire "attachment" ?', options: ['Sujet', 'Pièce jointe', 'Réponse', 'Signature'], correct: 1 }
    ]
  },
  {
    id: 'a1_07', level: 'A1', module: 'Questions',
    title: 'Poser des questions',
    icon: '❓', skill: 'speaking',
    vocabulary: [
      { en: 'What', fr: 'Quoi/Que', ex: 'What is your name?' },
      { en: 'Where', fr: 'Où', ex: 'Where do you work?' },
      { en: 'When', fr: 'Quand', ex: 'When is the meeting?' },
      { en: 'Who', fr: 'Qui', ex: 'Who is your manager?' },
      { en: 'Why', fr: 'Pourquoi', ex: 'Why are you late?' },
      { en: 'How', fr: 'Comment', ex: 'How are you?' },
      { en: 'Yes', fr: 'Oui', ex: 'Yes, of course.' },
      { en: 'No', fr: 'Non', ex: 'No, thank you.' },
      { en: 'Maybe', fr: 'Peut-être', ex: 'Maybe tomorrow.' },
      { en: 'I don\'t know', fr: 'Je ne sais pas', ex: 'I don\'t know yet.' }
    ],
    grammar: {
      title: 'Questions au présent',
      rules: ['Avec to be : Are you ready?', 'Avec autres verbes : Do you work?', 'He/She/It : Does she work?', 'Mots interrogatifs avant : Where do you work?']
    },
    exercises: [
      { type: 'mcq', q: '___ is your name?', options: ['What', 'Where', 'When', 'Why'], correct: 0 },
      { type: 'mcq', q: '___ you ready?', options: ['Do', 'Does', 'Are', 'Is'], correct: 2 },
      { type: 'fill', sentence: '___ is the meeting?', correct: 'When', hint: 'Quand' },
      { type: 'translate', fr: 'Comment allez-vous ?', correct: 'how are you', keywords: ['how', 'you'] },
      { type: 'speak', text: 'Where do you work?', hint: 'Demande où travaille la personne' },
      { type: 'listen', text: 'Who is your manager?', q: 'Quelle est la question ?', options: ['Where is your manager?', 'When is your manager?', 'Who is your manager?', 'Why is your manager?'], correct: 2 }
    ]
  },
  {
    id: 'a1_08', level: 'A1', module: 'Daily',
    title: 'Routine professionnelle',
    icon: '☀️', skill: 'professional',
    vocabulary: [
      { en: 'Wake up', fr: 'Se réveiller', ex: 'I wake up at 7.' },
      { en: 'Get dressed', fr: 'S\'habiller', ex: 'I get dressed quickly.' },
      { en: 'Have breakfast', fr: 'Petit-déjeuner', ex: 'I have breakfast at 8.' },
      { en: 'Go to work', fr: 'Aller au travail', ex: 'I go to work by metro.' },
      { en: 'Start work', fr: 'Commencer le travail', ex: 'I start work at 9.' },
      { en: 'Lunch break', fr: 'Pause déjeuner', ex: 'Lunch break is at noon.' },
      { en: 'Finish work', fr: 'Finir le travail', ex: 'I finish work at 6.' },
      { en: 'Go home', fr: 'Rentrer chez soi', ex: 'I go home at 7.' },
      { en: 'Have dinner', fr: 'Dîner', ex: 'We have dinner together.' },
      { en: 'Go to bed', fr: 'Se coucher', ex: 'I go to bed at 11.' }
    ],
    grammar: {
      title: 'Adverbes de fréquence',
      rules: ['Always (toujours) - 100%', 'Usually (habituellement) - 80%', 'Often (souvent) - 60%', 'Sometimes (parfois) - 40%', 'Never (jamais) - 0%', 'Position : avant le verbe principal']
    },
    exercises: [
      { type: 'mcq', q: 'I ___ start work at 9', options: ['always', 'always to', 'to always', 'am always'], correct: 0 },
      { type: 'fill', sentence: 'I have ___ at noon', correct: 'lunch', hint: 'Repas du midi' },
      { type: 'translate', fr: 'Je commence le travail à 9h', correct: 'i start work at 9', keywords: ['start', 'work'] },
      { type: 'speak', text: 'I always have lunch at noon', hint: 'Routine quotidienne' },
      { type: 'listen', text: 'I finish work at 6 PM', q: 'À quelle heure ?', options: ['5 PM', '6 PM', '7 PM', '8 PM'], correct: 1 }
    ]
  },

  // ====== A2 LEVEL ======
  {
    id: 'a2_01', level: 'A2', module: 'Past',
    title: 'Past Simple - Le passé',
    icon: '⏪', skill: 'grammar',
    vocabulary: [
      { en: 'Yesterday', fr: 'Hier', ex: 'I worked yesterday.' },
      { en: 'Last week', fr: 'La semaine dernière', ex: 'Last week was busy.' },
      { en: 'Ago', fr: 'Il y a', ex: 'Two days ago.' },
      { en: 'Worked', fr: 'Travaillé', ex: 'I worked late.' },
      { en: 'Went', fr: 'Allé', ex: 'I went to the meeting.' },
      { en: 'Said', fr: 'Dit', ex: 'She said yes.' },
      { en: 'Made', fr: 'Fait', ex: 'We made a decision.' },
      { en: 'Sent', fr: 'Envoyé', ex: 'I sent the email.' },
      { en: 'Got', fr: 'Reçu/Obtenu', ex: 'I got your message.' },
      { en: 'Already', fr: 'Déjà', ex: 'I already did it.' }
    ],
    grammar: {
      title: 'Past Simple',
      rules: ['Verbes réguliers : verbe + ed (work → worked)', 'Verbes irréguliers : à apprendre (go → went)', 'Question : Did + sujet + verbe', 'Négation : didn\'t + verbe']
    },
    exercises: [
      { type: 'mcq', q: 'I ___ to the office yesterday', options: ['go', 'went', 'goned', 'going'], correct: 1 },
      { type: 'mcq', q: 'She ___ the report last week', options: ['finish', 'finished', 'finishs', 'finishing'], correct: 1 },
      { type: 'fill', sentence: 'We ___ a meeting yesterday', correct: 'had', hint: 'Past de "have"' },
      { type: 'translate', fr: 'J\'ai envoyé l\'email', correct: 'i sent the email', keywords: ['sent', 'email'] },
      { type: 'speak', text: 'I worked late yesterday', hint: 'Action passée' },
      { type: 'mcq', q: '___ you call him?', options: ['Do', 'Did', 'Does', 'Done'], correct: 1 },
      { type: 'listen', text: 'I sent the email this morning', q: 'Quand ?', options: ['Yesterday', 'This morning', 'Last week', 'Tomorrow'], correct: 1 }
    ]
  },
  {
    id: 'a2_02', level: 'A2', module: 'Future',
    title: 'Le futur - Will & Going to',
    icon: '🔮', skill: 'grammar',
    vocabulary: [
      { en: 'Tomorrow', fr: 'Demain', ex: 'I\'ll call tomorrow.' },
      { en: 'Next week', fr: 'La semaine prochaine', ex: 'Meeting next week.' },
      { en: 'Will', fr: 'Futur', ex: 'I will help you.' },
      { en: 'Going to', fr: 'Aller (futur)', ex: 'I\'m going to call.' },
      { en: 'Soon', fr: 'Bientôt', ex: 'See you soon.' },
      { en: 'Plan', fr: 'Plan', ex: 'What\'s your plan?' },
      { en: 'Schedule', fr: 'Programmer', ex: 'Let\'s schedule a call.' },
      { en: 'Postpone', fr: 'Reporter', ex: 'Can we postpone?' },
      { en: 'Cancel', fr: 'Annuler', ex: 'I have to cancel.' },
      { en: 'Confirm', fr: 'Confirmer', ex: 'Please confirm.' }
    ],
    grammar: {
      title: 'Will vs Going to',
      rules: ['WILL : décision spontanée, prédiction', 'GOING TO : projet planifié', 'I\'ll help (spontané)', 'I\'m going to start a project (planifié)']
    },
    exercises: [
      { type: 'mcq', q: 'I ___ help you (spontané)', options: ['will', 'am going to', 'go', 'went'], correct: 0 },
      { type: 'mcq', q: 'We ___ launch next month (planifié)', options: ['will', 'are going to', 'go', 'launched'], correct: 1 },
      { type: 'fill', sentence: 'I ___ call you back', correct: 'will', hint: 'Promesse spontanée' },
      { type: 'translate', fr: 'Je vais lancer un projet', correct: 'i am going to launch a project', keywords: ['going', 'launch'] },
      { type: 'speak', text: 'I\'m going to start a new project', hint: 'Plan défini' },
      { type: 'mcq', q: 'Que veut dire "postpone" ?', options: ['Confirmer', 'Annuler', 'Reporter', 'Avancer'], correct: 2 }
    ]
  },
  {
    id: 'a2_03', level: 'A2', module: 'Meetings',
    title: 'Réunions & discussions',
    icon: '👥', skill: 'professional',
    vocabulary: [
      { en: 'Agenda', fr: 'Ordre du jour', ex: 'Let\'s see the agenda.' },
      { en: 'Topic', fr: 'Sujet', ex: 'Next topic, please.' },
      { en: 'Discuss', fr: 'Discuter', ex: 'We need to discuss this.' },
      { en: 'Agree', fr: 'Être d\'accord', ex: 'I agree with you.' },
      { en: 'Disagree', fr: 'Pas d\'accord', ex: 'I disagree.' },
      { en: 'Suggest', fr: 'Suggérer', ex: 'I suggest we wait.' },
      { en: 'Decide', fr: 'Décider', ex: 'Let\'s decide now.' },
      { en: 'Decision', fr: 'Décision', ex: 'It\'s a good decision.' },
      { en: 'Action item', fr: 'Action à faire', ex: 'These are the action items.' },
      { en: 'Wrap up', fr: 'Conclure', ex: 'Let\'s wrap up.' }
    ],
    grammar: {
      title: 'Modaux : can, could, should',
      rules: ['CAN : pouvoir/capacité (I can speak English)', 'COULD : pourrait (Could you help me?)', 'SHOULD : devrait (You should call him)', 'Suivis du verbe sans "to"']
    },
    exercises: [
      { type: 'mcq', q: '___ you help me with this?', options: ['Could', 'Should', 'Will', 'Did'], correct: 0 },
      { type: 'mcq', q: 'You ___ call him now', options: ['can', 'should', 'will', 'could'], correct: 1 },
      { type: 'fill', sentence: 'I ___ with your idea', correct: 'agree', hint: 'D\'accord' },
      { type: 'translate', fr: 'Concluons cette réunion', correct: "let's wrap up this meeting", keywords: ['wrap', 'meeting'] },
      { type: 'speak', text: 'I suggest we postpone the meeting', hint: 'Faire une suggestion' },
      { type: 'listen', text: 'What are the action items?', q: 'Que demande-t-on ?', options: ['Le planning', 'Les actions à faire', 'Les décisions', 'L\'agenda'], correct: 1 }
    ]
  },
  {
    id: 'a2_04', level: 'A2', module: 'Phone',
    title: 'Appels téléphoniques',
    icon: '📞', skill: 'speaking',
    vocabulary: [
      { en: 'Hello, this is...', fr: 'Bonjour, c\'est...', ex: 'Hello, this is John speaking.' },
      { en: 'May I speak to', fr: 'Puis-je parler à', ex: 'May I speak to Mr. Smith?' },
      { en: 'Hold on, please', fr: 'Patientez s\'il vous plaît', ex: 'Hold on, please.' },
      { en: 'Speaking', fr: 'Lui-même', ex: 'Speaking. How can I help?' },
      { en: 'Wrong number', fr: 'Mauvais numéro', ex: 'Sorry, wrong number.' },
      { en: 'Call back', fr: 'Rappeler', ex: 'I\'ll call you back.' },
      { en: 'Leave a message', fr: 'Laisser un message', ex: 'Can I leave a message?' },
      { en: 'Voicemail', fr: 'Messagerie vocale', ex: 'Leave a voicemail.' },
      { en: 'Available', fr: 'Disponible', ex: 'He\'s not available now.' },
      { en: 'Speak up', fr: 'Parler plus fort', ex: 'Could you speak up?' }
    ],
    grammar: {
      title: 'Politesse formelle',
      rules: ['Could you... (plus poli que Can you)', 'Would you mind... (Voulez-vous...)', 'May I... (Puis-je... le plus formel)', 'I\'m calling about... (J\'appelle au sujet de...)']
    },
    exercises: [
      { type: 'mcq', q: 'Phrase la plus polie :', options: ['Give me Mr. Smith', 'I want Mr. Smith', 'May I speak to Mr. Smith?', 'Where is Mr. Smith?'], correct: 2 },
      { type: 'fill', sentence: 'Could you ___ up, please?', correct: 'speak', hint: 'Parler plus fort' },
      { type: 'translate', fr: 'Je vous rappelle plus tard', correct: "i'll call you back later", keywords: ['call', 'back'] },
      { type: 'speak', text: 'Hello, this is John speaking', hint: 'Se présenter au téléphone' },
      { type: 'listen', text: 'May I leave a message?', q: 'Que demande-t-on ?', options: ['Parler à quelqu\'un', 'Laisser un message', 'Rappeler plus tard', 'Vérifier le numéro'], correct: 1 }
    ]
  },
  {
    id: 'a2_05', level: 'A2', module: 'Emails',
    title: 'Emails professionnels',
    icon: '✉️', skill: 'writing',
    vocabulary: [
      { en: 'Following up', fr: 'Faire suite', ex: 'I\'m following up on...' },
      { en: 'As discussed', fr: 'Comme convenu', ex: 'As discussed in our meeting.' },
      { en: 'Please find attached', fr: 'Ci-joint', ex: 'Please find attached the report.' },
      { en: 'Let me know', fr: 'Faites-moi savoir', ex: 'Let me know if you have questions.' },
      { en: 'At your convenience', fr: 'À votre convenance', ex: 'At your convenience.' },
      { en: 'I look forward to', fr: 'Je suis impatient de', ex: 'I look forward to hearing from you.' },
      { en: 'Apologies for', fr: 'Excuses pour', ex: 'My apologies for the delay.' },
      { en: 'Could you confirm', fr: 'Pourriez-vous confirmer', ex: 'Could you confirm the time?' },
      { en: 'Kind regards', fr: 'Cordialement', ex: 'Kind regards, Marie' },
      { en: 'Best wishes', fr: 'Meilleurs vœux', ex: 'Best wishes, John' }
    ],
    grammar: {
      title: 'Phrases d\'email type',
      rules: ['Pour commencer : I hope this email finds you well', 'Pour annoncer : I am writing to...', 'Pour conclure : Looking forward to...', 'Pour s\'excuser : I apologize for...']
    },
    exercises: [
      { type: 'mcq', q: 'Phrase pour conclure :', options: ['Hello', 'Looking forward to your reply', 'How are you?', 'Subject'], correct: 1 },
      { type: 'fill', sentence: 'Please find ___ the document', correct: 'attached', hint: 'Pièce jointe' },
      { type: 'translate', fr: 'Désolé pour le retard', correct: 'apologies for the delay', keywords: ['apologies', 'delay'] },
      { type: 'speak', text: 'I look forward to hearing from you', hint: 'Formule de fin' },
      { type: 'mcq', q: 'Que veut dire "as discussed" ?', options: ['Pour discuter', 'Comme convenu', 'À discuter', 'En discussion'], correct: 1 }
    ]
  },
  {
    id: 'a2_06', level: 'A2', module: 'Comparing',
    title: 'Comparaisons',
    icon: '⚖️', skill: 'grammar',
    vocabulary: [
      { en: 'Better', fr: 'Mieux', ex: 'This is better.' },
      { en: 'Worse', fr: 'Pire', ex: 'It\'s worse than before.' },
      { en: 'More', fr: 'Plus', ex: 'I need more time.' },
      { en: 'Less', fr: 'Moins', ex: 'Less expensive.' },
      { en: 'Faster', fr: 'Plus rapide', ex: 'This is faster.' },
      { en: 'Slower', fr: 'Plus lent', ex: 'My laptop is slower.' },
      { en: 'Bigger', fr: 'Plus grand', ex: 'A bigger team.' },
      { en: 'Smaller', fr: 'Plus petit', ex: 'A smaller office.' },
      { en: 'The best', fr: 'Le meilleur', ex: 'The best option.' },
      { en: 'The worst', fr: 'Le pire', ex: 'The worst day.' }
    ],
    grammar: {
      title: 'Comparatifs & superlatifs',
      rules: ['Adj court + er : faster, bigger, smaller', 'Adj long : more + adj : more interesting', 'Superlatif : the + er/est ou the most', 'Irréguliers : good→better→best, bad→worse→worst']
    },
    exercises: [
      { type: 'mcq', q: 'My computer is ___ than yours', options: ['fast', 'faster', 'fastest', 'more fast'], correct: 1 },
      { type: 'mcq', q: 'This is ___ option', options: ['good', 'better', 'the best', 'most good'], correct: 2 },
      { type: 'fill', sentence: 'This solution is ___ interesting', correct: 'more', hint: 'Plus + adj long' },
      { type: 'translate', fr: 'C\'est mieux comme ça', correct: "it's better this way", keywords: ['better'] },
      { type: 'speak', text: 'This option is much better', hint: 'Comparer 2 choses' }
    ]
  },

  // ====== B1 LEVEL ======
  {
    id: 'b1_01', level: 'B1', module: 'Present Perfect',
    title: 'Present Perfect',
    icon: '🔄', skill: 'grammar',
    vocabulary: [
      { en: 'I have done', fr: 'J\'ai fait', ex: 'I have done it.' },
      { en: 'Just', fr: 'Juste', ex: 'I have just finished.' },
      { en: 'Already', fr: 'Déjà', ex: 'I have already sent it.' },
      { en: 'Yet', fr: 'Encore (négatif/question)', ex: 'Have you done it yet?' },
      { en: 'Ever', fr: 'Jamais (question)', ex: 'Have you ever been there?' },
      { en: 'Never', fr: 'Jamais (négatif)', ex: 'I have never been to NYC.' },
      { en: 'Since', fr: 'Depuis (date)', ex: 'I\'ve worked here since 2020.' },
      { en: 'For', fr: 'Depuis (durée)', ex: 'I\'ve worked here for 3 years.' },
      { en: 'Recently', fr: 'Récemment', ex: 'I\'ve recently joined.' },
      { en: 'Lately', fr: 'Dernièrement', ex: 'How have you been lately?' }
    ],
    grammar: {
      title: 'Present Perfect',
      rules: ['Have/Has + participe passé', 'Action passée avec lien au présent', 'Avec since/for : durée', 'Avec just/already/yet/ever/never']
    },
    exercises: [
      { type: 'mcq', q: 'I ___ the email already', options: ['sent', 'have sent', 'send', 'sending'], correct: 1 },
      { type: 'mcq', q: 'She ___ here for 3 years', options: ['work', 'worked', 'has worked', 'working'], correct: 2 },
      { type: 'fill', sentence: 'We ___ already discussed this', correct: 'have', hint: 'We + ___ + participe' },
      { type: 'translate', fr: 'Je viens juste de finir', correct: 'i have just finished', keywords: ['have', 'just', 'finished'] },
      { type: 'speak', text: 'I have just finished the report', hint: 'Action récente' },
      { type: 'mcq', q: 'Have you ever ___ to London?', options: ['be', 'was', 'been', 'gone'], correct: 2 }
    ]
  },
  {
    id: 'b1_02', level: 'B1', module: 'Conditionals',
    title: 'Conditionnels',
    icon: '🔀', skill: 'grammar',
    vocabulary: [
      { en: 'If', fr: 'Si', ex: 'If you have time.' },
      { en: 'Would', fr: 'Conditionnel', ex: 'I would help you.' },
      { en: 'Could', fr: 'Pourrais', ex: 'I could come.' },
      { en: 'Might', fr: 'Pourrait peut-être', ex: 'I might be late.' },
      { en: 'Otherwise', fr: 'Sinon', ex: 'Hurry, otherwise we\'ll be late.' },
      { en: 'Unless', fr: 'À moins que', ex: 'Unless you call.' },
      { en: 'In case', fr: 'Au cas où', ex: 'In case of problems.' },
      { en: 'Provided', fr: 'À condition que', ex: 'Provided you agree.' },
      { en: 'Even if', fr: 'Même si', ex: 'Even if it rains.' },
      { en: 'As long as', fr: 'Tant que', ex: 'As long as you\'re happy.' }
    ],
    grammar: {
      title: 'Conditionnel 1 & 2',
      rules: ['Type 1 : If + present, will + verbe (réel)', 'If you call, I will answer', 'Type 2 : If + past, would + verbe (hypothétique)', 'If I had time, I would help']
    },
    exercises: [
      { type: 'mcq', q: 'If you ___, I will help', options: ['ask', 'asked', 'will ask', 'asking'], correct: 0 },
      { type: 'mcq', q: 'If I ___ you, I would accept', options: ['am', 'was', 'were', 'be'], correct: 2, exp: 'Avec hypothèse on dit "If I were"' },
      { type: 'fill', sentence: 'I ___ help if I had time', correct: 'would', hint: 'Conditionnel hypothétique' },
      { type: 'translate', fr: 'Si tu peux, appelle-moi', correct: 'if you can call me', keywords: ['if', 'can', 'call'] },
      { type: 'speak', text: 'If I had more time, I would learn Spanish', hint: 'Conditionnel hypothétique' }
    ]
  }
];

// ==========================================
// STATE MANAGEMENT
// ==========================================
let state = {
  currentPage: 'home',
  currentLesson: null,
  currentExercise: 0,
  hearts: 5,
  lessonAnswers: [],
  selectedOption: null,
  feedbackShown: false
};

let progress = {
  xp: 0,
  streak: 0,
  lastActivity: null,
  currentLevel: 'A1',
  lessonsCompleted: [],
  perfectLessons: 0,
  wordsLearned: 0,
  totalExercises: 0,
  correctAnswers: 0,
  voiceCount: 0,
  profession: 'general',
  weakWords: {},
  knownWords: {},
  unlockedAchievements: [],
  skills: {
    speaking: 0, listening: 0, reading: 0, writing: 0,
    vocabulary: 0, grammar: 0
  }
};

// ==========================================
// INIT & STORAGE
// ==========================================
function loadProgress() {
  try {
    const saved = localStorage.getItem('englishProV2');
    if (saved) progress = { ...progress, ...JSON.parse(saved) };
  } catch(e) { console.error(e); }
  
  // Update streak
  const today = new Date().toDateString();
  const last = progress.lastActivity ? new Date(progress.lastActivity).toDateString() : null;
  
  if (last !== today && last) {
    const yesterday = new Date();
    yesterday.setDate(yesterday.getDate() - 1);
    if (last !== yesterday.toDateString()) {
      progress.streak = 0; // Reset streak if more than 1 day
    }
  }
}

function saveProgress() {
  progress.lastActivity = new Date().toISOString();
  try {
    localStorage.setItem('englishProV2', JSON.stringify(progress));
  } catch(e) { console.error(e); }
}

function resetProgress() {
  if (confirm('Es-tu sûr de vouloir tout réinitialiser ? Cette action est irréversible.')) {
    localStorage.removeItem('englishProV2');
    location.reload();
  }
}

// ==========================================
// UI UPDATES
// ==========================================
function updateUI() {
  // Top bar
  document.getElementById('streakCount').textContent = progress.streak;
  document.getElementById('xpCount').textContent = progress.xp;
  
  // Greeting based on time
  const hour = new Date().getHours();
  let greeting = 'Bonjour';
  if (hour < 12) greeting = 'Bonjour ☀️';
  else if (hour < 18) greeting = 'Bon après-midi 🌤️';
  else greeting = 'Bonsoir 🌙';
  document.getElementById('greeting').textContent = greeting;
  
  // Hero
  const completionRate = (progress.lessonsCompleted.length / LESSONS.length) * 100;
  document.getElementById('heroProgress').style.width = completionRate + '%';
  document.getElementById('heroLessonsDone').textContent = progress.lessonsCompleted.length;
  document.getElementById('heroLevel').textContent = progress.currentLevel;
  
  // Stats
  document.getElementById('statXP').textContent = progress.xp;
  const accuracy = progress.totalExercises > 0
    ? Math.round((progress.correctAnswers / progress.totalExercises) * 100) : 0;
  document.getElementById('statAccuracy').textContent = accuracy + '%';
  document.getElementById('statWords').textContent = progress.wordsLearned;
  
  // Recommended lessons
  renderRecommendedLessons();
  renderAllLessons();
  renderVocabList();
  renderProfile();
  
  // Check achievements
  checkAchievements();
}

function renderRecommendedLessons() {
  const container = document.getElementById('recommendedLessons');
  const currentLevelLessons = LESSONS.filter(l => l.level === progress.currentLevel);
  const nextLessons = currentLevelLessons.filter(l => !progress.lessonsCompleted.includes(l.id)).slice(0, 3);
  
  if (nextLessons.length === 0) {
    container.innerHTML = '<div class="empty"><div class="empty-icon">🎉</div><div class="empty-title">Niveau ' + progress.currentLevel + ' terminé !</div><div class="empty-text">Passe au niveau suivant</div></div>';
    return;
  }
  
  container.innerHTML = nextLessons.map(lesson => `
    <div class="lesson-card" onclick="startLesson('${lesson.id}')">
      <div class="lesson-icon">${lesson.icon}</div>
      <div class="lesson-content">
        <div class="lesson-level-tag">${lesson.level} · ${lesson.module}</div>
        <div class="lesson-title">${lesson.title}</div>
        <div class="lesson-meta">
          <span>${lesson.vocabulary.length} mots</span>
          <span>·</span>
          <span>${lesson.exercises.length} exercices</span>
        </div>
      </div>
      <div class="lesson-arrow">›</div>
    </div>
  `).join('');
}

function renderAllLessons() {
  // Levels grid
  const levelGrid = document.getElementById('levelGrid');
  levelGrid.innerHTML = Object.entries(LEVELS).map(([key, lv]) => {
    const completed = LESSONS.filter(l => l.level === key && progress.lessonsCompleted.includes(l.id)).length;
    const total = LESSONS.filter(l => l.level === key).length;
    return `
      <div class="level-card ${progress.currentLevel === key ? 'active' : ''}" onclick="setLevel('${key}')">
        <div class="level-card-name">${key}</div>
        <div class="level-card-label">${lv.label}</div>
        <div class="level-card-progress">${completed}/${total}</div>
      </div>
    `;
  }).join('');
  
  document.getElementById('currentLevelTitle').textContent = progress.currentLevel + ' - ' + LEVELS[progress.currentLevel].label;
  
  // Lessons of current level
  const allContainer = document.getElementById('allLessons');
  const lessons = LESSONS.filter(l => l.level === progress.currentLevel);
  
  if (lessons.length === 0) {
    allContainer.innerHTML = '<div class="empty"><div class="empty-icon">🚧</div><div class="empty-title">Bientôt disponible</div><div class="empty-text">Ce niveau sera étendu prochainement. Reviens voir Claude !</div></div>';
    return;
  }
  
  allContainer.innerHTML = lessons.map((lesson, idx) => {
    const completed = progress.lessonsCompleted.includes(lesson.id);
    return `
      <div class="lesson-card ${completed ? 'completed' : ''}" onclick="startLesson('${lesson.id}')">
        <div class="lesson-icon ${completed ? 'completed' : ''}">${completed ? '✓' : lesson.icon}</div>
        <div class="lesson-content">
          <div class="lesson-level-tag">Leçon ${idx + 1} · ${lesson.module}</div>
          <div class="lesson-title">${lesson.title}</div>
          <div class="lesson-meta">
            <span>${lesson.vocabulary.length} mots</span>
            <span>·</span>
            <span>${lesson.exercises.length} exercices</span>
          </div>
        </div>
        <div class="lesson-arrow">›</div>
      </div>
    `;
  }).join('');
}

function setLevel(level) {
  progress.currentLevel = level;
  saveProgress();
  updateUI();
  showToast('🎯', 'Niveau ' + level + ' sélectionné');
}

function renderVocabList() {
  const container = document.getElementById('vocabList');
  const allWords = [];
  LESSONS.forEach(lesson => {
    lesson.vocabulary.forEach(word => {
      const key = word.en.toLowerCase();
      if (progress.knownWords[key]) {
        allWords.push({ ...word, lesson: lesson.title, isWeak: progress.weakWords[key] });
      }
    });
  });
  
  if (allWords.length === 0) {
    container.innerHTML = '<div class="empty"><div class="empty-icon">📖</div><div class="empty-title">Pas encore de vocabulaire</div><div class="empty-text">Commence une leçon pour apprendre des mots</div></div>';
    return;
  }
  
  container.innerHTML = allWords.map(word => `
    <div class="word-item">
      <div class="word-item-content">
        <div class="word-item-en">${word.en}${word.isWeak ? ' ⚠️' : ''}</div>
        <div class="word-item-fr">${word.fr}</div>
      </div>
      <button class="word-play" onclick="speakText('${word.en.replace(/'/g, "\\'")}')">▶</button>
    </div>
  `).join('');
}

function renderProfile() {
  // Profession
  const professionGrid = document.getElementById('professionGrid');
  professionGrid.innerHTML = PROFESSIONS.map(p => `
    <div class="profession-item ${progress.profession === p.id ? 'selected' : ''}" onclick="setProfession('${p.id}')">
      <div class="profession-icon">${p.icon}</div>
      <div>${p.name}</div>
    </div>
  `).join('');
  
  // Skills
  const skillsContainer = document.getElementById('skillsList');
  const skillNames = {
    speaking: '🎙️ Speaking',
    listening: '🎧 Listening',
    reading: '📖 Reading',
    writing: '✍️ Writing',
    vocabulary: '📚 Vocabulary',
    grammar: '⚙️ Grammar'
  };
  const colors = ['#6366F1', '#EC4899', '#10B981', '#F59E0B', '#3B82F6', '#8B5CF6'];
  
  skillsContainer.innerHTML = Object.entries(skillNames).map(([key, name], i) => {
    const value = Math.min(100, progress.skills[key] || 0);
    return `
      <div class="skill-row">
        <div class="skill-header">
          <div class="skill-name">${name}</div>
          <div class="skill-percent">${value}%</div>
        </div>
        <div class="skill-bar">
          <div class="skill-bar-fill" style="width: ${value}%; background: ${colors[i]}"></div>
        </div>
      </div>
    `;
  }).join('');
  
  // Achievements
  const achievementsContainer = document.getElementById('achievementsList');
  achievementsContainer.innerHTML = ACHIEVEMENTS.map(a => {
    const unlocked = progress.unlockedAchievements.includes(a.id);
    return `
      <div class="achievement ${unlocked ? 'unlocked' : 'locked'}">
        <div class="achievement-icon">${unlocked ? a.icon : '🔒'}</div>
        <div class="achievement-content">
          <div class="achievement-title">${a.title}</div>
          <div class="achievement-desc">${a.desc}</div>
        </div>
      </div>
    `;
  }).join('');
}

function setProfession(id) {
  progress.profession = id;
  saveProgress();
  updateUI();
  showToast('💼', 'Profil mis à jour');
}

function checkAchievements() {
  ACHIEVEMENTS.forEach(a => {
    if (!progress.unlockedAchievements.includes(a.id) && a.condition(progress)) {
      progress.unlockedAchievements.push(a.id);
      showToast(a.icon, 'Badge débloqué : ' + a.title);
      triggerConfetti();
    }
  });
  saveProgress();
}

// ==========================================
// NAVIGATION
// ==========================================
function switchPage(page, btn) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + page).classList.add('active');
  document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
  if (btn) btn.classList.add('active');
  state.currentPage = page;
  updateUI();
}

// ==========================================
// LESSON LOGIC
// ==========================================
function startLesson(lessonId) {
  const lesson = LESSONS.find(l => l.id === lessonId);
  if (!lesson) return;
  
  state.currentLesson = lesson;
  state.currentExercise = 0;
  state.hearts = 5;
  state.lessonAnswers = [];
  state.selectedOption = null;
  state.feedbackShown = false;
  
  document.getElementById('lessonPlayer').classList.add('active');
  renderLesson();
}

function closeLesson() {
  document.getElementById('lessonPlayer').classList.remove('active');
  state.currentLesson = null;
}

function renderLesson() {
  const lesson = state.currentLesson;
  if (!lesson) return;
  
  // Total = vocabulary intro + exercises + dialogue (if any)
  const hasIntro = state.currentExercise === 0;
  const totalSteps = lesson.exercises.length + (lesson.dialogue ? 1 : 0) + 1; // +1 for vocab intro
  
  // Update progress bar (we'll consider step 0 = vocab+grammar intro)
  let currentStep = state.currentExercise + 1;
  const progressPercent = (currentStep / totalSteps) * 100;
  document.getElementById('lessonProgressFill').style.width = progressPercent + '%';
  
  // Update hearts
  document.getElementById('lessonHearts').innerHTML = '❤️ ' + state.hearts;
  
  const body = document.getElementById('lessonBody');
  
  // Step 0: Show vocabulary + grammar intro
  if (state.currentExercise === 0 && !state.lessonAnswers.length) {
    let html = `
      <div class="exercise-prompt">Leçon</div>
      <div class="exercise-question">${lesson.title}</div>
    `;
    
    // Show first vocabulary card
    const firstWord = lesson.vocabulary[0];
    html += `
      <div class="vocab-card">
        <div class="vocab-word-en">${firstWord.en}</div>
        <div class="vocab-word-fr">${firstWord.fr}</div>
        <div class="vocab-example">"${firstWord.ex}"</div>
        <div class="vocab-controls">
          <button class="vocab-control-btn" onclick="speakText('${firstWord.en.replace(/'/g, "\\'")}')">🔊 Écouter</button>
        </div>
      </div>
    `;
    
    // Show grammar
    if (lesson.grammar) {
      html += `
        <div class="grammar-card">
          <div class="grammar-title">📐 ${lesson.grammar.title}</div>
          ${lesson.grammar.rules.map(r => `<div class="grammar-rule">• ${r}</div>`).join('')}
        </div>
      `;
    }
    
    html += `
      <div style="margin-top: auto;">
        <button class="continue-btn" onclick="startExercises()">Commencer les exercices →</button>
      </div>
    `;
    
    body.innerHTML = html;
    return;
  }
  
  // Show exercise (state.currentExercise is 1-indexed for actual exercises)
  const exerciseIndex = state.currentExercise - 1;
  
  // After last exercise, show dialogue if exists
  if (exerciseIndex >= lesson.exercises.length) {
    if (lesson.dialogue) {
      renderDialogue();
    } else {
      completeLesson();
    }
    return;
  }
  
  const ex = lesson.exercises[exerciseIndex];
  let html = '';
  
  if (ex.type === 'mcq') {
    html = `
      <div class="exercise-prompt">Question ${exerciseIndex + 1}/${lesson.exercises.length}</div>
      <div class="exercise-question">${ex.q}</div>
      <div class="options">
        ${ex.options.map((opt, i) => `
          <button class="option ${state.selectedOption === i ? (state.feedbackShown ? (i === ex.correct ? 'correct' : 'incorrect') : 'selected') : ''} ${state.feedbackShown && i === ex.correct ? 'correct' : ''}" onclick="selectOption(${i})">
            <div class="option-letter">${String.fromCharCode(65 + i)}</div>
            <div>${opt}</div>
          </button>
        `).join('')}
      </div>
      ${renderFeedback(ex)}
      <button class="continue-btn" onclick="${state.feedbackShown ? 'nextExercise()' : 'submitMCQ()'}" ${state.selectedOption === null && !state.feedbackShown ? 'disabled' : ''}>
        ${state.feedbackShown ? 'Continuer' : 'Vérifier'}
      </button>
    `;
  } else if (ex.type === 'fill') {
    html = `
      <div class="exercise-prompt">Question ${exerciseIndex + 1}/${lesson.exercises.length}</div>
      <div class="exercise-question">Complète :</div>
      <div class="exercise-sentence">${ex.sentence.replace('___', '<input type="text" id="fillInput" class="text-input" style="display:inline-block;width:140px;margin:0 4px;text-align:center" ' + (state.feedbackShown ? 'disabled' : 'autofocus') + '>')}</div>
      ${ex.hint && !state.feedbackShown ? `<div class="hint">💡 ${ex.hint}</div>` : ''}
      ${renderFeedback(ex)}
      <button class="continue-btn" onclick="${state.feedbackShown ? 'nextExercise()' : 'submitFill()'}">${state.feedbackShown ? 'Continuer' : 'Vérifier'}</button>
    `;
  } else if (ex.type === 'translate') {
    html = `
      <div class="exercise-prompt">Question ${exerciseIndex + 1}/${lesson.exercises.length}</div>
      <div class="exercise-question">Traduis en anglais :</div>
      <div class="exercise-sentence">${ex.fr}</div>
      <textarea class="text-input" id="translateInput" placeholder="Ta traduction..." ${state.feedbackShown ? 'disabled' : ''}></textarea>
      ${renderFeedback(ex)}
      <button class="continue-btn" onclick="${state.feedbackShown ? 'nextExercise()' : 'submitTranslate()'}">${state.feedbackShown ? 'Continuer' : 'Vérifier'}</button>
    `;
  } else if (ex.type === 'speak') {
    html = `
      <div class="exercise-prompt">Question ${exerciseIndex + 1}/${lesson.exercises.length}</div>
      <div class="exercise-question">Prononce cette phrase :</div>
      <div class="exercise-sentence">${ex.text}</div>
      <button class="speak-button" onclick="speakText('${ex.text.replace(/'/g, "\\'")}')">🔊 Écouter le modèle</button>
      ${ex.hint ? `<div class="hint">💡 ${ex.hint}</div>` : ''}
      <button class="voice-button" id="voiceBtn" onclick="toggleVoice('${ex.text.replace(/'/g, "\\'")}')">🎙️ Appuie pour parler</button>
      <div class="voice-status" id="voiceStatus"></div>
      <div class="voice-result" id="voiceResult" style="display:none"></div>
      ${renderFeedback(ex)}
      <button class="continue-btn" id="speakContinueBtn" onclick="nextExercise()" style="display:${state.feedbackShown ? 'block' : 'none'}">Continuer</button>
      <button class="continue-btn" onclick="skipSpeak()" style="background:var(--bg-elevated);color:var(--text-secondary);${state.feedbackShown ? 'display:none' : ''}">Passer</button>
    `;
  } else if (ex.type === 'listen') {
    html = `
      <div class="exercise-prompt">Question ${exerciseIndex + 1}/${lesson.exercises.length}</div>
      <div class="exercise-question">${ex.q}</div>
      <button class="voice-button" onclick="speakText('${ex.text.replace(/'/g, "\\'")}')">🔊 Écouter</button>
      <div class="options">
        ${ex.options.map((opt, i) => `
          <button class="option ${state.selectedOption === i ? (state.feedbackShown ? (i === ex.correct ? 'correct' : 'incorrect') : 'selected') : ''} ${state.feedbackShown && i === ex.correct ? 'correct' : ''}" onclick="selectOption(${i})">
            <div class="option-letter">${String.fromCharCode(65 + i)}</div>
            <div>${opt}</div>
          </button>
        `).join('')}
      </div>
      ${renderFeedback(ex)}
      <button class="continue-btn" onclick="${state.feedbackShown ? 'nextExercise()' : 'submitMCQ()'}" ${state.selectedOption === null && !state.feedbackShown ? 'disabled' : ''}>${state.feedbackShown ? 'Continuer' : 'Vérifier'}</button>
    `;
  }
  
  body.innerHTML = html;
}

function startExercises() {
  state.currentExercise = 1;
  // Mark vocabulary as learned
  state.currentLesson.vocabulary.forEach(w => {
    progress.knownWords[w.en.toLowerCase()] = true;
  });
  progress.wordsLearned = Object.keys(progress.knownWords).length;
  saveProgress();
  renderLesson();
}

function renderFeedback(ex) {
  if (!state.feedbackShown) return '';
  const correct = state.lessonAnswers[state.lessonAnswers.length - 1]?.correct;
  
  let correction = '';
  if (!correct) {
    if (ex.type === 'mcq' || ex.type === 'listen') correction = `<div class="feedback-correction">Bonne réponse : ${ex.options[ex.correct]}</div>`;
    else if (ex.type === 'fill') correction = `<div class="feedback-correction">Bonne réponse : ${ex.correct}</div>`;
    else if (ex.type === 'translate') correction = `<div class="feedback-correction">Bonne réponse : ${ex.correct}</div>`;
  }
  
  return `
    <div class="feedback ${correct ? 'correct' : 'incorrect'}">
      <div class="feedback-title">${correct ? '✅ Excellent !' : '❌ Pas tout à fait'}</div>
      <div class="feedback-text">${ex.exp || (correct ? 'Bien joué !' : 'Continue, tu vas y arriver !')}</div>
      ${correction}
    </div>
  `;
}

function selectOption(idx) {
  if (state.feedbackShown) return;
  state.selectedOption = idx;
  renderLesson();
}

function submitMCQ() {
  const lesson = state.currentLesson;
  const ex = lesson.exercises[state.currentExercise - 1];
  if (state.selectedOption === null) return;
  
  const correct = state.selectedOption === ex.correct;
  state.lessonAnswers.push({ correct, exercise: ex });
  state.feedbackShown = true;
  
  recordAnswer(correct, ex);
  renderLesson();
}

function submitFill() {
  const ex = state.currentLesson.exercises[state.currentExercise - 1];
  const input = document.getElementById('fillInput')?.value.trim().toLowerCase();
  if (!input) return;
  
  const correct = input === ex.correct.toLowerCase();
  state.lessonAnswers.push({ correct, exercise: ex });
  state.feedbackShown = true;
  
  recordAnswer(correct, ex);
  renderLesson();
}

function submitTranslate() {
  const ex = state.currentLesson.exercises[state.currentExercise - 1];
  const input = document.getElementById('translateInput')?.value.trim().toLowerCase();
  if (!input) return;
  
  // Check keywords
  const allKeywords = ex.keywords.every(k => input.includes(k.toLowerCase()));
  state.lessonAnswers.push({ correct: allKeywords, exercise: ex });
  state.feedbackShown = true;
  
  recordAnswer(allKeywords, ex);
  renderLesson();
}

function recordAnswer(correct, exercise) {
  progress.totalExercises++;
  if (correct) {
    progress.correctAnswers++;
    progress.xp += 10;
  } else {
    state.hearts--;
    progress.xp = Math.max(0, progress.xp + 2);
    
    // Track weak words
    if (exercise.type === 'fill' && exercise.correct) {
      progress.weakWords[exercise.correct.toLowerCase()] = (progress.weakWords[exercise.correct.toLowerCase()] || 0) + 1;
    }
  }
  
  // Update skill based on exercise type
  const skillMap = {
    mcq: 'grammar',
    fill: 'grammar',
    translate: 'writing',
    speak: 'speaking',
    listen: 'listening'
  };
  const skill = skillMap[exercise.type] || 'vocabulary';
  progress.skills[skill] = Math.min(100, (progress.skills[skill] || 0) + 1);
  
  saveProgress();
}

function nextExercise() {
  state.currentExercise++;
  state.selectedOption = null;
  state.feedbackShown = false;
  
  if (state.hearts <= 0) {
    showToast('💔', 'Plus de cœurs ! Relance la leçon');
    setTimeout(() => closeLesson(), 1500);
    return;
  }
  
  renderLesson();
}

function skipSpeak() {
  state.lessonAnswers.push({ correct: true, exercise: { type: 'speak' } });
  nextExercise();
}

function renderDialogue() {
  const lesson = state.currentLesson;
  const body = document.getElementById('lessonBody');
  
  let html = `
    <div class="exercise-prompt">Dialogue pratique</div>
    <div class="exercise-question">${lesson.dialogue.title}</div>
    <div style="margin-bottom: 16px;">
  `;
  
  lesson.dialogue.lines.forEach((line, i) => {
    html += `
      <div class="dialogue-line ${line.speaker === 'You' ? 'you' : ''}">
        <div class="dialogue-speaker">${line.speaker}</div>
        <div class="dialogue-text">${line.text}</div>
        <div class="dialogue-fr">${line.fr}</div>
        <div class="dialogue-controls">
          <button class="mini-btn" onclick="speakText('${line.text.replace(/'/g, "\\'")}')">🔊 Écouter</button>
        </div>
      </div>
    `;
  });
  
  html += `
    </div>
    <div class="hint">💡 Lis chaque ligne à voix haute en suivant l'audio</div>
    <button class="continue-btn" onclick="completeLesson()">Terminer la leçon ✓</button>
  `;
  
  body.innerHTML = html;
}

function completeLesson() {
  const lesson = state.currentLesson;
  
  if (!progress.lessonsCompleted.includes(lesson.id)) {
    progress.lessonsCompleted.push(lesson.id);
    progress.xp += 50;
    
    const allCorrect = state.lessonAnswers.every(a => a.correct);
    if (allCorrect) progress.perfectLessons++;
  }
  
  // Auto level up if all lessons of current level done
  const currentLessons = LESSONS.filter(l => l.level === progress.currentLevel);
  const allCompleted = currentLessons.every(l => progress.lessonsCompleted.includes(l.id));
  if (allCompleted) {
    const idx = levelOrder.indexOf(progress.currentLevel);
    if (idx < levelOrder.length - 1) {
      progress.currentLevel = levelOrder[idx + 1];
      showToast('🚀', 'Niveau ' + progress.currentLevel + ' débloqué !');
    }
  }
  
  // Update streak
  const today = new Date().toDateString();
  const last = progress.lastActivity ? new Date(progress.lastActivity).toDateString() : null;
  if (last !== today) {
    progress.streak++;
  }
  
  saveProgress();
  triggerConfetti();
  showToast('🎉', 'Leçon terminée ! +50 XP');
  
  setTimeout(() => {
    closeLesson();
    updateUI();
  }, 1500);
}

// ==========================================
// VOICE FEATURES
// ==========================================
let recognition = null;
let isRecording = false;

function initVoice() {
  const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
  if (!SpeechRecognition) return false;
  
  recognition = new SpeechRecognition();
  recognition.lang = 'en-US';
  recognition.continuous = false;
  recognition.interimResults = false;
  return true;
}

function speakText(text) {
  if (!('speechSynthesis' in window)) {
    showToast('⚠️', 'Synthèse vocale non disponible');
    return;
  }
  
  window.speechSynthesis.cancel();
  const utterance = new SpeechSynthesisUtterance(text);
  utterance.lang = 'en-US';
  utterance.rate = 0.9;
  utterance.pitch = 1;
  
  // Try to find a good English voice
  const voices = window.speechSynthesis.getVoices();
  const englishVoice = voices.find(v => v.lang.startsWith('en') && (v.name.includes('Samantha') || v.name.includes('Daniel') || v.name.includes('Karen'))) 
    || voices.find(v => v.lang.startsWith('en'));
  if (englishVoice) utterance.voice = englishVoice;
  
  window.speechSynthesis.speak(utterance);
}

function toggleVoice(targetText) {
  if (!recognition && !initVoice()) {
    showToast('⚠️', 'Reconnaissance vocale non disponible sur ce navigateur');
    return;
  }
  
  const btn = document.getElementById('voiceBtn');
  const status = document.getElementById('voiceStatus');
  const result = document.getElementById('voiceResult');
  
  if (isRecording) {
    recognition.stop();
    return;
  }
  
  isRecording = true;
  btn.classList.add('recording');
  btn.innerHTML = '🔴 Parle maintenant... (touche pour arrêter)';
  status.textContent = 'En écoute...';
  result.style.display = 'none';
  
  recognition.onresult = (event) => {
    const transcript = event.results[0][0].transcript;
    result.style.display = 'block';
    result.innerHTML = '<strong>Tu as dit :</strong> ' + transcript;
    
    // Compare
    const target = targetText.toLowerCase().replace(/[^a-z\s]/g, '').trim();
    const said = transcript.toLowerCase().replace(/[^a-z\s]/g, '').trim();
    
    // Calculate similarity
    const targetWords = target.split(/\s+/);
    const saidWords = said.split(/\s+/);
    const matches = targetWords.filter(w => saidWords.includes(w)).length;
    const similarity = (matches / targetWords.length) * 100;
    
    const correct = similarity >= 60;
    state.lessonAnswers.push({ correct, exercise: { type: 'speak' } });
    state.feedbackShown = true;
    
    progress.voiceCount++;
    recordAnswer(correct, { type: 'speak' });
    
    if (correct) {
      result.innerHTML += '<div style="color: var(--accent-success); margin-top: 8px; font-weight: 700;">✅ Bien prononcé ! (' + Math.round(similarity) + '% match)</div>';
    } else {
      result.innerHTML += '<div style="color: var(--accent-warning); margin-top: 8px; font-weight: 700;">🎯 ' + Math.round(similarity) + '% match - Réessaie !</div>';
    }
    
    document.getElementById('speakContinueBtn').style.display = 'block';
    saveProgress();
  };
  
  recognition.onerror = (event) => {
    status.textContent = 'Erreur : ' + event.error;
    isRecording = false;
    btn.classList.remove('recording');
    btn.innerHTML = '🎙️ Réessayer';
  };
  
  recognition.onend = () => {
    isRecording = false;
    btn.classList.remove('recording');
    btn.innerHTML = '🎙️ Reparler';
    if (!document.getElementById('voiceResult').textContent) {
      status.textContent = '';
    }
  };
  
  try {
    recognition.start();
  } catch(e) {
    showToast('⚠️', 'Impossible de démarrer la reconnaissance');
    isRecording = false;
    btn.classList.remove('recording');
  }
}

// ==========================================
// QUICK PRACTICE
// ==========================================
function startQuickPractice(type) {
  // Find a relevant lesson
  let lesson;
  if (type === 'speaking') {
    lesson = LESSONS.find(l => l.level === progress.currentLevel && l.exercises.some(e => e.type === 'speak'));
  } else if (type === 'listening') {
    lesson = LESSONS.find(l => l.level === progress.currentLevel && l.exercises.some(e => e.type === 'listen'));
  } else if (type === 'vocabulary') {
    showVocabReview();
    return;
  } else {
    lesson = LESSONS.find(l => l.level === progress.currentLevel && !progress.lessonsCompleted.includes(l.id));
  }
  
  if (lesson) startLesson(lesson.id);
  else showToast('💡', 'Pas de pratique rapide disponible. Essaie une leçon complète !');
}

function showVocabReview() {
  const allKnownWords = [];
  LESSONS.forEach(l => {
    l.vocabulary.forEach(w => {
      if (progress.knownWords[w.en.toLowerCase()]) allKnownWords.push(w);
    });
  });
  
  if (allKnownWords.length < 5) {
    showToast('📚', 'Apprends d\'abord plus de mots !');
    return;
  }
  
  // Pick random 10
  const shuffled = allKnownWords.sort(() => Math.random() - 0.5).slice(0, 10);
  showCardReview(shuffled, 0);
}

function showCardReview(words, index) {
  if (index >= words.length) {
    closeModal();
    showToast('✨', 'Révision terminée !');
    return;
  }
  
  const word = words[index];
  document.getElementById('modalBody').innerHTML = `
    <div style="text-align: center;">
      <div style="font-size: 13px; color: var(--text-secondary); margin-bottom: 8px;">Carte ${index + 1}/${words.length}</div>
      <div class="vocab-card" style="margin-bottom: 16px;">
        <div class="vocab-word-en">${word.en}</div>
        <div class="vocab-word-fr">${word.fr}</div>
        <div class="vocab-example">"${word.ex}"</div>
      </div>
      <button class="speak-button" onclick="speakText('${word.en.replace(/'/g, "\\'")}')">🔊 Écouter</button>
      <div style="display: flex; gap: 8px; margin-top: 16px;">
        <button class="continue-btn" style="background: var(--gradient-danger);" onclick="markWeak('${word.en}'); showCardReview(${JSON.stringify(words).replace(/"/g, '&quot;')}, ${index + 1})">😕 Difficile</button>
        <button class="continue-btn" onclick="showCardReview(${JSON.stringify(words).replace(/"/g, '&quot;')}, ${index + 1})">😊 Connu</button>
      </div>
    </div>
  `;
  document.getElementById('modal').classList.add('active');
}

function markWeak(word) {
  progress.weakWords[word.toLowerCase()] = (progress.weakWords[word.toLowerCase()] || 0) + 1;
  saveProgress();
}

function reviewWeakWords() {
  const weakWords = [];
  Object.keys(progress.weakWords).forEach(key => {
    LESSONS.forEach(l => {
      const found = l.vocabulary.find(w => w.en.toLowerCase() === key);
      if (found) weakWords.push(found);
    });
  });
  
  if (weakWords.length === 0) {
    showToast('🎯', 'Aucun mot difficile à réviser !');
    return;
  }
  
  showCardReview(weakWords.slice(0, 10), 0);
}

// ==========================================
// URGENCY MODE
// ==========================================
function openUrgencyMode() {
  document.getElementById('modalBody').innerHTML = `
    <h2 style="margin-bottom: 16px; font-size: 22px;">⚡ Mode Urgence</h2>
    <p style="color: var(--text-secondary); margin-bottom: 20px; font-size: 14px;">Choisis ta situation pour un coaching express :</p>
    
    <div style="display: flex; flex-direction: column; gap: 10px;">
      <button class="quick-action" style="text-align: left; flex-direction: row; align-items: center;" onclick="showUrgencyContent('meeting')">
        <div class="quick-action-icon" style="background: var(--gradient-primary)">👥</div>
        <div>
          <div class="quick-action-title">Réunion dans peu</div>
          <div class="quick-action-desc">Vocabulaire & phrases clés</div>
        </div>
      </button>
      <button class="quick-action" style="text-align: left; flex-direction: row; align-items: center;" onclick="showUrgencyContent('call')">
        <div class="quick-action-icon" style="background: var(--gradient-warning)">📞</div>
        <div>
          <div class="quick-action-title">Appel client</div>
          <div class="quick-action-desc">Pour parler au téléphone</div>
        </div>
      </button>
      <button class="quick-action" style="text-align: left; flex-direction: row; align-items: center;" onclick="showUrgencyContent('email')">
        <div class="quick-action-icon" style="background: var(--gradient-cool)">📧</div>
        <div>
          <div class="quick-action-title">Email à écrire</div>
          <div class="quick-action-desc">Modèles & formules</div>
        </div>
      </button>
      <button class="quick-action" style="text-align: left; flex-direction: row; align-items: center;" onclick="showUrgencyContent('presentation')">
        <div class="quick-action-icon" style="background: var(--gradient-success)">🎤</div>
        <div>
          <div class="quick-action-title">Présentation</div>
          <div class="quick-action-desc">Phrases pour présenter</div>
        </div>
      </button>
      <button class="quick-action" style="text-align: left; flex-direction: row; align-items: center;" onclick="showUrgencyContent('interview')">
        <div class="quick-action-icon" style="background: var(--gradient-danger)">💼</div>
        <div>
          <div class="quick-action-title">Entretien</div>
          <div class="quick-action-desc">Questions & réponses types</div>
        </div>
      </button>
    </div>
  `;
  document.getElementById('modal').classList.add('active');
}

const URGENCY_CONTENT = {
  meeting: {
    title: '👥 Phrases pour réunion',
    phrases: [
      { en: 'Let\'s start the meeting', fr: 'Commençons la réunion' },
      { en: 'Could you repeat that, please?', fr: 'Pouvez-vous répéter ?' },
      { en: 'I agree with you', fr: 'Je suis d\'accord' },
      { en: 'I disagree, here\'s why...', fr: 'Pas d\'accord, voici pourquoi...' },
      { en: 'Can I ask a question?', fr: 'Puis-je poser une question ?' },
      { en: 'Let\'s move on to the next topic', fr: 'Passons au sujet suivant' },
      { en: 'To summarize...', fr: 'Pour résumer...' },
      { en: 'What are the next steps?', fr: 'Quelles sont les prochaines étapes ?' },
      { en: 'Let\'s wrap up', fr: 'Concluons' },
      { en: 'I\'ll send you a follow-up email', fr: 'Je vous enverrai un email de suivi' }
    ]
  },
  call: {
    title: '📞 Appels téléphoniques',
    phrases: [
      { en: 'Hello, this is [Name] speaking', fr: 'Bonjour, c\'est [Nom] à l\'appareil' },
      { en: 'May I speak to Mr. Smith, please?', fr: 'Puis-je parler à M. Smith ?' },
      { en: 'I\'m calling about...', fr: 'J\'appelle au sujet de...' },
      { en: 'Could you speak more slowly, please?', fr: 'Plus lentement, s\'il vous plaît' },
      { en: 'Sorry, I didn\'t catch that', fr: 'Désolé, je n\'ai pas compris' },
      { en: 'Could you spell that for me?', fr: 'Pouvez-vous épeler ?' },
      { en: 'Let me check and call you back', fr: 'Je vérifie et je vous rappelle' },
      { en: 'Can I leave a message?', fr: 'Puis-je laisser un message ?' },
      { en: 'Thank you for your time', fr: 'Merci pour votre temps' },
      { en: 'Have a nice day', fr: 'Bonne journée' }
    ]
  },
  email: {
    title: '📧 Email professionnel',
    phrases: [
      { en: 'I hope this email finds you well', fr: 'J\'espère que vous allez bien' },
      { en: 'I am writing to inform you that...', fr: 'Je vous écris pour vous informer que...' },
      { en: 'Following up on our conversation', fr: 'Suite à notre conversation' },
      { en: 'Please find attached', fr: 'Veuillez trouver ci-joint' },
      { en: 'Could you please confirm...', fr: 'Pourriez-vous confirmer...' },
      { en: 'I would appreciate if...', fr: 'Je vous saurais gré de...' },
      { en: 'Thank you for your prompt reply', fr: 'Merci pour votre réponse rapide' },
      { en: 'I look forward to hearing from you', fr: 'Dans l\'attente de votre retour' },
      { en: 'Please let me know if you have any questions', fr: 'N\'hésitez pas si vous avez des questions' },
      { en: 'Best regards', fr: 'Cordialement' }
    ]
  },
  presentation: {
    title: '🎤 Présentation',
    phrases: [
      { en: 'Good morning everyone, thank you for coming', fr: 'Bonjour tout le monde, merci d\'être venus' },
      { en: 'Today, I\'ll be talking about...', fr: 'Aujourd\'hui, je vais parler de...' },
      { en: 'My presentation is divided into three parts', fr: 'Ma présentation se divise en 3 parties' },
      { en: 'Let me start by...', fr: 'Permettez-moi de commencer par...' },
      { en: 'As you can see on this slide', fr: 'Comme vous pouvez le voir sur cette diapo' },
      { en: 'Let\'s move on to...', fr: 'Passons à...' },
      { en: 'In conclusion...', fr: 'En conclusion...' },
      { en: 'Thank you for your attention', fr: 'Merci pour votre attention' },
      { en: 'Are there any questions?', fr: 'Avez-vous des questions ?' },
      { en: 'That\'s a great question', fr: 'Excellente question' }
    ]
  },
  interview: {
    title: '💼 Entretien d\'embauche',
    phrases: [
      { en: 'Tell me about yourself', fr: 'Parlez-moi de vous' },
      { en: 'I have X years of experience in...', fr: 'J\'ai X ans d\'expérience en...' },
      { en: 'My greatest strength is...', fr: 'Ma plus grande force est...' },
      { en: 'I am looking for new challenges', fr: 'Je cherche de nouveaux défis' },
      { en: 'What are the responsibilities?', fr: 'Quelles sont les responsabilités ?' },
      { en: 'I am a team player', fr: 'Je travaille bien en équipe' },
      { en: 'I\'m passionate about...', fr: 'Je suis passionné par...' },
      { en: 'Why are you interested in this position?', fr: 'Pourquoi ce poste vous intéresse ?' },
      { en: 'When can you start?', fr: 'Quand pouvez-vous commencer ?' },
      { en: 'Thank you for this opportunity', fr: 'Merci pour cette opportunité' }
    ]
  }
};

function showUrgencyContent(type) {
  const content = URGENCY_CONTENT[type];
  document.getElementById('modalBody').innerHTML = `
    <h2 style="margin-bottom: 16px; font-size: 20px;">${content.title}</h2>
    <p style="color: var(--text-secondary); margin-bottom: 16px; font-size: 13px;">Touche 🔊 pour écouter chaque phrase</p>
    ${content.phrases.map(p => `
      <div class="word-item">
        <div class="word-item-content">
          <div class="word-item-en">${p.en}</div>
          <div class="word-item-fr">${p.fr}</div>
        </div>
        <button class="word-play" onclick="speakText('${p.en.replace(/'/g, "\\'")}')">▶</button>
      </div>
    `).join('')}
    <button class="continue-btn" onclick="closeModal()" style="margin-top: 16px;">Fermer</button>
  `;
}

function closeModal() {
  document.getElementById('modal').classList.remove('active');
}

document.getElementById('modal').addEventListener('click', (e) => {
  if (e.target.id === 'modal') closeModal();
});

// ==========================================
// EFFECTS
// ==========================================
function showToast(icon, text) {
  const toast = document.getElementById('toast');
  document.getElementById('toastIcon').textContent = icon;
  document.getElementById('toastText').textContent = text;
  toast.classList.add('show');
  setTimeout(() => toast.classList.remove('show'), 3000);
}

function triggerConfetti() {
  const container = document.getElementById('confettiContainer');
  const colors = ['#6366F1', '#EC4899', '#10B981', '#F59E0B', '#3B82F6'];
  
  for (let i = 0; i < 30; i++) {
    setTimeout(() => {
      const confetti = document.createElement('div');
      confetti.className = 'confetti';
      confetti.style.left = Math.random() * 100 + '%';
      confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
      confetti.style.animationDelay = Math.random() * 0.5 + 's';
      confetti.style.animationDuration = (2 + Math.random() * 2) + 's';
      container.appendChild(confetti);
      
      setTimeout(() => confetti.remove(), 3500);
    }, i * 50);
  }
}

// ==========================================
// PWA INSTALL
// ==========================================
function checkInstall() {
  // Show banner if Safari iOS not in standalone mode
  const isIOS = /iPad|iPhone|iPod/.test(navigator.userAgent);
  const isStandalone = window.navigator.standalone === true;
  if (isIOS && !isStandalone && !localStorage.getItem('installDismissed')) {
    setTimeout(() => {
      document.getElementById('installBanner').classList.add('show');
    }, 2000);
  }
}

// ==========================================
// INIT
// ==========================================
window.addEventListener('load', () => {
  loadProgress();
  initVoice();
  // Force voices to load
  if ('speechSynthesis' in window) {
    window.speechSynthesis.getVoices();
    window.speechSynthesis.onvoiceschanged = () => window.speechSynthesis.getVoices();
  }
  updateUI();
  checkInstall();
  
  // Welcome message
  if (progress.totalExercises === 0) {
    setTimeout(() => showToast('👋', 'Bienvenue ! Commence ta première leçon'), 1000);
  } else if (progress.streak > 0) {
    setTimeout(() => showToast('🔥', progress.streak + ' jours d\'affilée ! Continue !'), 1000);
  }
});

// Handle PWA back gesture
window.addEventListener('popstate', (e) => {
  if (state.currentLesson) {
    closeLesson();
    e.preventDefault();
  } else if (document.getElementById('modal').classList.contains('active')) {
    closeModal();
    e.preventDefault();
  }
});
</script>

</body>
</html>

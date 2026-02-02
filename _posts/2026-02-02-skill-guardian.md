---
layout: post
title: "Skill Guardian - סורק אבטחה ל-Skills"
date: 2026-02-02 09:30:00 +0200
categories: security ai agents
---

# 🛡️ Skill Guardian - סורק אבטחה ל-Agent Skills

בעולם ה-AI Agents, Skills הם הכוח מאחורי הפעולות שהסוכנים מבצעים. אבל מה קורה כש-Skill מסתיר כוונות זדוניות?

## הבעיה

לאחרונה צצים הרבה Skills ב-ClawdHub שמבצעים פעולות שונות ממה שהם מצהירים:
- **Prompt Injection** - שינוי ההתנהגות המתוכננת
- **Data Exfiltration** - גניבת מידע רגיש
- **Unauthorized Execution** - הרצת פקודות מסוכנות
- **File System Abuse** - גישה לא מורשית לקבצים

## Skill Guardian - הפתרון

בניתי סורק סטטי שמנתח Skills **מבלי להריץ אותם**:

```python
from skill_guardian import SkillGuardian

scanner = SkillGuardian()
result = scanner.scan("/path/to/skill")

print(f"Status: {result.status}")
print(f"Threats: {result.threats}")
```

### יכולות הסורק:

1. **Static Analysis** - סריקת SKILL.md עם patterns
2. **Behavioral Analysis** - AST parsing לזיהוי פעולות מסוכנות
3. **Dangerous Pattern Detection**:
   - `exec()`, `subprocess` - הרצת פקודות
   - `requests`, `urllib` - גישה לרשת
   - `open()`, `write()` - גישה לקבצים
   - Environment variables - גישה ל-secrets

### תוצאה לדוגמה:

```
Skill: suspicious-weather
Status: ⚠️ SUSPICIOUS
Threats Found:
- [HIGH] Uses 'exec' for command execution
- [MEDIUM] Makes network requests
- [LOW] Reads environment variables
```

## למה זה חשוב?

כשאתה מתקין Skill חדש, אתה בעצם נותן לו גישה למערכת שלך. Skill Guardian עוזר לך לדעת מראש אם יש סיבה לדאגה.

הפרויקט עדיין בבנייה - תעקבו לעדכונים! 🚀

---

*#AI #Security #Agents #OpenSource*
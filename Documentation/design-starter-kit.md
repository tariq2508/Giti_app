# Design Starter Kit: Personal Music Streamer App

A simple, elegant design system for the music streamer app, using a light color palette with light green, light blue, and white. This kit provides a foundation for consistent, beautiful UI across iOS, Android, and Web.

---

## 1. Color Palette

| Name           | Color Code | Usage                        |
|----------------|------------|------------------------------|
| Primary Green  | #7ED957    | Primary actions, highlights  |
| Accent Blue    | #6EC1E4    | Secondary actions, links     |
| Background     | #FFFFFF    | App background, cards        |
| Light Gray     | #F5F7FA    | Surfaces, input backgrounds  |
| Text Dark      | #222B45    | Main text                    |
| Text Light     | #8F9BB3    | Secondary text, placeholders |
| Border         | #E4E9F2    | Dividers, borders            |

---

## 2. Typography

- **Font Family:**
  - System default (San Francisco for iOS, Roboto for Android, Segoe UI for Web)
- **Font Weights:**
  - Regular, Medium, Bold
- **Font Sizes:**
  - Title: 24-28px
  - Subtitle: 18-20px
  - Body: 16px
  - Caption: 12-14px

---

## 3. Spacing & Layout

- **Spacing Scale:** 4, 8, 16, 24, 32 px
- **Border Radius:** 12px (cards, buttons, inputs)
- **Elevation/Shadow:**
  - Subtle shadow for cards: `0 2px 8px rgba(110, 193, 228, 0.08)`
- **Container Width:**
  - Mobile: 90% of screen width
  - Web: Max 1200px, centered

---

## 4. Buttons

- **Primary Button**
  - Background: #7ED957 (Primary Green)
  - Text: #FFFFFF
  - Border Radius: 12px
  - Padding: 12px 24px
  - Shadow: Yes (subtle)

- **Secondary Button**
  - Background: #6EC1E4 (Accent Blue)
  - Text: #FFFFFF
  - Border Radius: 12px
  - Padding: 12px 24px
  - Shadow: Yes (subtle)

- **Text Button**
  - Background: transparent
  - Text: #6EC1E4 (Accent Blue)
  - Padding: 8px 12px

---

## 5. Inputs & Forms

- **Input Background:** #F5F7FA (Light Gray)
- **Border:** 1px solid #E4E9F2
- **Text:** #222B45
- **Placeholder:** #8F9BB3
- **Border Radius:** 12px
- **Padding:** 12px

---

## 6. Example UI Components

### Card
```jsx
<View style={{
  backgroundColor: '#FFFFFF',
  borderRadius: 12,
  padding: 16,
  shadowColor: '#6EC1E4',
  shadowOpacity: 0.08,
  shadowRadius: 8,
  shadowOffset: { width: 0, height: 2 },
  marginBottom: 16,
}}>
  {/* Content here */}
</View>
```

### Primary Button
```jsx
<TouchableOpacity style={{
  backgroundColor: '#7ED957',
  borderRadius: 12,
  paddingVertical: 12,
  paddingHorizontal: 24,
  shadowColor: '#6EC1E4',
  shadowOpacity: 0.08,
  shadowRadius: 8,
  shadowOffset: { width: 0, height: 2 },
}}>
  <Text style={{ color: '#FFFFFF', fontWeight: 'bold', fontSize: 16 }}>Play</Text>
</TouchableOpacity>
```

### Input
```jsx
<TextInput
  style={{
    backgroundColor: '#F5F7FA',
    borderColor: '#E4E9F2',
    borderWidth: 1,
    borderRadius: 12,
    padding: 12,
    color: '#222B45',
    fontSize: 16,
  }}
  placeholder="Search..."
  placeholderTextColor="#8F9BB3"
/>
```

---

## 7. Iconography
- Use simple, line-based icons (e.g., [Feather Icons](https://feathericons.com/), [Material Icons](https://fonts.google.com/icons))
- Icon color: #6EC1E4 (Accent Blue) or #8F9BB3 (Text Light)

---

## 8. Imagery & Album Art
- Album art and images should have rounded corners (12px radius)
- Use subtle drop shadows for elevation

---

## 9. Example Screen Layout

```
+-------------------------------+
|        App Bar (Title)        |
+-------------------------------+
|  Search Input                 |
+-------------------------------+
|  Playlist Card                |
|  (Album Art, Title, Artist)   |
+-------------------------------+
|  Primary Button (Play)        |
+-------------------------------+
```

---

## 10. Usage Tips
- Keep UI clean and uncluttered
- Use plenty of white space
- Use green for primary actions, blue for secondary
- Use subtle shadows and rounded corners for a modern look

---

This starter kit is a foundation—feel free to expand and adapt as the app grows! 
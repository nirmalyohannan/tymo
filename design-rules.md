# UI Design Rules

### Material Design Standards

1. **Typography**:

   - Use Material Design typography scale
   - Primary text: Roboto 16sp
   - Secondary text: Roboto 14sp
   - Headlines: Roboto 20sp-96sp

2. **Color System**:

   - Primary text: #000000 (black)
   - Secondary text: #333333 (dark gray)
   - Background: #FFFFFF (white)
   - Surface: #F5F5F5 (light gray)
   - Error color: #B00020 (red)
   - Dark mode text: #FFFFFF (white)
   - Dark mode background: #121212 (dark)
   - Dark mode surface: #1E1E1E (darker gray)
   - Avoid saturated colors, use grayscale tones

3. **Elevation**:

   - Cards: 1dp-12dp elevation
   - Dialogs: 24dp elevation
   - Floating Action Button: 6dp elevation

4. **Spacing**:

   - Small: 8dp
   - Medium: 16dp
   - Large: 24dp
   - Extra Large: 32dp

5. **Shape**:

   - Small components: 4dp rounded corners
   - Medium components: 8dp rounded corners
   - Large components: 16dp rounded corners

6. **Iconography**:
   - Use Material Icons
   - Standard size: 24dp
   - Small size: 18dp

### Light/Dark Mode Implementation

1. **Theme Setup**:

   - Define ThemeData for both light/dark modes
   - Use Theme.of(context) for styling
   - Implement theme switching via Provider/Bloc

2. **Text Contrast**:

   - Light mode: Dark text on light background
   - Dark mode: Light text on dark background
   - Minimum contrast ratio: 4.5:1

3. **Image Adaptation**:

   - Use ColorFiltered for dark mode images
   - Provide alternative assets if needed

4. **Elevation Adjustments**:

   - Increase elevation slightly in dark mode
   - Elements which are interactive and elevated should animate hover slightly on hover

5. **Accessibility**:
   - Support dynamic type scaling
   - Ensure touch targets ≥48dp
   - Provide semantic labels
   - Test with screen readers

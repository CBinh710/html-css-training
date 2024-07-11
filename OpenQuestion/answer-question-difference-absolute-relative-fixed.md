
# What is the difference between position: absolute, relative, fixed?

1. **`position: static`** (Default):
   - Every element starts with this position.
   - It follows the normal flow of the document.
   - No special positioning behavior.
   - Rarely used explicitly.

2. **`position: relative`**:
   - Relative to its normal position (itself).
   - If no other positioning attributes (e.g., `top`, `left`, etc.) are set, it behaves like `static`.
   - Useful for shifting an element based on its regular position.
   - Commonly used for fine-tuning alignment.

3. **`position: absolute`**:
   - Positioned relative to the nearest positioned ancestor (or the document body if none).
   - Taken out of the normal flow (other elements act as if it doesn't exist).
   - Useful for creating overlays, tooltips, or absolutely positioned elements within a container.

4. **`position: fixed`**:
   - Positioned relative to the viewport (browser window).
   - Doesn't move with scrolling; stays fixed in place.
   - Ignores any relative parents (or ancestors).
   - Great for sticky headers, navigation bars, or persistent elements.

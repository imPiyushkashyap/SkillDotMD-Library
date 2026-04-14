---
name: remotion
description: Use this skill when working with Remotion. Triggers when user mentions Remotion or imports from it.
---

# Remotion

## What this is
Remotion is a tool for creating videos programmatically using React. It allows developers to create high-quality videos with dynamic content, animations, and effects. With Remotion, you can render videos on the server or client-side, making it a versatile solution for various use cases.

## Installation
```bash
npm install remotion
```

## Key concepts
Remotion provides several key concepts for creating videos, including:
* **Composition**: The root component of a Remotion video, which can contain other components, videos, or images.
* **Video**: A component that renders a video, which can be used as a child of a Composition.
* **Audio**: A component that renders an audio track, which can be used to add sound to a video.
* **Sequence**: A component that renders a sequence of videos or images.

Example:
```jsx
import { Video, Sequence } from 'remotion';

const MyVideo = () => {
  return (
    <Sequence>
      <Video src="https://example.com/video1.mp4" />
      <Video src="https://example.com/video2.mp4" />
    </Sequence>
  );
};
```

## Correct usage patterns
To create a video with Remotion, you need to create a Composition component and render it using the `render` function.
```jsx
import { render } from 'remotion';

const MyComposition = () => {
  return (
    <div>
      <h1>Hello World!</h1>
    </div>
  );
};

render(<MyComposition />, {
  width: 1080,
  height: 720,
  fps: 30,
});
```

## Common mistakes to avoid
* Forgetting to import the necessary components from Remotion.
* Not providing the correct props to the Composition component.
* Not handling errors properly when rendering a video.

## File and folder conventions
Remotion projects typically have the following structure:
* `src`: The source code directory, which contains the Composition and other components.
* `public`: The public directory, which contains the rendered video files.
* `remotion.config.js`: The configuration file, which specifies the rendering options and other settings.
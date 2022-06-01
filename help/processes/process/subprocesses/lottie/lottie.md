## Lottie

Upload a Lottie animation, which should be rendered in the conversation background. 

Lottie is a file format for vectorial animation and a lighter alternative to animated GIFs. You can design your own Lottie animations with Adobe After Effects or find a large number of Lottie animations at [lottiefiles.com](https://lottiefiles.com).

To use a Lottie animation in LoyJoy, upload a Lottie animation JSON file in the Lottie process module. The animation will be rendered in the chat background when passing through the Lottie process module.

Further configuration options are:

- Alignment: Align the Lottie animation at the top,center,bottom,right and left of the chat background.
- Size adjustment: With `Meet` the Lottie animation will be fully visible, eventually leading to borders around the animation. With `Slice` the Lottie animation will be visible in cover mode, filling the complete chat background, however being cut to fit the chat background.
- Loop Lottie animation: Normally a Lottie animation stops after reaching the end of its timeline. This options restarts the Lottie animation from the start, with infinite loops by default.
- Number of loops: Limit the number of loops from infitie to a specific number.
- Freeze last frame: After completing the last loop, the Lottie animation by default will disappear. With this option the Lottie animation will stay in the chat background.

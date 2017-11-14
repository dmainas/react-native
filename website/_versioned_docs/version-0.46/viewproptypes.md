---
id: version-0.46-viewproptypes
original_id: viewproptypes
title: viewproptypes
---
<a id="content"></a><h1><a class="anchor" name="viewproptypes"></a>ViewPropTypes <a class="hash-link" href="docs/viewproptypes.html#viewproptypes">#</a></h1><div><noscript></noscript><h3><a class="anchor" name="props"></a>Props <a class="hash-link" href="docs/viewproptypes.html#props">#</a></h3><div class="props"><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilitylabel"></a>accessibilityLabel?: <span class="propType">node</span> <a class="hash-link" href="docs/viewproptypes.html#accessibilitylabel">#</a></h4><div><p>Overrides the text that's read by the screen reader when the user interacts
with the element. By default, the label is constructed by traversing all the
children and accumulating all the <code>Text</code> nodes separated by space.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessible"></a>accessible?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#accessible">#</a></h4><div><p>When <code>true</code>, indicates that the view is an accessibility element. By default,
all the touchable elements are accessible.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="hitslop"></a>hitSlop?: <span class="propType">{top: number, left: number, bottom: number, right: number}</span> <a class="hash-link" href="docs/viewproptypes.html#hitslop">#</a></h4><div><p>This defines how far a touch event can start away from the view.
Typical interface guidelines recommend touch targets that are at least
30 - 40 points/density-independent pixels.</p><p>For example, if a touchable view has a height of 20 the touchable height can be extended to
40 with <code>hitSlop={{top: 10, bottom: 10, left: 0, right: 0}}</code></p><blockquote><p>The touch area never extends past the parent view bounds and the Z-index
of sibling views always takes precedence if a touch hits two overlapping
views.</p></blockquote></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onaccessibilitytap"></a>onAccessibilityTap?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onaccessibilitytap">#</a></h4><div><p>When <code>accessible</code> is true, the system will try to invoke this function
when the user performs accessibility tap gesture.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onlayout"></a>onLayout?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onlayout">#</a></h4><div><p>Invoked on mount and layout changes with:</p><p><code>{nativeEvent: { layout: {x, y, width, height}}}</code></p><p>This event is fired immediately once the layout has been calculated, but
the new layout may not yet be reflected on the screen at the time the
event is received, especially if a layout animation is in progress.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onmagictap"></a>onMagicTap?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onmagictap">#</a></h4><div><p>When <code>accessible</code> is <code>true</code>, the system will invoke this function when the
user performs the magic tap gesture.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onmoveshouldsetresponder"></a>onMoveShouldSetResponder?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onmoveshouldsetresponder">#</a></h4><div><p>Does this view want to "claim" touch responsiveness? This is called for every touch move on
the <code>View</code> when it is not the responder.</p><p><code>View.props.onMoveShouldSetResponder: (event) =&gt; [true | false]</code>, where <code>event</code> is a
synthetic touch event as described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onmoveshouldsetrespondercapture"></a>onMoveShouldSetResponderCapture?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onmoveshouldsetrespondercapture">#</a></h4><div><p>If a parent <code>View</code> wants to prevent a child <code>View</code> from becoming responder on a move,
it should have this handler which returns <code>true</code>.</p><p><code>View.props.onMoveShouldSetResponderCapture: (event) =&gt; [true | false]</code>, where <code>event</code> is a
synthetic touch event as described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onrespondergrant"></a>onResponderGrant?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onrespondergrant">#</a></h4><div><p>The View is now responding for touch events. This is the time to highlight and show the user
what is happening.</p><p><code>View.props.onResponderGrant: (event) =&gt; {}</code>, where <code>event</code> is a synthetic touch event as
described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onrespondermove"></a>onResponderMove?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onrespondermove">#</a></h4><div><p>The user is moving their finger.</p><p><code>View.props.onResponderMove: (event) =&gt; {}</code>, where <code>event</code> is a synthetic touch event as
described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderreject"></a>onResponderReject?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onresponderreject">#</a></h4><div><p>Another responder is already active and will not release it to that <code>View</code> asking to be
the responder.</p><p><code>View.props.onResponderReject: (event) =&gt; {}</code>, where <code>event</code> is a synthetic touch event as
described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderrelease"></a>onResponderRelease?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onresponderrelease">#</a></h4><div><p>Fired at the end of the touch.</p><p><code>View.props.onResponderRelease: (event) =&gt; {}</code>, where <code>event</code> is a synthetic touch event as
described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderterminate"></a>onResponderTerminate?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onresponderterminate">#</a></h4><div><p>The responder has been taken from the <code>View</code>. Might be taken by other views after a call to
<code>onResponderTerminationRequest</code>, or might be taken by the OS without asking (e.g., happens
with control center/ notification center on iOS)</p><p><code>View.props.onResponderTerminate: (event) =&gt; {}</code>, where <code>event</code> is a synthetic touch event as
described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderterminationrequest"></a>onResponderTerminationRequest?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onresponderterminationrequest">#</a></h4><div><p>Some other <code>View</code> wants to become responder and is asking this <code>View</code> to release its
responder. Returning <code>true</code> allows its release.</p><p><code>View.props.onResponderTerminationRequest: (event) =&gt; {}</code>, where <code>event</code> is a synthetic touch
event as described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onstartshouldsetresponder"></a>onStartShouldSetResponder?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onstartshouldsetresponder">#</a></h4><div><p>Does this view want to become responder on the start of a touch?</p><p><code>View.props.onStartShouldSetResponder: (event) =&gt; [true | false]</code>, where <code>event</code> is a
synthetic touch event as described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onstartshouldsetrespondercapture"></a>onStartShouldSetResponderCapture?: <span class="propType">function</span> <a class="hash-link" href="docs/viewproptypes.html#onstartshouldsetrespondercapture">#</a></h4><div><p>If a parent <code>View</code> wants to prevent a child <code>View</code> from becoming responder on a touch start,
it should have this handler which returns <code>true</code>.</p><p><code>View.props.onStartShouldSetResponderCapture: (event) =&gt; [true | false]</code>, where <code>event</code> is a
synthetic touch event as described above.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="pointerevents"></a>pointerEvents?: <span class="propType">enum('box-none', 'none', 'box-only', 'auto')</span> <a class="hash-link" href="docs/viewproptypes.html#pointerevents">#</a></h4><div><p>Controls whether the <code>View</code> can be the target of touch events.</p><ul><li><code>'auto'</code>: The View can be the target of touch events.</li><li><code>'none'</code>: The View is never the target of touch events.</li><li><code>'box-none'</code>: The View is never the target of touch events but it's
subviews can be. It behaves like if the view had the following classes
in CSS:<div class="prism language-javascript"><span class="token punctuation">.</span>box<span class="token operator">-</span>none <span class="token punctuation">{</span>
 pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> none<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token punctuation">.</span>box<span class="token operator">-</span>none <span class="token operator">*</span> <span class="token punctuation">{</span>
 pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> all<span class="token punctuation">;</span>
<span class="token punctuation">}</span></div></li><li><code>'box-only'</code>: The view can be the target of touch events but it's
subviews cannot be. It behaves like if the view had the following classes
in CSS:<div class="prism language-javascript"><span class="token punctuation">.</span>box<span class="token operator">-</span>only <span class="token punctuation">{</span>
 pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> all<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token punctuation">.</span>box<span class="token operator">-</span>only <span class="token operator">*</span> <span class="token punctuation">{</span>
 pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> none<span class="token punctuation">;</span>
<span class="token punctuation">}</span></div><blockquote><p>Since <code>pointerEvents</code> does not affect layout/appearance, and we are
already deviating from the spec by adding additional modes, we opt to not
include <code>pointerEvents</code> on <code>style</code>. On some platforms, we would need to
implement it as a <code>className</code> anyways. Using <code>style</code> or not is an
implementation detail of the platform.</p></blockquote></li></ul></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="removeclippedsubviews"></a>removeClippedSubviews?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#removeclippedsubviews">#</a></h4><div><p>This is a special performance property exposed by <code>RCTView</code> and is useful
for scrolling content when there are many subviews, most of which are
offscreen. For this property to be effective, it must be applied to a
view that contains many subviews that extend outside its bound. The
subviews must also have <code>overflow: hidden</code>, as should the containing view
(or one of its superviews).</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="style"></a>style?: <span class="propType">stylePropType</span> <a class="hash-link" href="docs/viewproptypes.html#style">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="testid"></a>testID?: <span class="propType">string</span> <a class="hash-link" href="docs/viewproptypes.html#testid">#</a></h4><div><p>Used to locate this view in end-to-end tests.</p><blockquote><p>This disables the 'layout-only view removal' optimization for this view!</p></blockquote></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilitycomponenttype"></a><span class="platform">android</span>accessibilityComponentType?: <span class="propType">AccessibilityComponentTypes</span> <a class="hash-link" href="docs/viewproptypes.html#accessibilitycomponenttype">#</a></h4><div><p>Indicates to accessibility services to treat UI component like a
native one. Works for Android only.</p><p>Possible values are one of:</p><ul><li><code>'none'</code></li><li><code>'button'</code></li><li><code>'radiobutton_checked'</code></li><li><code>'radiobutton_unchecked'</code></li></ul></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilityliveregion"></a><span class="platform">android</span>accessibilityLiveRegion?: <span class="propType">enum('none', 'polite', 'assertive')</span> <a class="hash-link" href="docs/viewproptypes.html#accessibilityliveregion">#</a></h4><div><p>Indicates to accessibility services whether the user should be notified
when this view changes. Works for Android API &gt;= 19 only.
Possible values:</p><ul><li><code>'none'</code> - Accessibility services should not announce changes to this view.</li><li><code>'polite'</code>- Accessibility services should announce changes to this view.</li><li><code>'assertive'</code> - Accessibility services should interrupt ongoing speech to immediately announce changes to this view.</li></ul><p>See the <a href="http://developer.android.com/reference/android/view/View.html#attr_android:accessibilityLiveRegion" target="_blank">Android <code>View</code> docs</a>
for reference.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="collapsable"></a><span class="platform">android</span>collapsable?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#collapsable">#</a></h4><div><p>Views that are only used to layout their children or otherwise don't draw
anything may be automatically removed from the native hierarchy as an
optimization. Set this property to <code>false</code> to disable this optimization and
ensure that this <code>View</code> exists in the native view hierarchy.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="importantforaccessibility"></a><span class="platform">android</span>importantForAccessibility?: <span class="propType">enum('auto', 'yes', 'no', 'no-hide-descendants')</span> <a class="hash-link" href="docs/viewproptypes.html#importantforaccessibility">#</a></h4><div><p>Controls how view is important for accessibility which is if it
fires accessibility events and if it is reported to accessibility services
that query the screen. Works for Android only.</p><p>Possible values:</p><ul><li><code>'auto'</code> - The system determines whether the view is important for accessibility -
default (recommended).</li><li><code>'yes'</code> - The view is important for accessibility.</li><li><code>'no'</code> - The view is not important for accessibility.</li><li><code>'no-hide-descendants'</code> - The view is not important for accessibility,
nor are any of its descendant views.</li></ul><p>See the <a href="http://developer.android.com/reference/android/R.attr.html#importantForAccessibility" target="_blank">Android <code>importantForAccessibility</code> docs</a>
for reference.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="nativeid"></a><span class="platform">android</span>nativeID?: <span class="propType">string</span> <a class="hash-link" href="docs/viewproptypes.html#nativeid">#</a></h4><div><p>Used to locate this view from native classes.</p><blockquote><p>This disables the 'layout-only view removal' optimization for this view!</p></blockquote></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="needsoffscreenalphacompositing"></a><span class="platform">android</span>needsOffscreenAlphaCompositing?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#needsoffscreenalphacompositing">#</a></h4><div><p>Whether this <code>View</code> needs to rendered offscreen and composited with an alpha
in order to preserve 100% correct colors and blending behavior. The default
(<code>false</code>) falls back to drawing the component and its children with an alpha
applied to the paint used to draw each element instead of rendering the full
component offscreen and compositing it back with an alpha value. This default
may be noticeable and undesired in the case where the <code>View</code> you are setting
an opacity on has multiple overlapping elements (e.g. multiple overlapping
<code>View</code>s, or text and a background).</p><p>Rendering offscreen to preserve correct alpha behavior is extremely
expensive and hard to debug for non-native developers, which is why it is
not turned on by default. If you do need to enable this property for an
animation, consider combining it with renderToHardwareTextureAndroid if the
view <strong>contents</strong> are static (i.e. it doesn't need to be redrawn each frame).
If that property is enabled, this View will be rendered off-screen once,
saved in a hardware texture, and then composited onto the screen with an alpha
each frame without having to switch rendering targets on the GPU.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="rendertohardwaretextureandroid"></a><span class="platform">android</span>renderToHardwareTextureAndroid?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#rendertohardwaretextureandroid">#</a></h4><div><p>Whether this <code>View</code> should render itself (and all of its children) into a
single hardware texture on the GPU.</p><p>On Android, this is useful for animations and interactions that only
modify opacity, rotation, translation, and/or scale: in those cases, the
view doesn't have to be redrawn and display lists don't need to be
re-executed. The texture can just be re-used and re-composited with
different parameters. The downside is that this can use up limited video
memory, so this prop should be set back to false at the end of the
interaction/animation.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilitytraits"></a><span class="platform">ios</span>accessibilityTraits?: <span class="propType"><span><span>AccessibilityTraits, </span><span>[AccessibilityTraits]</span></span></span> <a class="hash-link" href="docs/viewproptypes.html#accessibilitytraits">#</a></h4><div><p>Provides additional traits to screen reader. By default no traits are
provided unless specified otherwise in element.</p><p>You can provide one trait or an array of many traits.</p><p>Possible values for <code>AccessibilityTraits</code> are:</p><ul><li><code>'none'</code> - The element has no traits.</li><li><code>'button'</code> - The element should be treated as a button.</li><li><code>'link'</code> - The element should be treated as a link.</li><li><code>'header'</code> - The element is a header that divides content into sections.</li><li><code>'search'</code> - The element should be treated as a search field.</li><li><code>'image'</code> - The element should be treated as an image.</li><li><code>'selected'</code> - The element is selected.</li><li><code>'plays'</code> - The element plays sound.</li><li><code>'key'</code> - The element should be treated like a keyboard key.</li><li><code>'text'</code> - The element should be treated as text.</li><li><code>'summary'</code> - The element provides app summary information.</li><li><code>'disabled'</code> - The element is disabled.</li><li><code>'frequentUpdates'</code> - The element frequently changes its value.</li><li><code>'startsMedia'</code> - The element starts a media session.</li><li><code>'adjustable'</code> - The element allows adjustment over a range of values.</li><li><code>'allowsDirectInteraction'</code> - The element allows direct touch interaction for VoiceOver users.</li><li><code>'pageTurn'</code> - Informs VoiceOver that it should scroll to the next page when it finishes reading the contents of the element.</li></ul><p>See the <a href="docs/accessibility.html#accessibilitytraits-ios" target="_blank">Accessibility guide</a>
for more information.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilityviewismodal"></a><span class="platform">ios</span>accessibilityViewIsModal?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#accessibilityviewismodal">#</a></h4><div><p>A value indicating whether VoiceOver should ignore the elements
within views that are siblings of the receiver.
Default is <code>false</code>.</p><p>See the <a href="docs/accessibility.html#accessibilitytraits-ios" target="_blank">Accessibility guide</a>
for more information.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="shouldrasterizeios"></a><span class="platform">ios</span>shouldRasterizeIOS?: <span class="propType">bool</span> <a class="hash-link" href="docs/viewproptypes.html#shouldrasterizeios">#</a></h4><div><p>Whether this <code>View</code> should be rendered as a bitmap before compositing.</p><p>On iOS, this is useful for animations and interactions that do not
modify this component's dimensions nor its children; for example, when
translating the position of a static view, rasterization allows the
renderer to reuse a cached bitmap of a static view and quickly composite
it during each frame.</p><p>Rasterization incurs an off-screen drawing pass and the bitmap consumes
memory. Test and measure when using this property.</p></div></div></div></div><p class="edit-page-block"><a target="_blank" href="https://github.com/facebook/react-native/blob/master/Libraries/Components/View/ViewPropTypes.js">Improve this page</a> by sending a pull request!</p><div class="docs-prevnext"><a class="docs-prev" href="docs/shadow-props.html#content">← Prev</a><a class="docs-next" href="docs/viewstyleproptypes.html#content">Next →</a></div>
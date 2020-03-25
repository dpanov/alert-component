# Project notes

1. Buttons (including the close one) and links don't have hover and focus effects
3. Some of the annotated values differ from what the actual values are
   1. the space between **Info summary** and the text below it is 4 pixels
   2. The outlined button in the last alert has different paddings compared to the other outlined buttons
2. Inline alert with link - close button is not at the same position. Is this intentional?
4. Is the action button always positioned to the right when there's no title in the alert?
5. How often will these alerts pop up? Wondering if we should add the alert icons as inline SVGs (easier to change the icon color) or add them as <img> (better performance-wise, because the images will be cached).
7. Is the action button really a button? What is its function?
8. Which browsers should be supported?
9.  Do we want dark mode support?
10. Will the layout change on different resolutions, especially for phones?


# Variations
1. Standard - always three columns: "icon content close". When the alert can't be closed, the close column is empty, but the space between the columns is still there. That's how we get the 40 px space on the right. Action button is always at the bottom
1. Inline - Has four columns: "icon content action close". Unless the close button is missing, then it should have three columns. It's a bit weird that by design, when the action button is missing there are still four columns, and the close button should bet placed in the third column.
Variations:
   2. Closable, no action button
   3. Closable and has action button
   4. Not closable and no action button
   5. Has action button, but not closable


# Alert resources and exmaples
 - https://inclusive-components.design/notifications/
 - https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/Alert_Role
 - https://www.w3.org/WAI/tutorials/forms/notifications/
 - https://developer.paciellogroup.com/blog/2012/06/html5-accessibility-chops-aria-rolealert-browser-support/
 - https://www.deque.com/blog/aria-modal-alert-dialogs-a11y-support-series-part-2/
 - https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_alert_role

Research more about role="alert" and consider using it


<alert type="warning" 
       is-closable="true"
       action-title="Action" 
       onActionClicked={ someFunction }
       onClose={ someOtherFunction } 
       title="Info summary">
   <strong>Theon the ground</strong> think impact investing
</alert>

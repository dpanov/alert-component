# Project notes

1. Inline alert with link - close button is not at the same position. Is this intentional?
2. Buttons (including the close one) and links doesn't have hover effects
3. Some of the annotated values differ from what the actual values are
   1. the space between info summary and the text below it is 4 pixels
   3. The outlined button in the last alert has different paddings compared to the other outlined buttons
4. Is the action button always positioned to the right when there's no title in the alert?
5. How often will these alerts pop up? Wondering if we should add the alert icons as inline SVGs (easier to change the icon color) or add them as <img> (better performance-wise, because the images will be cached).
6. The action button and the close button don't have any hover and/or focus states
7. Is the action button really a button? What's is its function?
8. Which browsers should be supported?
9. Dark mode support?
10. Action button - will it always look like that? Do we have situations where we want different styles for it?

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

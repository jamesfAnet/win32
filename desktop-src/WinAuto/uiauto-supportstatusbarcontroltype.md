---
title: StatusBar Control Type
description: This topic provides information about Microsoft UI Automation support for the StatusBar control type.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- UI Automation,support for StatusBar control type
- UI Automation,StatusBar control type
- UI Automation,tree structure for StatusBar control type
- UI Automation,properties for StatusBar control type
- UI Automation,control patterns for StatusBar control type
- UI Automation,events for StatusBar control type
- tree structures,StatusBar control type
- properties,StatusBar control type
- control patterns,StatusBar control type
- events,StatusBar control type
- support for StatusBar control type
- StatusBar control type
- control types,tree structure for StatusBar control type
- control types,control patterns for StatusBar control type
- control types,support for StatusBar
- control types,StatusBar
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# StatusBar Control Type

This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.

A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.

The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type. The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.

This topic contains the following sections.

-   [Typical Tree Structure](#typical-tree-structure)
-   [Relevant Properties](#relevant-properties)
-   [Required Control Patterns](#required-control-patterns)
-   [Required Events](#required-events)
-   [Remarks](#remarks)
-   [Related topics](#related-topics)

## Typical Tree Structure

The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view. For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Control View</th>
<th>Content View</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>StatusBar
<ul>
<li>Edit (0 or more)</li>
<li>ProgressBar (0 or many)</li>
<li>Image (0 or many)</li>
<li>Button (0 or many)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Edit (0 or more)</li>
<li>ProgressBar (0 or many)</li>
<li>Image (0 or many)</li>
<li>Button (0 or many)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## Relevant Properties

The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls. For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).



| UI Automation Property                                                                                              | Value         | Notes                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA\_AutomationIdPropertyId**](https://www.bing.com/search?q=**UIA\_AutomationIdPropertyId**)                 | See notes.    | The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.                                                                                                        |
| [**UIA\_BoundingRectanglePropertyId**](https://www.bing.com/search?q=**UIA\_BoundingRectanglePropertyId**)       | See notes.    | The bounding rectangle of a status bar must encompass all of the controls contained within it.                                                                                                                      |
| [**UIA\_ClickablePointPropertyId**](https://www.bing.com/search?q=**UIA\_ClickablePointPropertyId**)             | See notes.    | Supported if there is a bounding rectangle. If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point. |
| [**UIA\_ControlTypePropertyId**](https://www.bing.com/search?q=**UIA\_ControlTypePropertyId**)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA\_IsContentElementPropertyId**](https://www.bing.com/search?q=**UIA\_IsContentElementPropertyId**)         | TRUE          | The status bar control is always included in the content view of the UI Automation tree.                                                                                                                            |
| [**UIA\_IsControlElementPropertyId**](https://www.bing.com/search?q=**UIA\_IsControlElementPropertyId**)         | TRUE          | The status bar control is always included in the control view of the UI Automation tree.                                                                                                                            |
| [**UIA\_IsKeyboardFocusablePropertyId**](https://www.bing.com/search?q=**UIA\_IsKeyboardFocusablePropertyId**)   | Depends       | If the control can receive keyboard focus, it must support this property.                                                                                                                                           |
| [**UIA\_IsOffscreenPropertyId**](https://www.bing.com/search?q=**UIA\_IsOffscreenPropertyId**)                   | Depends       | If a status bar control is not currently visible, it will return TRUE for this property.                                                                                                                            |
| [**UIA\_LabeledByPropertyId**](https://www.bing.com/search?q=**UIA\_LabeledByPropertyId**)                       | NULL          | The status bar control typically does not have a label.                                                                                                                                                             |
| [**UIA\_LocalizedControlTypePropertyId**](https://www.bing.com/search?q=**UIA\_LocalizedControlTypePropertyId**) | See notes.    | Localized string corresponding to the **StatusBar** control type. The default value is "status bar" for en-US or English (United States).                                                                           |
| [**UIA\_NamePropertyId**](https://www.bing.com/search?q=**UIA\_NamePropertyId**)                                 | See notes.    | The status bar control does not need a name unless more than one is used within an application. In this case, distinguish each bar with names such as "Internet Status" or "Application Status".                    |
| [**UIA\_OrientationPropertyId**](https://www.bing.com/search?q=**UIA\_OrientationPropertyId**)                   | Depends       | A value indicating the control's orientation: horizontal or vertical.                                                                                                                                               |



 

## Required Control Patterns

The following table lists the UI Automation control patterns required to be supported for status bar controls. For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Control Pattern                               | Support  | Notes                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Optional | Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information. |



 

## Required Events

The following table lists the UI Automation events that status bar controls are required to support. For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).



| UI Automation Event                                                                                                                   | Notes                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA\_AutomationFocusChangedEventId**](https://www.bing.com/search?q=**UIA\_AutomationFocusChangedEventId**)                                      |                                                                                   |
| [**UIA\_BoundingRectanglePropertyId**](https://www.bing.com/search?q=**UIA\_BoundingRectanglePropertyId**) property-changed event. |                                                                                   |
| [**UIA\_IsEnabledPropertyId**](https://www.bing.com/search?q=**UIA\_IsEnabledPropertyId**) property-changed event.                 | If the control supports the **IsEnabled** property, it must support this event.   |
| [**UIA\_IsOffscreenPropertyId**](https://www.bing.com/search?q=**UIA\_IsOffscreenPropertyId**) property-changed event.             | If the control supports the **IsOffscreen** property, it must support this event. |
| [**UIA\_StructureChangedEventId**](https://www.bing.com/search?q=**UIA\_StructureChangedEventId**)                                                  |                                                                                   |



 

## Remarks

We recommend that edit controls be used as child grid elements in a status bar. Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property. Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.

## Related topics

<dl> <dt>

**Conceptual**
</dt> <dt>

[UI Automation Control Types Overview](uiauto-controltypesoverview.md)
</dt> <dt>

[UI Automation Overview](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




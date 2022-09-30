<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Assignment4</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .pm { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation.Marker */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0px solid transparent;
  border-right: 0px solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0px solid transparent;
  border-bottom: 0px solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
	border:1px solid transparent;
  background-color: transparent;
  position: absolute;
	z-index:1;
	right:3%;
	top: 0;
	bottom: 0;
	margin: auto;
	padding: 7px 0;
	display: none;
	vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
	content: "X";
	display: block;
	width: 15px;
	height: 15px;
	text-align: center;
	color:#000;
	font-weight: normal;
	font-size: 12px;
	cursor: pointer;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
  background: inherit;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-bottom:10px;
  margin-top:0; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  font-size:36px;
  line-height:40px; }

h2.bp3-heading, .bp3-running-text h2{
  font-size:28px;
  line-height:32px; }

h3.bp3-heading, .bp3-running-text h3{
  font-size:22px;
  line-height:25px; }

h4.bp3-heading, .bp3-running-text h4{
  font-size:18px;
  line-height:21px; }

h5.bp3-heading, .bp3-running-text h5{
  font-size:16px;
  line-height:19px; }

h6.bp3-heading, .bp3-running-text h6{
  font-size:14px;
  line-height:16px; }
.bp3-ui-text{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none; }

.bp3-monospace-text{
  font-family:monospace;
  text-transform:none; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  font-size:14px;
  line-height:1.5; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15);
    margin:20px 0; }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  color:#106ba3;
  text-decoration:none; }
  a:hover{
    color:#106ba3;
    cursor:pointer;
    text-decoration:underline; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  font-size:smaller;
  padding:2px 5px; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  color:#182026;
  display:block;
  font-size:13px;
  line-height:1.4;
  margin:10px 0;
  padding:13px 15px 12px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit;
    font-size:inherit;
    padding:0; }

.bp3-running-text kbd, .bp3-key{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-family:inherit;
  font-size:12px;
  height:24px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  line-height:24px;
  min-width:24px;
  padding:3px 6px;
  vertical-align:middle; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  margin:0 0 10px;
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    font-size:40px;
    margin-right:20px;
    margin-top:0; }

.bp3-alert-contents{
  word-break:break-word; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  cursor:default;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  height:30px;
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-breadcrumbs > li{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }
    .bp3-breadcrumbs > li::after{
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 00-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 001.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      content:"";
      display:block;
      height:16px;
      margin:0 5px;
      width:16px; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    font-size:inherit;
    font-weight:inherit;
    vertical-align:baseline; }

.bp3-breadcrumbs-collapsed{
  background:#ced9e0;
  border:none;
  border-radius:3px;
  cursor:pointer;
  margin-right:2px;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    content:"";
    display:block;
    height:16px;
    width:16px; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    color:#182026;
    text-decoration:none; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  min-height:30px;
  min-width:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      background-color:#106ba3;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      background-color:#0e5a8a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      background-color:#0d8050;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      background-color:#0a6640;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      background-color:#bf7326;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      background-color:#a66321;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      background-color:#c23030;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      background-color:#a82a2a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-height:40px;
    min-width:40px;
    font-size:16px;
    padding:5px 15px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      margin:0;
      position:absolute; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button.bp3-minimal:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button.bp3-outlined{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    border:1px solid rgba(24, 32, 38, 0.2);
    -webkit-box-sizing:border-box;
            box-sizing:border-box; }
    .bp3-button.bp3-outlined:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-outlined:active, .bp3-button.bp3-outlined.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-outlined{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-outlined:hover, .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-outlined:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover, .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover, .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover, .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover, .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled:hover{
      border-color:rgba(92, 112, 128, 0.1); }
    .bp3-dark .bp3-button.bp3-outlined{
      border-color:rgba(255, 255, 255, 0.4); }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        border-color:rgba(255, 255, 255, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      border-color:rgba(16, 107, 163, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        border-color:rgba(16, 107, 163, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        border-color:rgba(72, 175, 240, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          border-color:rgba(72, 175, 240, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      border-color:rgba(13, 128, 80, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        border-color:rgba(13, 128, 80, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        border-color:rgba(61, 204, 145, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          border-color:rgba(61, 204, 145, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      border-color:rgba(191, 115, 38, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        border-color:rgba(191, 115, 38, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        border-color:rgba(255, 179, 102, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          border-color:rgba(255, 179, 102, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      border-color:rgba(194, 48, 48, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        border-color:rgba(194, 48, 48, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        border-color:rgba(255, 115, 115, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          border-color:rgba(255, 115, 115, 0.2); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    border-bottom-right-radius:0;
    border-top-right-radius:0;
    margin-right:-1px; }
  .bp3-button-group.bp3-minimal .bp3-button{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      height:100%;
      width:unset; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  font-size:14px;
  line-height:1.5;
  background-color:rgba(138, 155, 168, 0.15);
  border-radius:3px;
  padding:10px 12px 9px;
  position:relative;
  width:100%; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout .bp3-heading{
    line-height:20px;
    margin-bottom:5px;
    margin-top:0; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  opacity:0.9;
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  width:100%; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }

.bp3-dialog{
  background:#ebf1f5;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text;
  width:500px; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    background:#293742;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-dialog-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding-left:20px;
  padding-right:5px;
  z-index:30; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    background:#30404d;
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  margin:20px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-multistep-dialog-panels{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }

.bp3-multistep-dialog-left-panel{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column; }
  .bp3-dark .bp3-multistep-dialog-left-panel{
    background:#202b33; }

.bp3-multistep-dialog-right-panel{
  background-color:#f5f8fa;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  border-radius:0 0 6px 0;
  -webkit-box-flex:3;
      -ms-flex:3;
          flex:3;
  min-width:0; }
  .bp3-dark .bp3-multistep-dialog-right-panel{
    background-color:#293742;
    border-left:1px solid rgba(16, 22, 26, 0.4); }

.bp3-multistep-dialog-footer{
  background-color:#ffffff;
  border-radius:0 0 6px 0;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  padding:10px; }
  .bp3-dark .bp3-multistep-dialog-footer{
    background:#30404d;
    border-top:1px solid rgba(16, 22, 26, 0.4); }

.bp3-dialog-step-container{
  background-color:#f5f8fa;
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-dialog-step-container{
    background:#293742;
    border-bottom:1px solid rgba(16, 22, 26, 0.4); }
  .bp3-dialog-step-container.bp3-dialog-step-viewed{
    background-color:#ffffff; }
    .bp3-dark .bp3-dialog-step-container.bp3-dialog-step-viewed{
      background:#30404d; }

.bp3-dialog-step{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#f5f8fa;
  border-radius:6px;
  cursor:not-allowed;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:4px;
  padding:6px 14px; }
  .bp3-dark .bp3-dialog-step{
    background:#293742; }
  .bp3-dialog-step-viewed .bp3-dialog-step{
    background-color:#ffffff;
    cursor:pointer; }
    .bp3-dark .bp3-dialog-step-viewed .bp3-dialog-step{
      background:#30404d; }
  .bp3-dialog-step:hover{
    background-color:#f5f8fa; }
    .bp3-dark .bp3-dialog-step:hover{
      background:#293742; }

.bp3-dialog-step-icon{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:rgba(92, 112, 128, 0.6);
  border-radius:50%;
  color:#ffffff;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:25px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:25px; }
  .bp3-dark .bp3-dialog-step-icon{
    background-color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#2b95d6; }
  .bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#8a9ba8; }

.bp3-dialog-step-title{
  color:rgba(92, 112, 128, 0.6);
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  padding-left:10px; }
  .bp3-dark .bp3-dialog-step-title{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-title{
    color:#2b95d6; }
  .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
    color:#182026; }
    .bp3-dark .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
      color:#f5f8fa; }
.bp3-drawer{
  background:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    height:50%;
    left:0;
    right:0;
    top:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-bottom{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-left{
    bottom:0;
    left:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-right{
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    background:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-drawer-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding:5px;
  padding-left:20px;
  position:relative; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  overflow:auto; }

.bp3-drawer-footer{
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  padding:10px 20px;
  position:relative; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  cursor:text;
  display:inline-block;
  max-width:100%;
  position:relative;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    bottom:-3px;
    left:-3px;
    position:absolute;
    right:-3px;
    top:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  color:inherit;
  display:inherit;
  font:inherit;
  letter-spacing:inherit;
  max-width:inherit;
  min-width:inherit;
  position:relative;
  resize:none;
  text-transform:inherit;
  vertical-align:top; }

.bp3-editable-text-input{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0;
  white-space:pre-wrap;
  width:100%; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    left:0;
    position:absolute;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    border-radius:inherit;
    z-index:2; }
    .bp3-control-group .bp3-input:focus{
      border-radius:3px;
      z-index:14; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    border-radius:inherit;
    z-index:4; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-left-container,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group .bp3-select:focus-within{
    z-index:5; }
  .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:-1px; }
  .bp3-control-group:not(.bp3-vertical) > .bp3-divider:not(:first-child){
    margin-left:6px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    border-radius:0 3px 3px 0;
    margin-right:0; }
  .bp3-control-group > :only-child{
    border-radius:3px;
    margin-right:0; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group .bp3-numeric-input:not(:first-child) .bp3-input-group{
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-control-group.bp3-fill{
    width:100%; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      border-radius:3px 3px 0 0;
      margin-top:0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  cursor:pointer;
  display:block;
  margin-bottom:10px;
  position:relative;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    left:0;
    opacity:0;
    position:absolute;
    top:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    cursor:pointer;
    display:inline-block;
    font-size:16px;
    height:1em;
    margin-right:10px;
    margin-top:-3px;
    position:relative;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none;
    vertical-align:middle;
    width:1em; }
    .bp3-control .bp3-control-indicator::before{
      content:"";
      display:block;
      height:1em;
      width:1em; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    background:#d8e1e8;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-left:10px;
    margin-top:1px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 00-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0012 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:auto; }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      background:#ffffff;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      height:calc(1em - 4px);
      left:0;
      margin:2px;
      position:absolute;
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      width:calc(1em - 4px); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    font-size:0.7em;
    text-align:center; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    line-height:0;
    margin-left:0.5em;
    margin-right:1.2em;
    visibility:hidden; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    line-height:1em;
    margin-left:1.2em;
    margin-right:0.5em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    line-height:1em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    line-height:0;
    visibility:hidden; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      background:#202b33;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  cursor:pointer;
  display:inline-block;
  height:30px;
  position:relative; }
  .bp3-file-input input{
    margin:0;
    min-width:200px;
    opacity:0; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      background:rgba(206, 217, 224, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(92, 112, 128, 0.6);
        cursor:not-allowed;
        outline:none; }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        background:rgba(57, 75, 89, 0.5);
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          -webkit-box-shadow:none;
                  box-shadow:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:rgba(92, 112, 128, 0.6);
  left:0;
  padding-right:80px;
  position:absolute;
  right:0;
  top:0;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-file-upload-input::after{
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026;
    min-height:24px;
    min-width:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    border-radius:3px;
    content:"Browse";
    line-height:24px;
    margin:3px;
    position:absolute;
    right:0;
    text-align:center;
    top:0;
    width:70px; }
    .bp3-file-upload-input::after:hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-file-upload-input:active::after{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-large .bp3-file-upload-input{
    font-size:16px;
    height:40px;
    line-height:40px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-height:30px;
      min-width:30px;
      line-height:30px;
      margin:5px;
      width:85px; }
  .bp3-dark .bp3-file-upload-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        background-color:#30404d;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        background-color:#202b33;
        background-image:none;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:active::after{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    color:#5c7080;
    font-size:12px;
    margin-top:5px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      line-height:40px;
      margin:0 10px 0 0; }
    .bp3-form-group.bp3-inline label.bp3-label{
      line-height:30px;
      margin:0 10px 0 0; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-input-left-container:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-input-left-container:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-height:24px;
    min-width:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-icon{
    z-index:1; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon{
    color:#5c7080; }
    .bp3-input-group > .bp3-input-left-container > .bp3-icon:empty,
    .bp3-input-group > .bp3-icon:empty{
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-height:30px;
    min-width:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle; }
  .bp3-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-input.bp3-large{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-bottom:15px;
  margin-top:0; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    font-weight:400;
    vertical-align:top;
    width:100%; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  min-height:0;
  padding:0;
  width:30px; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  -moz-appearance:none;
  -webkit-appearance:none;
  border-radius:3px;
  height:30px;
  padding:0 25px 0 10px;
  width:100%; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  background:none;
  -webkit-box-shadow:none;
          box-shadow:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    background:rgba(167, 182, 194, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026;
    text-decoration:none; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    background:rgba(115, 134, 148, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      color:rgba(167, 182, 194, 0.6);
      cursor:not-allowed; }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  font-size:16px;
  height:40px;
  padding-right:35px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    background-color:#202b33;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  background-color:rgba(206, 217, 224, 0.5);
  -webkit-box-shadow:none;
          box-shadow:none;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  color:#5c7080;
  pointer-events:none;
  position:absolute;
  right:7px;
  top:7px; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  letter-spacing:normal;
  position:relative;
  vertical-align:middle; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    right:12px;
    top:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select option:disabled, .bp3-dark
  .bp3-select option:disabled{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    text-align:left;
    vertical-align:top; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td,
  .bp3-running-text table tfoot tr:first-child th,
  table.bp3-html-table tfoot tr:first-child th,
  .bp3-running-text table tfoot tr:first-child td,
  table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td,
  .bp3-dark .bp3-running-text table tfoot tr:first-child th,
  .bp3-running-text .bp3-dark table tfoot tr:first-child th,
  .bp3-dark table.bp3-html-table tfoot tr:first-child th,
  .bp3-dark .bp3-running-text table tfoot tr:first-child td,
  .bp3-running-text .bp3-dark table tfoot tr:first-child td,
  .bp3-dark table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-bottom:6px;
  padding-top:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td,
table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
  table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table{ }
  .bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
    background:rgba(92, 112, 128, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td,
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
      -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
              box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
    background-color:rgba(92, 112, 128, 0.3);
    cursor:pointer; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
    background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  padding-bottom:0;
  top:40px; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-left:0;
  margin-right:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  font-family:"Icons20";
  font-size:inherit;
  font-style:normal;
  font-weight:400;
  line-height:1; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagnosis::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-lab-test::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }
  .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{ }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  background:#ffffff;
  border-radius:3px;
  color:#182026;
  list-style:none;
  margin:0;
  min-width:180px;
  padding:5px;
  text-align:left; }

.bp3-menu-divider{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px; }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  color:inherit;
  line-height:20px;
  padding:5px 7px;
  text-decoration:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    color:#5c7080;
    margin-top:2px; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit !important;
    color:rgba(92, 112, 128, 0.6) !important;
    cursor:not-allowed !important;
    outline:none !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    font-size:16px;
    line-height:22px;
    padding:9px 7px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-right:10px;
      margin-top:1px; }

button.bp3-menu-item{
  background:none;
  border:none;
  text-align:left;
  width:100%; }
.bp3-menu-header{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px;
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    line-height:17px;
    margin:0;
    padding:10px 7px 0 1px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    font-size:18px;
    padding-bottom:5px;
    padding-top:15px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item{ }
  .bp3-dark .bp3-menu-item.bp3-intent-primary{
    color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-success{
    color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning{
    color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger{
    color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item::before,
  .bp3-dark .bp3-menu-item > .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item .bp3-menu-item-label{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
    background-color:rgba(138, 155, 168, 0.3); }
  .bp3-dark .bp3-menu-item.bp3-disabled{
    color:rgba(167, 182, 194, 0.6) !important; }
    .bp3-dark .bp3-menu-item.bp3-disabled::before,
    .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  background-color:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  height:50px;
  padding:0 15px;
  position:relative;
  width:100%;
  z-index:10; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    left:0;
    position:fixed;
    right:0;
    top:0; }

.bp3-navbar-heading{
  font-size:16px;
  margin-right:15px; }

.bp3-navbar-group{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px;
  margin:0 10px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:100%;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  text-align:center;
  width:100%; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  bottom:0;
  left:0;
  position:static;
  right:0;
  top:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    overflow:hidden;
    position:fixed; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    overflow:auto;
    position:fixed; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  bottom:0;
  left:0;
  position:fixed;
  right:0;
  top:0;
  opacity:1;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  z-index:20; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }
  .bp3-panel-stack-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-panel-stack2{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack2-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack2-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack2-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack2-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack2-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack2-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-view{
    background-color:#30404d; }
  .bp3-panel-stack2-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter, .bp3-panel-stack2-push .bp3-panel-stack2-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter-active, .bp3-panel-stack2-push .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter, .bp3-panel-stack2-pop .bp3-panel-stack2-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter-active, .bp3-panel-stack2-pop .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  border-radius:3px;
  display:inline-block;
  z-index:20; }
  .bp3-popover .bp3-popover-arrow{
    height:30px;
    position:absolute;
    width:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      height:20px;
      margin:5px;
      width:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-bottom:17px;
    margin-top:-17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-left:-17px;
    margin-right:17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover .bp3-popover-content{
    border-radius:3px;
    position:relative; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  border-radius:2px;
  content:"";
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg); }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  left:0;
  position:absolute;
  right:0;
  top:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  background:rgba(92, 112, 128, 0.2);
  border-radius:40px;
  display:block;
  height:8px;
  overflow:hidden;
  position:relative;
  width:100%; }
  .bp3-progress-bar .bp3-progress-meter{
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    border-radius:40px;
    height:100%;
    position:absolute;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:100%; }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  color:transparent !important;
  cursor:default;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  height:40px;
  min-width:150px;
  width:100%;
  cursor:default;
  outline:none;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    cursor:not-allowed;
    opacity:0.5; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  height:6px;
  left:0;
  right:0;
  top:5px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  height:16px;
  left:0;
  position:absolute;
  top:0;
  width:16px; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab;
    z-index:2; }
  .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    background:#bfccd6;
    -webkit-box-shadow:none;
            box-shadow:none;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    background:#5c7080;
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-slider-handle .bp3-slider-label{
    background:#394b59;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    color:#f5f8fa;
    margin-left:8px; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      background:#e1e8ed;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-bottom-right-radius:0;
    border-top-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    border-bottom-left-radius:0;
    border-top-left-radius:0;
    margin-left:8px; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  font-size:12px;
  line-height:1;
  padding:2px 5px;
  position:absolute;
  vertical-align:top; }

.bp3-slider.bp3-vertical{
  height:150px;
  min-width:40px;
  width:40px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    bottom:0;
    height:auto;
    left:5px;
    top:0;
    width:6px; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-left:0;
      margin-top:-8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      height:8px;
      margin-left:0;
      width:16px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-bottom-right-radius:3px;
      border-top-left-radius:0; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      border-bottom-left-radius:0;
      border-bottom-right-radius:0;
      border-top-left-radius:3px;
      margin-bottom:8px; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round;
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      padding:0 10px;
      width:100%; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        background-color:rgba(19, 124, 189, 0.2);
        -webkit-box-shadow:none;
                box-shadow:none; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      background-color:rgba(19, 124, 189, 0.2);
      border-radius:3px;
      bottom:0;
      height:auto;
      left:0;
      right:0;
      top:0; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  border:none;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  list-style:none;
  margin:0;
  padding:0;
  position:relative; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:#182026;
  cursor:pointer;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  font-size:14px;
  line-height:30px;
  max-width:100%;
  position:relative;
  vertical-align:top; }
  .bp3-tab a{
    color:inherit;
    display:block;
    text-decoration:none; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    background-color:transparent !important;
    -webkit-box-shadow:none !important;
            box-shadow:none !important; }
  .bp3-tab[aria-disabled="true"]{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    font-size:16px;
    line-height:40px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  left:0;
  pointer-events:none;
  position:absolute;
  top:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    background-color:#106ba3;
    bottom:0;
    height:3px;
    left:0;
    position:absolute;
    right:0; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#5c7080;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  color:#f5f8fa;
  font-size:12px;
  line-height:16px;
  max-width:100%;
  min-height:20px;
  min-width:20px;
  padding:2px 6px;
  position:relative; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-left:8px;
    padding-right:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    font-size:14px;
    line-height:20px;
    min-height:30px;
    min-width:30px;
    padding:5px 10px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-left:12px;
      padding-right:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  background:none;
  border:none;
  color:inherit;
  cursor:pointer;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin-bottom:-2px;
  margin-right:-6px !important;
  margin-top:-2px;
  opacity:0.5;
  padding:2px;
  padding-left:0; }
  .bp3-tag-remove:hover{
    background:none;
    opacity:0.8;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:0 5px 0 0; }
    .bp3-large .bp3-tag-remove:empty::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  line-height:inherit;
  min-height:30px;
  padding-left:5px;
  padding-right:0; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    color:#5c7080;
    margin-left:2px;
    margin-right:7px;
    margin-top:7px; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    margin-right:7px;
    margin-top:5px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:20px;
    width:80px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-left:5px;
      margin-top:10px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-height:30px;
      min-width:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:20px 0 0;
  max-width:500px;
  min-width:300px;
  pointer-events:all;
  position:relative !important; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-delay:50ms;
            transition-delay:50ms;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    color:#5c7080;
    margin:12px;
    margin-right:0; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    background-color:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  left:0;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none;
  right:0;
  z-index:40; }
  .bp3-toast-container.bp3-toast-container-in-portal{
    position:fixed; }
  .bp3-toast-container.bp3-toast-container-inline{
    position:absolute; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0; }
  .bp3-toast-container.bp3-toast-container-bottom{
    bottom:0;
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-exit-active ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    height:22px;
    position:absolute;
    width:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      height:14px;
      margin:4px;
      width:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-bottom:11px;
    margin-top:-11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-left:-11px;
    margin-right:11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  list-style:none;
  margin:0;
  padding-left:0; }

.bp3-tree-root{
  background-color:transparent;
  cursor:default;
  padding-left:0;
  position:relative; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:30px;
  padding-right:5px;
  width:100%; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  cursor:pointer;
  padding:7px;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  margin-right:7px;
  position:relative; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  left:calc(50% - 250px);
  top:20vh;
  width:500px;
  z-index:21; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar .bp3-input{
    background-color:transparent;
    border-radius:0; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    background-color:transparent;
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MC45NzggNTAuOTc4IiBzdHlsZT0iZW5hYmxlLWJhY2tncm91bmQ6bmV3IDAgMCA1MC45NzggNTAuOTc4OyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+Cgk8Zz4KCQk8cGF0aCBzdHlsZT0iZmlsbDojMDEwMDAyOyIgZD0iTTQzLjUyLDcuNDU4QzM4LjcxMSwyLjY0OCwzMi4zMDcsMCwyNS40ODksMEMxOC42NywwLDEyLjI2NiwyLjY0OCw3LjQ1OCw3LjQ1OAoJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDAKCQkJYzYuODE2LDAsMTMuMjIxLTIuNjQ4LDE4LjAyOS03LjQ1OGM0LjgwOS00LjgwOSw3LjQ1Ny0xMS4yMTIsNy40NTctMTguMDNDNTAuOTc3LDE4LjY3LDQ4LjMyOCwxMi4yNjYsNDMuNTIsNy40NTh6CgkJCSBNNDIuMTA2LDQyLjEwNWMtNC40MzIsNC40MzEtMTAuMzMyLDYuODcyLTE2LjYxNSw2Ljg3MmgtMC4wMDJjLTYuMjg1LTAuMDAxLTEyLjE4Ny0yLjQ0MS0xNi42MTctNi44NzIKCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzIKCQkJYzQuNDMxLDQuNDMxLDYuODcxLDEwLjMzMiw2Ljg3MSwxNi42MTdDNDguOTc3LDMxLjc3Miw0Ni41MzYsMzcuNjc1LDQyLjEwNiw0Mi4xMDV6Ii8+CgkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik0yMy41NzgsMzIuMjE4Yy0wLjAyMy0xLjczNCwwLjE0My0zLjA1OSwwLjQ5Ni0zLjk3MmMwLjM1My0wLjkxMywxLjExLTEuOTk3LDIuMjcyLTMuMjUzCgkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUKCQkJYzAtMS4wOTYtMC4yNi0yLjA4OC0wLjc3OS0yLjk3OWMtMC41NjUtMC44NzktMS41MDEtMS4zMzYtMi44MDYtMS4zNjljLTEuODAyLDAuMDU3LTIuOTg1LDAuNjY3LTMuNTUsMS44MzIKCQkJYy0wLjMwMSwwLjUzNS0wLjUwMywxLjE0MS0wLjYwNywxLjgxNGMtMC4xMzksMC43MDctMC4yMDcsMS40MzItMC4yMDcsMi4xNzRoLTIuOTM3Yy0wLjA5MS0yLjIwOCwwLjQwNy00LjExNCwxLjQ5My01LjcxOQoJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQoJCQljMCwxLjE0Mi0wLjEzNywyLjExMS0wLjQxLDIuOTExYy0wLjMwOSwwLjg0NS0wLjczMSwxLjU5My0xLjI2OCwyLjI0M2MtMC40OTIsMC42NS0xLjA2OCwxLjMxOC0xLjczLDIuMDAyCgkJCWMtMC42NSwwLjY5Ny0xLjMxMywxLjQ3OS0xLjk4NywyLjM0NmMtMC4yMzksMC4zNzctMC40MjksMC43NzctMC41NjUsMS4xOTljLTAuMTYsMC45NTktMC4yMTcsMS45NTEtMC4xNzEsMi45NzkKCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}
.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}
.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}
.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-border-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0px;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-warn-color0);
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px 5px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FileDialog-Checkbox {
  margin-top: 35px;
  display: flex;
  flex-direction: row;
  align-items: end;
  width: 100%;
}

.jp-FileDialog-Checkbox > label {
  flex: 1 1 auto;
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
  overflow-x: auto;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 50px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -50px; margin-right: -50px;
  padding-bottom: 50px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 50px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
  outline: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -50px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .remote-caret {
  position: relative;
  border-left: 2px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .remote-caret > div {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -2px;
  font-size: 0.95em;
  background-color: rgb(250, 129, 0);
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 3;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .remote-caret.hide-name > div {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .remote-caret:hover > div {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
  margin: 8px 12px 0px 12px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: flex-start;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0px;
  padding-right: 2px;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 40px;
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent {
  width: 72px;
  background: var(--jp-brand-color1);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent:focus-visible {
  background-color: var(--jp-brand-color0);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent
  .jp-icon3 {
  fill: white;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileBrowser-filterBox {
  padding: 0px;
  flex: 0 0 auto;
  margin: 8px 12px 0px 12px;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing:focus-visible {
  border: 1px solid var(--jp-brand-color1);
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon:before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

body[data-format='mobile'] .jp-OutputArea-child {
  flex-direction: column;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-OutputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  margin-left: var(--jp-notebook-padding);
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
  overflow: hidden;
}

body[data-format='mobile'] .jp-InputArea {
  flex-direction: column;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
  overflow: hidden;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

body[data-format='mobile'] .jp-InputArea-editor {
  margin-left: var(--jp-notebook-padding);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-InputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

.jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
}

.jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-collapseHeadingButton {
  display: none;
}

.jp-MarkdownCell:hover .jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  position: absolute;
  right: 0;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook-render * {
  contain: none !important;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
  float: left;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt:before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body div {
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.CodeMirror.cm-s-jupyter .highlight pre {
/* weird, but --jp-code-padding defined to be 5px but 4px horizontal padding is hardcoded for pre.CodeMirror-line */
  padding: var(--jp-code-padding) 4px;
  margin: 0;

  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
  color: inherit;

}

.jp-OutputArea-output pre {
  line-height: inherit;
  font-family: inherit;
}

.jp-RenderedText pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
}

/* Using table instead of flexbox so that we can use break-inside property */
/* CSS rules under this comment should not be required anymore after we move to the JupyterLab 4.0 CSS */


.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  min-width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-OutputArea-child {
  display: table;
  width: 100%;
}

.jp-OutputPrompt {
  display: table-cell;
  vertical-align: top;
  min-width: var(--jp-cell-prompt-width);
}

body[data-format='mobile'] .jp-OutputPrompt {
  display: table-row;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  display: table-row;
}

.jp-OutputArea-output.jp-OutputArea-executeResult {
  width: 100%;
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }

  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}
</style>

<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: {
                    automatic: true
                    }
                }
            });

            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">
<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[3]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span> 
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">json</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="n">req</span><span class="o">=</span><span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">"https://api.covid19api.com/live/country/united-states"</span><span class="p">)</span><span class="o">.</span><span class="n">json</span><span class="p">()</span>
<span class="n">covid</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">req</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
RangeIndex: 24480 entries, 0 to 24479
Data columns (total 13 columns):
 #   Column       Non-Null Count  Dtype 
---  ------       --------------  ----- 
 0   ID           24480 non-null  object
 1   Country      24480 non-null  object
 2   CountryCode  24480 non-null  object
 3   Province     24480 non-null  object
 4   City         24480 non-null  object
 5   CityCode     24480 non-null  object
 6   Lat          24480 non-null  object
 7   Lon          24480 non-null  object
 8   Confirmed    24480 non-null  int64 
 9   Deaths       24480 non-null  int64 
 10  Recovered    24480 non-null  int64 
 11  Active       24480 non-null  int64 
 12  Date         24480 non-null  object
dtypes: int64(4), object(9)
memory usage: 2.4+ MB
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[5]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Confirmed</th>
      <th>Deaths</th>
      <th>Recovered</th>
      <th>Active</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>2.448000e+04</td>
      <td>24480.000000</td>
      <td>24480.0</td>
      <td>2.448000e+04</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>1.169896e+06</td>
      <td>15378.652002</td>
      <td>0.0</td>
      <td>1.154518e+06</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.522009e+06</td>
      <td>18818.213672</td>
      <td>0.0</td>
      <td>1.504000e+06</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.508262e+05</td>
      <td>2670.000000</td>
      <td>0.0</td>
      <td>2.485832e+05</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>7.225890e+05</td>
      <td>9371.000000</td>
      <td>0.0</td>
      <td>7.122190e+05</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>1.468140e+06</td>
      <td>19855.000000</td>
      <td>0.0</td>
      <td>1.450549e+06</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.116657e+07</td>
      <td>95311.000000</td>
      <td>0.0</td>
      <td>1.107126e+07</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Lets look at this graphically. Lets use a new graphing library called Seaborn.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">sns</span><span class="o">.</span><span class="n">set_theme</span><span class="p">(</span><span class="n">style</span><span class="o">=</span><span class="s2">"ticks"</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">relplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">covid</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s2">"Lat"</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">"Lon"</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s2">"Deaths"</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="s2">"Confirmed"</span><span class="p">,</span>
            <span class="n">sizes</span><span class="o">=</span><span class="p">(</span><span class="mi">40</span><span class="p">,</span><span class="mi">400</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[6]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;seaborn.axisgrid.FacetGrid at 0x1161a6680&gt;</pre>
</div>

</div>
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
class="
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This didn't work. Why? Well lets inspect Lat data type.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[7]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="p">[</span><span class="s1">'Lat'</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[7]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&#39;18.35&#39;</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Ok! Its a string. Now we need to convert that to a floating number. Lets do that:</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[8]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="p">[</span><span class="s1">'Lat'</span><span class="p">]</span> <span class="o">=</span> <span class="n">covid</span><span class="p">[</span><span class="s1">'Lat'</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">'float16'</span><span class="p">)</span>
<span class="n">covid</span><span class="p">[</span><span class="s1">'Lon'</span><span class="p">]</span> <span class="o">=</span> <span class="n">covid</span><span class="p">[</span><span class="s1">'Lon'</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">'float16'</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now lets see if we have this correct</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
RangeIndex: 24480 entries, 0 to 24479
Data columns (total 13 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   ID           24480 non-null  object 
 1   Country      24480 non-null  object 
 2   CountryCode  24480 non-null  object 
 3   Province     24480 non-null  object 
 4   City         24480 non-null  object 
 5   CityCode     24480 non-null  object 
 6   Lat          24480 non-null  float16
 7   Lon          24480 non-null  float16
 8   Confirmed    24480 non-null  int64  
 9   Deaths       24480 non-null  int64  
 10  Recovered    24480 non-null  int64  
 11  Active       24480 non-null  int64  
 12  Date         24480 non-null  object 
dtypes: float16(2), int64(4), object(7)
memory usage: 2.1+ MB
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">sns</span><span class="o">.</span><span class="n">set_theme</span><span class="p">(</span><span class="n">style</span><span class="o">=</span><span class="s2">"ticks"</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">relplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">covid</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s2">"Lon"</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">"Lat"</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s2">"Deaths"</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="s2">"Confirmed"</span><span class="p">,</span>
            <span class="n">sizes</span><span class="o">=</span><span class="p">(</span><span class="mi">40</span><span class="p">,</span><span class="mi">400</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[10]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;seaborn.axisgrid.FacetGrid at 0x116c881c0&gt;</pre>
</div>

</div>
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAkQAAAHkCAYAAADfFDApAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjYuMCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy89olMNAAAACXBIWXMAAA9hAAAPYQGoP6dpAACD1ElEQVR4nOzdeVxU5f4H8M+ZfWDYd0EUQcUdF1RKzbSr3rLFtMXEyqU0K28u1yW9ZpotRlppVpaaLWaZlt30lmXZ9nPDyiVAxQUV2feB2ef8/iAmR3YYGGA+79fL143nPOc538N48cuzCqIoiiAiIiJyYRJnB0BERETkbEyIiIiIyOUxISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhIiIiIhcHhOiKsTHxyM+Pt7ZYRAREVEzkTk7gJYoIyPD2SEQERFRM2IPEREREbk8JkRERETk8pgQERERkctjQkREREQujwkRERERuTwmREREROTymBARERGRy2NCRERERC6PCRERERG5PCZERERE5PKYEBEREZHLY0JERERELo8JEREREbk8nnbfClgMBkC0wlCYD9FshszNHTJ3D1glEsjlcmeHR0RE1OoxIWrhLEYD9NlXYcjLsZUZAAgSKTSdOsMkipArFM4LkIiIqA3gkFkLZjabYSzIt0uGKohWC0rOnYFEtDohMiIioraFCVELJlgs0OdkVF9BtMKQnwOzydR8QREREbVBTIhaMNFqgWg211jHVFwMwWpppoiIiIjaJiZELZlQ1zp1qUhERETVaTUJ0RdffIFbb70VvXr1wm233Yb//e9/tmtXrlzBjBkz0K9fPwwZMgSvvvoqLJbW32siCBJIFMoa6yi8/QAZ58YTERE1RqtIiHbv3o0lS5Zg0qRJ2LNnD8aOHYu5c+fi999/h8lkwrRp0wAA27dvx/Lly/Hxxx/jjTfecHLUjSdKZVCHhFV7XZDJoPDygVQqbcaoiIiI2p4W37UgiiJee+01PPjgg5g0aRIA4LHHHkNiYiKOHDmC9PR0XL16FZ9++im8vLzQpUsX5OXlYfXq1Zg5cyYUrXhJukwmg+CugVtYB5RdvQxY/15RJlWpoekYBatEAqZDREREjdPiE6ILFy4gPT0dt99+u135pk2bAADLly9Hjx494OXlZbs2ePBgaLVaJCcno0+fPs0ar6NJFUqIXr7w8vCGxaCDaDZDqlJDkEohVaqYDBERETlAix8yu3DhAgCgrKwM06ZNQ1xcHO655x58//33AIDMzEwEBwfb3RMYGAgAyMioYcl6KyKTyyFVKqHw9IbS1x8yN3dIlSpnh0VERNRmtPgeIq1WCwBYuHAhnnjiCcyfPx/ffPMNZs2ahS1btkCv18PT09PuHqWyfCKywWCott2RI0dWey0jIwMhISEOiJ6IiIhagxafEFWc1TVt2jSMGzcOANCtWzckJSVhy5YtUKlUMBqNdvdUJEJubm7NGywRERG1Si0+IQoKCgIAdOnSxa48KioKBw4cwMCBA3HmzBm7a9nZ2Xb3VmX//v3VXqup94iIiIjanhY/h6hHjx5wd3fH8ePH7crPnDmD8PBwxMbGIikpyTa0BgCHDh2Cu7s7oqOjmztcIiIiaoVafEKkUqkwffp0vPHGG/jqq69w6dIlvPnmm/j1118xZcoU3HLLLQgICMBTTz2FlJQUfPfdd1izZg2mTp3aqpfcExERUfNp8UNmADBr1iyo1WqsXbsWWVlZiIyMxLp16zBo0CAAwLvvvotnn30W9957L7y8vPDAAw9g1qxZTo6aiIiIWgtBFEXR2UG0NBVziGqaZ0RERERtR4sfMiMiIiJqakyIiIiIyOUxISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhIiIiIhcHhMiIiIicnlMiIiIiMjlMSEiIiIil8eEiIiIiFweEyIiIiJyeUyIiIiIyOUxISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhIiIiIhcHhMiIiIicnlMiIiIiMjlMSEiIiIil8eEiIiIiFweEyIiIiJyeUyIiIiIyOUxISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhIiIiIhcHhMiIiIicnlMiIiIiMjlMSEiIiIil8eEiIiIiFweEyIiIiJyeUyIiIiIyOW1ioQoKysLXbt2rfRn165dAIDk5GTEx8cjJiYGI0aMwPvvv+/kiImIiKg1kTk7gLpISUmBUqnEd999B0EQbOUeHh4oKCjAlClTMGLECDz77LP4448/8Oyzz8Ld3R3jx493YtRERETUWrSKhOjMmTPo2LEjAgMDK13bunUr5HI5VqxYAZlMhsjISKSlpWHjxo1MiIiIiKhOWsWQ2enTpxEZGVnltcTERAwcOBAy2d+53eDBg3Hx4kXk5uY2V4hERETUirWKhOjMmTPIz8/HpEmTcMMNN2DixIn46aefAACZmZkIDg62q1/Rk5SRkdHssRIREVHr0+KHzMxmM86fP4+oqCgsWrQIGo0Ge/bswaOPPootW7ZAr9dDoVDY3aNUKgEABoOh2nZHjhxZ7bWMjAyEhIQ45gWIiIioxWvxCZFMJsPhw4chlUqhUqkAAD179sTZs2exadMmqFQqGI1Gu3sqEiE3N7dmj5eIiIhanxafEAGAu7t7pbLOnTvjl19+QXBwMLKzs+2uVXwdFBRUbZv79++v9lpNvUdERETU9rT4OURnz55Fv379cPjwYbvyU6dOISoqCrGxsTh27BgsFovt2qFDhxAREQE/P7/mDpeIiIhaoRafEEVGRqJTp05YsWIFEhMTce7cObzwwgv4448/8Nhjj2H8+PHQarVYsmQJUlNTsWvXLrz33nuYMWOGs0MnIiKiVkIQRVF0dhC1yc3NxSuvvIKff/4ZxcXF6N69O+bPn48BAwYAAE6cOIFVq1YhKSkJAQEBmDp1KuLj4xv8vIohs5qG1YiIiKjtaBUJUXNjQlQ3FqMREARI5XJnh0JERNQorWJSNbUcpjIdYLVAe+kyTNpSCBCg8PGGW7sQCBIJZGqVs0MkIiKqNyZEVGemsjLkHz8JfXaOXXlZRgYKk1Pg3j4M3tFdIFOrG/0si8kEWC0QzWYAgCCTARIpe6OIiKhJMCGiOjGXlSH7/w7BXFpWdQVRROmlyzCXlcG/X0yjkiKL0QBDbg70WRkQreWrBwWJFKqgECj9AyBVKBvcNhERUVVa/Cozcj6zTo+CP5OrT4auYcjNQ+mVdLttEOrDYjRAn5UBXcYVWzIEAKLVAl3GFeizMmAxVr8DORERUUMwIaJaiVYryjIy61y/5PxFWPX2SYvFaITFoIe5rBRmvQ4Wg76ah4nQZ2dV27Y+OwvgOgAiInIwDplRrfTZ2fVKQix6PawGA+BefnSKxWBA2ZU0GArybO3I3Nzh3qETIFdArvx7CMykLQFQ07NEmLQlkCo5eZuIiByHPURUK1MdhsquZ9bpAJQnQ8VnkmDIz7VLqsxlpShKOQWY7M+hg9Vae+N1qUNERFQPTIioVoKk/n9NBIkUAGAqLoRFr6u6kiii9NIFu+Ezmbum1rbrUoeIiKg+mBBRrVT+9T8TTu7hDrNeD31O9fOBAMBcqsW1e4MKUilkbtUnPDI3dwgyGUylZTCVlsKkLYVZX818JCIiojriHCKqlczdHVKVCpY6Jh4qfz9AIgUgQrSYa7/B+ndCJFWqoOkUhZLU05V6lqQqFTQRnaHPzkXxufOw6PQQJAKUvr7wiOoEqUIBmZtbfV6NiIgIABMiqgNBqYBXdBfk/3GiTvW9u0dD7qaGxWiAVO1ecyIlkUCQ2ndUSpUqeER1hcVggLEgDwCg8PGDRCZH1v8dhlmrtatfdjUDZVczoArwh29Mb4dsDElERK6FQ2ZUK5lMBnVAADy7RNVcURDg378vJKryFWBShRLq4HY13qL0CwCqmKMkVaqg8PSCpkMnaDp0gggBV7//sVIydC19Ti7yfj8Oc1n9J4ETEVHVXOXIU/YQUZ3I3NTQdOgAdUAAik6fgT437++LggC3kGB4dekMQaGA/JrzzAS5HG6h4ShLv1RFm+5wCwmDVK6o8dnmsjIU/HGiTqvLDLl5MJVoOXRGRG3K5MmTceTIEdvXgiBArVYjIiICd911Fx544AHIZI79J724uBjPPfcc7rnnHsTGxtriAIAPPvjAoc9qCZgQUZ3J3dSQu6khdesDWEVYzWYIQvk5Y4JEWuXBrjKlCvDzh9zLG/rMqzDryiCRyaAKDIbMXQOpsvZjOKxmM4yFRXWOs/jsOcg9NEyKiKhN6d69O5555hkAgMViQVFREX766Se88MILSExMxKuvvgpJA1YFVyc5ORm7d+/G+PHjHdZmS8aEiOpNXs9EQ6ZUAUpA0r4jRKsVgiDUKRGqoM/Kqb3SNQz5+dzMmojaHI1Gg5iYGLuyESNGoFOnTli1ahW++uor3HHHHc4Jrg3gHCKqF4vRCLNOB2NRIQz5eTCVlto2YayNVKGATKWqVzIElPcQ1Zvo2M0bLQY9LPq//lR37AgRkRPEx8cjKCgI27dvt5Xt2LEDt912G3r27Inhw4dj3bp1lc6Y3LFjB+6++27ExMSgd+/euPPOO/G///0PAHD48GE8+OCDAIAHH3zQNlQGlM8peueddzB8+HD07t0b9913H06c+HvRjV6vx/LlyzFs2DD07NkTY8aMwaZNm5ryW+AQ7CGiOrPo9dBevgRdxlWI1/wfS6bxgFfnLpCoVJCpHH+khlRVz9PtBQEWvQGG/EKo/H0bNXRmNhhgNeqhS78Mc2n5hG6p2g1u7dpDqnard3JHRORoEokEcXFx2LNnD8xmMzZt2oS1a9ciPj4eixcvRnJyMtatW4eMjAw8//zzAICPPvoIzz33HJ588kn0798fRUVFeOeddzB//nz07dsXPXr0wLJly7BixQosW7YMgwYNsj3v2LFjMBqN+M9//gOz2YwXX3wRjz32GH788UfIZDI8//zz+OWXX7Bw4UL4+/vjp59+wurVq+Ht7d2ih9+YEFGdmPV6FCX/CWNhYeVr2hLk/fEbfHr1gSiRQBAECBYLrH8lTRKpFKJUCplcXq9nWgwGQLRCHRQIuacHSq+ko+xKOkRLzb0/6uAglGVkojj1PGQadwTdMAhyd/d6PRsAzEYjLNpiaC+es49LV4aSc6fhFtYBch9fyBRMiojIufz9/WEymZCVlYUNGzbgvvvuw9KlSwEAQ4YMgbe3N5YuXYopU6agc+fOuHz5MqZNm4ZZs2bZ2ggNDcXdd9+NY8eO4bbbbkNUVPnK4qioKNt/A4BCocDGjRvh7e0NoHzy9dKlS5Gamoro6GgcOXIEN954I2677TYAwKBBg+Dm5gY/v/pv8tucmBBRnRjy86pMhmxEEYVJp+AfOxCGnByUZaZD/GuoS5DJ4RbSDkJAUJ16VEwmEwSzCaWXLsBU/NdkaokESh9/aOIGIefIMViNxmrv14S3R07ibwAAs7YUWb8eRvCQOMjc6rc/kSCKKL10sdrrZemX4O3tU682iYiaQsXS+KNHj0Kv12PEiBEwXzPdYMSIEQCAX3/9FZ07d8aiRYsAlCcz58+fR1paGg4fPgwAMNbw8xUoT5AqkiEACAsLAwCUlJQAKE+Atm/fjszMTNx000246aab8PjjjzvmRZsQEyKqlVmnQ+mlysvmryeazTAVFUGfl2NLhsrLTSi9nAZzqRbuHTrVOqwmmE0oSj5pNywHqxWGvGyYy7Tw6xeDnENHqrxX07EDDIVFsBpNf8dfWorS9AyISnco3FXlq9y8qu8xshgNsBgNEI0miFZLtfUgijCVFEOqdPwwIRFRfWRlZUGlUtlWmT366KNV1svOzgYAXLp0CcuWLcPBgwchl8vRqVMnREdHA6h93yG366YhVDzT+tfWKEuWLEFwcDC+/PJLrFy5EitXrkTfvn2xfPly2zNaIiZEVDtRhEVXt80ODQUFkLm5V1nfkJ8HdbswoIaEyGI0oCz9sn0ydO11XRkgmiH39ICpuMRWLkgl8OjUCVK1Gnm/H690X8n581B1iMRvG3fDr3MYOtzcDyovDVRe9uemWYxGlF6+ANFshsLLt9b3ramnioioOZjNZhw+fBj9+vWDp6cnACAhIQEdO3asVNff3x9WqxWPPvoo5HI5PvvsM3Tr1g0ymQypqanYvXt3o+NRKBR47LHH8Nhjj+Hq1av44YcfsGHDBsybNw979uxpdPtNhavMyMFq/s1CdzUdlpqSCFGEsTC/xjaMBXnwiu4CVVAg1CHB8O7RDQGDYmHW6apMhgDAXKaDUqMGRBF5Zy7jt7d342piCnRFf+98bTabYSzIhVlbAqvZBGkdJohzryMicrZPPvkEOTk5mDhxIvr06QO5XI6srCz06tXL9kcmk2HNmjW4cuUKCgoKcOHCBUyYMMF2DQB++uknAH/39Eil0nrHotfrMXr0aGzevBkA0K5dO0yaNAm33XYbrl696qA3bhrsIaLaCQKkajUsdVher/D0gi4ns9rrFoO+1mGo2jYRslostphgsaL0ylXkn/iz1tiud/H7Y5Ap5Qjs0xl6gwlubnLoc8u7k0WzGSIAiVwBq6nqBE6QSiFVMyEiouah1Wrxxx9/AChPWgoKCvDLL7/gk08+wR133IFRo0YBAKZPn47XXnsNWq0WgwYNQlZWFl577TUIgoDo6Gh4eHggNDQUH330EYKDg+Hp6Ymff/4Z77//PgBA99fPeg8PDwDAgQMH4OXlVafhLpVKhR49emD9+vWQy+Xo2rUrLly4gM8//xyjR49ugu+K4zAholrJ1Gq4tw9H8ZnTNdYTZLLyxKmGs8QkcjkEoYaOSUGARKGE1WioPh53DYwFRSg5d6HW2Gui8HADVEqkX8jEdx/vxx3T/wml+e+5R7qsDLh36ISS82cqHxsiCPDo1AVWiRT1/x2KiKj+kpKScN999wEoP7rD3d0dXbp0wfLly3HPPffY6j311FMICAjAtm3b8O6778LLywtxcXGYO3euLcnZsGEDVq1ahUWLFkGhUCAqKgpvvvkmnn/+eSQmJmLy5Mno3Lkzxo4di48++gg///wzvvrqqzrFuWLFCrz66qvYvHkzcnJy4OfnhwkTJuBf//qX478pDiSIrnJqWz2MHDkSALB//34nR9JymPV6FP55Eqbi4mrr+PTsBV1OFkxFhdXW8YruAaVP9XNzzGYzTHnZNa7u8u4Zg9KrWSg4caouoQMA5J4ekPmF4M8dBwAAvt06wq9fV3y8difSU9MBALPXzoSvvNRuQrjM3QPq4FAYC/JgLCoAREDu5Q11YDBEiRQyRc3nsBERUevAOURUJzKVCj49ekHdLrTS6fQyN3f49ukLmYcnxGt6WCq1ofn7fLHynZ91MJeVlf+3qfw+mUwGhY8fFD5V71eh6RgJSKRwCw6qFEdN3NuHI+3X8gTKv1ckpO2DsfapN2zJEAD8uOtXKHwC7O4zl5ag5PxpWK0WqEPCoInsUj6kJwhMhoiI2hAOmVGdSVUqaDpGQBPeARadDqLFDKlKDUEmg0xdvsePV9fuKLl4Hsb8PLt7lb7+0HTsBKsgwFqqRenli7CUlZZflEig9PWHOrgdpAolpAol3Nt3gDq4HfTZmbCaTZCp3aEMCAQECWRKJUxWHXx7dUf+8dp7iRQ+3rAKMmiv5kIT4gdVZBjeXPSubeJghZO//olJC++DpazEtis1gPLl9UWFUHj5wlymh0SphtUqcqiMiKgNYUJE9SL7a2PFigToelKlqrwXp0MEzGWlAATI3NwgCBJIlUqIujIUnUmynzhttcKQmw2rwQD38AhIlUpIlaryPyp1+SRsqcxuxYNcrQZCguEjiiioYUK10s8X7hGR+OO9/0GQStD+loHYsGRTpWQIAASJAIvRBIVPEOSevjBriyBaLZAq3SDTeCIn8RRKr2RCHeSPkKGDqngaERG1VkyIyOFsSZPKPmmyGA3QXb1S7SoyU0kRRIsZwN+7WUtkMlz/19RsNAIWC8wlJVB4eiD0luEoTc9AycVLsBoMEKRSKP384BYWhrL8Evy+ZS8sBhMCekXiyPe/ozi/BFWZOHc88o8no/TiZSi8PKDpEAqJXIaSy+nQXjpqi1uXlYv0AwcRMmwQlJ6aKtsiIqLWhQkRNR8R5ROTa2DIz4PMrfpdpM16PXRXr0J78eLfmzcKAjSRUfDu2QtmgxEWkxnFl3Nw5v19MJX9fTK9b69IfLTwnSrb9fTzRHinYBQePAoAMBaVIP9ESnnzUkmlJM6Qm4/Sq1lMiIiI2ggmRNSM6rCgsYZFjxVHiFQ6RkQUoT2XCs8effD7lr1VPkaqlKOsVA9dqb7yRQA33XUjjJcu276Wa9zh26sL1AF+EC1mCFIpjMWlyDuZAkNeIQCg8M/T8GgfArk79yIiImrtuMqMmpEAmcajxhqKaw4MvJ5otVZ/ppoowlxciJB+Xaq87NHOH2mnr1TbdvfYLii7Wr6hpDrIH+1GDAYsZSg5lwztxbMoOZcCc0kuggfHwDOqAwDAVFIKi7H6VXVERNR6MCGiZiNVKuHWLqz66yo1JIqqj8uwmM0wFRdDUsNS97LLaWg/uBv8uoZXuqb0dEdWeq5dmUwuQ+w/+uOxF6bD288TEAGJUoGgQTEovXDWfqUZAIteB+3Fs/DuGgGlr3d5mYFnmRERtQUcMqNmJciV0EREofTSBbsDXGXuGmg6RkKq/HtCtdmghyAChvxcmEu1EKRS+PTsCYvJiOKU07D+tXeRIJdDFRQMubcvrCYLIkb2R8cR/WExmJDx22nkJl2AR7tA9GsfjK59OsFkNMMn2Bce3u7I+C0Vp3f8hKDHbwcAeHeJgD4vq8bjRfRZ6fDt2QUZPx0pn19EREStHhMialYypRIQBHhF94TVYIDVYoFUpYIgkVZKhkxFhdBeOGc3r0ifnQWpuwa+MTHIP3kSbmHhsEKGyweTkP3nTxAtfy+nV3prEH3Hjeh4cz9k/nYGxSmXYDYYIZXLYDEaofSJgl/7AOSevgyjzgDv7p2hiegAi8EAqcYXEokEFp0WxsIciKa/h8YsujKo24UDEsEuZiIiar2YEFGzq9jhWaqs/jR5q14P7fnUKq9ZSrUovZIG35i++HPHAeSdqTw3SO3nie4Tbkbaj78j9/SlShOttZn5yDh2Gh6h/rhxxliIFguy0zJwbv8XsJr+OrpDEODTOQxhg3tAppBAn3np714tqxWaDmGQKuT1/wYQEbUSVqsV69evx44dO1BSUoLY2FgsW7YM7du3d3ZoDsf+fmpxzHo9Si+n1VxHWwKzTo+iy9mVrik83NDjnpvx56ffIzelcjJkIwgIv7EXso+fwYnN/0VmYsrfyRAAiCIKzlzGyfe/xvnvfoNb+ygIsvLfIQSJFL49oyFTsYeIiNquDRs2YNu2bVi5ciW2b98Oq9WK6dOnw2hse/MnmRBRkzLr9TCWFKP06hWUXr0CY0kxzHo9LJbq5+hAFGHWVr15ol3bJYXw7hBcqTz6rqFI/vxn6AtqbiNqzECUZuQi40hSrc8qupiJ07t/gVtYJ8g0HrBYRZgh1HofEVFjiaIIk7YYhoI8mLTFaK4z2Y1GIzZv3ozZs2dj+PDhiI6Oxtq1a5GZmYl9+/Y1SwzNqdUlRBcuXEDfvn2xa9cuW1lycjLi4+MRExODESNG4P3333dihAQAZoMBxuIiFCWfQuGp4yhNu4DStAsoPHUcRcknYdGWwGyoek+gOu1XBACiCInM/kQxta8nrCYzSrPya7xVoVHDI9gXmcdS6vYsANqruchJvgT3DpHQ6s3w8POq871ERA1hLCpAYcoJlJw/g9LLF1By/gwKU07UusmtI6SkpKC0tBRxcXG2Mk9PT3Tv3h1Hjx5t8uc3t1aVEJlMJsyfPx9lZWW2soKCAkyZMgXh4eHYuXMnHn/8cSQkJGDnzp1OjNS1mc1mWA16FCadhEWvq3Tdov/rmk4Hs9lcuQFBsA1N1URQqFCWV2xXFjqoO64crr3HJ3RgN2T+drrWetfLOJqMkvxSKJQ86Z6ImpaxqADatHN2izoAQDSZoE071+RJUWZm+d5sISEhduWBgYG2a21Jq0qI1q1bB43G/qiETz/9FHK5HCtWrEBkZCTGjx+Phx9+GBs3bnRSlASzGcWpp2vcdRoASs6dAapKiKQyqAIrD4VdS5BKIUoU0Gbk2ZV7tQ9E4YWMWkP069IeBanVb9RYHVOpHjAY4B3gXe97iYjqShRFlF6tZiPav5RevdSkw2c6XfkvtIrr9n9TKpUwGAxN9lxnaTUJ0dGjR/HJJ5/gxRdftCtPTEzEwIEDIbumR2Hw4MG4ePEicnNzr2+GmoHVaIC1Dv9nsRqNsBoNsOgNMJWVwfzX//lkcjnUQSGQuVd/ppkqtCPOf3escpuWyqfYX0+QSMp3mL7uB4kgqducoJIqJnITETmSubSkUs/Q9USTCebS2udbNpRKVb4S+PoJ1AaDAWq1uqpbWrVWsey+uLgYCxYswNKlSyt13WVmZqJLF/vjGgIDAwEAGRkZ8Pf3b7Y4qZyxqLDWOjIPT7iFhMJcpkNRyllYjUYIMhnc2oVA5e8HUSqFZ5fu0OdmQ5951bYJo8LbF3LfQFz86WT5CrIGkMgkEM3liZNXRDuEDuoOhUYNWC0QpFLoCkqQfigJJVeqTnzsVqIRETUBay3JUH3rNUTFv7fZ2dkID//7BIDs7Gx07dq1yZ7rLK0iIVq+fDn69u2L22+/vdI1vV5fZXcegBq79EaOHFnttYyMjEqJF9VDLT24Sl9/KLx9kXfsD1iv/80jNxeCVArvHt2h8veHMigEKr+A8t4cQYDFbEHixq9Qll312LlEKgGEmmOwGM2QqhXoMfEWwGxA6YWzKC77e66TTOOODkO6w2TohjO7f4Zote91kmva3m9GRNSySOR12+OsrvUaIjo6GhqNBocPH7YlRMXFxUhKSkJ8fHyTPddZWnxC9MUXXyAxMRH//e9/q7yuUqmq7M4DADc3nkLuDHJPDyC96msyjQcUPn7IPXqs2jlGosWCghMn4dOzB5RBgZBd0zVrKdPBp2MIyrILoAn2RUCPjpCrlLAYTchLTUfhxQz4RoUh/2wN84MEAWpvDQqTk6DPyql02awtReGfSXALDUWXO4fi9Oc/2l337dz2NiQjopZF5u4BQS6vcdhMkMshc6/5wOzGUCgUiI+PR0JCAnx9fREaGoqXX34ZwcHBGDVqVJM911lafEK0c+dO5OXlYfjw4XblzzzzDPbu3Yvg4GBkZ9sPbVR8HRQUVG27+/fvr/ZaTb1HVDupyg0SubzKrly3kFDk/X6i1gnXAFDwZxKCAwMAlO9nBKsVgtWKqDED0GFIT+jzC1B6KR2WwiJI5XJ0GNwFKj9f+EaG1pgQdRjaB7rMzCqToWuVpafDu4c3PEIDUJJeXtezQzAk8hb/fxsiauUEQYB7u3Bo085VW8e9XTgEoWn3Q5s9ezbMZjOWLl0KvV6P2NhYbNq0CfIm7JlyFkFsrh2eGigrKwt6vf1+NaNGjcL8+fNxxx13YPfu3di+fTu+/fZbSKXle9KsWbMG+/btw9dff92gZ1YkRDUlTVSZWaezDW1ZzWaUnDsDi+7vLRIkShXcQsKQd+z3Orfp1S0a6qBAFJ89A0N+PtRBwZB7+iDjl6OwGisnXIJUgoDYGOi0RiR9Zt+z025AV4Tf2ANyNyWyfj0Eax1Oqpd7aKAMCUfKzgOAIKD3w7fBs331iTYRkSMZiwrKV5Nd8wumIJfDvV04FF4+Toys7Wnxv+pW18vj5+eHoKAgjB8/Hu+++y6WLFmC6dOn48SJE3jvvffw7LPPNnOkrsus08Gs1aL43HkYC8rn9ii8vOAR2QmQCCg5fxawWqHw8kZZRv32rii7cgUSuRSG/HzIvbwh9/JB+vf/V+0cIdFiRfah3xA4qC8iRvTDhe9/AwBEjhoAv04B0J4/Da/OXeuUDAGAqUQLr+7lXdJRtw+B0ltTyx1ERI6j8PKB3NMb5tISWE0mSP4aJmvqniFX1OITotr4+fnh3XffxapVqzBu3DgEBARgwYIFGDdunLNDcwlmnR5Fp89Al2G/94+xqAh5v/0OVWAAfHrGQJd5FXIPTxhy67eRmNVkgiAt/2vqHtYeV388XKeNrLOP/IGOd42GvkiLstwi+HcJQen5M5DIFVX2LNVEEIAek0bDLcAHSo/qtwIgImoKgiBArvF0dhhtXqtMiE6ftt9huHfv3vjkk0+cFI3rMRqNyM7MhUqtgkJbXCkZupY+OwdyD094dIqACEC4XM1s62oIMhlEiwVStRoWgxEWXR03AxNFaC+lo9PI/pAqZChKPlVebDHXe1WG3F0N95DAet1DREStS6vZmJGcLyc7F1cuZ+CDd3fgX48swaXUiyi9eKHW+7SXLsFqNEIqk8EtLLRez1QHBcNQkA+Fjy9KLtRvZ+mS85dgyMmB1aC3zWUSrVYIUgESRd2SIpm7GwSptPaKRETUqrXKHiJqXqIoIuNqNt55fSt2f/Y1zObyk+qDAnxhOVv7rs2iyQSL0QSZG6Dw8IBEoai0/1B11EEByPvjd7iFtS/fXboeLEZj+Yqw69YN6LKz4BHRAUWnU2ttw6tLZ0hUyno9l4iIWh/2EFGNcrPzcOzwccTfNRM7t++xJUP1ZTIYkJeTD8hk8O3Tu073eHXtAl12NiCK5cNmdezVqSBVKMp3lZbY/zU35OVCHRgApZ9vjfe7hQRDFeBvW71IRERtFxMiqlZOVi6OHvoD0yfOQW52fqXrtZ8a9rfiUj0O//ob8guKIfP0gP+A/tUPRQlC+XL74GCUpZcPkxkL8uHRMaxe8Ws6hEKXlQ1dZg4U3tcsTxVFFJ1Ohk/3rvCK7gLJdTudS1UqeHePhjokBMXnG3Y8CBERtS4cMqMqlZXpcDrpHBb/6zlYrVWnPj8dOIxbekXAlF85WbqW3MsTib8l4en5L+L1TS+g/6A+UHp7IfimodDn5aH00hVYTUZIZDKog4Ph1i4EoiBAAKD09YUhPx8WnQ5SlQJStbJuE6sFAe7tgpBx9iyMRcUIunEgTCXFEC3lPVyixYzCpFNQ+vkhcFB/QCIpX30mlP9vYco5lKZnwjOyA6xWKyQS/u5ARNSWtfiNGZ2BGzMCVy5n4L5bp6OkWFttnaCQALy/bQ0sZ1OAapImCAJknbti5oxlOH82DRoPd3y6912EhbezVTGV6QDRCggCJEql3RCVRa9H8blU6LKyIPf0gjowBOk/VL8PUYWAAb1gLiuD9mJ5D4/K3w9+MT2gvZwG0zWHz0oUSriHhcNUakDub6dgNZntzi7zjOqAoBsGMCEiImrj+FOeKsm4moUX/vNqjckQAGRl5GD1ixshi+oCibLyxGOJQgFZZGe8sWEbzp9NAwBoS0qx6j+vIuNqlq2e3E0Nubs75G5ulebrSFUqeERGIXBwHNyCgyCRSxB6y5BqV4mV71TdB4Ig2JIhANDn5iHz/45CqtTAp2cfeEX3gHeP3vDq2g1lmXnIOvgbLAZjpYNcVb4+TIaIyGUVFhZi2bJlGDZsGPr164eJEyciMTHRdv3gwYO4++670adPH4wZMwZ79uyxu99gMODZZ59FXFwc+vbti3nz5iH/ulEFR7ThCOwhqoKr9xCdST6HCWOm1rl+777dMG/howj09YT0r+XtFqUK+aV6vJawGUcOVj6qY8f/NqFr96gGxWcyGiEaTdDn5KPozHlYDOWryTwi2sMtOBDatEuQKJSQqlUQBAEWvQGlV9JhyMuHRCGHpkM41MGBgFWEVK0qv56eiaLUi3Y7WAsSCTqOGwMFN2MkIhc1depU5OTk4JlnnoGfnx8++OAD7Ny5E59//jlEUcS4ceMwZcoU3HHHHThw4ADWrFmDd999F3FxcQCAxYsXIzExES+88AIUCgWeeeYZuLu748MPPwQAnDt3rtFtOAoToiq4ckKUl1eA1154G1/s+F+97w0JDUJU1whIBAnOp6bhclr1mzDeMX405i55DL5+DT+Lx2qxwKI3lPfqCAIkchmsBhO06VnIPXkWhoJiQBQh93CHf+8u8AgLgkmnR96JMyi6cBmwlv/VFyQSeHYKg2+3SFh0euQcOwGr0QTPyA7w798Lcjd1g2MkImos0SpCl50Li04PqVoFdaA/BEnTH92RlpaGUaNGYdu2bejfv395LKKIUaNGYezYscjLy0NycjJ27Nhhu2fevHkoLCzEpk2bkJWVheHDh+Ott97CTTfdBAC4cOECxowZg+3bt6Nv375YtmxZo9twFE6qJjv6Mj2+/u/3Dbo3Iz0LGelZtVcE8PVXP+CxOVMAv7q3bzGWD2kJcjmkUikkUikk7m4AAKO2DLqcAlzc8xMs151TJugNUPl64fKBIyi7WnnfJNFqRVHqJRSlXoJ7u0C0u/kG5B9Pgn+/nkyGiMiptJfSkXP0OMxlOluZzE2NgNg+0ITXb6Pb+vLx8cHGjRvRq1cvW5kgCBAEAcXFxUhMTMQtt9xid8/gwYOxatUqiKKIY8eO2coqREREICgoCEePHkXfvn0d0oajcHIE2dHrDNDr63g8RiMYDUboyvS11jPp9TCVlqEk7TJyjv6OnCO/o+DEnzAWFcNUWvZXHQMMhcU49/n+SsmQRC5Dh9E34upPiVUmQ9crvZqN9B+PIujGWMj/SraIiJxBeykdGT8eskuGAMBcpkPGj4egvVS/o5Dqy9PTEzfddBMU12xN8s033yAtLQ1Dhw5FZmYmgoOD7e4JDAyETqdDQUEBsrKy4OPjA+V1c0wDAwORmVl+0Lcj2nAU9hCRnXNnaz+Kw1HOnj6PqK4R1V43lZXBWFiM7MOJEE1mW7kuEyg+ex7q4EAEDOgLq9mCi1/9WGlHagDw79MV+X+mQp9fWOe49HmFyDz0B4Jv6AsFkyIicgLRKiLn6PEa6+QcPQ73sHbNMnwGAL/99hsWL16MUaNGYfjw4dDr9XbJEgDb10ajETqdrtJ1AFAqlTAYyn/xdkQbjsIeIrJz9Urdhrwc86zqs3uLxQJTiRZZvx6yS4aupcvMRs5vxwFRLD+i43qCAM+OoSg6V//NFQtT0yCa67P1JBG1VKLVCqvJCHNZKUylJbAYjbBaGrbrfnPRZedW6hm6nrlMB112brPE891332Hq1KmIiYlBQkICgPKkxHjdMUwVX6vVaqhUqkrXgfJVY2q12mFtOAp7iMiO2Vx18tHcz7Lq9chN/KPq/YYEQBPeHh4dw2E1GWEqLkKHUXEQpFLk/nkOBSkXAFGEZ4d20F7OqLLnqFZWEUWpafCLiebRHUStmNVigamkCGXpabaNWSEIUAWGQOUXCImsZf4zaNHVPqWgPvUa48MPP8SqVaswZswYvPTSS7Yem5CQEGRn209FyM7OhpubGzw8PBAcHIzCwkIYjUa7Xp7s7GwEBQU5rA1HYQ8R2fHw9Gi2Z/n5+cBcqoU+LxemkmKYdTpbkmTR6WH+a46QHYmAoLhYKDw1yD9+HAUnTqLw5CkUnjyBwlMn4Bnqi4ixwyBIJdCEBqHkYsPH2IvOX4JZW0UMRNRqWA16lF46/3cyBACiCH3WVRiLC9BSF1pL1SqH1muobdu2YeXKlZg0aRLWrFljl5QMGDAAR44csat/6NAh9OvXDxKJBP3794fVarVNjAbKV4hlZWUhNjbWYW04ChMistOtZ+dme1bXrh2ReywRBSeOIzfxKPL/+A3mgnyYDQboc6vedMs/pjf0OTnQXrgA8boeJtFsQenFizDl5yJseCykSjnMhspdrXVl0Tf8XiJyPqvFjLLM6n8p0mddhWg2NWNEdacO9IesllWuMjc11IH+TRbDhQsX8Pzzz+Mf//gHZsyYgdzcXOTk5CAnJwclJSWYPHkyTpw4gYSEBJw7dw6bN2/G119/jenTpwMAgoKCcNttt2Hp0qU4fPgwTpw4gblz52LgwIGIiYkBAIe04ShMiMiOj69Xsz3L29vD7rc2i16PglMnYSktrbK+VKWETOMGXUbNKwv0WVlQemnK9yZqxHCXIONQGVFrJlqtsOiq7+W1mkwttodIkAgIiO1TY52A2D5NOqH6m2++gclkwrfffoshQ4bY/Vm1ahU6d+6MDRs24Mcff8Rdd92FHTt24OWXX7ZtqAgAK1euRFxcHJ544glMmzYNnTp1wuuvv2677og2HIUbM1bBlTdmvHolE/96ZAlOJ6U6rM3O0Z0QOygGXl4alJSU4tjREzCbLVj32mIIGZcr1Zeq3eAR2RkZP/xiV+7drQsseh0MOTm1PlPp7w9FYDAKks6h+MKVBsXtFdkeIUNjoXDnXkRErZHVZELJ+dOwGKqZZyMI8I7uBYm88iqmlsKZ+xC5mpY5m4ycpl1YMKbMnIhFs1c2uq1b7xiJBx8eD5XZAmtGHiwGI6QKOcaPHgafDu0gLStGVb+7WXRlkKqUkKrVsOj+/iGg8PJEcVZGnZ5tLCqCMjAYPt0iG5wQ+cd0YzJE1IpJ5HIoA4JRduVildcV3n5AC180oQkPhXtYO6fsVO1qmBBRJTH9e8LbxwuFBUUNul8ikeCFVxaji58vin45jtLr5/GcvYSiw38ieGAPeHaORknq6UorwcylpfDv2wtZ/3fNZDsBtZ5ybyOKfy21tULhpYGxqOaDaq+n8PKodfyeiFo+hYcXTB5eMJXY/zyTKlVwC24HiaRlJ0RA+fCZW3CAs8No8ziHiCrxC/DByoRFDb7/2efnIVKpQv7hU5V2jq5gMZqQ/ssfyDlxHppOVU3kFqHw80HAwH7AX6fNG4uKIfeu2xwnhbcX9HlFyDlxGu2GxgJCPX6bEgSE3TwISk9N3e8hohZJIpfDPawjPCKjofD2g8LLB5qOUfDo1KVFD5VR82NCRJUolUp07RGFUbcNr/e93Xp2Qe/IDij683yd6ueeOgd9QRkUXt5/FwoCFF7ekKvVUAUGoP0/R8K3T08YC0ugCQ+vU7tuoWEQFAoExvaGNqcIoTcPhiCp/a+7IJGgw5ihUPg03/YDRNS0JHI55O4auLfvAPf2EVB4ejMZoko4ZEZVCg4JxPz/PI7MjByc+O3POt/3yIz7UVrHZKhCxpFT6PTPwTAWFQIA3NqF2nqFKg5X9YiKgHtYO0AA1CEh0GVUP5dIFRIMuZcnLu85ivxz5Utug2M6I/zWm5B34nTVmzUKAjzC2yFwQA8oPDU81JWoDRIESfnQO1EV2ENE1QoOCUTChuW4YVjdNr9y17ihc6dw6HIK6vUcQ0EJrFYBglwOdXAI3MM7QHbdQX5SqRRydzfI3dzgFd0Vmk4REK6bDClIpdB0ioBX1y44+tZuWzIEAJl/nMXxD74F1Bp0vH0EAmN7wbdHZ/j26IyQIf0RNWE0PNsHIOfQUcDKIzuIiFwNe4ioRsEhgVj+0gIc+uUYXnjmNehqOFsnpF0QjAXFDXqOLrcQ/gMGAhAhU9W886pMrYKmUwQ04e1hKtHCYjBAqlJBrnGHaLHAWFKKbnfciIs/n0Temb+X9RtKynDu20Sc3/8bPNsHQuFe/hzrhVx0/oc3CpPOlFfkThRERC6HCRHVKrhdIEaMGYLYuBh8/ule7PhwNwryK69AkyvkgKVhvStWo7nWROhaMoUCUCggSiQQyspQfCYVhty/DzmUqlSIuLErwgZG48S2/RCv6fURrVYUpdlv7hjYLRxKP18Y8gvqNwGbiIjaBCZEVCeenh7w9PTAtJkPYNy9t6Igvwgnfv8Tvx89iaLCEgBAx07h8AjwQWED2pfXsN9PbnYe9HqjbdW9UilHQJA/TDodDDm5KDhxstI9Fr0e2tSzUIWEoPvdQ/HnZz/W+Py0X06ix51xkKlVdZp8TUREbQsTIqoXtbsaoe5qhLYPQc8+0bhjwhiUaXWAALi5qSC3AldkUohmS+2N/UWQCNC0D7Yry7yaDV2ZHt9//QtOHkvC+dQ0GHQGKFVKdIwKR+9+3RH/8B0oOHmqxrb1GRnw6tkbKh8P6AtKqq1XllMIiVIJ726duf8QEZEL4q/C1CgajTsCg/0RGOQPjYcGgkwK3+iIerXh3Tkckr/ODcvNyceZpHN4Zu5qPPDPmXj3tQ9x+JffkJOZh+IiLXKy8nD019+RmnIeBecv1mm+jy7jCsJv6FF7IBJJk58cTUTUWl24cAF9+/bFrl27bGXJycmIj49HTEwMRowYgffff9/uHqvVitdffx1Dhw5FTEwMHnnkEVy+bH9kkyPacAQmRORQCnc12t3QBzK1svbKAKRKBUKH9oNC44bszFzs/PArTBn3L5w4llTjff0H9oREW7cJ3Ma8fHi1D6y1nkShgNzdrU5tEhG5EpPJhPnz56Os7O8DlwoKCjBlyhSEh4dj586dePzxx5GQkICdO3fa6mzYsAHbtm3DypUrsX37dlitVkyfPh1Go9FhbTgKEyJyOKm7Cl3vGwNZLeeAydRKdL1vNGTuKmRn5uK1F97BexvK/7LX+gyptF6LwYRaJkpLFTJIebo9EbVAotWK/HPpyPjjLPLPpdstEmku69atg0Zjv3v/p59+CrlcjhUrViAyMhLjx4/Hww8/jI0bNwIAjEYjNm/ejNmzZ2P48OGIjo7G2rVrkZmZiX379jmsDUdhQkQOJ5fLofD1QPf42xB2U3/INfa9LjJ3NdoN6YvuD46Fws8ThUVafPLeF/h+7891fsbZ0xchcXevWzweHijLq7k3KaRfV0hV3LmWiFqWrFPn8fOLH+LYxi9x6uPvcGzjl/j5xQ+Rdap+G+A2xtGjR/HJJ5/gxRdftCtPTEzEwIEDIZP9PR158ODBuHjxInJzc5GSkoLS0lLExcXZrnt6eqJ79+44evSow9pwFE6qpiYhk8kg89IgsG9X+HbtCIvJXL7hoUQCqUIGmZsKUrkcAJCdkYuPN39e57ZDwoJw9/1j4BkaiJyrV2utr2oXipT/HauxTvsbekLhxvlDRNRyZJ06jxMffFOp3FBUihMffIPek0cjqGenJo2huLgYCxYswNKlSxESEmJ3LTMzE126dLErCwwsn56QkZGBzMzy7U2uvy8wMNB2zRFtOAoTImpSUoUCUkX1PS8Z6Vl44enXINZx/Cs4NBDr3lkOc/Jp6CQi3MJCUXYlvdr6ck9PWAU5StJzq63T6Zb+kCrldXo+EVFzEK1WnP7ylxrrnP7yVwR279ikW4UsX74cffv2xe23317pml6vh+K6n+/Kv04ZMBgM0OnKN/Ktqk5RUZHD2nAUDpmRUxUVFOPcmYt1rv9cwr9hSTkDs7YU+SeSofTxgyYiosofCOrgYLh16owTH31XbXsRN/dDu9juUHvzMFciajkKLmTAUFRaYx1DkRYFF6o/17GxvvjiCyQmJuKZZ56p8rpKpao0sdlgMAAA3NzcoPprs92q6qjVaoe14SjsISKnMRqN+O+Ouk+Ki+zaEV4KCQwl2vICUUTWwaPw7NQRfrEDYNZqYdEbIMhkUPp4w2I0oTijEFaL/Z5IglSCwJ6d0HFYDOQaFdTemiqeRkTkPIaSstor1aNeQ+zcuRN5eXkYPny4XfkzzzyDvXv3Ijg4GNnZ2XbXKr4OCgqC2Wy2lYWHh9vV6dq1KwA4pA1HYUJETpOblY9TfyTXuf6kh+4EMq4bMxaB4nMXUXzuIhReHpAolRDNZuQWnIRELkPw0DgMmH4bLGYLLAYT5Bo3KNzVEGRSqDzrNimbiKi5KT3qtgVIXes1REJCAvR6vV3ZqFGjMHv2bNxxxx3YvXs3tm/fDovFAulfh20fOnQIERER8PPzg4eHBzQaDQ4fPmxLZoqLi5GUlIT4+HgAQGxsbKPbcBQOmZHTCIKA82cv1bl+eEQoDIXVjxkbi0qgz86FIb8QEEVYjSaIFjMyD/yKkpQzcPf3hJu/J9S+nkyGiKhF84kIgdKr5p9TSi8NfCJCaqzTGEFBQejQoYPdHwDw8/NDUFAQxo8fD61WiyVLliA1NRW7du3Ce++9hxkzZgAon/cTHx+PhIQE7N+/HykpKZgzZw6Cg4MxatQoAHBIG47SKnqI8vLy8OKLL+Lnn3+GwWBAbGwsFi5ciMjISADlu1yuWrUKp06dgq+vLx5++GE8+OCDTo6aaiOKIswmc5M+Q6pSosPt/4BELoNcwySIiFoHQSJB1zuGVLnKrELXO2506tmLfn5+ePfdd7Fq1SqMGzcOAQEBWLBgAcaNG2erM3v2bJjNZixduhR6vR6xsbHYtGkT5H+tMnZEG44iiHVd3uNE999/P6xWK5YuXQp3d3e89tpr+P3337Fv3z7o9Xr885//xIgRIzBt2jT88ccfePbZZ/HMM89g/PjxDXreyJEjAQD79+935GvQdTLSszD+5ql1XmG27Pl/oZenorwHqA4kcjnCxtzMRIiIWq2sU+dx+stf7CZYK7006HrHjU2+5N7VtPgeoqKiIoSGhmLGjBm2vQpmzZqFO++8E2fPnsXBgwdtu1zKZDJERkYiLS0NGzdubHBCRM3DarEitH0wrlyq2yqJbe9/iRdWPQHUMSHyiIqARMHl9ETUegX17ITA7h3LV52VlEHp4QafiBCn9gy1VS3+O+rl5YVXXnnFlgzl5+fjvffeQ3BwMKKiomrd5ZJaLi9vT3Tr3bnO9VNTLqDYZK1Tj49ELodnZIca90AiImoNBIkEvpGhCInpDN/IUCZDTaRVfVf/85//IC4uDnv27MGqVavg5uaGzMxMBAcH29W7dpdLark0nu4Yc+fIet2zZN7LkHbrClkNSZFEIYf/0MEQVHU7YJaIiKjFD5ld66GHHsJ9992Hjz76CI8//ji2bdtW6y6X1amYJ1SVjIyMStuEU9OIiAqHj583CvIK61Q/Mz0bsx99Fi++tghqswnW9Ksw/bUvkVSlhCysHQRfXxgECTyum3BXVFgMvVZf/tuVKEIE4O3rCaWaiRMRkatrVQlRVFQUAGDVqlU4fvw4Pvzww1p3uaSWzdvHE48vmIrnFq6p8z1XL2fiwbufQq++3fDgtHEI7hkOAQLyikrw8TtfYNCwfhg99mYAQGFeEYx6I3779QT++L9TuJCShuLCEkikEgS2C0Bkt44Y+s/BCOkQDG8/TyiUHGIjInJFLT4hys/Px8GDBzF69GjbPCGJRIKoqChkZ2fXustldWpaQVZT7xE5ltpdjdgb+mBAXB8kHjxer3tP/p6Mfz9hv7Fjj5iuGDYyDp7eHsjNzMMX7+3F97t/rrS832K2IP3CVaRfuIqf9v4fvP288NDc+xEd0xl+Qb6Nfi8iImpdWvwcotzcXMydOxcHDx60lZlMJiQlJSEyMhKxsbE4duwYLNccz3DtLpfU8gUGB2DJC3PQoVNYo9oJCQvCijULofFww/nki/jPtOex77Mf6rTXUWFeEV5b8jbeXrUVuZn5jYqDiIhanxafEHXp0gXDhg3Dc889h6NHj+LMmTNYtGgRiouL8fDDD9e6yyW1DsGhgVi7+Tn0iGnY2TRdunfCuvdfQECgHzLSsvDMIy8iL6ug3u388X8n8fK815kUERG5mFaxMWNJSQleeeUVfPfddygpKcGAAQOwaNEidO5cvmT7xIkTWLVqFZKSkhAQEICpU6c26owTbszoPFkZOfjx24N4M2EL9LrqJ8VXUCoVmDZ7EkbfcTMCg/2RfTUXiyevQEmRtlFxDBzRD1PmPcDhMyIiF9EqEqLmxoTIuQoKiqAv1ePI//2OPZ99izPJ52HQ/50cKZUKREZH4Na7RuKG4bFQu6ng7euF3Mx8bF3zMQ5/f8whcSxcOxv9h8Y4pC0iImrZWvykanI9Pj5egI8X7rx3DAbd2BdWUYTRYILVaoVEIoFCKYcAAUHtAiC5ZoMyfZneYckQAHzw6qdoHxmGwHb+DmuTiKi1+eKLL7Bx40ZcvnwZ4eHheOKJJ/DPf/4TAHDlyhWsXLkSR48ehZubGyZMmIAnn3zSdnI9AHz00UfYvHkzcnJy0LNnTyxduhTdu3e3XXdEG47Q4ucQkWsLDg1Cu7BgdIxsj06dO6BjZHu0CwtGSFiQXTKkLSnDN59979BnX03LRHFBsUPbJCJqTXbv3o0lS5Zg0qRJ2LNnD8aOHYu5c+fi999/h8lkwrRp0wAA27dvx/Lly/Hxxx/jjTfesN3/+eefY/Xq1fjXv/6FXbt2ISwsDFOmTEF+fvk8TUe04ShMiKhNKC0qxW+/nHB4u8d+qt9WAEREjma1WHH51EUk/3wKl09dhNVibZbniqKI1157DQ8++CAmTZqE8PBwPPbYY7jhhhtw5MgRfPPNN7h69SpWr16NLl264JZbbsHcuXOxdetW2/6Ab731FuLj43HHHXcgKioKzz//PNRqNXbs2AEADmnDUThkRm2EiJyrjj+77szJc8jPKYBvgI/D2yYiqs3ZQ8n4ftM30Ob93Vut8fPEiGmj0XlwtyZ99oULF5Ceno7bb7/drnzTpk0AgOXLl6NHjx7w8vKyXRs8eDC0Wi2Sk5MRFhaGixcvIi4uznZdJpNhwIABOHr0KGbMmIHExMRGt+Eo7CGiNsFoMDVJu3lZ+U3WNhFRTc4eSsaXq3fYJUMAoM0rxperd+DsoeRq7nSMCxcuAADKysowbdo0xMXF4Z577sH335dPT6jtLNHMzEwAqHQUVmBgoO2aI9pwFCZERDXgEkwicgarxYrvN31TY50fNn3TpMNnWm359iULFy7E2LFjsXnzZtx4442YNWsWDh48WOtZojqdDgCqrFNxxJYj2nAUDplRmyBXymuv1AA+/l6QyaW1VyQicqD05EuVeoauV5JXjPTkS2jfs2OTxCD/64DsadOmYdy4cQCAbt26ISkpCVu2bKn1LFGVSgUAVdZRq9UA4JA2HIU9RNQmCAD8ghw/z6dzz0j4B/EIGCJqXtqCum0uW9d6DVFxHmiXLl3syqOionDlypVazxKtGOaqqk5F245ow1GYEFGboPZwQ+9BPRzebv+hfRzeJhFRbTQ+GofWa4gePXrA3d0dx4/br7Y9c+YMwsPDERsbi6SkJNvQGlB+lqi7uzuio6Ph5+eHiIgIHD582HbdbDYjMTERsbGxAOCQNhyFCRG1CZ5eGtx6/z8c2mZAO3/4BnJ1GRE1v9Bu4dD4edZYx8PPE6HdwpssBpVKhenTp+ONN97AV199hUuXLuHNN9/Er7/+iilTpuCWW25BQEAAnnrqKaSkpOC7777DmjVrMHXqVNucn6lTp2LLli34/PPPkZqaiqeffhp6vR4TJkwAAIe04SicQ0RthrunG3oN6o6Th5Mc0t7EWXfDP5hnmRFR85NIJRgxbTS+XF39Xjs3TxsNibRp+zVmzZoFtVqNtWvXIisrC5GRkVi3bh0GDRoEAHj33Xfx7LPP4t5774WXlxceeOABzJo1y3b/vffei5KSErz66qsoLCxEz549sWXLFvj6lv9sVSqVjW7DUXiWWRV4llnrlXklGwsnLYeuVN+odnoN6o5Zy6bycFcicqqq9iHy8PPEzc2wD5GrYUJUBSZErVdZSRnOp6Rh1ZNrYDFbGtRGSHgQlr4xDwEhPMOMiJzParGWrzor0ELjo0Fot/Am7xlyRfyOUpvi5uGGsMhQLH1jHtw93et9f2SPCCxZz2SIiFoOiVSC9j07otvQnmjfsyOToSbC7yq1Od6+nojqEYGXPnwGg0YOgCAItd6jclPhobn3Y/7qx3m6PRGRC+KQWRU4ZNZ25GXnw6g34cB/f8Gpo8m4ePYyTH8dxeHp44FO3TrixlED0a1fV6jclPD09nByxERE5AxMiKrAhKjtsVgsyMsqAEQRVlEs7zUSAYVaDh8/b2eHR0RETsZl9+QSpFIph8KIiKhaDZpD9OCDD+LcuXNVXktJScHtt9/eqKCIiIiImlOde4gSExNRMbp25MgRHD16FPn5+ZXq/fDDD7h8+bLjIiQiIiJqYnVOiHbs2IHdu3dDEAQIgoBnn322Up2KhGns2LGOi5CIiIioidV5UnVJSQmSk5MhiiIeeughLFu2DFFRUXZ1JBIJPD090blz5zotdW6pOKmaiIio/CDVN954A1988QUKCwvRvXt3/Pvf/0ZMTAwAIDk5GatWrcKpU6fg6+uLhx9+GA8++KDtfqvVivXr12PHjh0oKSlBbGwsli1bhvbt29vqOKINhxAb4PDhw2JJSUlDbm0VRowYIY4YMcLZYRARETnV66+/Lt54443izz//LF68eFFcsmSJ2L9/fzErK0vMz88XBw0aJC5evFhMTU0VP/vsM7FXr17iZ599Zrt/3bp14qBBg8QffvhBTE5OFqdOnSqOGjVKNBgMoiiKDmnDURq87D4rKwvHjh2D0Wi0lVmtVuh0OiQmJmLt2rUOS9qaG3uIiIiopbBarEj+/QwKc4vg7e+Fbn27NNtu1XfeeSfi4uKwaNEiAIBWq0X//v2xbt06XLhwAR9++CF++OEHyGTlM3DWrFmDb775Bt988w2MRiMGDx6M+fPn44EHHgAAFBcXY+jQoVi1ahXGjh2Lt99+u9FtOEqDlt1//fXXmD9/Psxms21oTKzY2wVAp06dHBYgERGRqzr8/TG8l/Ax8rMLbGW+gT54eP5EDBrRv8mf7+fnhx9++AHx8fEICQnBJ598AoVCgejoaOzYsQMDBw60JTIAMHjwYLz99tvIzc3F1atXUVpairi4ONt1T09PdO/eHUePHsXYsWORmJjY6DYcpUEp5ltvvYUePXpg165duPvuu3HnnXdiz549+Pe//w2pVIqnn37aYQESERG5osPfH8OaBRvskiEAyM8uwJoFG3D4+2NNHsOSJUsgl8sxcuRI9OrVC2vXrsXrr7+O8PBwZGZmIjg42K5+YGAgACAjIwOZmZkAgJCQkEp1Kq45og1HaVBCdOHCBTzyyCPo3r07Bg0ahJSUFERGRmLq1Kl48MEH8dZbbzk0SCIiIlditVjxXsLHNdbZ+sp2WC3WJo0jNTUVHh4eeOONN/DJJ5/g7rvvxvz585GcnAy9Xg+FQmFXX6lUAgAMBgN0Oh0AVFnHYDAAgEPacJQGDZlJJBJ4eXkBADp06IDz58/DarVCIpFg2LBh+Pzzzx0aJBERkStJ/v1MpZ6h6+Vl5SP59zPoMSC6SWLIyMjAvHnz8N5772HAgAEAgF69eiE1NRXr1q2DSqWym0cMwJakuLm5QaVSAQCMRqPtvyvqqNVqAHBIG47SoB6iTp064bfffrP9t9FoREpKCoDyyU7XvxwRERHVXWFukUPrNcTx48dhMpnQq1cvu/I+ffogLS0NwcHByM7OtrtW8XVQUJBtmKuqOkFBQQDgkDYcpUEJ0f3334/XXnsNa9euhYeHBwYPHozFixfjgw8+wCuvvIIePXo4NEgiIiJX4u3v5dB6DVExt+f06dN25WfOnEHHjh0RGxuLY8eOwWKx2K4dOnQIERER8PPzQ3R0NDQaDQ4fPmy7XlxcjKSkJMTGxgKAQ9pwlAYlRPfccw+WLFli6wlauXIlDAYDVq1aBYvFgiVLljg0SCIiIlfSrW8X+Ab61FjHL8gX3fp2abIYevfujf79+2PhwoU4dOgQLl68iFdffRUHDx7Eo48+ivHjx0Or1WLJkiVITU3Frl278N5772HGjBkAyuf9xMfHIyEhAfv370dKSgrmzJmD4OBgjBo1CgAc0oajNHgfouuJooiCggKcPn0ae/fuxcqVKx3RrFNwHyIiInK2ilVm1Zm7elaTL70vKirCq6++igMHDqCoqAhdunTB3LlzMXDgQADAiRMnsGrVKiQlJSEgIABTp05FfHy87X6LxYI1a9Zg165d0Ov1tl2mw8LCbHUc0YYjOCwhqrB161a8+OKLSE5OdmSzzYoJERERtQRV7UPkF+SLh+bd3yz7ELmSBq0yo6ZjMRgAiBCtVggSCSCRQiqXOzssIiJygkEj+iP2pr5O26nalTAhaiFMJhMEswll6ZdhKi4sLxQkUPr6QR0cCulf+zIQEZFrkUglTba0nv7GFLOFEMwmFJ9O+jsZAgDRCkNeDopTU2AxOnYDKiIiIvobE6IWwGI0oCz9EkSrpcrrVoMehvxcmM3mZo6MiIjINdR5yOzBBx+sUz1Hny3iEqwiTMU1b65lyM2G0scPkHGUk4iIyNHq3EMkimKd/gQFBdm2+HaUwsJCLFu2DMOGDUO/fv0wceJEJCYm2q4fPHgQd999N/r06YMxY8Zgz549Dn1+UxPF2s+isZpMzRAJERGRa6pzd8MHH3zQlHHUaO7cucjJycGaNWvg5+eHDz74ANOmTcPnn38OURQxY8YMTJkyBS+//DIOHDiABQsWwNfXF3FxcU6LuT4EiQQQBKCGHRCkSlW114iIiKhxWvz4S1paGn799Vds27YN/fuX77nwn//8Bz///DP++9//Ii8vD127dsWcOXMAAJGRkUhKSsK7777bahIiCBIovH1hLMirtooqMJhJERERURNp8ZOqfXx8sHHjRrvD5QRBgCAIKC4uRmJiYqXEZ/DgwTh27BgcvOdkk5EqFHBrFwaJQlHldZnGE3LPpjuvhoiIyNW1+ITI09MTN910ExTXJAvffPMN0tLSMHToUGRmZtoOoKsQGBgInU6HgoKC65trsaRKFTy7dIcquB0EWflGjBKlCu7tO0LTsROkCu5DRERE1FRa/JDZ9X777TcsXrwYo0aNwvDhw6HX6+2SJQC2rysOn61KxfEcVcnIyEBISIhjAq4HqUIJVVAIVH4BAAQAIofJiIjI5uTJk3j//fdx9OhR5OfnIzAwEHFxcXj00UfRvn17hz/vvffewzvvvIOSkhLMnDkTBw8eBODcecVVWbRoEY4cOYLvv/++wW20qoTou+++w/z589GvXz8kJCQAAJRKZaXEp+JrtVrd7DE2llQqA6St6mMhIqJm8NFHH+H555/HoEGDMG/ePAQGBiItLQ2bNm3Cvn37sHXrVkRHO25Ha61Wi5deegnDhw/H1KlTERYW5vAT5luSVvMv74cffohVq1ZhzJgxeOmll2y9QCEhIcjOzrarm52dDTc3N3h4eFTbXk0Ht9bUe0RERNTcjh07hlWrVmHSpElYsmSJrXzQoEG45ZZbcNddd+Hpp5/Grl27HPbMoqIiWK1W3HLLLYiNjXVYuy1Vi59DBADbtm3DypUrMWnSJKxZs8ZuiGzAgAE4cuSIXf1Dhw6hX79+kEhaxetRK2W11r5/FBGRI2zatAkeHh6YO3dupWu+vr5YtGgRRo4cibKyMlgsFnz00Ue4/fbb0bt3bwwfPhwJCQkwGP4+AmrRokV4+OGHsXPnTowePRo9e/bEnXfeiZ9++gkAsGvXLowYMQIA8PTTT6Nr164AgMmTJ2Py5Mm2drp27Yr169fj7rvvRu/evbF+/Xrs2rULvXr1QmJiIsaPH49evXph9OjR+P7773H+/Hk89NBD6NOnD/7xj39U2jfw6tWrmDt3LgYOHIg+ffrgoYceQlJSkl2doqIiLF68GAMHDkRsbCxefvllh/w8bvE9RBcuXMDzzz+Pf/zjH5gxYwZyc3Nt11QqFSZPnoxx48YhISEB48aNw48//oivv/4a7777rhOjprbKrNfDajRAn5MN0WqBzM0dSj9/CIKEB/ASUZMQRRG//PILRowYUe1UkFtvvdX230uWLMHu3bvxyCOPYMCAAUhKSsIbb7yB5ORkvPvuuxAEAQBw6tQpZGdnY/bs2dBoNHjttdfw5JNP4qeffsLw4cOxfv16PPHEE3jssccwfPjwauN76623MG/ePERERCA0NBQnT56E2WzGvHnz8MQTTyAkJAQJCQmYP38+/P39MXHiRMycORPr16/HwoUL0b9/fwQHByM/Px/3338/1Go1/vOf/0CtVmPr1q2YNGkSPvvsM0RGRsJqtWL69OlIT0/HwoUL4e3tjXfffRcnT55EYGBgo77PLT4h+uabb2AymfDtt9/i22+/tbs2btw4vPjii9iwYQNefvllbN26FWFhYXj55Zdbzx5E1CqYTCYIJiOKTifBotfbyg3IQemli1AFhcAtNAyCRAKpvOrtE4iIGqKgoAAGgwFhYWG11k1NTcVnn32GefPm4dFHHwUA3HjjjQgMDMSCBQvw008/4aabbgIAlJSUYNeuXQgPDwcAuLm5IT4+HocOHcLo0aPRrVs3AEB4eDhiYmKqfeaAAQMwZcoU29cnT56E1WrFzJkzcc899wAAiouLMWfOHDz00EO2uh4eHhg/fjxOnTqF4OBgbN26FYWFhfj4448RGhoKABg2bBhuvfVWvPbaa3j99dfx008/4cSJE3jnnXcwbNgwAEBcXJytN6sxWnxCNHPmTMycObPGOsOGDbN9Y4iagsRiRv6fJyBWc8CuPisDEK1Qh4RBFCSQ8cw5InIQqVQKALBYqj4A/FoVU0huu+02u/LbbrsNixcvxuHDh20Jka+vry0ZAmDbwkan09UrvorE6Xp9+/a1/befnx8AoE+fPrYyb29vAOXJElB+DFe3bt0QFBRkO8xcIpFg2LBh+PLLLwEAiYmJkMvlGDp0qK0dNzc33HTTTTh69Gi94r4ef2oT1cJiMqL0anq1yVAFfXYW1IHBECxSHsJLRA7j5eUFd3d3XL16tdo6ZWVlMJlMKCoqPyg8ICDA7rpMJoOPjw9KSkpsZdcPv1UMpdV3Po6bm1uV5RqNplJZTau/CwsLkZaWhh49elR5XafToaioCN7e3rZYK1z/vg3Bn9pEtRAtFhhysupUV5+XC3VIaBNHRESuZsiQITh8+DAMBgOUVcxX/PTTT/HSSy9h9uzZAICcnBzbsBNQPuxfUFAAHx+fZou5vjw8PDBw4EAsWLCgyusKhQI+Pj4oKCiAxWKx9ZwB5clUY3EZFlFtrCLEOv7GZNGVASJXnxGRY02dOhWFhYV49dVXK13LycnB5s2bERUVhX/84x8AUGn11p49e2CxWGxngrZEAwcOxIULFxAREYFevXrZ/uzevRufffYZpFIp4uLiYDab8d1339nuMxqN+PXXXxv9fPYQEdVGqL2KjUQCQSKtvR4RUT3ExMTgX//6F1599VWcO3cOd911F3x8fHD27Fls2rQJBoMBr776KiIjIzFu3Di8/vrr0Ol0iI2NRXJyMtavX49BgwbZzb1paR5++GHs3r0bDz/8MKZOnQofHx/s3bsXn376KRYvXgygfAL1kCFDsHTpUuTl5SE0NBTvv/8+8vPzbfOUGooJEVFtBAmkajUsdZhoqPL1hyCpTwZFRFQ3jz32GLp3727bsbqoqAghISEYPnw4Zs6caTtyatWqVejQoQN27tyJd955B4GBgXjwwQcxa9asFr0/X1BQELZv345XXnkFy5cvh8FgQMeOHbFq1SpMmDDBVm/9+vVISEjA66+/DoPBgFtvvRX33ntvjRsu14UgtpYj4ZtRxU7Vjf3mUtuhy85EybmzNdYRpDL49u4LqYrnzxERtTYtN1UkakEUXj5Q+NbQHSsI8IruDit7h4iIWiUOmRHVgVSphEfHSBg8vVCWkQ7rNVvgK7x94R7eEYJcDpmCmzISEbVGTIiI6kiqVEIZGAyFjx9gtUAURQhSKSBIIOOxHURErRoTIqJ6kEqlgJSryIiI2hrOISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiMjlWa3Weh9qSm0LJ1UTEZHLshgNsBoNMBTkAQCU3n6QKJWQKrhy1NUwISIiIpdkMRpRevkCzKVaW5mxIA8yNw3cwztByn3FXAqHzIiIyOVYzCYY8nPskqEK5jItDHnZsJhNToisZbFarXj99dcxdOhQxMTE4JFHHsHly5errV9QUIB58+YhNjYWAwcOxLPPPgtdHc6BbAmYEBERkeuxWGHIy6n2siE/B7BwTtGGDRuwbds2rFy5Etu3b4fVasX06dNhNBqrrD979mykpaXhvffew2uvvYYff/wRy5cvb96gG4hDZkRE5HoEQLSYq70sWizNGEzN0tPT8b///Q/5+fnw9fXFP//5T4SGhjb5c41GIzZv3oz58+dj+PDhAIC1a9di6NCh2LdvH8aOHWtX//fff8eRI0ewd+9eREZGAgBWrFiB6dOnY+7cuQgKCmrymBuDCREREbkeEZAolLAaDVVelrSASdVmsxkvvfQSvvjiCwiCAIlEAqvVirfffht33XUXFi5cCJms6f4ZT0lJQWlpKeLi4mxlnp6e6N69O44ePVopIUpMTERAQIAtGQKAgQMHQhAEHDt2DLfeemuTxeoIHDIjIiKXI1UqoQoMqfa6KiAYUiefUViRDImiCKvVCrPZDKvVClEU8cUXX+Cll15q0udnZmYCAEJC7L9PgYGBtmvXysrKqlRXoVDA29sbGRkZTReogzAhIiIilyTXeEAVEAxAsCtXBQRB7uHlnKD+cuXKFVsyVJWKpCg9Pb3JYqiYDK24brWdUqmEwVC5Z02n01WqW1P9loYJERERuSgBSt8AeHXpAffwTtB0iIRX155Q+gU6fcn9119/DUEQaqwjCAL+97//NVkMKpUKACpNoDYYDFCr1VXWr2qytcFggJubW9ME6UBMiIiIyOVYjAYYcrNQdPokik6fhC7jCsoyrsCQl+vs0AAA+fn5kEhq/idaIpEgPz+/yWKoGP7Kzs62K8/Ozq5ygnRwcHClukajEYWFhQgMDGyyOB2FCREREbkUi8UCU1Eh9DmZwF9DUlajAVaDHvqcDJiKC2E2V78CrTn4+vrWepSI1WqFr69vk8UQHR0NjUaDw4cP28qKi4uRlJSE2NjYSvVjY2ORmZmJtLQ0W9mRI0cAAP3792+yOB2FCREREbkWswm6nOon+eqzMyHUsCS/OYwZM6ba+UMVRFHEP//5zyaLQaFQID4+HgkJCdi/fz9SUlIwZ84cBAcHY9SoUbBYLMjJyYFerwcA9OnTB/369cOcOXNw4sQJHDp0CMuWLcNdd93V4pfcA0yIiIjI1YgiRFP1u1BbTUYANScjTS0sLAx33XVXtfOIBEHAXXfd1eT7Ec2ePRsTJkzA0qVLMXHiREilUmzatAlyuRwZGRkYMmQI9u7da4tp/fr1CAsLw0MPPYSnnnoKw4YNazUbMwpibSmoCxo5ciQAYP/+/U6OhIiIHM1i0KMo5RSqT3oEeEX3cvqy++r2IRJFsVn2IXI1TIiqwISIiKjtshiNKLt6CaaigiqvK7x8oG4X7vSVZhWu3anaz88PY8aMaZadql0NU0siInIpUoUCbiFhKC7TVho6k8gVUIeEtZhkCABCQ0Mxffp0Z4fR5jEhIiIilyNVquAZ1Q3GgnwYi8qXriu8faHw9oW0BRzbQc2PCREREbkkqUIJhX8gFN4+AABRKoOUc3JcFj95IiJyWVKpFJBKnR0GtQBcdk9EREQujwkRERERuTwmREREROTyOIeIiIioBdNqtUhNTUVZWRnc3NwQFRUFjUbj7LDaHCZERERELdDZs2fx6aefYu/evTAYDLZypVKJ2267Dffccw86d+7cpDFYrVasX78eO3bsQElJCWJjY7Fs2TK0b9++2phffvllHD9+HBKJBLGxsVi0aBHatWvXpHE6QqsbMnv77bcxefJku7Lk5GTEx8cjJiYGI0aMwPvvv++k6IiIiBpHFEVs3boVEydOxJdffmmXDAGAwWDA7t27MXHiRGzdurXWQ2AbY8OGDdi2bRtWrlyJ7du3w2q1Yvr06TAajZXqFhQUYMqUKVCpVPjggw/wzjvvID8/H9OnT6/0Di1Rq0qIPvroI7z66qt2ZRUfQHh4OHbu3InHH38cCQkJ2Llzp3OCJCIiaoT3338f69atAwBYLJYq61SUr1u3rsk6AYxGIzZv3ozZs2dj+PDhiI6Oxtq1a5GZmYl9+/ZVqv/dd9+hrKwMq1evRpcuXdCzZ0+8/PLLOHfuHH777bcmidGRWkVClJWVhZkzZyIhIQEdO3a0u/bpp59CLpdjxYoViIyMxPjx4/Hwww9j48aNzgmWiIiogc6ePWtLhupq3bp1OHv2rMNjSUlJQWlpKeLi4mxlnp6e6N69O44ePVqpflxcHDZs2ACVSmUrk0jK04zi4mKHx+dorSIh+vPPPyGXy/Hll1+iT58+dtcSExMxcOBAuxN/Bw8ejIsXLyI3N7e5QyUiImqwHTt2lG8WWQ9SqRSfffaZw2PJzMwEAISEhNiVBwYG2q5dKywsDIMHD7Yr27hxI1QqFWJjYx0en6O1ioRoxIgRWLduXZWTuDIzMxEcHGxXFhgYCADIyMholviIiIgaS6vVYs+ePdUOk1XHYrHgq6++glardWg8Op0OAKC47qBbpVJZpzlBH3zwAT788EPMnz8fvr6+Do2tKbT6VWZ6vb7KDwtAjR/YyJEjq72WkZFRKSMmIiJqSqmpqQ2efGwwGJCamoqYmBiHxVMx9GU0Gu2GwQwGA9RqdbX3iaKI1157DW+++SYee+yxSguhWqpW0UNUE5VKVWm2e8VfKDc3N2eEREREVG9lZWVOvf96FR0D2dnZduXZ2dkICgqq8h6TyYR///vfeOutt7B48WI89dRTDo2pKbX6HqLg4OAqPywA1X5gALB///5qr9XUe0RERNQUGvtLvKM7AaKjo6HRaHD48GGEh4cDKJ8cnZSUhPj4+CrvWbBgAb799lu88soruO222xwaT1Nr9QlRbGwstm/fDovFYpuIdujQIURERMDPz8/J0REREdVNVFRUnefnXE+pVCIqKsqh8SgUCsTHxyMhIQG+vr4IDQ3Fyy+/jODgYIwaNQoWiwX5+fnw8PCASqXCrl27sHfvXixYsAADBw5ETk6Ora2KOi1Zqx8yGz9+PLRaLZYsWYLU1FTs2rUL7733HmbMmOHs0IiIiOpMo9Hgtttua9Aqs7FjxzbJcR6zZ8/GhAkTsHTpUkycOBFSqRSbNm2CXC5HRkYGhgwZgr179wIAvvrqKwDA6tWrMWTIELs/FXVaMkFsyi0um8CiRYuQnp6ODz74wFZ24sQJrFq1CklJSQgICMDUqVOr7c6ri4ohs5qG1YiIiBzt7NmzmDhxYr3v+/jjj5v8GI+2rtUlRM2BCRERETnL1q1b67U545NPPomHHnqoCSNyDa1+yIyIiKgtefDBB/Hkk08CQLXDZxXlTz75JB588MFmi60ta/WTqomIiNoSQRDw0EMP4YYbbsCOHTuwZ8+eSqfdjx07FhMmTOAwmQNxyKwKHDIjIqKWQqvVIjU1FWVlZXBzc0NUVFSTTKB2dewhIiIiasE0Go1Dd6CmqnEOEREREbk8JkRERETk8jhkRkRE1IJptVrk5OTY5hAFBARwDlETYEJERETUwoiiiN9++w07duzA999/D6vVarsmkUgwYsQI3HPPPejXrx8EQXBipG0HEyIiIqIWJCUlBUuXLsXFixchlUrtkiEAsFqt+OGHH/Ddd9+hY8eOeO655xAdHe2kaNsOziEiIiJqIQ4fPoxp06bh0qVLAACLxVJlvYryS5cuYdq0aTh8+HCTxGO1WvH6669j6NChiImJwSOPPILLly/X6d4vv/wSXbt2xZUrV5okNkdjQkRERNQCpKSkYO7cuTAajZV6hapjtVphNBoxd+5cpKSkODymDRs2YNu2bVi5ciW2b98Oq9WK6dOnw2g01nhfeno6VqxY4fB4mhITIiIiIicTRRFLliyByWRCffdLFkURJpMJS5curfe9NTEajdi8eTNmz56N4cOHIzo6GmvXrkVmZib27dtX7X1WqxX//ve/0aNHD4fF0hyYEBERETnZb7/9hrS0tDr3DF3ParXi4sWL+P333x0WU0pKCkpLSxEXF2cr8/T0RPfu3XH06NFq73vrrbdgMpkwY8YMh8XSHJgQEREROdmOHTuqPci1rqRSKT799FMHRQRkZmYCAEJCQuzKAwMDbdeud+LECWzevBkvv/xyo9+nuTEhIiIiciKtVovvv/++2gnUdWWxWPD9999Dq9U6JC6dTgcAUCgUduVKpdLusNkKZWVlmD9/PubPn4+OHTs6JIbmxISIiIjIiXJycho8VHY9q9WK3Nxch7SlUqkAoNIEaoPBALVaXan+c889h4iICNx///0OeX5z4z5ERERETlRWVubQ9kpLSx3STsVQWXZ2NsLDw23l2dnZ6Nq1a6X6O3fuhEKhQN++fQH8vTXA2LFjMXPmTMycOdMhcTUVJkRERERO5Obm5tD23N3dHdJOdHQ0NBoNDh8+bEuIiouLkZSUhPj4+Er1r195dvz4cfz73//Gxo0b0aVLF4fE1JSYEBERETlRQEAAJBKJQ4bNJBIJ/P39HRBV+dyh+Ph4JCQkwNfXF6GhoXj55ZcRHByMUaNGwWKxID8/Hx4eHlCpVOjQoYPd/RUTr9u1awdvb2+HxNSUOIeIiIjIiTQaDUaMGOGQVWYjRoxw6MGvs2fPxoQJE7B06VJMnDgRUqkUmzZtglwuR0ZGBoYMGYK9e/c67HnOJIiO3MWpjRg5ciQAYP/+/U6OhIiIXMGxY8ccsm/Pxo0b0a9fPwdE5HrYQ0RERORk/fr1Q8eOHSGRNOyfZYlEgo4dO9omNFP9MSEiIiJyMkEQ8Nxzz0Eul0MQhHrfK5fL8dxzz9X7XvobEyIiIqIWIDo6GmvWrIFCoahzT5FEIoFCocCaNWsQHR3dxBG2bUyIiIiIWohBgwZh06ZNtmXu1U20rigPDw/Hpk2bMGjQoGaLsa3isnsiIqIWJDo6Gjt27MDvv/+OTz/9FN9//73dknyJRIKbb74Z9957L/r27cthMgdhQkRERNTCCIKAfv36oV+/ftBqtcjNzUVpaSnc3d3h7+/v0KX1VI4JERERUQtUWFiIAwcO4M8//0Rqair0ej1UKhWioqLQo0cPDB8+vFVseNhacB+iKnAfIiIicpbMzEy8+eab+Oabb2A2myGTyWA2m23XK76WyWQYPXo0Zs2ahaCgICdG3DZwUjUREVEL8dVXX+Gee+7B119/bUuCrk2Grv3abDbj66+/xoQJE/DVV181e6xtDYfMiIiIWoAtW7bgjTfeqNc9FosFOp0Oy5cvR25uLh5++OGmCc4FsIeIiIjIyb766qt6J0PXW79+vcN7iqxWK15//XUMHToUMTExeOSRR3D58uVq65tMJrzyyiu2+vHx8UhOTnZoTE2FCREREZETZWZm4qWXXnJIWy+99BKysrIc0hYAbNiwAdu2bcPKlSuxfft2WK1WTJ8+HUajscr6y5cvx65du/D8889j586d8PX1xSOPPIKSkhKHxdRUmBARERE50ZtvvlltglFfRqMRGzZscFhbmzdvxuzZszF8+HBER0dj7dq1yMzMxL59+yrVv3z5Mnbu3IlVq1Zh6NChiIyMxHPPPQeFQoFTp045JKamxISIiIjISQoLC/HNN9/AYrE4pD2LxYJvvvkGhYWFjW4rJSUFpaWliIuLs5V5enqie/fuOHr0aKX6v/76Kzw8PDBs2DC7+t9//71dGy0VEyIiIiInOXDgQKVVZI1lNptx4MCBRreTmZkJAAgJCbErDwwMtF271oULF9C+fXvs27cPd999N2688UY88sgjOHfuXKNjaQ5MiIiIiJzkzz//hEzm2AXfMpkMSUlJjW5Hp9MBABQKhV25UqmEwWCoVF+r1SItLQ0bNmzA3Llz8eabb0Imk+GBBx5AXl5eo+NpakyIiIiInCQ1NbVJeojOnj3b6HZUKhUAVJrfZDAYoFarK9WXyWTQarVYu3YthgwZgt69e2Pt2rUAgM8//7zR8TS1NpMQ1XdpIBERkbPp9foW227FUFl2drZdeXZ2dpU7YwcHB0MmkyEyMtJWplKp0L59e1y5cqXR8TS1NpMQ1XdpIBERkbNV9MK0xHajo6Oh0Whw+PBhW1lxcTGSkpIQGxtbqX5sbCzMZjNOnjxpK9Pr9bh8+TI6dOjQ6HiaWptIiOq7NJCIiKgliIqKapI5RJ07d250OwqFAvHx8UhISMD+/fuRkpKCOXPmIDg4GKNGjYLFYkFOTo6tN2rAgAG44YYbsHDhQiQmJiI1NRULFiyAVCrFnXfe2eh4mlqbSIjquzSQiIioJejRo0eTzCHq3r27Q9qaPXs2JkyYgKVLl2LixImQSqXYtGkT5HI5MjIyMGTIEOzdu9dWf926dRg4cCCeeOIJTJgwAVqtFu+//z58fX0dEk9TahOn3e/btw9PPvkkjh8/btdN+K9//Qt6vR5vv/12vdrjafdERNQcCgsLMWbMGIcmRTKZDF9//TW8vb0d1qYraBOHu9a0NLCoqKjKeyqSnqpkZGRU2neBiIjI0by9vTF69Gh8/fXXDtmcUSqVYvTo0UyGGqBNDJnVd2kgERFRSzFr1qxKv9A3lEKhwKxZsxzSlqtpEz1E1y4NDA8Pt5VnZ2eja9euVd5T03BYTb1HREREjhQUFISFCxdi+fLljW5r4cKFVS6Jp9q1iR6i+i4NJCIiaknGjh2Lxx9/vFFtPPHEExg7dqyDInI9baKH6Nqlgb6+vggNDcXLL79sWxpIRETU0k2ZMgUBAQF46aWXYDAYYLVaa71HIpFAqVRi4cKFTIYaqU0kRED50kCz2YylS5dCr9cjNjbWtjSQiIioNRg0aBD69u2L//u//6tTfavVir59+2LQoEFNHFnb1yaW3Tsal90TEVFz27dvH5577jkYDIZ6rTiTSqVQKpVYunQpR0UaoU3MISIiImrNtm/fjqeffho6na7ey+8tFgt0Oh2efvppbN++vYkibPuYEBERETnRvn37kJCQAABo6KBNxX0JCQk8sqqBmBARERE5SU5ODp577jkIguCQ9gRBwKpVq5Cbm+uQ9qxWK15//XUMHToUMTExeOSRR3D58uVq6+fl5WHevHkYPHgwBg0ahDlz5iArK8shsTQ1JkREREROsnr1ahgMhgb3DF1PFEXo9Xq89NJLDmlvw4YN2LZtG1auXInt27fDarVi+vTplTZCrvDUU0/h6tWr2LJlC7Zs2YKrV682ejuB5sKEiIiIyAnS09Nx4MABhxzZcS2LxYIDBw7g6tWrjWrHaDRi8+bNmD17NoYPH47o6GisXbsWmZmZVQ7LFRcX48iRI3jkkUfQrVs3dO/eHY8++ihOnjyJwsLCRsXSHJgQEREROcHnn3/usKGy6wmCgF27djWqjZSUFJSWliIuLs5W5unpie7du+Po0aOV6qtUKri7u+OLL76AVquFVqvF7t27ERERAU9Pz0bF0hyYEBERETnBr7/+WqfNFxvCarXWeS+j6mRmZgJApcPOAwMDbdeupVAo8OKLL+LIkSMYMGAAYmNjcfz4cbzzzjuQSFp+utHyIyQiImpjTCYTzp8/36TPOHfuHEwmU4Pv1+l0AFDp4FmlUgmDwVCpviiKSE5ORt++ffHRRx9h69ataNeuHWbNmgWtVtvgOJoLEyIiIqJmlpGR4fC5Q9ezWCzIyMho8P0qlQoAKk2gNhgMUKvVler/73//w4cffoiXX34Z/fv3x8CBA/HWW28hPT0dn332WYPjaC5MiIiIiJpZdau0WtJzKobKsrOz7cqzs7MRFBRUqX5iYiIiIiKg0WhsZV5eXoiIiEBaWlqD42guTIiIiIia2fXDUC3xOdHR0dBoNDh8+LCtrLi4GElJSYiNja1UPzg4GGlpaXbDaWVlZbhy5Qo6duzY4DiaCxMiIiKiZhYSEgKpVNqkz5BKpZUmRNeHQqFAfHw8EhISsH//fqSkpGDOnDkIDg7GqFGjYLFYkJOTA71eDwC46667AJTvRZSSkoKUlBTMnTsXSqUSd999tyNeqUkxISIiImpmcrkcnTp1atJnREZGQi6XN6qN2bNnY8KECVi6dCkmTpwIqVSKTZs2QS6XIyMjA0OGDMHevXsBlK8+27ZtG0RRxEMPPYQpU6ZALpdj27Zt8PDwcMQrNSmedl8FnnZPRERNbf369Xj//febZOm9RCLBgw8+iCeeeMLhbbdV7CEiIiJygnHjxjnsyI7riaLYKoapWhImRERERE4QGhqK4cOHO3wukVQqxfDhw9GuXTuHttvWMSEiIiJykgULFkCpVDr0tHuVSoWFCxc6pD1XwoSIiIjISQICArB06VKHnna/ZMkS+Pv7O6Q9V8KEiIiIyIlGjRqF+fPnA0CDe4oq7ps/fz5GjRrlsNhcCRMiIiIiJ7v//vuxYsWKBs8nkslkWLFiBe6//34HR+Y6mBARERE5WWpqKrZs2dLg883MZjO2bNmC1NRUB0fmOpgQEREROdHx48cxZcoUXLp0qcFziURRxKVLlzBlyhQcP37cwRG6BiZERERETpKamoonnngCBoOhwb1DFSwWCwwGA5544gn2FDUAEyIiIiInMJlMWLx4MYxGo8N2q7ZarTAajXj66adhMpkc0qarYEJERETkBJs2bcLFixcb3TN0PYvFggsXLmDTpk0ObRcA3n77bUyePLnGOgUFBZg3bx5iY2MxcOBAPPvss9DpdA6PxdGYEBERETWzoqIibN26tUmP7ti6dSuKiooc1uZHH32EV199tdZ6s2fPRlpaGt577z289tpr+PHHH7F8+XKHxdFUmBARERE1s//+978wm81N+gyz2Yyvvvqq0e1kZWVh5syZSEhIQMeOHWus+/vvv+PIkSN46aWX0KNHD8TFxWHFihXYvXs3srKyGh1LU2JCRERE1Mw+//zzJusduv45jfXnn39CLpfjyy+/RJ8+fWqsm5iYiICAAERGRtrKBg4cCEEQcOzYsUbH0pRkzg6AiIjIlWi1WqSlpTX5c0RRRFpaGrRaLTQaTYPbGTFiBEaMGFGnullZWQgJCbErUygU8Pb2RkZGRoNjaA7sISIiImpGKSkpzfYsURRx+vTpZnueTqeDQqGoVK5UKmEwGJotjoZgQkRERNSM0tPT2+zzVCoVjEZjpXKDwQA3N7dmi6MhmBARERE1o+beH6iqBKWpBAcHIzs7u9LzCwsLERgY2GxxNAQTIiIiomYkl8ub9XlVDWE1ldjYWGRmZtrNkTpy5AgAoH///s0WR0MwISIiImpGoaGhbeZ5FosFOTk50Ov1AIA+ffqgX79+mDNnDk6cOIFDhw5h2bJluOuuuxAUFNRkcTgCEyIiIqJmFB0d3WzPEgQBXbt2bbL2MzIyMGTIEOzdu9f2vPXr1yMsLAwPPfQQnnrqKQwbNqxVbMwoiM2xEUIrM3LkSADA/v37nRwJERG1RePHj2/U6fZ1IQgCOnTogM8++6zJntGWsIeIiIiomY0bN65NPactYEJERETUzG6//XbIZE27N7JMJsPYsWOb9BltSatKiJYtW4ZFixZVKj948CDuvvtu9OnTB2PGjMGePXucEB0REVHdeHl54aGHHoIgCE3SviAIeOihh+Dl5dUk7bdFrSIhslqtWLNmDT755JNK186dO4cZM2Zg6NCh2LVrF+655x4sWLAABw8edEKkREREdTNt2jR07NgRUqnUoe1KpVJERERg2rRpDm23rWvxCdG5c+fwwAMPYMeOHWjXrl2l61u3bkXXrl0xZ84cREZGYtq0aRgzZgzeffddJ0RLRERUN3K5HC+88AIUCgUkEsf8cyyRSKBQKPD88883+35HrV2LT4gOHTqEyMhIfPXVVwgLC6t0PTExEXFxcXZlgwcPxrFjx5rlJGEiIqKGioqKwvr166FUKhvdUySVSqFUKvHGG28gKirKQRG6jhafEE2aNAmrVq2Cn59fldczMzMRHBxsVxYYGAidToeCgoLmCJGIiKjB+vTpgy1btqBDhw4NnlNUscR+y5Yt6N27t4MjdA1NO8W9FleuXLHt+VOVgwcPwtfXt8Y29Hp9pW3JK76u6fyWmp6bkZGBkJCQGp9LRETkKFFRUfjoo4+wadMmbN26FWazGQBqHOmoSJ5kMhkeeughTJs2jcNkjeDUhCgoKMi2u2VV6jI7XqlUVkp8Kr5Wq9WNC5CIiKiZyOVyzJw5ExMnTsR///tffPHFF7h48WKVdSt6hMaNG4exY8dyNZkDODUhksvliIyMbFQbISEhlU7Wzc7OhpubGzw8PKq9r6ZdqGvqPSIiImpKXl5eiI+PR3x8PLRaLU6fPo309HQYjUYoFAqEhoaia9eu0Gg0zg61TXFqQuQIAwYMsJ2kW+HQoUPo16+fw2btExEROYNGo0H//v1b/EnxbUGrzxgmT56MEydOICEhAefOncPmzZvx9ddfY/r06c4OjYiIiFqJVp8Qde7cGRs2bMCPP/6Iu+66Czt27MDLL79caSk+ERERUXV42n0VeNo9ERGRa2n1PUREREREjcWEiIiIiFweEyIiIiJyeUyIiIiIyOUxISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhIiIiIhcHhOiJmQ1mWA1m50dBhEREdVC5uwA2iKL0QBTSTFMJUUQJBIofQMgUSggVSidHRoRERFVgQmRg1kMepScPwOryWgrMxbmQ+7lA7eQMCZFRERELRCHzBzIYjSgLP2SXTJUwVRUAHNZqROiIiIiotowIXIkUYRJW1ztZUNuNixGQzMGRERERHXBhMiBRFGs8brVbAJqqUNERETNjwmRAwmCBJBU/y2Vqd0Agd9yIiKilob/OjuQIJVC5RdY7XVVYAikCkUzRkRERER1wVVmDiSRyaD0C4RoscCQnwugfHhMkMrgHtYBgpTfbiIiopaI/0I7mFShgCowGKqAYFiMeggSCSRyBSARIJWxd4iIiKglYkLUBCr2GpIquecQERFRa8A5REREROTymBARERGRy2NCRERERC6PCRERERG5PCZERERE5PKYEBEREZHLY0JERERELo8JEREREbk8JkRERETk8pgQERERkctjQkREREQujwkRERERuTxBFEXR2UG0NL169YLFYkFISIizQyEiolYmJCQEH374obPDoHpiD1EVlEolZDKZs8OoUUZGBjIyMpwdRpNzhfd0hXcE+J5tiSu8I+A670nl2EPUSo0cORIAsH//fidH0rRc4T1d4R0Bvmdb4grvCLjOe1I59hARERGRy2NCRERERC6PCRERERG5PCZERERE5PKYEBEREZHLY0JERERELo/L7omIiMjlsYeIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhKgVWbZsGRYtWlSpfMqUKejatavdn8mTJ9uuGwwGPPvss4iLi0Pfvn0xb9485OfnN2fodVbdOx48eBB33303+vTpgzFjxmDPnj1211vTO1Y4duxYpc+ta9euOHz4sK1Obe/dGlitVrz++usYOnQoYmJi8Mgjj+Dy5cvODqvRsrKyqvz8du3aBQBITk5GfHw8YmJiMGLECLz//vtOjrh+3n77bbufI0Dt79QaP+uq3nPp0qWVPtcRI0bYrrfG96Q6EKnFs1gs4iuvvCJ26dJFXLhwYaXrcXFx4rZt28Ts7Gzbn4KCAtv1RYsWibfccot49OhR8fjx4+Jdd90lTpo0qRnfoHY1vWNqaqrYq1cvcc2aNWJqaqr47rvvit27dxf/7//+z1anNbzj9T766CPxlltusfvcsrOzRYPBIIpi3d67NVi3bp04aNAg8YcffhCTk5PFqVOniqNGjbK9Z2t14MABsVevXmJWVpbd56fT6cT8/Hxx0KBB4uLFi8XU1FTxs88+E3v16iV+9tlnzg67Tj788EMxOjpajI+Pt5XV5Z1a22dd1XuKoihOmDBBXLNmjd3nmpeXZ7ve2t6T6oYJUQuXmpoq3nfffeLgwYPF4cOHV0oWcnNzxS5duoh//vlnlfdnZmaK0dHR4oEDB2xl58+fF7t06SL+9ttvTRp7XdX2jv/5z3/ECRMm2JXNnTtXnDp1qiiKreMdq/LMM8+IM2fOrPZ6be/dGhgMBrFv377iRx99ZCsrKioSe/fuLf73v/91YmSNt3HjRvH222+v8tpbb70lDhkyRDSZTLayV155RRw1alRzhdcgmZmZ4owZM8SYmBhxzJgxdolCbe/Umj7rmt7TarWKMTEx4r59+6q8tzW9J9UPh8xauEOHDiEyMhJfffUVwsLCKl0/ffo0BEFARERElfcfO3YMADB48GBbWUREBIKCgnD06NGmCbqeanvHxMRExMXF2ZUNHjwYx44dgyiKreIdq3L69GlERkZWe722924NUlJSUFpaavcenp6e6N69e4v+bOqips8vMTERAwcOhEwms5UNHjwYFy9eRG5ubnOFWG9//vkn5HI5vvzyS/Tp08fuWm3v1Jo+65re89KlSygrK0OnTp2qvLc1vSfVj6z2KuRMkyZNqvH6mTNn4OHhgRUrVuDXX3+Fm5sbxowZg1mzZkGhUCArKws+Pj5QKpV29wUGBiIzM7MpQ6+z2t4xMzMTwcHBdmWBgYHQ6XQoKChoFe9YlbNnz8LHxwd33303srKy0KVLF8yZMwe9e/cGUPt7+/r6OiPseqn4/oeEhNiVt/TPpi7OnDkDHx8fTJo0CRcuXECHDh3w2GOPYdiwYcjMzESXLl3s6gcGBgIAMjIy4O/v74yQazVixAi7uTLXqu2dWtNnXdN7njlzBgDwwQcf4KeffoJEIsGwYcMwZ84ceHh4tKr3pPphQuREV65cwciRI6u9fvDgwVr/0Ttz5gwMBgN69+6NKVOmIDk5GatXr8bVq1exevVq6HQ6KBSKSvcplUoYDIZGv0NtHPGOer2+0jtUfG00Gp3+jlWp7b0PHDiAkpISlJWVYenSpZBKpfjwww8RHx+PXbt2ISoqqtb3bg10Oh0AVHoPpVKJoqIiZ4TkEGazGefPn0dUVBQWLVoEjUaDPXv24NFHH8WWLVuq/OwqEnZn/Z1srNreqa181mfOnIFEIkFgYCDeeustXLp0CatXr8bZs2exdevWNvOeVBkTIicKCgrC3r17q73u5eVVaxsrVqzAwoULbXW7dOkCuVyOOXPmYMGCBVCpVFX+42kwGKBWqxsefB054h2VSmWld6j4Wq1WO/0dq1LbewcGBuLo0aNQq9WQy+UAgF69eiEpKQkffPABnn322VrfuzVQqVQAyuOu+G/AuZ+NI8hkMhw+fBhSqdT2Xj179sTZs2exadOmKv9OViRCbm5uzR6vI9T2Tm3ls37sscfwwAMPwMfHB0D5z9SAgADce++9OHnyZJt5T6qMCZETyeXyGueQ1IVMJquUVHTu3BnA30MuhYWFMBqNdr/RZGdnIygoqFHPrgtHvGNISAiys7PtyrKzs+Hm5gYPDw+nv2NV6vLenp6edl9LJBJERkYiKysLQO3v3RpUDCtkZ2cjPDzcVp6dnY2uXbs6KyyHcHd3r1TWuXNn/PLLLwgODq7yswPgtL+TjVXbO5nNZltZa/6sJRKJLRmqcO3P1Lb8d9rVcVJ1Kzd58mQsXrzYruzkyZOQy+Xo2LEj+vfvD6vVapt4DAAXLlxAVlYWYmNjmzvcBhkwYACOHDliV3bo0CH069cPEomkVb7jTz/9hL59+9rtXWI2m5GSkoKoqCgAtb93axAdHQ2NRmO3t1JxcTGSkpJa7GdTF2fPnkW/fv3s3gsATp06haioKMTGxuLYsWOwWCy2a4cOHUJERAT8/PyaO1yHqO2d2spnvWDBAjz88MN2ZSdPngQAREVFtZn3pMpax09Vqtbo0aOxe/dufPzxx7h8+TL27t2L1atXY9q0adBoNAgKCsJtt92GpUuX4vDhwzhx4gTmzp2LgQMHIiYmxtnh18nkyZNx4sQJJCQk4Ny5c9i8eTO+/vprTJ8+HQBa5Tv269cPPj4+WLhwIU6dOoXTp09j4cKFKCwstP0wru29WwOFQoH4+HgkJCRg//79SElJwZw5cxAcHIxRo0Y5O7wGi4yMRKdOnbBixQokJibi3LlzeOGFF/DHH3/gsccew/jx46HVarFkyRKkpqZi165deO+99zBjxgxnh95gtb1TW/msR48ejYMHD2L9+vW4dOkSfvzxRzz99NMYO3YsIiMj28x7UhWcve6f6i4+Pr7KjRk//PBD8Z///KfYs2dP8eabbxbffPNN0WKx2K6XlpaKS5YsEQcMGCAOGDBAnDt3rpifn9+coddZde/4448/imPHjhV79uwpjhkzRtyzZ4/d9db0jhXS0tLEJ598Uhw4cKDYp08fcerUqeLp06ft6tT23q2B2WwWV69eLQ4ePFiMiYkRH3nkEfHy5cvODqvRcnJyxEWLFok33nij2KtXL/G+++4Tjx49art+/Phx8d5777X9//KDDz5wYrT1t3DhwkobFtb2Tq3xs67qPffu3SveddddYu/evcUbb7xRfPHFF0W9Xm+73hrfk2oniGIr2dCEiIiIqIlwyIyIiIhcHhMiIiIicnlMiIiIiMjlMSEiIiIil8eEiIiIiFweEyIiIiJyeUyIiIiIyOUxISIiIiKXx4SIyMVNnjwZkydPdnYYREROxYSIiIiIXB4TIiIiInJ5TIiIqFa//vorHnjgAfTv3x+DBg3CvHnzkJGRYbu+a9cudO/eHcePH8d9992HXr164eabb8amTZucGDURUd0xISKiGn3xxReYOnUqQkJCsGbNGixevBi///477rvvPuTl5dnqWa1WPPXUU7j11luxceNG9OvXD6tXr8bPP//sxOiJiOpG5uwAiKjlslqtSEhIwJAhQ/DKK6/Yyvv164dbb70VmzZtwoIFCwAAoihi1qxZuOeeewAA/fv3x7fffosDBw5g6NChTomfiKiu2ENERNW6cOECcnJyMHbsWLvy8PBw9O3bF0eOHLEr79u3r+2/FQoFfH19UVZW1iyxEhE1BhMiIqpWYWEhAMDf37/SNX9/f5SUlNiVqVQqu68lEglEUWyy+IiIHIUJERFVy9vbGwCQm5tb6VpOTg58fHyaOSIioqbBhIiIqhUREYGAgAB89dVXduWXL1/GH3/8gX79+jkpMiIix+KkaiJCZmYm3nvvvUrlXbp0wdy5c7F48WLMmzcPd9xxBwoKCrB+/Xp4eXlhypQpzR8sEVETYEJERLh06RJeeOGFSuUTJkzAqlWr4O7ujrfffhuPP/44NBoNhg4dirlz5yIgIMAJ0RIROZ4gcsYjERERuTjOISIiIiKXx4SIiIiIXB4TIiIiInJ5TIiIiIjI5TEhIiIiIpfHhIiI/r/dOhAAAAAAEORvPchFEcCeEAEAe0IEAOwJEQCwJ0QAwJ4QAQB7QgQA7AVu7g9cu10XOAAAAABJRU5ErkJggg==
"
class="
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">sns</span><span class="o">.</span><span class="n">relplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">covid</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s2">"Lon"</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">"Lat"</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s2">"Deaths"</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="s2">"Confirmed"</span><span class="p">,</span>
                <span class="n">sizes</span><span class="o">=</span><span class="p">(</span><span class="mi">40</span><span class="p">,</span><span class="mi">400</span><span class="p">))</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">ylim</span><span class="o">=</span><span class="p">(</span><span class="mi">25</span><span class="p">,</span><span class="mi">50</span><span class="p">),</span><span class="n">xlim</span><span class="o">=</span><span class="p">(</span><span class="o">-</span><span class="mi">150</span><span class="p">,</span><span class="o">-</span><span class="mi">50</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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3boVj8fDddddx5///GdSU1NZunQpCxcuJCEhgfPOO4+rrrqKZcuWccMNNzBu3DhSUlIoKSnhj3/8I2azmb///e+YzWZefPFFLrjgAt566y0GDhyIz+dj3rx5HDp0iBtuuIGYmBieffZZtm7dSlJSUof+niXZESHOz8H9hzvlTdnbchg8dGCnvEsIIQBKS0txOp2kp6e32DYnJ4e33nqL6667jiuuuAKA448/nqSkJK6//nrWrFnDCSecAEBlZSUrV66kT58+AFgsFubMmcO3337LSSedxNChQwHo06cPY8aMafKd48eP59JLL637/datW/H5fFx11VWcc845AFRUVHDttddy8cUX17WNjIxk9uzZ/Pjjj6SkpPDiiy9SVlbGv/71L9LS0gCYOnUqv//973nkkUd49NFHWbNmDVu2bOGZZ55h6tSpAEyaNKluFKojZBpLhLSqyupOe9d367fg8Xg67X0i+LxuN67KapwVVbhk5E6EIE3TAPB6vS22Xb++ppDqKaecUu/6KaecgqZprFu3ru5aXFxcXaIDkJKSAoDdbm9TfLVJ0dHGjh1b99/x8fEAjB49uu5aTEwMUJMIAaxdu5ahQ4eSnJyMx+PB4/GgqipTp07lm2++AWDjxo3o9XqmTJlS14/FYqlL4DpCRnZESKvsxGSnrLQcW7WdqOjITnunCA5XVTV+r4/SHXupOpCPz+NBMxqIzexPRK8kVIMOvcnU1WEKQXR0NBERERw+3PQIts1mw+12U15esyM1MbF+IVSdTkdsbCyVlZV1146eEqud3mrr+pemdqlardYG15qahgMoKytj3759DB8+vNH7drud8vJyYmJiGpxdePSftz0k2RGhrWcV+BYB4KqsJu+b7yndubfBv5/K/XmoBj0pE0cSM6gvBmtEYN5ZbcPv8VGdV4i7shpFVTBER2FJikM16NGZjAF5jwhPkydPZt26dTidTozGhv9W3nzzTe69917mz58PwJEjR+qmggDcbjelpaXExsZ2WsxtFRkZyYQJE7j++usbvW8wGIiNjaW0tBSv11s34gU1iVJHyTSWCGmRUQ0/PQRLdEwUloimP5mI0OeqqmbvR19SuiO3yUTZ53Jz+MvvOLI5G1cHRw5d1TYcxWXkfbmRHa/9m4OfrqVg/Rbyv/2B/R9/yc7XPyT/2x9wllfidro69C4Rvi677DLK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fD6WLVvGihUrqKysJCsri1tvvZXevXs32r64uJi7776br7/+Gr/fz3HHHceNN94Y8vV/unzNTq2LL76Yt99+u64ewU8//YTD4WhQedJorDk92ekMzNk9QgghRKAdOnSIL774os1rdFri9Xr54osvOHz4cED6e+KJJ3jttde48847ef311/H5fMybNw+Xy9Vo+7/+9a8cPnyY559/nueff57Dhw93uIZQZwiZkZ2MjAwAlixZwg8//MArr7yCyWRq8Bdem+RYLJYm+2quhk5zoz5CCCFEILzzzjsoihKwUZ1fUxSFlStX8uc//7lD/bhcLp577jkWLlzItGnTAHjooYeYMmUKq1evblDbp6KigvXr1/Pkk08ydOhQAK644gquueYaysrKQvrMri4d2SkpKeHDDz+sdyKsqqpkZGRQWFhISkoKhYWF9Z6p/X2oD5kJIYToub7++utWFQ5sD5/P1+paPc3Jzs6murqaSZMm1V2Liopi2LBhbNiwoUF7k8lEREQE7777LlVVVVRVVfHee+/Rv39/oqKiOhxPMHVpslNUVMSCBQtYu3Zt3TW32822bdsYOHAgWVlZbNq0qd4w4Lfffkv//v2Jj5cqrUIIIUKP2+1mz549QX3H7t27cbvdHeojPz8foME61qSkpLp7v2YwGLjnnntYv34948ePJysrix9++IFnnnmmXefodaYujW7w4MFMnTqVu+66iw0bNrBz505uvPFGKioquOSSS5g9ezZVVVXccsst5OTksHLlSl544QWuvPLKrgxbCCGEaFJeXl7A1+oczev1kpeX13LDZtjtdoBG18Y2ti7W7/ezfft2xo4dy6uvvsqLL75Ir169uOaaa6iqqupQLMHW5anYgw8+yKRJk7j22ms555xzKCsr49VXX6VXr17Ex8fz7LPPkpuby5lnnsmyZcu4/vrrOfPMM7s6bCGEEKJRTS3uDbX3mEymRvtxOp2YzeYG7T/66CNeeeUV7r//fsaNG8eECRN46qmnOHToEG+99VaHYgm2Ll+gHBkZyeLFi1m8eHGj90eNGsUbb7zRuUEJIYQQ7XT0SEmovqd2+qqwsJA+ffrUXS8sLGTIkCEN2m/cuJH+/ftjtVrrrkVHR9O/f3/27dvXoViCrctHdoQQQohwkpqaGvTz4jRN63DNuMzMTKxWa73zuioqKti2bRtZWVkN2qek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
"
class="
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="Dataset-COVID">Dataset COVID<a class="anchor-link" href="#Dataset-COVID">&#182;</a></h1>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Our goal is to correlate beds per 10,000 populations to mortality for COVID. Lets bring in another data set that tells us about the number of beds per sample. This table has one-line per hospital. We will need to aggregate or sum by county in order to get the total number of beds per county. First the API.</p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Loading-from-API">Loading from API<a class="anchor-link" href="#Loading-from-API">&#182;</a></h3>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[12]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">req</span><span class="o">=</span><span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">"https://www.communitybenefitinsight.org/api/get_hospitals.php"</span><span class="p">)</span><span class="o">.</span><span class="n">json</span><span class="p">()</span>
<span class="n">hospitals</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">req</span><span class="p">)</span>
<span class="n">hospitals</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[12]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>hospital_id</th>
      <th>hospital_org_id</th>
      <th>ein</th>
      <th>name</th>
      <th>name_cr</th>
      <th>street_address</th>
      <th>city</th>
      <th>state</th>
      <th>zip_code</th>
      <th>fips_state_and_county_code</th>
      <th>hospital_bed_count</th>
      <th>chrch_affl_f</th>
      <th>urban_location_f</th>
      <th>children_hospital_f</th>
      <th>memb_counc_teach_hosps_f</th>
      <th>medicare_provider_number</th>
      <th>county</th>
      <th>hospital_bed_size</th>
      <th>updated_dt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1</td>
      <td>630307951</td>
      <td>Mizell Memorial Hospital</td>
      <td>Mizell Memorial Hospital</td>
      <td>702 Main Street</td>
      <td>Opp</td>
      <td>AL</td>
      <td>36462</td>
      <td>01039</td>
      <td>99</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>010007</td>
      <td>Covington County</td>
      <td>&lt;100 beds</td>
      <td>June 15, 2022</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2</td>
      <td>630578923</td>
      <td>St Vincents East</td>
      <td>St Vincents East</td>
      <td>50 Medical Park Drive East</td>
      <td>Birmingham</td>
      <td>AL</td>
      <td>35235</td>
      <td>01073</td>
      <td>362</td>
      <td>N</td>
      <td>Y</td>
      <td>N</td>
      <td>Y</td>
      <td>010011</td>
      <td>Jefferson County</td>
      <td>&gt;299 beds</td>
      <td>June 15, 2022</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>3</td>
      <td>630312913</td>
      <td>Shelby Baptist Medical Center</td>
      <td>Shelby Baptist Medical Center</td>
      <td>1000 First Street North</td>
      <td>Alabaster</td>
      <td>AL</td>
      <td>35007</td>
      <td>01117</td>
      <td>252</td>
      <td>N</td>
      <td>Y</td>
      <td>N</td>
      <td>N</td>
      <td>010016</td>
      <td>Shelby County</td>
      <td>100-299 beds</td>
      <td>June 15, 2022</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>4</td>
      <td>630459034</td>
      <td>Callahan Eye Foundation Hosp</td>
      <td>Callahan Eye Foundation Hosp</td>
      <td>1720 University Boulevard</td>
      <td>Birmingham</td>
      <td>AL</td>
      <td>35233</td>
      <td>01073</td>
      <td>106</td>
      <td>N</td>
      <td>Y</td>
      <td>N</td>
      <td>Y</td>
      <td>010018</td>
      <td>Jefferson County</td>
      <td>100-299 beds</td>
      <td>June 15, 2022</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>5</td>
      <td>581973570</td>
      <td>Cherokee Medical Center</td>
      <td>Cherokee Medical Center</td>
      <td>400 Northwood Drive</td>
      <td>Centre</td>
      <td>AL</td>
      <td>35960</td>
      <td>01019</td>
      <td>60</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>010022</td>
      <td>Cherokee County</td>
      <td>&lt;100 beds</td>
      <td>June 15, 2022</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Create-HospitalInfoPerCounty-Table">Create HospitalInfoPerCounty Table<a class="anchor-link" href="#Create-HospitalInfoPerCounty-Table">&#182;</a></h3>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>The field we want is <code>hospital_bed_count</code> summed for each <code>county</code>. One thing to realize is that <code>county</code> is not unique in the US. There are more than one Jefferson Counties. So lets create a new column called <code>state_county</code></p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hospitals</span><span class="p">[</span><span class="s1">'state_county'</span><span class="p">]</span><span class="o">=</span><span class="n">hospitals</span><span class="p">[</span><span class="s1">'state'</span><span class="p">]</span><span class="o">+</span><span class="s1">'_'</span><span class="o">+</span><span class="n">hospitals</span><span class="p">[</span><span class="s1">'county'</span><span class="p">]</span>
<span class="n">hospitals</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[16]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>hospital_id</th>
      <th>hospital_org_id</th>
      <th>ein</th>
      <th>name</th>
      <th>name_cr</th>
      <th>street_address</th>
      <th>city</th>
      <th>state</th>
      <th>zip_code</th>
      <th>fips_state_and_county_code</th>
      <th>hospital_bed_count</th>
      <th>chrch_affl_f</th>
      <th>urban_location_f</th>
      <th>children_hospital_f</th>
      <th>memb_counc_teach_hosps_f</th>
      <th>medicare_provider_number</th>
      <th>county</th>
      <th>hospital_bed_size</th>
      <th>updated_dt</th>
      <th>state_county</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1</td>
      <td>630307951</td>
      <td>Mizell Memorial Hospital</td>
      <td>Mizell Memorial Hospital</td>
      <td>702 Main Street</td>
      <td>Opp</td>
      <td>AL</td>
      <td>36462</td>
      <td>01039</td>
      <td>99</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>010007</td>
      <td>Covington County</td>
      <td>&lt;100 beds</td>
      <td>June 15, 2022</td>
      <td>AL_Covington County</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2</td>
      <td>630578923</td>
      <td>St Vincents East</td>
      <td>St Vincents East</td>
      <td>50 Medical Park Drive East</td>
      <td>Birmingham</td>
      <td>AL</td>
      <td>35235</td>
      <td>01073</td>
      <td>362</td>
      <td>N</td>
      <td>Y</td>
      <td>N</td>
      <td>Y</td>
      <td>010011</td>
      <td>Jefferson County</td>
      <td>&gt;299 beds</td>
      <td>June 15, 2022</td>
      <td>AL_Jefferson County</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>3</td>
      <td>630312913</td>
      <td>Shelby Baptist Medical Center</td>
      <td>Shelby Baptist Medical Center</td>
      <td>1000 First Street North</td>
      <td>Alabaster</td>
      <td>AL</td>
      <td>35007</td>
      <td>01117</td>
      <td>252</td>
      <td>N</td>
      <td>Y</td>
      <td>N</td>
      <td>N</td>
      <td>010016</td>
      <td>Shelby County</td>
      <td>100-299 beds</td>
      <td>June 15, 2022</td>
      <td>AL_Shelby County</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>4</td>
      <td>630459034</td>
      <td>Callahan Eye Foundation Hosp</td>
      <td>Callahan Eye Foundation Hosp</td>
      <td>1720 University Boulevard</td>
      <td>Birmingham</td>
      <td>AL</td>
      <td>35233</td>
      <td>01073</td>
      <td>106</td>
      <td>N</td>
      <td>Y</td>
      <td>N</td>
      <td>Y</td>
      <td>010018</td>
      <td>Jefferson County</td>
      <td>100-299 beds</td>
      <td>June 15, 2022</td>
      <td>AL_Jefferson County</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>5</td>
      <td>581973570</td>
      <td>Cherokee Medical Center</td>
      <td>Cherokee Medical Center</td>
      <td>400 Northwood Drive</td>
      <td>Centre</td>
      <td>AL</td>
      <td>35960</td>
      <td>01019</td>
      <td>60</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>N</td>
      <td>010022</td>
      <td>Cherokee County</td>
      <td>&lt;100 beds</td>
      <td>June 15, 2022</td>
      <td>AL_Cherokee County</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>5 rows x 22 columns</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[17]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">HospitalInfoPerCounty</span><span class="o">=</span><span class="n">hospitals</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">'state_county'</span><span class="p">],</span> <span class="n">as_index</span><span class="o">=</span><span class="kc">False</span><span class="p">)[</span><span class="s1">'hospital_bed_count'</span><span class="p">]</span><span class="o">.</span><span class="n">agg</span><span class="p">(</span><span class="s1">'sum'</span><span class="p">)</span>
<span class="n">HospitalInfoPerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[17]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>hospital_bed_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AK_Anchorage Municipality</td>
      <td>401</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AK_Fairbanks North Star Borough</td>
      <td>162</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AK_Kenai Peninsula Borough</td>
      <td>49622</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AK_Ketchikan Gateway Borough</td>
      <td>25</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AK_Kodiak Island Borough</td>
      <td>25</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>That’s not right!</p>
<p>Ok – there clearly aren’t 49622 in AK_Kenai Peninsula Borough. Lets inspect further. And we’ll have to address it, but the <code>county</code> have  <code>County</code> in the end. Lets fix one thing at a time. First, lets see the types.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hospitals</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
RangeIndex: 3423 entries, 0 to 3422
Data columns (total 20 columns):
 #   Column                      Non-Null Count  Dtype 
---  ------                      --------------  ----- 
 0   hospital_id                 3423 non-null   object
 1   hospital_org_id             3423 non-null   object
 2   ein                         3423 non-null   object
 3   name                        3423 non-null   object
 4   name_cr                     3423 non-null   object
 5   street_address              3423 non-null   object
 6   city                        3423 non-null   object
 7   state                       3423 non-null   object
 8   zip_code                    3423 non-null   object
 9   fips_state_and_county_code  3423 non-null   object
 10  hospital_bed_count          3423 non-null   object
 11  chrch_affl_f                3423 non-null   object
 12  urban_location_f            3423 non-null   object
 13  children_hospital_f         3423 non-null   object
 14  memb_counc_teach_hosps_f    3423 non-null   object
 15  medicare_provider_number    3423 non-null   object
 16  county                      3422 non-null   object
 17  hospital_bed_size           3423 non-null   object
 18  updated_dt                  3423 non-null   object
 19  state_county                3422 non-null   object
dtypes: object(20)
memory usage: 535.0+ KB
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Turning-a-string-into-a-number-in-hospitals.hospital_bed_count">Turning a string into a number in <code>hospitals.hospital_bed_count</code><a class="anchor-link" href="#Turning-a-string-into-a-number-in-hospitals.hospital_bed_count">&#182;</a></h3><p>We need to make <code>hospital_bed_count</code> a number... but how?</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hospitals</span><span class="p">[</span><span class="s1">'hospital_bed_count'</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[19]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&#39;99&#39;</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Ok! Its a string. Now we need to convert that to a floating number. Lets do that:</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[22]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hospitals</span><span class="p">[</span><span class="s1">'hospital_bed_count'</span><span class="p">]</span><span class="o">=</span> <span class="n">hospitals</span><span class="p">[</span><span class="s1">'hospital_bed_count'</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">'float16'</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now lets see if we have this correct</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[23]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hospitals</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
RangeIndex: 3423 entries, 0 to 3422
Data columns (total 20 columns):
 #   Column                      Non-Null Count  Dtype  
---  ------                      --------------  -----  
 0   hospital_id                 3423 non-null   object 
 1   hospital_org_id             3423 non-null   object 
 2   ein                         3423 non-null   object 
 3   name                        3423 non-null   object 
 4   name_cr                     3423 non-null   object 
 5   street_address              3423 non-null   object 
 6   city                        3423 non-null   object 
 7   state                       3423 non-null   object 
 8   zip_code                    3423 non-null   object 
 9   fips_state_and_county_code  3423 non-null   object 
 10  hospital_bed_count          3423 non-null   float16
 11  chrch_affl_f                3423 non-null   object 
 12  urban_location_f            3423 non-null   object 
 13  children_hospital_f         3423 non-null   object 
 14  memb_counc_teach_hosps_f    3423 non-null   object 
 15  medicare_provider_number    3423 non-null   object 
 16  county                      3422 non-null   object 
 17  hospital_bed_size           3423 non-null   object 
 18  updated_dt                  3423 non-null   object 
 19  state_county                3422 non-null   object 
dtypes: float16(1), object(19)
memory usage: 514.9+ KB
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Create-HospitalInfoPerCounty-and-summing-for-hospital_bed_count">Create <code>HospitalInfoPerCounty</code> and summing for <code>hospital_bed_count</code><a class="anchor-link" href="#Create-HospitalInfoPerCounty-and-summing-for-hospital_bed_count">&#182;</a></h3><p>We need to create a dataframe that is unique by <code>state_county</code>, and we need to sum across entries on <code>hospital_bed_count</code>.  This is because the state and county may not be unique (e.g. multiple entries for different days).  Its always important to know what tables are unique for a table.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[24]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">HospitalInfoPerCounty</span><span class="o">=</span><span class="n">hospitals</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">'state_county'</span><span class="p">],</span> <span class="n">as_index</span><span class="o">=</span><span class="kc">False</span><span class="p">)[</span><span class="s1">'hospital_bed_count'</span><span class="p">]</span><span class="o">.</span><span class="n">agg</span><span class="p">(</span><span class="s1">'sum'</span><span class="p">)</span>
<span class="n">HospitalInfoPerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[24]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>hospital_bed_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AK_Anchorage Municipality</td>
      <td>401.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AK_Fairbanks North Star Borough</td>
      <td>162.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AK_Kenai Peninsula Borough</td>
      <td>77.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AK_Ketchikan Gateway Borough</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AK_Kodiak Island Borough</td>
      <td>25.0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Substitution-and-curating">Substitution and curating<a class="anchor-link" href="#Substitution-and-curating">&#182;</a></h3><p>Sometimes data is not fully structured, as is case here.. This is really sub-optimal, but there are times when you want an approximate solution to understand the scope of the problem. In this case, lets just focus on those that end in <code>County</code> and remove that text, noting we won’t get all matches, but we should get a majority.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[25]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">HospitalInfoPerCounty</span><span class="p">[</span><span class="s1">'state_county'</span><span class="p">]</span><span class="o">=</span><span class="n">HospitalInfoPerCounty</span><span class="p">[</span><span class="s1">'state_county'</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s1">' County'</span><span class="p">,</span><span class="s1">''</span><span class="p">)</span>
<span class="n">HospitalInfoPerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[25]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>hospital_bed_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AK_Anchorage Municipality</td>
      <td>401.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AK_Fairbanks North Star Borough</td>
      <td>162.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AK_Kenai Peninsula Borough</td>
      <td>77.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AK_Ketchikan Gateway Borough</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AK_Kodiak Island Borough</td>
      <td>25.0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Create-CovidPerCounty-DataFrame">Create <code>CovidPerCounty</code> DataFrame<a class="anchor-link" href="#Create-CovidPerCounty-DataFrame">&#182;</a></h3><p>We need to work on <code>covid</code>, and curate it for use in order to compare with <code>HospitalInfoPerCounty</code>.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[26]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">json</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="n">req</span><span class="o">=</span><span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">"https://webhooks.mongodb-stitch.com/api/client/v2.0/app/covid-19-qppza/service/REST-API/incoming_webhook/us_only?min_date=2021-01-15T00:00:00.000Z&amp;max_date=2021-01-15T00:00:00.000Z"</span><span class="p">)</span><span class="o">.</span><span class="n">json</span><span class="p">()</span>
<span class="n">covid</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">req</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Lets examing the resulting table. We will see that the states is not a two letter code. Lets convert that using a dictionary.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[27]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[27]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>_id</th>
      <th>uid</th>
      <th>country_iso2</th>
      <th>country_iso3</th>
      <th>country_code</th>
      <th>fips</th>
      <th>county</th>
      <th>state</th>
      <th>country</th>
      <th>combined_name</th>
      <th>population</th>
      <th>loc</th>
      <th>date</th>
      <th>confirmed</th>
      <th>deaths</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63338f9a8c6fbf5bd7bef707</td>
      <td>84001001</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1001.0</td>
      <td>Autauga</td>
      <td>Alabama</td>
      <td>US</td>
      <td>Autauga, Alabama, US</td>
      <td>55869.0</td>
      <td>{'type': 'Point', 'coordinates': [-86.6441, 32...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>5103</td>
      <td>55</td>
      <td>28</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>63338f9a8c6fbf5bd7befada</td>
      <td>84001003</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1003.0</td>
      <td>Baldwin</td>
      <td>Alabama</td>
      <td>US</td>
      <td>Baldwin, Alabama, US</td>
      <td>223234.0</td>
      <td>{'type': 'Point', 'coordinates': [-87.7221, 30...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>16002</td>
      <td>179</td>
      <td>161</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>63338f9a8c6fbf5bd7befead</td>
      <td>84001005</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1005.0</td>
      <td>Barbour</td>
      <td>Alabama</td>
      <td>US</td>
      <td>Barbour, Alabama, US</td>
      <td>24686.0</td>
      <td>{'type': 'Point', 'coordinates': [-85.3871, 31...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>1712</td>
      <td>36</td>
      <td>16</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>63338f9a8c6fbf5bd7bf0280</td>
      <td>84001007</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1007.0</td>
      <td>Bibb</td>
      <td>Alabama</td>
      <td>US</td>
      <td>Bibb, Alabama, US</td>
      <td>22394.0</td>
      <td>{'type': 'Point', 'coordinates': [-87.1251, 32...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>2130</td>
      <td>47</td>
      <td>17</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>63338f9a8c6fbf5bd7bf0653</td>
      <td>84001009</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1009.0</td>
      <td>Blount</td>
      <td>Alabama</td>
      <td>US</td>
      <td>Blount, Alabama, US</td>
      <td>57826.0</td>
      <td>{'type': 'Point', 'coordinates': [-86.5679, 33...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>5264</td>
      <td>83</td>
      <td>45</td>
      <td>3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">us_state_to_abbrev</span> <span class="o">=</span> <span class="p">{</span>
<span class="s2">"Alabama"</span><span class="p">:</span> <span class="s2">"AL"</span><span class="p">,</span><span class="s2">"Alaska"</span><span class="p">:</span> <span class="s2">"AK"</span><span class="p">,</span><span class="s2">"Arizona"</span><span class="p">:</span> <span class="s2">"AZ"</span><span class="p">,</span><span class="s2">"Arkansas"</span><span class="p">:</span> <span class="s2">"AR"</span><span class="p">,</span> <span class="s2">"California"</span><span class="p">:</span> <span class="s2">"CA"</span><span class="p">,</span>
<span class="s2">"Colorado"</span><span class="p">:</span> <span class="s2">"CO"</span><span class="p">,</span><span class="s2">"Connecticut"</span><span class="p">:</span> <span class="s2">"CT"</span><span class="p">,</span><span class="s2">"Delaware"</span><span class="p">:</span> <span class="s2">"DE"</span><span class="p">,</span><span class="s2">"Florida"</span><span class="p">:</span> <span class="s2">"FL"</span><span class="p">,</span><span class="s2">"Georgia"</span><span class="p">:</span> <span class="s2">"GA"</span><span class="p">,</span>
<span class="s2">"Hawaii"</span><span class="p">:</span> <span class="s2">"HI"</span><span class="p">,</span><span class="s2">"Idaho"</span><span class="p">:</span> <span class="s2">"ID"</span><span class="p">,</span><span class="s2">"Illinois"</span><span class="p">:</span> <span class="s2">"IL"</span><span class="p">,</span><span class="s2">"Indiana"</span><span class="p">:</span> <span class="s2">"IN"</span><span class="p">,</span><span class="s2">"Iowa"</span><span class="p">:</span> <span class="s2">"IA"</span><span class="p">,</span><span class="s2">"Kansas"</span><span class="p">:</span> <span class="s2">"KS"</span><span class="p">,</span>
<span class="s2">"Kentucky"</span><span class="p">:</span> <span class="s2">"KY"</span><span class="p">,</span><span class="s2">"Louisiana"</span><span class="p">:</span> <span class="s2">"LA"</span><span class="p">,</span><span class="s2">"Maine"</span><span class="p">:</span> <span class="s2">"ME"</span><span class="p">,</span><span class="s2">"Maryland"</span><span class="p">:</span> <span class="s2">"MD"</span><span class="p">,</span><span class="s2">"Massachusetts"</span><span class="p">:</span> <span class="s2">"MA"</span><span class="p">,</span>
<span class="s2">"Michigan"</span><span class="p">:</span> <span class="s2">"MI"</span><span class="p">,</span><span class="s2">"Minnesota"</span><span class="p">:</span> <span class="s2">"MN"</span><span class="p">,</span><span class="s2">"Mississippi"</span><span class="p">:</span> <span class="s2">"MS"</span><span class="p">,</span><span class="s2">"Missouri"</span><span class="p">:</span> <span class="s2">"MO"</span><span class="p">,</span><span class="s2">"Montana"</span><span class="p">:</span> <span class="s2">"MT"</span><span class="p">,</span>
<span class="s2">"Nebraska"</span><span class="p">:</span> <span class="s2">"NE"</span><span class="p">,</span><span class="s2">"Nevada"</span><span class="p">:</span> <span class="s2">"NV"</span><span class="p">,</span><span class="s2">"New Hampshire"</span><span class="p">:</span> <span class="s2">"NH"</span><span class="p">,</span><span class="s2">"New Jersey"</span><span class="p">:</span> <span class="s2">"NJ"</span><span class="p">,</span><span class="s2">"New Mexico"</span><span class="p">:</span> <span class="s2">"NM"</span><span class="p">,</span>
<span class="s2">"New York"</span><span class="p">:</span> <span class="s2">"NY"</span><span class="p">,</span><span class="s2">"North Carolina"</span><span class="p">:</span> <span class="s2">"NC"</span><span class="p">,</span><span class="s2">"North Dakota"</span><span class="p">:</span> <span class="s2">"ND"</span><span class="p">,</span><span class="s2">"Ohio"</span><span class="p">:</span> <span class="s2">"OH"</span><span class="p">,</span>
<span class="s2">"Oklahoma"</span><span class="p">:</span> <span class="s2">"OK"</span><span class="p">,</span><span class="s2">"Oregon"</span><span class="p">:</span> <span class="s2">"OR"</span><span class="p">,</span><span class="s2">"Pennsylvania"</span><span class="p">:</span> <span class="s2">"PA"</span><span class="p">,</span><span class="s2">"Rhode Island"</span><span class="p">:</span> <span class="s2">"RI"</span><span class="p">,</span>
<span class="s2">"South Carolina"</span><span class="p">:</span> <span class="s2">"SC"</span><span class="p">,</span><span class="s2">"South Dakota"</span><span class="p">:</span> <span class="s2">"SD"</span><span class="p">,</span><span class="s2">"Tennessee"</span><span class="p">:</span> <span class="s2">"TN"</span><span class="p">,</span><span class="s2">"Texas"</span><span class="p">:</span> <span class="s2">"TX"</span><span class="p">,</span>
<span class="s2">"Utah"</span><span class="p">:</span> <span class="s2">"UT"</span><span class="p">,</span><span class="s2">"Vermont"</span><span class="p">:</span> <span class="s2">"VT"</span><span class="p">,</span><span class="s2">"Virginia"</span><span class="p">:</span> <span class="s2">"VA"</span><span class="p">,</span><span class="s2">"Washington"</span><span class="p">:</span> <span class="s2">"WA"</span><span class="p">,</span>
<span class="s2">"West Virginia"</span><span class="p">:</span> <span class="s2">"WV"</span><span class="p">,</span><span class="s2">"Wisconsin"</span><span class="p">:</span> <span class="s2">"WI"</span><span class="p">,</span><span class="s2">"Wyoming"</span><span class="p">:</span> <span class="s2">"WY"</span><span class="p">,</span>
<span class="s2">"District of Columbia"</span><span class="p">:</span> <span class="s2">"DC"</span><span class="p">,</span><span class="s2">"American Samoa"</span><span class="p">:</span> <span class="s2">"AS"</span><span class="p">,</span><span class="s2">"Guam"</span><span class="p">:</span> <span class="s2">"GU"</span><span class="p">,</span> <span class="s2">"Northern Mariana Islands"</span><span class="p">:</span> <span class="s2">"MP"</span><span class="p">,</span>
<span class="s2">"Puerto Rico"</span><span class="p">:</span> <span class="s2">"PR"</span><span class="p">,</span><span class="s2">"United States Minor Outlying Islands"</span><span class="p">:</span> <span class="s2">"UM"</span><span class="p">,</span><span class="s2">"U.S. Virgin Islands"</span><span class="p">:</span> <span class="s2">"VI"</span><span class="p">,</span>
<span class="p">}</span>
<span class="n">covid</span><span class="p">[</span><span class="s1">'state'</span><span class="p">]</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="n">us_state_to_abbrev</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">covid</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[28]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>_id</th>
      <th>uid</th>
      <th>country_iso2</th>
      <th>country_iso3</th>
      <th>country_code</th>
      <th>fips</th>
      <th>county</th>
      <th>state</th>
      <th>country</th>
      <th>combined_name</th>
      <th>population</th>
      <th>loc</th>
      <th>date</th>
      <th>confirmed</th>
      <th>deaths</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63338f9a8c6fbf5bd7bef707</td>
      <td>84001001</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1001.0</td>
      <td>Autauga</td>
      <td>AL</td>
      <td>US</td>
      <td>Autauga, Alabama, US</td>
      <td>55869.0</td>
      <td>{'type': 'Point', 'coordinates': [-86.6441, 32...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>5103</td>
      <td>55</td>
      <td>28</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>63338f9a8c6fbf5bd7befada</td>
      <td>84001003</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1003.0</td>
      <td>Baldwin</td>
      <td>AL</td>
      <td>US</td>
      <td>Baldwin, Alabama, US</td>
      <td>223234.0</td>
      <td>{'type': 'Point', 'coordinates': [-87.7221, 30...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>16002</td>
      <td>179</td>
      <td>161</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>63338f9a8c6fbf5bd7befead</td>
      <td>84001005</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1005.0</td>
      <td>Barbour</td>
      <td>AL</td>
      <td>US</td>
      <td>Barbour, Alabama, US</td>
      <td>24686.0</td>
      <td>{'type': 'Point', 'coordinates': [-85.3871, 31...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>1712</td>
      <td>36</td>
      <td>16</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>63338f9a8c6fbf5bd7bf0280</td>
      <td>84001007</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1007.0</td>
      <td>Bibb</td>
      <td>AL</td>
      <td>US</td>
      <td>Bibb, Alabama, US</td>
      <td>22394.0</td>
      <td>{'type': 'Point', 'coordinates': [-87.1251, 32...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>2130</td>
      <td>47</td>
      <td>17</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>63338f9a8c6fbf5bd7bf0653</td>
      <td>84001009</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1009.0</td>
      <td>Blount</td>
      <td>AL</td>
      <td>US</td>
      <td>Blount, Alabama, US</td>
      <td>57826.0</td>
      <td>{'type': 'Point', 'coordinates': [-86.5679, 33...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>5264</td>
      <td>83</td>
      <td>45</td>
      <td>3</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Creating-a-key-to-join-our-tables">Creating a key to join our tables<a class="anchor-link" href="#Creating-a-key-to-join-our-tables">&#182;</a></h3><p>The dataframe <code>covid</code> may not be fully unique per <code>state</code> or <code>county</code>. Lets create a new column that we can merge on which concatenates both.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[29]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">covid</span><span class="p">[</span><span class="s1">'state_county'</span><span class="p">]</span><span class="o">=</span><span class="n">covid</span><span class="p">[</span><span class="s1">'state'</span><span class="p">]</span><span class="o">+</span><span class="s1">'_'</span><span class="o">+</span><span class="n">covid</span><span class="p">[</span><span class="s1">'county'</span><span class="p">]</span>
<span class="n">covid</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[29]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>_id</th>
      <th>uid</th>
      <th>country_iso2</th>
      <th>country_iso3</th>
      <th>country_code</th>
      <th>fips</th>
      <th>county</th>
      <th>state</th>
      <th>country</th>
      <th>combined_name</th>
      <th>population</th>
      <th>loc</th>
      <th>date</th>
      <th>confirmed</th>
      <th>deaths</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
      <th>state_county</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63338f9a8c6fbf5bd7bef707</td>
      <td>84001001</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1001.0</td>
      <td>Autauga</td>
      <td>AL</td>
      <td>US</td>
      <td>Autauga, Alabama, US</td>
      <td>55869.0</td>
      <td>{'type': 'Point', 'coordinates': [-86.6441, 32...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>5103</td>
      <td>55</td>
      <td>28</td>
      <td>0</td>
      <td>AL_Autauga</td>
    </tr>
    <tr>
      <th>1</th>
      <td>63338f9a8c6fbf5bd7befada</td>
      <td>84001003</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1003.0</td>
      <td>Baldwin</td>
      <td>AL</td>
      <td>US</td>
      <td>Baldwin, Alabama, US</td>
      <td>223234.0</td>
      <td>{'type': 'Point', 'coordinates': [-87.7221, 30...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>16002</td>
      <td>179</td>
      <td>161</td>
      <td>2</td>
      <td>AL_Baldwin</td>
    </tr>
    <tr>
      <th>2</th>
      <td>63338f9a8c6fbf5bd7befead</td>
      <td>84001005</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1005.0</td>
      <td>Barbour</td>
      <td>AL</td>
      <td>US</td>
      <td>Barbour, Alabama, US</td>
      <td>24686.0</td>
      <td>{'type': 'Point', 'coordinates': [-85.3871, 31...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>1712</td>
      <td>36</td>
      <td>16</td>
      <td>0</td>
      <td>AL_Barbour</td>
    </tr>
    <tr>
      <th>3</th>
      <td>63338f9a8c6fbf5bd7bf0280</td>
      <td>84001007</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1007.0</td>
      <td>Bibb</td>
      <td>AL</td>
      <td>US</td>
      <td>Bibb, Alabama, US</td>
      <td>22394.0</td>
      <td>{'type': 'Point', 'coordinates': [-87.1251, 32...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>2130</td>
      <td>47</td>
      <td>17</td>
      <td>0</td>
      <td>AL_Bibb</td>
    </tr>
    <tr>
      <th>4</th>
      <td>63338f9a8c6fbf5bd7bf0653</td>
      <td>84001009</td>
      <td>US</td>
      <td>USA</td>
      <td>840</td>
      <td>1009.0</td>
      <td>Blount</td>
      <td>AL</td>
      <td>US</td>
      <td>Blount, Alabama, US</td>
      <td>57826.0</td>
      <td>{'type': 'Point', 'coordinates': [-86.5679, 33...</td>
      <td>2021-01-15T00:00:00.000Z</td>
      <td>5264</td>
      <td>83</td>
      <td>45</td>
      <td>3</td>
      <td>AL_Blount</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Creating-a-dataframe-with-unique-CovidPreCount">Creating a dataframe with unique CovidPreCount<a class="anchor-link" href="#Creating-a-dataframe-with-unique-CovidPreCount">&#182;</a></h3><p>We will group and sum for <code>deaths</code>, <code>population</code>, and <code>confirmed</code>.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[30]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">CovidPerCounty</span><span class="o">=</span><span class="n">covid</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">'state_county'</span><span class="p">],</span> <span class="n">as_index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span><span class="o">.</span><span class="n">agg</span><span class="p">({</span><span class="s1">'deaths'</span><span class="p">:</span><span class="s1">'sum'</span><span class="p">,</span><span class="s1">'confirmed'</span><span class="p">:</span><span class="s1">'sum'</span><span class="p">,</span><span class="s1">'population'</span><span class="p">:</span><span class="s1">'sum'</span><span class="p">,</span><span class="s1">'confirmed_daily'</span><span class="p">:</span><span class="s1">'mean'</span><span class="p">,</span><span class="s1">'deaths_daily'</span><span class="p">:</span><span class="s1">'mean'</span><span class="p">})</span>
<span class="n">CovidPerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">15</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[30]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>deaths</th>
      <th>confirmed</th>
      <th>population</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AK_Aleutians East</td>
      <td>0</td>
      <td>40</td>
      <td>3337.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AK_Aleutians West</td>
      <td>0</td>
      <td>242</td>
      <td>5634.0</td>
      <td>3.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AK_Anchorage</td>
      <td>129</td>
      <td>24530</td>
      <td>288000.0</td>
      <td>92.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AK_Bethel</td>
      <td>12</td>
      <td>2911</td>
      <td>18386.0</td>
      <td>26.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AK_Bristol Bay</td>
      <td>0</td>
      <td>0</td>
      <td>836.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>AK_Bristol Bay plus Lake and Peninsula</td>
      <td>0</td>
      <td>163</td>
      <td>2428.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>AK_Chugach</td>
      <td>3</td>
      <td>241</td>
      <td>6751.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>AK_Copper River</td>
      <td>0</td>
      <td>175</td>
      <td>2699.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>AK_Denali</td>
      <td>0</td>
      <td>63</td>
      <td>2097.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>AK_Dillingham</td>
      <td>1</td>
      <td>150</td>
      <td>4916.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>AK_Fairbanks North Star</td>
      <td>23</td>
      <td>5576</td>
      <td>96849.0</td>
      <td>46.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>AK_Haines</td>
      <td>0</td>
      <td>23</td>
      <td>2530.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>AK_Hoonah-Angoon</td>
      <td>0</td>
      <td>0</td>
      <td>2148.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>AK_Juneau</td>
      <td>5</td>
      <td>1098</td>
      <td>31974.0</td>
      <td>4.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>AK_Kenai Peninsula</td>
      <td>19</td>
      <td>3821</td>
      <td>58708.0</td>
      <td>11.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Create-mortality-within-CovidPerCounty">Create mortality within CovidPerCounty<a class="anchor-link" href="#Create-mortality-within-CovidPerCounty">&#182;</a></h3>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[32]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">CovidPerCounty</span><span class="p">[</span><span class="s1">'mortality'</span><span class="p">]</span><span class="o">=</span><span class="n">CovidPerCounty</span><span class="p">[</span><span class="s1">'deaths'</span><span class="p">]</span><span class="o">/</span><span class="n">CovidPerCounty</span><span class="p">[</span><span class="s1">'confirmed'</span><span class="p">]</span>
<span class="n">CovidPerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[32]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>deaths</th>
      <th>confirmed</th>
      <th>population</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
      <th>mortality</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AK_Aleutians East</td>
      <td>0</td>
      <td>40</td>
      <td>3337.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AK_Aleutians West</td>
      <td>0</td>
      <td>242</td>
      <td>5634.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AK_Anchorage</td>
      <td>129</td>
      <td>24530</td>
      <td>288000.0</td>
      <td>92.0</td>
      <td>0.0</td>
      <td>0.005259</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AK_Bethel</td>
      <td>12</td>
      <td>2911</td>
      <td>18386.0</td>
      <td>26.0</td>
      <td>0.0</td>
      <td>0.004122</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AK_Bristol Bay</td>
      <td>0</td>
      <td>0</td>
      <td>836.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Joining-CovidPerCounty-and-HospitalInfoPerCounty">Joining <code>CovidPerCounty</code> and <code>HospitalInfoPerCounty</code><a class="anchor-link" href="#Joining-CovidPerCounty-and-HospitalInfoPerCounty">&#182;</a></h3><h3 id="Join-HospitalInfoPerCounty-and-CovidPerCounty-by-state_county.">Join <code>HospitalInfoPerCounty</code> and <code>CovidPerCounty</code> by <code>state_county</code>.<a class="anchor-link" href="#Join-HospitalInfoPerCounty-and-CovidPerCounty-by-state_county.">&#182;</a></h3>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[33]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Hospital_Covid_PerCounty</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">HospitalInfoPerCounty</span><span class="p">,</span><span class="n">CovidPerCounty</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">'state_county'</span><span class="p">)</span>
<span class="n">Hospital_Covid_PerCounty</span><span class="o">=</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="s1">'population'</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">50000</span><span class="p">]</span>
<span class="n">Hospital_Covid_PerCounty</span><span class="o">=</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="s1">'population'</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">300000</span><span class="p">]</span>
<span class="n">Hospital_Covid_PerCounty</span><span class="o">=</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="s1">'confirmed'</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">10</span><span class="p">]</span>
<span class="n">Hospital_Covid_PerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[33]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>hospital_bed_count</th>
      <th>deaths</th>
      <th>confirmed</th>
      <th>population</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
      <th>mortality</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AL_Baldwin</td>
      <td>240.0</td>
      <td>179</td>
      <td>16002</td>
      <td>223234.0</td>
      <td>161.0</td>
      <td>2.0</td>
      <td>0.011186</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AL_Blount</td>
      <td>65.0</td>
      <td>83</td>
      <td>5264</td>
      <td>57826.0</td>
      <td>45.0</td>
      <td>3.0</td>
      <td>0.015767</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AL_Calhoun</td>
      <td>552.0</td>
      <td>200</td>
      <td>10982</td>
      <td>113605.0</td>
      <td>119.0</td>
      <td>3.0</td>
      <td>0.018212</td>
    </tr>
    <tr>
      <th>8</th>
      <td>AL_Cullman</td>
      <td>115.0</td>
      <td>104</td>
      <td>7960</td>
      <td>83768.0</td>
      <td>38.0</td>
      <td>10.0</td>
      <td>0.013065</td>
    </tr>
    <tr>
      <th>9</th>
      <td>AL_Elmore</td>
      <td>69.0</td>
      <td>101</td>
      <td>7723</td>
      <td>81209.0</td>
      <td>53.0</td>
      <td>0.0</td>
      <td>0.013078</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>To get the final plot of People Per Hospital Bed vs Mortality: 
Check to make sure mortality is a number first.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[35]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Hospital_Covid_PerCounty</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
Int64Index: 563 entries, 0 to 1669
Data columns (total 8 columns):
 #   Column              Non-Null Count  Dtype  
---  ------              --------------  -----  
 0   state_county        563 non-null    object 
 1   hospital_bed_count  563 non-null    float32
 2   deaths              563 non-null    int64  
 3   confirmed           563 non-null    int64  
 4   population          563 non-null    float64
 5   confirmed_daily     563 non-null    float64
 6   deaths_daily        563 non-null    float64
 7   mortality           563 non-null    float64
dtypes: float32(1), float64(4), int64(2), object(1)
memory usage: 37.4+ KB
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now, we will create <code>people_per_bed</code> within Hospital_Covid_PerCounty similar to how we created mortality within CovidPerCounty as above.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[42]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="s1">'people_per_bed'</span><span class="p">]</span><span class="o">=</span> <span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="s1">'population'</span><span class="p">]</span><span class="o">/</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">[</span><span class="s1">'hospital_bed_count'</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Double check that <code>people_per_bed</code> is accurate.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[43]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">people_per_bed</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[43]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0     930.141667
1     889.630769
2     205.806159
8     728.417391
9    1176.942029
dtype: float64</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[44]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Hospital_Covid_PerCounty</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[44]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state_county</th>
      <th>hospital_bed_count</th>
      <th>deaths</th>
      <th>confirmed</th>
      <th>population</th>
      <th>confirmed_daily</th>
      <th>deaths_daily</th>
      <th>mortality</th>
      <th>people_per_bed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AL_Baldwin</td>
      <td>240.0</td>
      <td>179</td>
      <td>16002</td>
      <td>223234.0</td>
      <td>161.0</td>
      <td>2.0</td>
      <td>0.011186</td>
      <td>930.141667</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AL_Blount</td>
      <td>65.0</td>
      <td>83</td>
      <td>5264</td>
      <td>57826.0</td>
      <td>45.0</td>
      <td>3.0</td>
      <td>0.015767</td>
      <td>889.630769</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AL_Calhoun</td>
      <td>552.0</td>
      <td>200</td>
      <td>10982</td>
      <td>113605.0</td>
      <td>119.0</td>
      <td>3.0</td>
      <td>0.018212</td>
      <td>205.806159</td>
    </tr>
    <tr>
      <th>8</th>
      <td>AL_Cullman</td>
      <td>115.0</td>
      <td>104</td>
      <td>7960</td>
      <td>83768.0</td>
      <td>38.0</td>
      <td>10.0</td>
      <td>0.013065</td>
      <td>728.417391</td>
    </tr>
    <tr>
      <th>9</th>
      <td>AL_Elmore</td>
      <td>69.0</td>
      <td>101</td>
      <td>7723</td>
      <td>81209.0</td>
      <td>53.0</td>
      <td>0.0</td>
      <td>0.013078</td>
      <td>1176.942029</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now that we have both <code>mortality</code> and <code>people_per_bed</code> within Hospital_Covid_PerCounty, we can create the final plot.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[61]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">sns</span><span class="o">.</span><span class="n">relplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">Hospital_Covid_PerCounty</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s2">"people_per_bed"</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">"mortality"</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s2">"confirmed"</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="s2">"population"</span><span class="p">,</span>
                <span class="n">sizes</span><span class="o">=</span><span class="p">(</span><span class="mi">40</span><span class="p">,</span><span class="mi">400</span><span class="p">))</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">ylim</span><span class="o">=</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mf">0.06</span><span class="p">),</span><span class="n">xlim</span><span class="o">=</span><span class="p">(</span><span class="o">-</span><span class="mi">500</span><span class="p">,</span><span class="mi">6500</span><span class="p">),</span><span class="n">title</span><span class="o">=</span><span class="s1">'PEOPLE PER HOSPITAL BED VS. MORTALITY'</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjwAAAH2CAYAAAB0lFbVAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjYuMCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy89olMNAAAACXBIWXMAAA9hAAAPYQGoP6dpAAEAAElEQVR4nOzdd3hUVfrA8e/0Se8NQigBQu+hCdIEe0Esq4KK4vpbUSzYUBdFZVFBVEBdUBRde0EUrCusUqR3SOghkN779Du/P2JGhkySSUgIhPfzPDwPuffcc89MJjPvnPOec1ROp9OJEEIIIUQLpm7uBgghhBBCNDUJeIQQQgjR4knAI4QQQogWTwIeIYQQQrR4EvAIIYQQosWTgEcIIYQQLZ4EPEIIIYRo8STgEUIIIUSLJwGPEEIIIVo8bXM3oKWbNGkSW7ZscTum0+kIDw9n1KhRPPTQQwQFBQGwcOFCFi1aVGt9e/bswWAwuH5OS0vjnXfeYf369eTk5BAUFESPHj2YOHEiw4YNc7v2ySef5JtvvnE7ptVqCQkJYciQITzyyCPExMS4teXgwYM1tiUtLY0xY8bU2t7nnnuOW265xeM5T49Xo9EQEBDAgAEDeOihh+jUqRMAmzdv5vbbb6/1Xu+88w4XX3xxjWV1Oh2hoaEMHjyYxx57jIiIiBrrevLJJ9myZQtr1qzxeH706NEMHDiQl156ye349u3bWbZsGTt27KCkpITIyEiGDBnC5MmTiY+Pr1bP9u3beeedd9i5cyfl5eWEh4czdOhQ/vGPf9CmTRtXufq8jpYvX86MGTNYvXo1sbGxJCQk1Pyk/WnOnDlcf/31ABw/fpxLL72U4OBg1q1bh16vdytb9Xs/9RpvjB49mvT0dNfPKpWKoKAg+vbty0MPPUSXLl1c5zy9Vk8VHh7Ohg0bPJZVqVQYjUbatGnDpZdeypQpUzAajR7rMZvNXHTRRfTv358lS5Z4LJOXl8eIESP4+9//zoMPPgh4/3vzRtXfgV6vZ+PGjfj7+1cr8+mnn/Lcc8/RunXraq/JgwcPsnTpUjZt2kRBQQHh4eH069ePO+64g969e7uV9fQ6UqlU+Pr60q5dO+644w6uvfZagGZ73Zz6t+fN3z3Ajz/+yHXXXUf37t355JNPUKlUbucVReHWW28lJSWF7777jqioqDrrFC2PBDxnQbdu3Xj22WddP9tsNvbv38/8+fNJTk7m008/dfsD/fzzz2us69Q3kY0bNzJ16lSio6OZMmUK8fHxFBQUsGrVKu6++27uuOMOnnrqKbfrIyIi3IIMu91OSkoK8+bNY+fOnaxatarGD4ea/OMf/2DkyJEez3nz5n/q43U4HGRkZPDaa69x22238f3337sFJjNnzqR79+4e6zk9oDi9bHl5Odu3b2fJkiWkpKTw5Zdf1tm2+liyZAnz589n2LBhPPXUU0RERJCamsqnn37K+PHjmTNnDldeeaWr/MaNG5kyZQpjx45l9uzZBAQEcOLECd577z1uuOEGvvzyS+Li4lzl6/s6qnL66+nmm2/mhhtu4MYbb3QdO/U+X3/9NfHx8aSmpvLTTz9xzTXXNMrzAzBixAjuu+8+oPK1l5OTw3vvvccdd9zBDz/8QFhYmKvs6a/VU+l0OrefTy2rKAqlpaVs27aNxYsXs379ej744AO3LwpVjEYjV155JV9//TUFBQWEhoZWK7Ny5UocDgcTJkwA6v9785bdbmfNmjUen+8ffvjB4zXffvstTz/9NN26dePhhx+mdevWZGVl8dVXX3HLLbfw2GOPMXnyZLdrTn8dORwOsrKyWLZsGY8//jjBwcGMGDHinHjddO/e3a0d+/fv5/nnn6/2tx0bG8sDDzzAvHnz+OSTT7jtttvc6vnoo4/YuXMn8+fPl2DnAiYBz1ng7+9Pnz593I4lJiZSXl7OggUL2L17t9v508t6kp2dzbRp0+jXrx9vvvmm25v5ZZddxrJly5gzZw6dOnVye4PS6/XV6h8wYAA6nY4nnniC1atXu30oeyMuLs6rNtfk9Gv79+9PTEwMt912G9988w1///vfXec6duzo9b08lb3ooouwWq288847HDlyhI4dOza43af63//+x6uvvsoDDzzA/fff7zo+cOBArrvuOqZPn86TTz5J586dXb1W//73v+nVqxevv/66q/ygQYMYMWIEY8eO5f3333f7YKrv66iKp2PR0dEejzscDlasWMHNN9/Mzp07+eyzzxo14AkNDa123549e3LJJZfw008/uX1QeXqt1sRT2REjRtC7d2+mTp3Ke++9xz/+8Q+P195www18/vnn/Pjjj9U+KAG++eYbhgwZQmxsLFD/35u3+vXrx48//ljt+c7Ozmbbtm107dqVkpIS1/GkpCSefvpprr32Wl544QXU6r8yFK655hpmz57Nyy+/TEJCAkOHDnWd8/Q6Arj44osZMmQIy5cvZ8SIEefE6+b0tlosFsDz3/Zdd93Fzz//zKuvvsro0aNdvdVpaWm89tprXHHFFfV+bxMti+TwNKMePXoAkJGRUe9rly1bRkVFBS+++KLHb6533nknffr04e2338ab/WF79uwJ4Dbk0JyqnpumaE9gYCCAx96Qhlq0aBEdOnRg6tSp1c7pdDqef/55NBoN77zzjut4Xl6ex99NZGQkzzzzDBdddJFX9z6T19HpqoZGR44cyTXXXMP27ds5cuTIGddbm6qhuKZwySWX0KdPHz777LMay/Tq1YtOnTqxcuXKaueSk5M5ePAgN9xwg+tYY/3eTnfFFVewfv16ysrK3I7/9NNPtG/f3m3IDyoDL19fX5555hm3YKfKY489RkxMDG+++aZX9zcYDOj1+gb9XTTH6+Z0Go2GOXPmYLVaee6551zHn332Wfz8/BoUhIqWRQKeZpSSkgJUH/ax2+0e/ymK4iqzfv16unbtSnR0dI31X3755aSnp5OcnOx1WxrSFa8oisf2OhyOetdVV3vqc6/TyxYVFfHLL7+wdOlSevXqRfv27etsR02/i1MVFBSwb98+Ro0aVeOHRXBwMEOHDmX16tWuYyNHjmTnzp1MmjSJr776ipMnT7rO3XjjjVxyySV1tg9qfh01xNdff02nTp3o0aMH48aNw8/Pr9Zgob6cTqfrObRarWRkZDB79mzCw8O5/PLLq5Wv6fn3JoivctFFF5GVlVVr8DxhwgR27tzp9jsAWLFiBcHBwYwdO9Z1rLF+b6e79NJLcTgc1XJ0fvjhh2o9E4qisGHDBoYMGYKPj4/H+vR6PZdccgnbt2+nsLDQdfzU34HdbsdisXDs2DFmzJhBeXm5K4enPpr6deOtTp06cf/99/Pbb7+xZs0afvjhB9avX8/s2bMJDg4+6+0R5xYZ0joLqt5gqhQXF7Nlyxbefvtt+vbt6/qGXqWmHJXbbruNmTNnApXdtBdffHGt923bti1Q2UvSrVs31/FT21JWVsbevXuZM2cOsbGxNebi1Obpp5/m6aefrnbc19eXnTt31nn9qe0xm80cOHCAf/3rXwQEBFTrFr/zzjs91tGpUydWrVpVZ9mgoCDGjBnDY4895vFb8anS09Nr/F2cXg6gdevWtZZr27Ytq1evpri4mKCgIB588EFKS0v56quvXImk0dHRjBgxgjvvvJMOHTq4XV/f11F9FRYWsmbNGh555BEAfHx8uOKKK/j222+ZPn16jR+s9bFixQpWrFjhdkylUjF37txq+TO1Pf+PP/44d999t1f3DA8PByp7Zmr6HV177bW8+uqrrFy50i3HaOXKlVx99dVuuXP1/b15Kzw8nMTERLdhrfT0dHbv3s0rr7zC22+/7SpbVFREWVmZV685p9NJZmYmISEhAGzdurXa86pSqejcuTNvvPEGo0aNqle7z8brpj6mTJnCL7/8wpw5czCbzdx8882MGDHirLZBnJsk4DkLPL3BqNVqhg4dyvPPP1+tV+Crr77yWM+pCZ1OpxOttvZfn0ajcZWtUtOHSO/evXn++efrnbAMcP/993sMlKruXxdP7enUqROLFi2qNpNq1qxZHst7andVWUVRWL16Ne+++y6TJk3igQce8KpdERERbh8ypzo1H6Tq+T09kfZ0p/8+9Ho9zz//PA888AC///47mzZtYvPmzXz++ecsX76c+fPnM27cONf19X0d1dd3332Hw+Fg5MiRrlyRsWPH8uWXX/LDDz+4knbPxKhRo1zDfk6nk4KCAn788UceffRRTCYTN910k6tsbc9/VX6GN6qe79qen9DQUEaNGuUW8Kxbt478/Hy34Syo/++tPq644gpefPFFysrK8Pf35/vvv6d79+6uLy+nq+9rDir/3mbNmgVATk4Or7/+Ojabjddff71BwdrZeN3Uh1arZc6cOUyYMIGoqCieeOKJs3p/ce6SgOcsOPUNRqVSYTAYiImJ8Tj9FP7Kp6lN69at68xvqepqb9WqlevY6R8ier2e6OjoM8qjaN26tVdtrsmpAZ5OpyMiIsItuDtV+/btvb7XqWV79+6NTqdj0aJFGAwGt0Tomuj1+hrvdeo3/qpv2d78Pvz8/Kp1rUdERHDDDTe4Plg3bdrEY489xnPPPccll1zi6omq7+uovpYvX46iKB6Hlj777LNG+eAKDg6u9pyOHDmSnJwc5s6dy4QJE1wf0rU9//WRnZ0NUOfsnAkTJnDvvfeyf/9+unfvzooVK+jZs2e13Jkq3v7e6mPs2LE8//zzrtlaP/74I1dffXW1ciEhIfj6+pKWllZrfVXvAacGiH5+fm7Pa+/evbnmmmu46667WL58uceZarU5G6+b+kpISCAyMpLExET8/PzO+v3FuUlyeM6CqjeYnj170qNHDzp16nTGH1KjR49m7969tX7I/vTTT8TExLgNZ1V9iFT9S0hIaNKkUW+c2p4uXbrUGOycqX/84x906dKFBQsWcOjQoUarNywsjD59+vDzzz+75VmdqqysjA0bNjB69GgAdu/ezdChQ11ryZxq8ODB3H333eTn57vlXjTF66jK/v37OXDgANOmTePDDz90+zdp0iT27NnjVS5YQ/Xo0YOSkhK3x9tY/vjjD9q2bVtnwDN8+HAiIyNZtWoVJSUlrFmzplrvTkN+b/VRtU7UTz/9xPHjxzlw4ABXXHFFtXIqlYpRo0axbt06ysvLPdblcDj49ddf6devX61BTHh4ODNnziQzM5PZs2fXq73N/boRoj4k4DlPTZo0CX9/f2bMmIHZbK52/pNPPmHLli3ce++9Dfqm2RJptVqee+457HY7L774YqPWff/995OSksL8+fOrnXM4HDz77LOYzWamTJkCQLt27TCZTHz44Yceg6SUlBQiIiLq/W27ob7++msMBgN33HEHgwYNcvt39913o1ar+fTTT5vs/nv37iUoKMiVZ9JYfvvtN/bu3Vvj4pen0mg0jB8/np9//pk1a9ag0Wi46qqr3Mqcjd9b1Wytr776iv79+9c4MeHee+/FZDIxc+ZMj0n78+fPJzU1lf/7v/+r856XXXYZw4cPZ9WqVdUWJqxNc79uhKgPGdI6B+3atavGc+3btycoKIjIyEjeeOMNpk2bxvXXX8/tt99OfHw8xcXF/Pjjj3z//ffcdtttXr3R12bZsmXVjgUGBrqtlHrixIka2xwUFOTVbChvHTlyxOM0fKgcYqgribNv375cc801fPvtt/z4448eu+EbYvjw4Tz55JO88sorJCcnM2HCBCIjI0lLS+PTTz8lOTmZ2bNnu4ZHgoKCeOKJJ3j22We59dZbuemmm2jTpg2lpaX897//5ZtvvmHevHmNOnW+JlarlVWrVjFy5EiPPUYxMTEMHDiQlStX8vjjj7uOb9iwwW1dmCqXX355jb0pBQUFbq8Vk8nEihUr2LhxI4888ohb3pfVaq31byEhIcGVEHtqWafTSUlJCdu2bePDDz9k0KBBTJw4sbanwOX6669n8eLFvP3221x22WXVno/6/t6ysrLIysqiW7du1VYe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CCGEEKLFk4BHCCGEEC2eBDxCCCGEaPEk4BFCCCFEiycBjxBCCCFaPAl4hBBCCNHiScAjhBBCiBZPAh4hhBBCtHgS8AghhBCixZOARwghhBAtXrMHPIqisGDBAoYPH06fPn245557OHnyZI3lCwsLmT59OomJiQwcOJBZs2ZhMpncyowbN46EhAS3f08++WRTPxQhhBBCnKO0zd2At956i08++YSXXnqJ6Oho5s6dy5QpU1i5ciV6vb5a+WnTpmEymVi2bBklJSU8/fTTVFRU8PLLLwNQUVHByZMnWbx4Md27d3ddZzQaz9pjEkIIIcS5pVl7eKxWK++99x7Tpk1j5MiRdOnShddee42srCx++eWXauV37tzJli1bePnll+nevTtDhgzh+eef59tvvyU7OxuAI0eOoCgKffv2JSIiwvUvICDgbD88IYQQQpwjmjXgOXDgAOXl5QwZMsR1LDAwkG7durF169Zq5bdt20ZERATx8fGuYwMHDkSlUrF9+3YADh48SHh4OEFBQU3/AIQQQghxXmjWIa2srCwAYmJi3I5HRka6zp0qOzu7Wlm9Xk9wcDCZmZlAZcDj6+vLtGnT2LFjByEhIUyYMIHbb78dtbrm+G7MmDE1nsvMzKx2XyGEEEKcP5q1h6cq2fj0XB2DwYDFYvFY3lNez6nlDx8+TElJCZdeeilLly7llltu4Y033mDhwoVN8AiEEEIIcT5o1h6eqkRiq9XqllRssVjw8fHxWN5qtVY7brFY8PX1BeCdd97BYrG4cnYSEhIoKyvj7bff5oEHHqixl2f16tU1trO23h8hhBBCnPuatYenapgoJyfH7XhOTg5RUVHVykdHR1cra7VaKSoqIjIyEqjsLTo9Qblz585UVFRQXFzcmM0XQgghxHmiWQOeLl264O/vz+bNm13HSkpKSEpKIjExsVr5xMREsrKySE1NdR3bsmULAP3798fpdHLJJZewaNEit+v27t1LREQEISEhTfRIhBBCCHEua9YhLb1ez8SJE5k3bx6hoaG0bt2auXPnEh0dzbhx43A4HBQUFBAQEIDRaKR3797069ePhx9+mOeee46KigpmzpzJdddd5+oRGjt2LEuXLqVDhw706NGDjRs38u677/L0008350MVQgghRDNSOZ1OZ3M2wOFwMH/+fJYvX47ZbCYxMZGZM2cSGxtLWloaY8aM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
"
class="
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>No Correlation Is Obvious! Surprise – buying more hospital beds is not obviously improving mortality.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div>
</body>







</html>

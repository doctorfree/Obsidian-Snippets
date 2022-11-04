# custom-checkboxes

```css
.markdown-preview-view .task-list-item-checkbox:hover,input[type=checkbox]:hover {
	filter: none;
	filter: brightness(1.1);
	transition: filter 240ms cubic-bezier(0, 0, 0.3, 1);
}

input[type=checkbox]:checked {
	display: inline-block;
	background: #8c8d3b;
	filter: saturate(1);
	border-color: transparent !important;
	width: 1rem;
	height: 1rem;
}

input[type=checkbox]:checked:before {
	content: ' ';
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(36, 20%, 95.1%)' viewBox='0 0 14 14'%3E%3Cpolygon points='5.5 11.9993304 14 3.49933039 12.5 2 5.5 8.99933039 1.5 4.9968652 0 6.49933039'%3E%3C/polygon%3E%3C/svg%3E");
	background-repeat: no-repeat;
	background-position: center center;
	background-size: 75%;
	transform: translateX(0px) translateY(1px);
	width: 100%;
	height: 100%;
	display: block;
}

input[type=checkbox]:checked:active,input[type=checkbox]:checked:hover {
	filter: brightness(1.1);
	transition: filter 240ms cubic-bezier(0, 0, 0.3, 1);
}

.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task]:is([data-task="x"]),
.markdown-preview-view ul > li[data-task='x'] {
	text-decoration:none;
	color: var(--text-faint) !important;
}

/* ──────────────────────────── Custom Checkboxes ─────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="1"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="B"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="X"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="n"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="⭐"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="a"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="p"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="c"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="W"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="❤"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="s"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="S"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="b"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="I"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="!"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="-"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task=">"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="?"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="<"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="l"],
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="i"],
.markdown-preview-view li[data-task="1"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="B"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="X"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="n"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="⭐"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="a"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="p"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="c"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="W"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="❤"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="s"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="S"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="b"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="I"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="!"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="-"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task=">"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="?"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="<"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="l"] .task-list-item-checkbox:checked,
.markdown-preview-view li[data-task="i"] .task-list-item-checkbox:checked {
	background-color: transparent !important;
	pointer-events: none;
}

.markdown-source-view.mod-cm6 .task-list-item-checkbox {
	transform: translateY(-1px);
}
/* ────────────────────────────────── Note ────────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="n"]:before,
.markdown-preview-view li[data-task="n"] .task-list-item-checkbox:checked::before {
	content: "📜";
	background: transparent;
	font-size: 1rem;
	transform: scale(0.85) translateY(-5px) translateX(-4px);
	color: var(--background-primary);
}

/* ────────────────────────────────── Star ────────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="⭐"]:before,
.markdown-preview-view li[data-task="⭐"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(41, 68.5%, 49.8%)' viewBox='0 0 32 32'%3E%3Cpath d='m16 2-4.55 9.22-10.17 1.47 7.36 7.18L6.9 30l9.1-4.78L25.1 30l-1.74-10.13 7.36-7.17-10.17-1.48Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-3px);
	padding: 2px;
}

/* ────────────────────────────────── Alarm ───────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="a"]:before,
.markdown-preview-view li[data-task="a"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(41, 68.5%, 49.8%)' viewBox='0 0 32 32'%3E%3Cpath d='M28.707 19.293 26 16.586V13a10.014 10.014 0 0 0-9-9.95V1h-2v2.05A10.014 10.014 0 0 0 6 13v3.586l-2.707 2.707A1 1 0 0 0 3 20v3a1 1 0 0 0 1 1h7v1a5 5 0 0 0 10 0v-1h7a1 1 0 0 0 1-1v-3a1 1 0 0 0-.293-.707ZM19 25a3 3 0 0 1-6 0v-1h6Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-3px);
	padding: 2px;
}

/* ────────────────────────────────── Pros ────────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="p"]:before,
.markdown-preview-view li[data-task="p"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(60.7, 41%, 39.2%)' viewBox='0 0 32 32'%3E%3Cpath d='M2 16h5v14H2zM23 30H9V15.197l3.042-4.563.845-5.917A2.01 2.01 0 0 1 14.867 3H15a3.003 3.003 0 0 1 3 3v6h8a4.005 4.005 0 0 1 4 4v7a7.008 7.008 0 0 1-7 7Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-3px);
	padding: 2px;
}

/* ────────────────────────────────── Cons ────────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="c"]:before,
.markdown-preview-view li[data-task="c"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(3.2, 85.8%, 61.4%)' viewBox='0 0 32 32'%3E%3Cpath d='M2 2h5v14H2zM23 2H9v14.803l3.042 4.563.845 5.917A2.01 2.01 0 0 0 14.867 29H15a3.003 3.003 0 0 0 3-3v-6h8a4.005 4.005 0 0 0 4-4V9a7.008 7.008 0 0 0-7-7Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-1.5px);
	padding: 2px;
}

/* ───────────────────────── Win / Success / Reward ───────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="W"]:before,
.markdown-preview-view li[data-task="W"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(41, 68.5%, 49.8%)' viewBox='0 0 32 32'%3E%3Cpath d='M26 7h-2V6a2.002 2.002 0 0 0-2-2H10a2.002 2.002 0 0 0-2 2v1H6a2.002 2.002 0 0 0-2 2v3a4.005 4.005 0 0 0 4 4h.322A8.169 8.169 0 0 0 15 21.934V26h-5v2h12v-2h-5v-4.069A7.966 7.966 0 0 0 23.74 16H24a4.005 4.005 0 0 0 4-4V9a2.002 2.002 0 0 0-2-2ZM8 14a2.002 2.002 0 0 1-2-2V9h2Zm18-2a2.002 2.002 0 0 1-2 2V9h2Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.2) translateX(-2px) translateY(-1px);
	padding: 2px;
}

/* ────────────────────────────────── Heart ───────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="❤"]:before,
.markdown-preview-view li[data-task="❤"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(3.2, 85.8%, 61.4%)' enable-background='new 0 0 32 32' viewBox='0 0 32 32' xml:space='preserve'%3E%3Cpath d='M22.5 4c-2 0-3.9.8-5.3 2.2L16 7.4l-1.1-1.1c-2.9-3-7.7-3-10.6-.1l-.1.1c-3 3-3 7.8 0 10.8L16 29l11.8-11.9c3-3 3-7.8 0-10.8C26.4 4.8 24.5 4 22.5 4z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-1px) translateY(-1px);
	padding-left: 2px;
}

/* ───────────────────────────────── Savings ──────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="s"]:before,
.markdown-preview-view li[data-task="s"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(41, 68.5%, 49.8%)' enable-background='new 0 0 32 32' viewBox='0 0 32 32' xml:space='preserve'%3E%3Cpath fill='none' d='M0 0h32v32H0V0z'/%3E%3Cpath d='M29 13h-2c-.1-1.6-.8-3.1-2-4.1V5c0-.6-.4-1-1-1-.2 0-.4.1-.6.2L19.7 7H15c-5.5 0-9.5 3.2-9.9 8H5c-.6 0-1-.4-1-1v-2H2v2c0 1.7 1.3 3 3 3h.1c.3 2.7 1.7 5 3.9 6.6V27c0 .6.4 1 1 1h4c.6 0 1-.4 1-1v-2h3v2c0 .6.4 1 1 1h4c.6 0 1-.4 1-1v-3.4c1.5-.7 2.5-2 2.8-3.6H29c.6 0 1-.4 1-1v-5c0-.6-.4-1-1-1zm-11 7v1h-2v-1h-2v-2h3.5c.3 0 .5-.2.5-.5s-.2-.5-.5-.5h-1c-1.2 0-2.3-.8-2.5-2-.2-1.3.6-2.6 2-2.9V11h2v1h2v2h-3.5c-.3 0-.5.3-.5.6s.2.5.5.5h1c1.2 0 2.3.8 2.5 2 .2 1.3-.6 2.6-2 2.9z'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.2) translateX(-1px) translateY(-.5px);
	padding-left: 2px;
}

/* ─────────────────────────── Savings alternative ────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="S"]:before,
.markdown-preview-view li[data-task="S"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(41, 68.5%, 49.8%)' enable-background='new 0 0 32 32' viewBox='0 0 32 32' xml:space='preserve'%3E%3Cpath fill='none' d='M0 0h32v32H0V0z'/%3E%3Cpath d='M29 13h-2c-.1-1.6-.8-3.1-2-4.1V5c0-.6-.4-1-1-1-.2 0-.4.1-.6.2L19.7 7H15c-5.5 0-9.5 3.2-9.9 8H5c-.6 0-1-.4-1-1v-2H2v2c0 1.7 1.3 3 3 3h.1c.3 2.7 1.7 5 3.9 6.6V27c0 .6.4 1 1 1h4c.6 0 1-.4 1-1v-2h3v2c0 .6.4 1 1 1h4c.6 0 1-.4 1-1v-3.4c1.5-.7 2.5-2 2.8-3.6H29c.6 0 1-.4 1-1v-5c0-.6-.4-1-1-1zm-9 0h-7v-2h7v2z'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.2) translateX(-1px) translateY(-.5px);
	padding-left: 2px;
}

/* ────────────────────────── Bookmark / Reference ────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="b"]:before,
.markdown-preview-view li[data-task="b"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(3.2, 85.8%, 61.4%)' viewBox='0 0 32 32'%3E%3Cpath d='M24 2H8a2 2 0 0 0-2 2v26l10-5.054L26 30V4a2 2 0 0 0-2-2Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-1px) translateY(-1px);
	padding-left: 2px;
}

/* ──────────────────────────── Idea / Lightbulb ──────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="I"]:before,
.markdown-preview-view li[data-task="I"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(41, 68.5%, 49.8%)' enable-background='new 0 0 32 32' viewBox='0 0 32 32' xml:space='preserve'%3E%3Cpath d='M11 22h10v4H11v-4zm2 4h6v4h-6v-4zm8-4c0-.9.5-1.5 1.5-2.4 2.3-1.8 3.6-4.7 3.5-7.6 0-5.5-4.5-10-10-10S6 6.5 6 12c-.1 2.9 1.1 5.8 3.5 7.6 1 .9 1.5 1.5 1.5 2.4'/%3E%3Cpath fill='none' d='M0 0h32v32H0V0z'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(0px) translateY(-2px);
	padding-left: 2px;
}

/* ───────────────────────────────── Failure ──────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="X"]:before,
.markdown-preview-view li[data-task="X"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(3.2, 85.8%, 61.4%)' width='32' height='32' enable-background='new 0 0 32 32' xml:space='preserve'%3E%3Cpath fill='none' d='M0 0h32v32H0z'/%3E%3Cpath d='M16 2C8.3 2 2 8.3 2 16s6.3 14 14 14 14-6.3 14-14S23.7 2 16 2zm5.4 21L16 17.6 10.6 23 9 21.4l5.4-5.4L9 10.6 10.6 9l5.4 5.4L21.4 9l1.6 1.6-5.4 5.4 5.4 5.4-1.6 1.6z'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-1.5px);
	padding: 2px;
}

/* ─────────────────────────────────── Bug ────────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="B"]:before,
.markdown-preview-view li[data-task="B"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(350.5, 79.1%, 62.5%)' enable-background='new 0 0 32 32' viewBox='0 0 32 32' xml:space='preserve'%3E%3Cpath fill='none' d='M0 0h32v32H0z'/%3E%3Cpath d='m16 11 8-2.1c-.9-1.7-2.3-3-4-3.9V2h-2v2.2c-1.3-.3-2.7-.3-4 0V2h-2v3c-1.7.9-3.1 2.2-4 3.9l8 2.1z'/%3E%3Cpath d='m29.8 20 .3-2-5.1-.8v-4.4l5.1-1.4-.5-1.9-4.8 1.3-7.8 2V17h-2v-4.2l-7.7-2.1-4.8-1.2-.5 1.9 5 1.4v4.4l-5.2.8.3 2 4.9-.8c0 1.2.3 2.4.8 3.6l-4.5 4.5 1.4 1.4 4.2-4.2c3.1 3.9 8.7 4.6 12.6 1.6.6-.5 1.1-1 1.6-1.6l4.2 4.2 1.4-1.4-4.5-4.5c.5-1.1.8-2.3.8-3.6l4.8.8z'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-2px);
	padding: 2px;
}

/* ───────────────────────────────── Success ──────────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="1"]:before,
.markdown-preview-view li[data-task="1"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(60.7, 41%, 39.2%)' id='icon' viewBox='0 0 32 32'%3E%3Cdefs%3E%3Cstyle%3E.cls-1%7Bfill:none%7D%3C/style%3E%3C/defs%3E%3Cpath d='M16 2a14 14 0 1 0 14 14A14 14 0 0 0 16 2Zm-2 19.59-5-5L10.59 15 14 18.41 21.41 11l1.596 1.586Z'/%3E%3Cpath id='inner-path' d='m14 21.591-5-5L10.591 15 14 18.409 21.41 11l1.595 1.585L14 21.591z' class='cls-1'/%3E%3Cpath id='_Transparent_Rectangle_' d='M0 0h32v32H0z' class='cls-1' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-1.5px);
	padding: 2px;
}

/* ─────────────────────────── Scheduled ('- [<]') ────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="<"]:before,
.markdown-preview-view li[data-task="<"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(340, 1.9%, 30.4%)' viewBox='0 0 32 32'%3E%3Cpath d='M26 4h-4V2h-2v2h-8V2h-2v2H6a2.002 2.002 0 0 0-2 2v20a2.002 2.002 0 0 0 2 2h20a2.002 2.002 0 0 0 2-2V6a2.002 2.002 0 0 0-2-2ZM6 6h4v2h2V6h8v2h2V6h4v4H6Zm0 6h5v6H6Zm13 14h-6v-6h6Zm0-8h-6v-6h6Zm2 8v-6h5l.001 6Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(0px) translateY(-1px);
	padding-left: 2px;
}

.theme-dark .markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="<"]:before,
.theme-dark .markdown-preview-view li[data-task="<"] > .task-list-item-checkbox:checked::before {
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(24, 4.4%, 77.8%)' viewBox='0 0 32 32'%3E%3Cpath d='M26 4h-4V2h-2v2h-8V2h-2v2H6a2.002 2.002 0 0 0-2 2v20a2.002 2.002 0 0 0 2 2h20a2.002 2.002 0 0 0 2-2V6a2.002 2.002 0 0 0-2-2ZM6 6h4v2h2V6h8v2h2V6h4v4H6Zm0 6h5v6H6Zm13 14h-6v-6h6Zm0-8h-6v-6h6Zm2 8v-6h5l.001 6Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
}

/* ─────────────────────────── Location ('- [l]') ─────────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="l"]:before,
.markdown-preview-view li[data-task="l"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' id='icon' fill='hsl(3.2, 85.8%, 61.4%)' viewBox='0 0 32 32'%3E%3Cdefs%3E%3Cstyle%3E.cls-1%7Bfill:none%7D%3C/style%3E%3C/defs%3E%3Cpath d='M16 2A11.013 11.013 0 0 0 5 13a10.889 10.889 0 0 0 2.216 6.6s.3.395.349.452L16 30l8.439-9.953c.044-.053.345-.447.345-.447l.001-.003A10.885 10.885 0 0 0 27 13 11.013 11.013 0 0 0 16 2Zm0 15a4 4 0 1 1 4-4 4.005 4.005 0 0 1-4 4Z'/%3E%3Ccircle id='_Inner-Path_' cx='16' cy='13' r='4' class='cls-1' data-name='&lt;Inner-Path&gt;'/%3E%3Cpath id='_Transparent_Rectangle_' d='M0 0h32v32H0z' class='cls-1' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-3.5px);
	color: var(--background-primary);
	padding: 2px;
}

/* ────────────────────────── Information ('- [i]') ───────────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="i"]:before,
.markdown-preview-view li[data-task="i"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' id='icon' fill='hsl(201.9, 25.9%, 52.4%)' viewBox='0 0 32 32'%3E%3Cdefs%3E%3Cstyle%3E.cls-1%7Bfill:none%7D%3C/style%3E%3C/defs%3E%3Cpath id='inner-path' d='M16 8a1.5 1.5 0 1 1-1.5 1.5A1.5 1.5 0 0 1 16 8Zm4 13.875h-2.875v-8H13v2.25h1.875v5.75H12v2.25h8Z' class='cls-1'/%3E%3Cpath d='M16 2a14 14 0 1 0 14 14A14 14 0 0 0 16 2Zm0 6a1.5 1.5 0 1 1-1.5 1.5A1.5 1.5 0 0 1 16 8Zm4 16.125h-8v-2.25h2.875v-5.75H13v-2.25h4.125v8H20Z'/%3E%3Cpath id='_Transparent_Rectangle_' d='M0 0h32v32H0z' class='cls-1' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(-2px) translateY(-1.5px);
	padding: 2px;
	color: var(--background-primary);
}

/* ─────────────── Icon for question/more info task ('- [?]') ─────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="?"]:before,
.markdown-preview-view li[data-task="?"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-color: none;
	background-size: 16px 16px;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' id='icon' fill='hsl(41, 68.5%, 49.8%)' viewBox='0 0 32 32'%3E%3Cdefs%3E%3Cstyle%3E.cls-1%7Bfill:none%7D%3C/style%3E%3C/defs%3E%3Cpath d='M16 2a14 14 0 1 0 14 14A14 14 0 0 0 16 2Zm0 23a1.5 1.5 0 1 1 1.5-1.5A1.5 1.5 0 0 1 16 25Zm1.142-7.754v2.501h-2.25V15h2.125a2.376 2.376 0 0 0 0-4.753h-1.5a2.378 2.378 0 0 0-2.375 2.375v.638h-2.25v-.638A4.628 4.628 0 0 1 15.517 8h1.5a4.624 4.624 0 0 1 .125 9.246Z'/%3E%3Cpath id='inner-path' d='M16 25a1.5 1.5 0 1 1 1.5-1.5A1.5 1.5 0 0 1 16 25Zm1.142-7.754v2.501h-2.25V15h2.125a2.376 2.376 0 0 0 0-4.753h-1.5a2.378 2.378 0 0 0-2.375 2.375v.638h-2.25v-.638A4.628 4.628 0 0 1 15.517 8h1.5a4.624 4.624 0 0 1 .125 9.246Z' class='cls-1'/%3E%3Cpath id='_Transparent_Rectangle_' d='M0 0h32v32H0z' class='cls-1' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	transform: scale(1.1) translateX(-2px) translateY(-1.5px);
	padding: 2px;
}

/* ─────────── Paper Plane icon for deferred/rescheduled ('- [>]') ────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task=">"]:before,
.markdown-preview-view li[data-task=">"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(340, 1.9%, 30.4%)' viewBox='0 0 32 32'%3E%3Cpath d='m27.45 15.11-22-11a1 1 0 0 0-1.08.12 1 1 0 0 0-.33 1L6.69 15H18v2H6.69L4 26.74A1 1 0 0 0 5 28a1 1 0 0 0 .45-.11l22-11a1 1 0 0 0 0-1.78Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
	background-size: 16px 16px;
	transform: scale(1.1) translateX(0.5px) translateY(-1.5px);
	padding-left: 0;
	color: var(--background-primary);
}
.theme-dark .markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task=">"]:before,
.theme-dark .markdown-preview-view li[data-task=">"] .task-list-item-checkbox:checked::before {
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='hsl(24, 4.4%, 77.8%)' viewBox='0 0 32 32'%3E%3Cpath d='m27.45 15.11-22-11a1 1 0 0 0-1.08.12 1 1 0 0 0-.33 1L6.69 15H18v2H6.69L4 26.74A1 1 0 0 0 5 28a1 1 0 0 0 .45-.11l22-11a1 1 0 0 0 0-1.78Z'/%3E%3Cpath fill='none' d='M0 0h32v32H0z' data-name='&lt;Transparent Rectangle&gt;'/%3E%3C/svg%3E");
}

/* ──────────────────── '!' for important task ('- [!]') ──────────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="!"]:before,
.markdown-preview-view li[data-task="!"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-size: 16px 16px;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' id='icon' x='0' y='0' fill='hsl(3.2, 85.8%, 61.4%)' enable-background='new 0 0 32 32' version='1.1' viewBox='0 0 32 32' xml:space='preserve'%3E%3Cstyle%3E.st0%7Bfill:none%7D%3C/style%3E%3Cpath id='inner-path' d='M16 26c-.8 0-1.5-.7-1.5-1.5S15.2 23 16 23s1.5.7 1.5 1.5S16.8 26 16 26zm-1.1-5h2.2v-9h-2.2v9z' class='st0'/%3E%3Cpath d='M16 6.2 4.6 28h22.7L16 6.2zM14.9 12h2.2v9h-2.2v-9zM16 26c-.8 0-1.5-.7-1.5-1.5S15.2 23 16 23s1.5.7 1.5 1.5S16.8 26 16 26z'/%3E%3Cpath d='M29 30H3c-.6 0-1-.4-1-1 0-.2 0-.3.1-.5l13-25c.3-.5.9-.6 1.4-.4.2.1.3.2.4.4l13 25c.3.5.1 1.1-.4 1.3-.2.2-.3.2-.5.2zM4.7 28h22.7L16 6.2 4.7 28z'/%3E%3Cpath id='_Transparent_Rectangle_' d='M0 0h32v32H0z' class='st0'/%3E%3Cpath d='M-2.9 15.3h26.4v2.9H-2.9z' transform='rotate(-62.979 10.321 16.712)'/%3E%3Cpath d='M8.3 15.6h26.4v2.9H8.3z' transform='rotate(-117.021 21.471 17.086)'/%3E%3Cpath d='M3.9 26.2h24.4v2.9H3.9z' transform='matrix(-.9999 -.01155 .01155 -.9999 31.881 55.41)'/%3E%3C/svg%3E");
	transform: scale(1.1) translateX(-2px) translateY(-2.5px);
	padding: 2px;
}

/* ────────────────── Icon for cancelled/non-task ('- [-]') ───────────────── */
.markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="-"]:before,
.markdown-preview-view li[data-task="-"] .task-list-item-checkbox:checked::before {
	content: "";
	background-repeat: no-repeat;
	background-size: 16px 16px;
	background-image: url("data:image/svg+xml,%3C%3Fxml version='1.0' encoding='utf-8'%3F%3E%3Csvg version='1.1' fill='hsl(24, 4.4%, 77.8%)' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' viewBox='0 0 32 32' style='enable-background:new 0 0 32 32;' xml:space='preserve'%3E%3Cstyle type='text/css'%3E .st0%7Bfill:none;%7D%0A%3C/style%3E%3Cg id='icon'%3E%3Crect id='_Transparent_Rectangle_' class='st0' width='32' height='32'/%3E%3Crect id='_Transparent_Rectangle__1_' x='0.2' y='-0.4' class='st0' width='32' height='32'/%3E%3C/g%3E%3Cg id='Layer_2'%3E%3Cpath d='M16,2C8.3,2,2,8.3,2,16s6.3,14,14,14s14-6.3,14-14S23.7,2,16,2z M24,17.6h-2.8h-10H8v-4h3.2h10H24V17.6z'/%3E%3C/g%3E%3C/svg%3E%0A");
	transform: scale(1.1) translateX(-2px) translateY(-1.5px);
	padding: 2px;
}
.theme-light .markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task="-"]:before,
.theme-light .markdown-preview-view li[data-task="-"] .task-list-item-checkbox:checked::before {
	background-image: url("data:image/svg+xml,%3C%3Fxml version='1.0' encoding='utf-8'%3F%3E%3Csvg version='1.1' fill='hsl(340, 1.9%, 30.4%)' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' viewBox='0 0 32 32' style='enable-background:new 0 0 32 32;' xml:space='preserve'%3E%3Cstyle type='text/css'%3E .st0%7Bfill:none;%7D%0A%3C/style%3E%3Cg id='icon'%3E%3Crect id='_Transparent_Rectangle_' class='st0' width='32' height='32'/%3E%3Crect id='_Transparent_Rectangle__1_' x='0.2' y='-0.4' class='st0' width='32' height='32'/%3E%3C/g%3E%3Cg id='Layer_2'%3E%3Cpath d='M16,2C8.3,2,2,8.3,2,16s6.3,14,14,14s14-6.3,14-14S23.7,2,16,2z M24,17.6h-2.8h-10H8v-4h3.2h10H24V17.6z'/%3E%3C/g%3E%3C/svg%3E%0A");
}

.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task]:is([data-task="-"]),
.markdown-preview-view ul li[data-task="-"].task-list-item.is-checked {
	color: var(--text-faint);
	text-decoration: line-through solid var(--text-faint) 2px;
}
```


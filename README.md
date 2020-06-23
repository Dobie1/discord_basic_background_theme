# discord_basic_background_theme

@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BetterDocsBlock.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/ThemeDevBadge.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BlurpleRecolor/BlurpleRecolor.css);

:root {
	--dtransparencyalpha:			0,0,0;
	--dgeneraltransparency:			0.15;
	--dmessagetransparency:			0.5;
	--dguildchanneltransparency:	0.15;
	--dmemberlisttransparency:		0.0;
	--daccentcolor:					190,78,180;
	
	--dfont:						Whitney, Helvetica Neue, Helvetica, Arial, sans-serif;
	--dtextshadow:					transparent;
	
	--dbackground:					url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BasicBackground/background.jpg);
	--dbackgroundsize:				cover;
	--dblur:						0px;
	--dbackdrop:					rgba(0,0,0,0.85);

	--vtransparencycolor:			var(--transparencycolor,			var(--dtransparencycolor));
	--vtransparencyalpha:			var(--transparencyalpha,			var(--dtransparencyalpha));
	--vmessagetransparency:			var(--messagetransparency,			var(--dmessagetransparency));
	--vusechatbubbles: 				calc(var(--vmessagetransparency) / (var(--vmessagetransparency) + 0.00000000000000000000001));
	--vguildchanneltransparency:	var(--guildchanneltransparency,		var(--dguildchanneltransparency));
	--vmemberlisttransparency:		var(--memberlisttransparency,		var(--dmemberlisttransparency));
	--vaccentcolor:					var(--accentcolor,					var(--daccentcolor));
	--vlinkcolor:					var(--vaccentcolor);
	
	--vfont:						var(--font,							var(--dfont));
	--vtextshadow:					var(--textshadow,					var(--dtextshadow));
	
	--vbackground:					var(--background,					var(--dbackground));
	--vbackgroundsize:				var(--backgroundsize,				var(--dbackgroundsize));
	--vbackgroundblur:				var(--backgroundblur,				var(--dblur));
	
	--vpopout:						var(--popout,						var(--vbackground));
	--vpopoutsize:					var(--popoutsize,					var(--vbackgroundsize));
	--vpopoutblur:					var(--popoutblur,					var(--vbackgroundblur));
	
	--vbackdrop:					var(--backdrop,						var(--dbackdrop));
	--vbackdropsize:				var(--backdropsize,					var(--vbackgroundsize));
	--vbackdropblur:				var(--backdropblur,					var(--vbackgroundblur));

	--fontwhite1: 					255,255,255;
	--fontwhite2: 					210,210,210;
	--fontwhite3: 					170,170,170;
	--fontwhite4: 					120,120,120;
}

.theme-light, .theme-dark {
	--header-primary: rgb(var(--fontwhite1));
	--header-secondary: rgb(var(--fontwhite2));
	--text-normal: rgb(var(--fontwhite2));
	--text-muted: rgb(var(--fontwhite4));
	--text-link: rgb(var(--vaccentcolor));
	--channels-default: rgb(var(--fontwhite4));
	--interactive-normal: rgb(var(--fontwhite3));
	--interactive-hover: rgb(var(--fontwhite2));
	--interactive-active: rgb(var(--fontwhite1));
	--interactive-muted: rgb(var(--fontwhite4));
	--elevation-low: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
	--elevation-high: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	--logo-primary: rgb(var(--fontwhite1));
}


/* ~~~~		0.		TABLE OF CONTENTS				~~~~ */
/*
	1.	TRANSPARENCY
	2.	BACKGROUND
	3.	TITLEBAR
	4.	GUILDLIST
	5.	CHANNELLIST
		1.	GUILDHEADER
		2.	CHANNELS
		3.	DMCHANNELS
		4.	ACCOUNT/VOICE/GOLIVE
	6.	CHAT
		1.	CHANNELHEADER
		2.	MESSAGES
			1.	MESSAGE
			2.	EMBEDS
			3.	NITROGIFT
			4.	INVITE
		3.	TEXTAREA
		4.	AUTOCOMPLETEMENU
		5.	MEMBERLIST
		6.	SEARCHPAGE
		7.	CALL
		8.	UNAVAILABLESCREEN
	7.	PEOPLES
	8.	STORE/NITRO
	9.	LIBRARY
	10.	DISCOVERY
	11.	USERSETTINGS
	12.	GUILDSETTINGS
	13.	MODALS
		1.	USERMODAL
		2.	GUILDADD/CREATION
		3.	REGIONSELECTMODAL
		4.	UPLOADMODAL
		5.	KEYBOARDSHORTCUTSMODAL
		6.	QUICKSWITCHER
		7.	INVITEMODAL
		8.	LOGINSCREEN
		9.	TERMACCEPTMODAL
		10.	DOWNLOADAPPMODAL
		11.	GUILDBOOSTMODAL
		12.	NEWUSERMODAL
		13.	REACTIONSMODAL
		14.	GUILDTEMPLATEMODAL
		15.	GUILDWELCOMEMODAL
	14.	POPOUTS
		1.	CONTEXTMENU
		2.	USERPOPOUT
		3.	EMOJIPICKER
		4.	PINS/MENTIONS
		5.	SEARCHPOPOUT
		6.	COLORPICKER
		7.	ADDROLE
		8.	EVERYONEMENTION
		9.	CHANNELFOLLOW
		10.	CHANNELFOLLOWINFO
	15.	GENERAL
		1.	TEXT
		2.	BUTTONS
		3.	INPUTS
		4.	SEARCHBARS
		5.	TAGS
		6.	ICONS
		7.	SCROLLBARS
		8.	NOTIFICATIONBAR
		9.	TOOLTIPS
		10.	TOASTS
	16.	BDSUPPORT
	17.	PLUGINSUPPORT
		1.	DATEVIEWER
		2.	SERVERFOLDERS
		3.	MEMBERCOUNT
		4.	SENDBUTTON
		5.	CHARCOUNTER
		6.	REPLYER
		7.	CITADOR
		8.	LINENUMBERS
		9.	PERMISSIONVIEWER
		10.	BETTERSEARCHPAGE
		11.	REPOCONTROLS
		12.	DIRECTDOWNLOAD
		13.	BETTERFORMATINGREDUX
		14.	PLUGIN/THEMEREPO
		15.	CHANNELHISTORY
		16.	DISPLAYLARGEMESSAGES
	18.	THEMESUPPORT
		1.	THEMEDEVBADGE
		2.	BETTERDOCSBLOCK
	19.	UPDATENOTICE
	20.	WATERMARK
*/


/* ~~~~		1.		TRANSPARENCY					~~~~ */

body,														/* body														*/
#app-mount .app-1q1i1E,										/* app					container							*/
#app-mount .app-2rEoOp,										/* app					inner								*/
#app-mount .container-16j22k,								/* app					loadingscreen						*/
#app-mount .bg-h5JY_x,										/* app					background							*/
#app-mount .layer-3QrUeG,									/* layer				container							*/
#app-mount .container-PNkimc,								/* channels				inner								*/
#app-mount .privateChannels-1nO12o,							/* dmchannels												*/
#app-mount .panels-j1Uci_ > *,								/* account/voice		inner								*/
#app-mount .chat-3bRxxu,									/* chat					container							*/
#app-mount .noChannel-Z1DQK7,								/* nochannel												*/
#app-mount .members-1998pB,									/* members													*/
#app-mount .content-MLh4nU,									/* unavailable												*/
#app-mount .container-1D34oG,								/* peoples													*/
#app-mount .applicationStore-1pNvnv,						/* nitro													*/
#app-mount .pageWrapper-1PgVDX,								/* guilddiscovery											*/
#app-mount .scroller-2FKFPG,								/* scroller													*/
#app-mount .standardSidebarView-3F1I7i,						/* settings													*/
#app-mount .scroller-305q3I,								/* settings				sidebar scroller					*/
#app-mount .contentRegion-3nDuYy {							/* settings				content								*/
	background: transparent;
}

#app-mount .sidebarRegion-VFTUkN {							/* settings				sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount {												/* app-mount												*/
	background-color: rgba(var(--vtransparencycolor), var(--vtransparencyalpha));
}
#app-mount .wrapper-1Rf91z {								/* guilds				container							*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 2));
}
#app-mount .sidebar-2K8pFh {								/* channels				container							*/
	background-color: rgba(var(--vtransparencycolor), var(--vguildchanneltransparency));
}
#app-mount .panels-j1Uci_ {									/* account/voice		container							*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) / 1.5));
}
#app-mount .container-1r6BKw.themed-ANHk51 {				/* channelheader		container							*/
	background-color: rgba(var(--vtransparencycolor), var(--vguildchanneltransparency));
}
#app-mount .membersWrap-2h-GB4 {							/* members				container							*/
	background-color: rgba(var(--vtransparencycolor), var(--vmemberlisttransparency));
}
#app-mount .nowPlayingColumn-2sl4cE {						/* peoples				now playing							*/
	background-color: rgba(var(--vtransparencycolor), var(--vmemberlisttransparency));
}

.themeDark-3Ap_7i, .themeLight-2aS1dz {						/* errorscreen												*/
	background-color: transparent;
	color: rgb(var(--fontwhite1));
}
#app-mount .note-450gs3 {
	color: rgb(var(--fontwhite2));
}
#app-mount .image-3zK3Wt {
	background-image: url(https://discordapp.com/assets/e9baf4b505eb54129f832556ea16538e.svg);
	opacity: 0.6;
}


/* ~~~~		2.		BACKGROUND						~~~~ */

body:before {
	content: "";
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	position: fixed;
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
}
#ace_settingsmenu_container,
.uploadArea-3QgLtW,
.backdropWithLayer-3_uhz4,
.backdrop-1wrmKB {
	background: var(--vbackdrop) center/var(--vbackdropsize) !important;
	filter: blur(var(--vbackdropblur));
	opacity: 1;
	animation: none;
}
.backdropWithLayer-3_uhz4 {
	z-index: -1;
}


/* ~~~~		3.		TITLEBAR						~~~~ */

.titleBar-AC4pGV {
	z-index: 1;
}
.titleBar-AC4pGV:after {
	content: "";
	pointer-events: none;
	position: absolute;
	z-index: -1;
	top: 0;
	left: 0;
	width: 100%;
	background-color: rgba(var(--vtransparencycolor), calc(0.1 + var(--vguildchanneltransparency) * 2));
}
.titleBar-AC4pGV:not(.typeMacOS-3EmCyP):after {
	height: 22px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP:after {
	height: 32px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP,
.titleBar-AC4pGV.typeMacOS-3EmCyP .macButtons-2MuSAC {
	width: 72px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP.typeMacOSWithFrame-3R_i5S .macButtons-2MuSAC {
	margin-top: 0;
	margin-right: 0;
}
.winButton-iRh8-Z {
	color: rgb(var(--fontwhite3));
}
.winButtonMinMax-PBQ2gm:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.winButtonClose-1HsbF-:hover,
.winButtonMinMax-PBQ2gm:hover {
	color: rgb(var(--fontwhite1));
}


/* ~~~~		4.		GUILDLIST						~~~~ */

.childWrapper-anI2G9,										/* homebutton/acronym	innerwrap							*/
#bd-pub-button {											/* publicbutton			innerwrap							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
	font-weight: 500;
}
.wrapper-1BJsBx:hover svg,
.wrapper-1BJsBx.selected-bZ3Lue svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.wrapper-1BJsBx:hover .childWrapper-anI2G9,
.wrapper-1BJsBx.selected-bZ3Lue .childWrapper-anI2G9,
#bd-pub-button:hover {
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
.noIcon-1a_FrS {											/* acronym				minicontainer						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}

.circleIconButton-jET_ig {									/* guildadd/discovery	innerwrap							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.circleIconButton-jET_ig.selected-ugP_am {
	color: rgb(var(--fontwhite1));
}

.guildIconUnavailable-5PMHDN,								/* guilderror			miniicon							*/
.guildsError-b7zR5H {										/* guilderror			innerwrap							*/
	background-color: rgba(240, 71, 71, 0.3);
}

.dragInner-_SHftW {											/* dragplaceholder											*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.guildSeparator-3s64Iy {									/* guildseparator											*/
	background-color: rgba(var(--fontwhite1), 0.2);
}

.item-2hkk8m {												/* unread/selectedpill										*/
	background-color: rgb(var(--fontwhite1));
}

.wrapper-21YSNc {											/* folder				outerwrap							*/
	margin-bottom: 8px;
}
.folder-21wGz3 {											/* folder				iconwrap							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.folder-21wGz3.hover-2ji_A7 {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.expandedFolderBackground-2sPsd- {							/* folder				background							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 15px 15px 24px 24px;
	top: 0;
	bottom: 0;
	transition: border-radius 3s ease, background-color 1s ease;
}
.expandedFolderBackground-2sPsd-.hover-2ji_A7 {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.wrapper-1Rf91z .wrapper-21YSNc .expandedGuilds-1JMD4M,
.wrapper-1Rf91z .wrapper-21YSNc [role="group"] {			/* folder				guildwrap							*/
	height: auto !important;
}
.wrapper-1Rf91z .wrapper-21YSNc .expandedGuilds-1JMD4M .listItem-2P_4kh:last-child,
.wrapper-1Rf91z .wrapper-21YSNc [role="group"] .listItem-2P_4kh:last-child {
	margin-bottom: 0;
}

.bar-30k2ka {												/* guild/channelbar		inner								*/
	color: rgb(var(--fontwhite1));
	box-shadow: 0 2px 6px rgba(var(--vtransparencycolor), 0.24);
}
.bar-30k2ka:not(.mention-1f5kbO) {
	overflow: hidden;
	background: transparent;
}
.bar-30k2ka:not(.mention-1f5kbO):after,
.bar-30k2ka:not(.mention-1f5kbO):before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.bar-30k2ka:not(.mention-1f5kbO):after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
}
.sidebar-2K8pFh .bar-30k2ka:not(.mention-1f5kbO):after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + var(--vguildchanneltransparency) * 0.85 + 0.1));
}
.wrapper-1Rf91z .bar-30k2ka:not(.mention-1f5kbO):after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + var(--vguildchanneltransparency) * 1.9 + 0.1));
}
.bar-30k2ka:not(.mention-1f5kbO):before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
	background-attachment: fixed;
}


/* ~~~~		5.		CHANNELLIST						~~~~ */

#app-mount .sidebar-2K8pFh {								/* channels				container							*/
	border-radius: 0;
}

/* ----		5.1.	GUILDHEADER						---- */

.container-2Rl01u .animatedContainer-1pJv5C {				/* banner				wrap								*/
	background: none;
	box-shadow: none;
}
.bannerImage-1jOskm {										/* banner				image								*/
	-webkit-mask: linear-gradient(rgba(0,0,0,0.9) 70%, rgba(0,0,0,0) 100%);
}
.bannerImage-1jOskm:before {
	display: none;
}

.header-2o-2hj,												/* header				inner								*/
.searchBar-6Kv8R2 {											/* header				searchbar							*/
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2), 0 1.5px 0 rgba(var(--vtransparencycolor), 0.05), 0 2px 0 rgba(var(--vtransparencycolor), 0.05);
}
.searchBar-6Kv8R2 .searchBarComponent-32dTOx {				/* header				searchbarinner						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
.header-2o-2hj,
.bannerVisible-14J9lQ .header-2o-2hj {
	color: rgb(var(--fontwhite1));
}
.clickable-2ap7je:not(.hasBanner-14PPlG) .header-2o-2hj:hover,
.selected-WP3kCM:not(.hasBanner-14PPlG) .header-2o-2hj {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.channelNotice-1-XFjC {										/* notice				container							*/
	box-shadow: inset 0 -1px 0 rgba(var(--fontwhite4), 0.3);
}
.close-relY5R {												/* notice				close								*/
	color: rgb(var(--fontwhite3));
}
.close-relY5R:hover {
	color: rgb(var(--fontwhite1));
}
.message-3SOT5P {											/* notice				text								*/
	color: rgb(var(--fontwhite2));
}


/* ----		5.2.	CHANNELS						---- */

.wrapper-CU3qI5 {											/* category				wrapper								*/
	color: rgb(var(--fontwhite3));
}
.wrapper-CU3qI5.muted-1NRuDm {
	color: rgb(var(--fontwhite4));
}
.wrapper-CU3qI5.muted-1NRuDm:hover,
.wrapper-CU3qI5:hover {
	color: rgb(var(--fontwhite1));
}
.wrapper-CU3qI5.muted-1NRuDm:hover .icon-WnO6o2,			/* category				icon								*/
.wrapper-CU3qI5:hover .icon-WnO6o2 {
	color: rgb(var(--fontwhite1));
}
.wrapper-CU3qI5 .name-IbjUBS {								/* category				name								*/
	color: rgb(var(--fontwhite3));
}
.wrapper-CU3qI5.muted-1NRuDm .name-IbjUBS {
	color: rgb(var(--fontwhite4));
}
.wrapper-CU3qI5.muted-1NRuDm:hover .name-IbjUBS,
.wrapper-CU3qI5:hover .name-IbjUBS {
	color: rgb(var(--fontwhite1));
}
.addButtonIcon-3u-3Hu {										/* category				addbutton							*/
	opacity: 0.5;
}
.addButtonIcon-3u-3Hu:hover {
	color: rgb(var(--fontwhite1));
	opacity: 1;
}

.wrapper-1ucjTd:hover .content-3at_AU {						/* channel				content								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.modeSelected-1zApJ_ .content-3at_AU,
.modeSelected-1zApJ_:hover .content-3at_AU {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.modeSelected-1zApJ_ .content-3at_AU svg,
.modeSelected-1zApJ_:hover .content-3at_AU svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.icon-1_QxNX {												/* channel				icon								*/
	color: rgb(var(--fontwhite3));
}
.modeMuted-3osy7j .icon-1_QxNX {
	color: rgb(var(--fontwhite4));
}
.modeConnected-2IEL4z .icon-1_QxNX,
.modeConnected-2IEL4z:hover .icon-1_QxNX,
.modeSelected-1zApJ_ .icon-1_QxNX,
.modeSelected-1zApJ_:hover .icon-1_QxNX,
.modeUnread-1zpFdA .icon-1_QxNX,
.modeUnread-1zpFdA:hover .icon-1_QxNX,
.notInteractive-YF5EXq.modeConnected-2IEL4z .icon-1_QxNX,
.notInteractive-YF5EXq.modeSelected-1zApJ_ .icon-1_QxNX,
.wrapper-1ucjTd:hover .icon-1_QxNX {
	color: rgb(var(--fontwhite1));
}
.name-3_Dsmg {												/* channel				name								*/
	color: rgb(var(--fontwhite3));
}
.modeMuted-3osy7j .name-3_Dsmg {
	color: rgb(var(--fontwhite4));
}
.modeConnected-2IEL4z .name-3_Dsmg,
.modeConnected-2IEL4z:hover .name-3_Dsmg,
.modeSelected-1zApJ_ .name-3_Dsmg,
.modeSelected-1zApJ_:hover .name-3_Dsmg,
.modeUnread-1zpFdA .name-3_Dsmg,
.modeUnread-1zpFdA:hover .name-3_Dsmg,
.notInteractive-YF5EXq.modeConnected-2IEL4z .name-3_Dsmg,
.notInteractive-YF5EXq.modeSelected-1zApJ_ .name-3_Dsmg,
.wrapper-1ucjTd:hover .name-3_Dsmg {
	color: rgb(var(--fontwhite1));
}
.modeSelected-1zApJ_ .actionIcon-2Hi9ZG,
.modeSelected-1zApJ_:hover .actionIcon-2Hi9ZG,
.wrapper-1ucjTd:hover .actionIcon-2Hi9ZG {
	color: rgb(var(--fontwhite1));
}
.actionIcon-2Hi9ZG {
	opacity: 0.5;
}
.actionIcon-2Hi9ZG:hover {
	opacity: 1.0;
}
.unread-3zKkbm {
	background-color: rgb(var(--fontwhite1));
}

#app-mount .channelIcon-1JSaVj {							/* channelselect		icon								*/
	color: rgb(var(--fontwhite3));
}
#app-mount .selected-3Qtv-u .channelIcon-1JSaVj {
	color: rgb(var(--fontwhite1));
}

.icon-3BcwQu,												/* voicechat			icon								*/
.username-lm8y6T {											/* voicechat			username							*/
	color: rgb(var(--fontwhite3));
}
.listDefault-2y5Z9D .clickable-23RaYz:hover .username-lm8y6T {
	color: rgb(var(--fontwhite2));
}
.listDefault-2y5Z9D .clickable-23RaYz.selected-3TGCSZ .username-lm8y6T,
.listDefault-2y5Z9D .clickable-23RaYz:hover .usernameSpeaking-2xbKKh,
.usernameSpeaking-2xbKKh {
	color: rgb(var(--fontwhite1));
}
.wrapper-pZmgj4 {											/* voicechat			limit								*/
	background-color: rgba(var(--vtransparencycolor), 0.15);
	color: rgb(var(--fontwhite3));
}
.modeConnected-2IEL4z .wrapper-pZmgj4 {
	color: rgb(var(--fontwhite1));
}
.wrapper-pZmgj4 .users-i_3-kL {
	background-color: transparent;
}
.wrapper-pZmgj4 .total-3tKGEB {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.wrapper-pZmgj4 .total-3tKGEB:after {
	border-right-color: rgba(var(--vtransparencycolor), 0.3);
}

.listDefault-2y5Z9D .clickable-23RaYz:hover .content-3xS9Lh {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}


/* ----		5.3.	DMCHANNELS						---- */

.channel-2QD9_O {											/* dmchannel/page		container						*/
	color: rgb(var(--fontwhite3));
}
.clickable-1JJAn8.channel-2QD9_O:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-1JJAn8.channel-2QD9_O:active,
.selected-aXhQR6.channel-2QD9_O {
	color: rgb(var(--fontwhite1));
}
.channel-2QD9_O:hover .layout-2DM8Md {						/* dmchannel/page		inner							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.selected-aXhQR6.channel-2QD9_O .layout-2DM8Md {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.selected-aXhQR6.channel-2QD9_O .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.channel-2QD9_O .linkButtonIcon-Mlm5d6 {
	color: rgb(var(--fontwhite2));
}
.channel-2QD9_O .name-uJV0GL {
	color: rgb(var(--fontwhite2));
}
.channel-2QD9_O .subtext-1RtU34 {
	color: rgb(var(--fontwhite3));
}
.channel-2QD9_O:hover .linkButtonIcon-Mlm5d6,
.channel-2QD9_O.selected-aXhQR6 .linkButtonIcon-Mlm5d6 {
	color: rgb(var(--fontwhite1));
}
.channel-2QD9_O:hover .name-uJV0GL,
.channel-2QD9_O.selected-aXhQR6 .name-uJV0GL {
	color: rgb(var(--fontwhite1));
}
.channel-2QD9_O:hover .subtext-1RtU34,
.channel-2QD9_O.selected-aXhQR6 .subtext-1RtU34 {
	color: rgb(var(--fontwhite2));
}

.header-zu8eWb {
	color: rgb(var(--fontwhite2));
}

.empty-388osJ {												/* loadingplaceholders										*/
	fill: rgb(var(--vaccentcolor));
}

/* ----		5.4.	ACCOUNT/VOICE/GOLIVE			---- */

.panels-j1Uci_ > * {										/* account/voice		inner								*/
	border: none;
}
.panels-j1Uci_ > * + * {
	border-top: 1px solid rgba(var(--fontwhite4), 0.2);
}

.title-eS5yk3 {												/* account/voice		title								*/
	color: rgb(var(--fontwhite1));
}
.subtext-3CDbHg {											/* account/voice		subtext								*/
	color: rgb(var(--fontwhite3));
}
.button-14-BFJ {
	color: rgb(var(--fontwhite3));
}
.button-14-BFJ.enabled-2cQ-u7,								/* account/voice		buttons								*/
.button-14-BFJ.enabled-2cQ-u7:hover {
	color: rgb(var(--fontwhite1));
}
.button-14-BFJ.enabled-2cQ-u7 {
	opacity: 0.7;
}
.button-14-BFJ.enabled-2cQ-u7:hover {
	opacity: 1;
	background-color: rgb(var(--vaccentcolor));
}
.button-14-BFJ.enabled-2cQ-u7:hover svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}


/* ~~~~		6.		CHAT							~~~~ */

/* ----		6.1.	CHANNELHEADER					---- */

.container-1r6BKw {											/* header				container							*/
	color: rgb(var(--fontwhite1));
}
.container-1r6BKw.themed-ANHk51 {							/* header				themedcontainer						*/
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2),0 1.5px 0 rgba(var(--vtransparencycolor), 0.05),0 2px 0 rgba(var(--vtransparencycolor), 0.05);
}

.title-29uC1r {												/* header				title								*/
	color: rgb(var(--fontwhite1));
}
.input-2A_zIr {												/* header				dmchannelinput						*/
	color: rgb(var(--fontwhite1));
}
.input-2A_zIr:focus {										/* header				dmchannelinput						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.input-2A_zIr:focus,
.outer-o9SjPm:hover .input-2A_zIr {
	box-shadow: inset 0 0 0 1px rgba(var(--vtransparencycolor), 0.2);
}
.topic-TCb_qw {												/* header				topic								*/
	color: rgb(var(--fontwhite2));
}
.children-19S4PO:after {									/* header				topicgradient						*/
	display: none;
}

.akaBadge-1M-1Gw {											/* header				aka									*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.icon-22AiRD {												/* header				typeicon							*/
	color: rgb(var(--fontwhite1));
}
.clickable-3rdHwn .icon-22AiRD,								/* header				actionicon							*/
#app-mount .link-2T7oYD {									/* header				linkicon							*/
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
.clickable-3rdHwn:hover .icon-22AiRD,
#app-mount .link-2T7oYD:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-3rdHwn:active .icon-22AiRD,
.clickable-3rdHwn.selected-1GqIat .icon-22AiRD,
#app-mount .link-2T7oYD:active {
	color: rgb(var(--fontwhite1));
}

.badge-2qGa_k:after {										/* header				iconbadge red dot					*/
	border: none;
}

.divider-3FBTu8 {											/* header				divider								*/
	background-color: rgba(var(--fontwhite1), 0.1);
}

.searchBar-3dMhjb {											/* header				searchbar							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.search-2oPWTC .DraftEditor-root .public-DraftEditorPlaceholder-root {
	color: rgb(var(--fontwhite3));
}
#app-mount .searchFilter-2ESiM3,
#app-mount .searchAnswer-3Dz2-q {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}

/* ----		6.2.	MESSAGES						---- */

.base-19D3Qq {												/* welcomemessage											*/
	padding-bottom: 0;
}
.base-34jWEe h1 {											/* welcomemessage		dmchannel							*/
	color: rgb(var(--fontwhite1));
}
.emptyChannelIcon-3IXV5M {									/* welcomemessage		empty channelicon					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.card-1yV8cG {												/* welcomemessage		first steps card					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.card-1yV8cG:hover {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
.divider-JfaTT5:not(.isUnread-3Ef-o9) {						/* divider				time								*/
	border-color: rgba(var(--fontwhite1), 0.2);
}
.divider-JfaTT5.hasContent-1cNJDh {							/* divider				hascontent							*/
	border-color: transparent;
}
.unreadPill-2HyYtt {										/* divider				unreadPill							*/
	color: rgb(var(--fontwhite1));
}
.content-1o0f9g {											/* divider				content								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
	width: 100%;
	text-align: center;
}

.hasMore-3e72_v {											/* bar					hasmore								*/
	box-shadow: inset 0 0 0 1px rgba(var(--fontwhite1), 0.1);
}
.hasMore-3e72_v:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.jumpToPresentBar-9P20AM {									/* bar					jumptopresent						*/
	overflow: hidden;
	background: transparent;
	opacity: 1;
}
.jumpToPresentBar-9P20AM:after,
.jumpToPresentBar-9P20AM:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.jumpToPresentBar-9P20AM:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.jumpToPresentBar-9P20AM:before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
	background-attachment: fixed;
}
.barButtonBase-3UKlW2 {										/* bar					text								*/
	color: rgb(var(--fontwhite1));
}

/* ====		6.2.1.	MESSAGE							==== */


#app-mount .message-2qRu38 {								/* message				confirm modal						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}
.message-2qnXI6,											/* message				container							*/
.message-2DieIs,											/* message				mention popout						*/
.message-2g38UB,											/* message				inbox								*/
.message-2qRu38 .wrapper-2a6GCs,
.messageGroupCozy-2iY6cT,
.messageGroupCozy-2Bj3ME {
	background-color: rgba(var(--vtransparencycolor), var(--vmessagetransparency));
}
.message-2qnXI6.selected-2P5D_Z,
.mouse-mode .message-2qnXI6:hover,
.mouse-mode.full-motion .message-2qnXI6:hover {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vmessagetransparency) * 1.2 * var(--vusechatbubbles) + 0.3 * (1 - var(--vusechatbubbles))));
}
.message-2qnXI6.localBot-GrCgVt {							/* message				localbot							*/
	background-image: linear-gradient(rgba(var(--vaccentcolor), calc(0.1 * (1 - var(--vusechatbubbles)))), rgba(var(--vaccentcolor), calc(0.2 * (1 - var(--vusechatbubbles)))));
}
.message-2qnXI6.mentioned-xhSam7 {							/* message				mentioned							*/
	background-image: linear-gradient(rgba(var(--vaccentcolor), calc(0.2 * (1 - var(--vusechatbubbles)))), rgba(var(--vaccentcolor), calc(0.2 * (1 - var(--vusechatbubbles)))));
}
.message-2qnXI6.localBot-GrCgVt:before,
.message-2qnXI6.mentioned-xhSam7:before {
	background-color: rgb(var(--vaccentcolor));
}
.message-2qnXI6.mentioned-xhSam7 .markup-2BOw-j {
	border-radius: 3px;
	background-color: rgba(var(--vaccentcolor), calc(0.3 * var(--vusechatbubbles)));
}
#app-mount .avatar-1BDn8e {
	position: absolute;
	top: 4px;
	left: calc(-70px * var(--vusechatbubbles) + 16px);
}
.container-3FojY8 .avatar-1BDn8e {
	left: calc(-10px * var(--vusechatbubbles));
}
.cozy-3raOZG .header-23xsNx:after {
	content: "";
	position: absolute;
	top: 12px;
	left: -32px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--vtransparencycolor), var(--vmessagetransparency));
}
.cozy-3raOZG .container-3FojY8 .header-23xsNx:after {
	left: 40px;
}
.messageGroupWrapper-o-Zw7G .messageGroupCozy-2iY6cT .header-23xsNx:after,
.searchResult-2N9RV4 .messageGroupCozy-2Bj3ME .header-23xsNx:after {
	top: 2px;
}
.cozy-3raOZG .timestamp-3ZCmNB.alt-1uNpEt {
	left: calc(-78px * var(--vusechatbubbles));
}
.cozy-3raOZG .iconContainer-3GkGRf {
	background-color: rgba(var(--vtransparencycolor), var(--vmessagetransparency));
	border-radius: 50%;
	left: calc(1px * (-58 * var(--vusechatbubbles) + -48 * (1 - var(--vusechatbubbles))));
	height: 25px;
	width: 25px;
	padding: 0;
}
.cozy-3raOZG .blockedSystemMessage-2Rk1ek .iconContainer-3GkGRf {
	background-color: transparent;
}
.cozy-3raOZG .iconContainer-3GkGRf:after {
	content: "";
	position: absolute;
	top: 2px;
	left: 26px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--vtransparencycolor), var(--vmessagetransparency));
}
.cozy-3raOZG .blockedSystemMessage-2Rk1ek .iconContainer-3GkGRf:after {
	display: none;
}
.selected-2P5D_Z.message-2qnXI6.cozy-3raOZG .header-23xsNx:after, 
.mouse-mode .message-2qnXI6.cozy-3raOZG:hover .header-23xsNx:after,
.mouse-mode.full-motion .message-2qnXI6.cozy-3raOZG:hover .header-23xsNx:after,
.selected-2P5D_Z.message-2qnXI6.cozy-3raOZG .iconContainer-3GkGRf:after,
.mouse-mode .message-2qnXI6.cozy-3raOZG:hover .iconContainer-3GkGRf:after,
.mouse-mode.full-motion .message-2qnXI6.cozy-3raOZG:hover .iconContainer-3GkGRf:after {
	border-right-color: rgba(var(--vtransparencycolor), calc(var(--vmessagetransparency) * 1.2));
}
#app-mount .localBot-GrCgVt.cozy-3raOZG .header-23xsNx:after,
#app-mount .mentioned-xhSam7.cozy-3raOZG .header-23xsNx:after {
	border-right-color: rgba(var(--vaccentcolor), calc(var(--vmessagetransparency) * 100000000000000000000000000000));
}
.message-2DieIs,
.message-2g38UB,
.zalgo-jN1Ica .messageContent-2qWWxC,
.zalgo-jN1Ica.cozy-3raOZG .header-23xsNx {
	overflow: visible;
}
.container-3FojY8 {
	padding: 0;
	overflow: visible;
}
#app-mount .cozyMessage-3V1Y8y {
	margin-left: calc(80px * var(--vusechatbubbles));
	padding-left: calc(1px * (10 * var(--vusechatbubbles) + 72 * (1 - var(--vusechatbubbles))));
}
#app-mount .cozy-3raOZG .header-23xsNx,
#app-mount .cozy-3raOZG .messageContent-2qWWxC {
	margin-left: 0;
	padding-left: 0;
}
.messageContainer-gbhlwo .wrapper-2a6GCs,
.messages-3G3erD .wrapper-2a6GCs,
.message-2qRu38 .wrapper-2a6GCs,
.messageGroupWrapper-o-Zw7G .messageGroupCozy-2iY6cT,
.searchResult-2N9RV4 .messageGroupCozy-2Bj3ME {
	border-radius: 5px;
	margin-left: calc(60px * var(--vusechatbubbles));
	padding-left: calc(1px * (10 * var(--vusechatbubbles) + 72 * (1 - var(--vusechatbubbles))));
}
.messages-3G3erD .wrapper-2a6GCs {
	border-radius: 0;
}

.expanded-13sWhZ {											/* message				expanded blocked					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 5px 5px 0 5px;
	margin-bottom: .5625rem;
}

.edited-DL9ECl {											/* message				editedtag							*/
	color: rgb(var(--fontwhite3));
}

.timestampCozy-1HNQR2,										/* message				timestamp							*/
.timestampCompact-29LLPQ,
.timestamp-1E3uAL {
	color: rgb(var(--fontwhite3));
}

.reaction-1hd86g {											/* message				reaction							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.reactionCount-2mvXRV {										/* message				reactioncount						*/
	color: rgb(var(--fontwhite4));
}
.reaction-1hd86g:hover .reactionCount-2mvXRV {
	color: rgb(var(--fontwhite2));
}

.wrapper-2aW0bm {											/* message				buttons								*/
	background-color: transparent;
	position: relative;
}
.wrapper-2aW0bm:after,
.wrapper-2aW0bm:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.wrapper-2aW0bm:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.wrapper-2aW0bm:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.separator-42rNt0 {											/* message				buttonsseparator					*/
	border-left-color: rgba(var(--fontwhite1), 0.1);
}
.button-1ZiXG9:hover {										/* message				button								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.button-1ZiXG9.selected-LCBEAU {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

#app-mount .localBotMessage-3cUzun,							/* message				localbotoperations					*/
#app-mount .operations-36ENbA {								/* message				editoperations						*/
	color: rgb(var(--fontwhite3));
}

.markup-2BOw-j {											/* message				markup								*/
	color: rgb(var(--fontwhite2));
}
.markup-2BOw-j code {										/* messageelement		code								*/
	background-color: transparent;
	border-color: transparent;
}
.markup-2BOw-j pre {										/* messageelement		pre									*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
.markup-2BOw-j .inline,										/* messageelement		inline								*/
.after_inlineCode-1KfVgj,
.before_inlineCode-1G9rTK,
.inlineCode-2ngu6Y {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.markup-2BOw-j .hljs {										/* messageelement		hljs								*/
	color: rgb(var(--fontwhite2));
}
.blockquoteDivider-2hH8H6 {									/* messageelement		quotedivider						*/
	background-color: rgb(var(--fontwhite4));
}

#app-mount .spoilerText-3p6IlD {							/* messageelement		spoiler								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .spoilerText-3p6IlD.hidden-HHr2R9 {				/* messageelement		hiddenspoiler						*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}

.container-3-pyIM {											/* systemmessage		content								*/
	color: rgb(var(--fontwhite3));
}
.icon-2Po-VO[style*="/assets/5da4cdab01d4d89c593c48c62ae0d937.svg"] {		/* systemmessage			pinicon									*/
	-webkit-mask: url(https://discordapp.com/assets/5da4cdab01d4d89c593c48c62ae0d937.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite3)) !important;
}
.icon-2Po-VO[style*="/assets/d80d1fdc43a3c42134a31a39581160ac.svg"] {		/* systemmessage			missedcall								*/
	-webkit-mask: url(https://discordapp.com/assets/d80d1fdc43a3c42134a31a39581160ac.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite3)) !important;
}
.icon-2Po-VO[style*="/assets/b8029fe196b8f1382e90bbe81dab50dc.svg"] {		/* systemmessage			joincallicon							*/
	-webkit-mask: url(https://discordapp.com/assets/b8029fe196b8f1382e90bbe81dab50dc.svg) center/cover no-repeat;
	background: rgb(var(--vaccentcolor)) !important;
}
.icon-2Po-VO[style*="/assets/c30220457097b064286a8759a9b6c4af.svg"] {		/* systemmessage			recievecallicon							*/
	-webkit-mask: url(https://discordapp.com/assets/c30220457097b064286a8759a9b6c4af.svg) center/cover no-repeat;
	background: rgb(var(--vaccentcolor)) !important;
}

/* ====		6.2.2.	EMBEDS							==== */

#app-mount .embedFull-2tM8-- {								/* embed				wrapper								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-left-color: rgb(var(--fontwhite4));
}
#app-mount .embedAuthorName-3mnTWj,							/* embed				author								*/
#app-mount .embedFieldName-NFrena,							/* embed				fieldname							*/
#app-mount .embedTitle-3OXDkz {								/* embed				title								*/
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .embedDescription-1Cuq9a,						/* embed				description							*/
#app-mount .embedFieldValue-nELq2s {						/* embed				fieldvalue							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .embedProvider-3k5pfl {							/* embed				provider							*/
	color: rgb(var(--fontwhite3)) !important;
}
#app-mount .embedFooterText-28V_Wb {						/* embed				footer								*/
	color: rgb(var(--fontwhite4));
}

#app-mount .attachment-33OFj0 {								/* attachment			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
	margin-left: 18px;
}
#app-mount .message-2qnXI6 .attachment-33OFj0 {
	margin-left: 0;
}
#app-mount .filename-3eBB_v {								/* attachment			filename							*/
	color:	rgb(var(--fontwhite1));
}
#app-mount .size-1Arx_I {									/* attachment			sizesize							*/
	color:	rgb(var(--fontwhite4));
}
#app-mount .metadata-3WGS0M {								/* attachment			metadata							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .cancelButton-3hVEV6,							/* attachment			cancelbutton						*/
#app-mount .downloadButton-23tKQp {							/* attachment			downloadbutton						*/
	color: rgb(var(--fontwhite4));
}
#app-mount .cancelButton-3hVEV6:hover,
#app-mount .downloadButton-23tKQp:hover {
	color: rgb(var(--fontwhite3));
}
#app-mount .cancelButton-3hVEV6:active,
#app-mount .downloadButton-23tKQp:active {
	color: rgb(var(--fontwhite2));
}
#app-mount .twitchSectionPlayButton-2RamGG {
	background-image: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none"><path d="M12.3333 10.002V22.002L22.3333 16.002L12.3333 10.002Z" fill="rgb(185,187,190)"/></svg>');
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-radius: 50%;
	object-position: -9999999px -9999999px;
}
#app-mount .twitchSectionPlayButton-2RamGG:hover {
	background-color: rgba(var(--vtransparencycolor), 0.8);
}

#app-mount .wrapper-2TxpI8 {								/* attachment			videowrapper						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .embedSuppressButton-1FonMn {					/* attachment			closebutton							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .embedSuppressButton-1FonMn:hover {
	color: rgb(var(--fontwhite3));
}

/* ====		6.2.3.	NITROGIFT						==== */

#app-mount .tile-2OwFgW {									/* gift					container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
#app-mount .title-1rUb9I {									/* gift					title								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .tagline-2nvxi0 {								/* gift					tagline								*/
	color: rgb(var(--fontwhite4));
}

/* ====		6.2.4.	INVITE							==== */

#app-mount .wrapper-35wsBm {								/* invite				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .guildIconImage-3qTk45 {							/* invite				icon								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .guildName-2hvnt_ {								/* invite				name								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .guildDetail-1nRKNE {							/* invite				details								*/
	color: rgb(var(--fontwhite4));
}


/* ----		6.3.	TEXTAREA						---- */

.form-2fGMdU {												/* textarea				form								*/
	position: relative;
	padding-top: 10px;
}
.form-2fGMdU > *,
.channelTextArea-rNsIhG {
	z-index: 1;
}
#app-mount .form-2fGMdU:after,
#app-mount .form-2fGMdU:before {
	display: flex;
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 8px;
	left: 0;
	height: unset;
	width: unset;
	pointer-events: none;
}
#app-mount .form-2fGMdU:after {
	background-color: rgba(var(--vtransparencycolor), var(--vtransparencyalpha));
}
#app-mount .form-2fGMdU:before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
	background-attachment: fixed;
}

.channelTextArea-rNsIhG {									/* textarea				channeltextarea						*/
	background-color: transparent;
	border-top-color: rgba(var(--fontwhite1), 0.1);
}

.scrollableContainer-2NUZem {								/* textarea				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.attachButtonPlus-jWVFah {									/* textarea				attachbuttoninner					*/
	fill: rgb(var(--fontwhite3));
}
.attachButton-2WznTc:hover .attachButtonPlus-jWVFah {
	fill: rgb(var(--fontwhite2));
}
.attachButton-2WznTc:active .attachButtonPlus-jWVFah {
	fill: rgb(var(--fontwhite1));
}
.attachWrapper-2TRKBi {										/* textarea				attachdivider						*/
	border-color: rgb(var(--fontwhite3));
}

#app-mount .textArea-12jD-V {								/* textarea				textarea							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .textArea-12jD-V::placeholder {
	color: rgb(var(--fontwhite4));
}
.placeholder-37qJjk,
.slateTextArea-1Mkdgw .hljs-comment,
.slateTextArea-1Mkdgw .hljs-quote {
	color: rgb(var(--fontwhite4));
}

.button-3AYNKb {											/* textarea				buttons								*/
	color: rgb(var(--fontwhite3));
}
.button-3AYNKb:hover,
.buttonWrapper-1ZmCpA:hover .icon-3D60ES {
	color: rgb(var(--fontwhite2));
}
.active-23Nm0T .icon-3D60ES,
.active-23Nm0T:hover .icon-3D60ES {
	color: rgb(var(--fontwhite1));
}
.sprite-2iCowe {											/* textarea				emojibutton							*/
	transform: none !important;
}

.base-gE7OpD {												/* textarea				typingusers							*/
	color: rgb(var(--fontwhite1));
}

.wrapper-39oAo3 {											/* textarea				placeholder							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}

.toolbar-2bjZV7 {											/* textarea				formattoolbar						*/
	background-color: rgb(var(--vaccentcolor));
}
.toolbar-2bjZV7:before {
	border-top-color: rgb(var(--vaccentcolor));
}
.divider-24xeUg {											/* textarea				formattoolbardivider				*/
	border-left-color: rgba(var(--fontwhite1), 0.1);
}
.active-2HPddW,												/* textarea				buttonactive						*/
.hover-28QbSq:hover {										/* textarea				buttonhover							*/
	background-color: rgba(var(--fontwhite1), 0.2);
}
.icon-KgGMGo {												/* textarea				buttonicon							*/
	color: rgb(var(--fontwhite2));
}
.active-2HPddW .icon-KgGMGo,
.hover-28QbSq:hover .icon-KgGMGo {
	color: rgb(var(--fontwhite1));
}

/* ----		6.4.	AUTOCOMPLETEMENU				---- */

#app-mount .autocomplete-1vrmpx {							/* autocomplete			container							*/
	background-color: transparent;
	overflow: hidden;
}
#app-mount .autocomplete-1vrmpx:after,
#app-mount .autocomplete-1vrmpx:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .autocomplete-1vrmpx:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
#app-mount .autocomplete-1vrmpx:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.theme-brand .autocomplete-1vrmpx {
	background: rgb(var(--vaccentcolor)) linear-gradient(rgba(var(--vtransparencycolor), 0.2), rgba(var(--vtransparencycolor), 0.2)) !important;
}
.theme-brand .autocomplete-1vrmpx:after,
.theme-brand .autocomplete-1vrmpx:before {
	display: none;
}
#app-mount .container-3ISnnM:after {
	box-shadow: inset 0 -7px 12px -7px rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .header-1TOWci {								/* autocomplete				header								*/
	box-shadow: 0 1px 0 0 rgba(var(--vtransparencycolor), 0.2), 0 1px 2px 0 rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .backButton-JyKGC1 {							/* autocomplete				backbutton							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .backButton-JyKGC1:hover {
	color: rgb(var(--fontwhite2));
}
#app-mount .focused-1En8bG,								/* autocomplete				result								*/
#app-mount .result-3w1ZcL:hover {
	box-shadow: 0 11px 22px 1px rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .emptyHintCard-2mUdMe {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .emptyHintText-1QDF9N {
	color: rgb(var(--fontwhite1));
}
#app-mount .endText-3SrwuD {
	color: rgb(var(--fontwhite3));
}
#app-mount .endContainer-1ZDW8j:after {
	background-image: url(https://discordapp.com/assets/0c735bf91232f2a2266e6ba9d6753565.svg);
	opacity: 0.6;
}
#app-mount .contentTitle-2tG_sM {						/* autocomplete				searchtitle							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .contentTitle-2tG_sM strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .divider-23swzi {							/* autocomplete				divider								*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .selectorSelected-1_M1WV {					/* autocomplete				rowselected							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .content-Qb0rXO {							/* autocomplete				rowcontent							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .iconForeground-1w5n7R {						/* autocomplete				icon								*/
	fill: rgb(var(--fontwhite3));
}
#app-mount .description-11DmNu,							/* autocomplete				description							*/
#app-mount .descriptionUsername-J_75O8 {				/* autocomplete				username							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .descriptionDiscriminator-3vUOCc {			/* autocomplete				discriminator						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .selectorSelected-1_M1WV .content-Qb0rXO {
	color: rgb(var(--fontwhite1));
}
#app-mount .selectorSelected-1_M1WV .iconForeground-1w5n7R {
	fill: rgb(var(--fontwhite2));
}
#app-mount .selectorSelected-1_M1WV .description-11DmNu,
#app-mount .selectorSelected-1_M1WV .descriptionUsername-J_75O8 {
	color: rgb(var(--fontwhite2));
}
#app-mount .selectorSelected-1_M1WV .descriptionDiscriminator-3vUOCc {
	color: rgb(var(--fontwhite2));
}

#app-mount .searchSuggestion-2K8OBX:hover {					/* gifpicker			suggestions							*/
	color: rgb(var(--fontwhite1));
}

#app-mount .placeholder-1kJjXI {							/* gifpicker			result placeholder					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}


/* ----		6.5.	MEMBERLIST						---- */

.member-3-YXUe {											/* member				container							*/
	color: rgb(var(--fontwhite3));
}
.clickable-1JJAn8.member-3-YXUe:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-1JJAn8.member-3-YXUe:active,
.selected-aXhQR6.member-3-YXUe {
	color: rgb(var(--fontwhite1));
}
.member-3-YXUe:hover .layout-2DM8Md {						/* member				inner								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.selected-aXhQR6.member-3-YXUe .layout-2DM8Md {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.selected-aXhQR6.member-3-YXUe .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.member-3-YXUe .name-uJV0GL {
	color: rgb(var(--fontwhite2));
}
.member-3-YXUe .activity-2Gy-9S {
	color: rgb(var(--fontwhite3));
}
.member-3-YXUe:hover .linkButtonIcon-Mlm5d6,
.member-3-YXUe.selected-aXhQR6 .linkButtonIcon-Mlm5d6 {
	color: rgb(var(--fontwhite1));
}
.member-3-YXUe:hover .name-uJV0GL,
.member-3-YXUe.selected-aXhQR6 .name-uJV0GL {
	color: rgb(var(--fontwhite1));
}
.member-3-YXUe:hover .activity-2Gy-9S,
.member-3-YXUe.selected-aXhQR6 .activity-2Gy-9S {
	color: rgb(var(--fontwhite2));
}
.member-3-YXUe.selected-aXhQR6 .premiumIcon-2IFPOX {
	color: rgb(var(--fontwhite1)) !important;
}

.membersGroup-v9BXpm {										/* roleheader												*/
	color: rgb(var(--fontwhite2));
}

.avatar-VxgULZ:before {										/* emptyavatar												*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.memberGroupsPlaceholder-3mwPub,							/* loadingplaceholders										*/
.placeholderAvatar-damqh6,
.placeholderUsername-2B_OA9 {
	background-color: rgb(var(--vaccentcolor));
}

/* ----		6.6.	SEARCHPAGE						---- */

#app-mount .searchResultsWrap-3-pOjs {						/* searchpage			container							*/
	background-color: transparent;
}
#app-mount .searchHeader-1EzJGH {							/* searchpage			header								*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 0.8));
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .searchHeader-1EzJGH .totalResults-1yK_Ym {		/* searchpage			results								*/
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
#app-mount .searchHeader-1EzJGH .tab-EiCZG6 {				/* searchpage			tab									*/
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
#app-mount .searchHeader-1EzJGH .tab-EiCZG6:hover {
	color: rgb(var(--fontwhite2));
	border-bottom-color: rgb(var(--fontwhite2));
}
#app-mount .searchHeader-1EzJGH .tab-EiCZG6.selected-3gXBLQ {
	color: rgb(var(--fontwhite1));
	border-bottom-color: rgb(var(--fontwhite1));
}
#app-mount .searchHeader-1EzJGH + div {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 0.5));
}
#app-mount .channelSeparator-dTqJ4K {						/* searchpage			separator							*/
	overflow: hidden;
	width: 390px;
}
#app-mount .channelSeparator-dTqJ4K:not(:empty):before {
	display: none;
}
#app-mount .channelSeparator-dTqJ4K .channelName-wvgELL {	/* searchpage			channelname							*/
	background: transparent;
	color: rgb(var(--fontwhite3));
}
#app-mount .channelSeparator-dTqJ4K .channelName-wvgELL:after {
	content: "";
	border-bottom: 1px solid rgba(var(--fontwhite3), 0.5);
	height: 1px;
	margin-left: 10px;
	position: absolute;
	pointer-events: none;
	top: 50%;
	width: 100vw;
	z-index: 0;
}
.searchResult-2N9RV4:before,								/* searchpage			result								*/
.searchResult-2N9RV4:after {
	display: none;
}
#app-mount .searchResult-2N9RV4 .hit-1CXhXT {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.1);
	box-shadow: none;
}
#app-mount .searchResult-2N9RV4.expanded-ovgtuV {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .searchResult-2N9RV4:not(.expanded-ovgtuV) .before-2BfuiJ.sibling-1HG8JI {
	-webkit-mask: linear-gradient(to bottom, rgba(0,0,0,1) 0%, rgba(0,0,0,0.9) 50%, rgba(0,0,0,0.1) 85%, rgba(0,0,0,0) 100%);
}
#app-mount .searchResult-2N9RV4:not(.expanded-ovgtuV) .after-1oc6Rt.sibling-1HG8JI {
	-webkit-mask: linear-gradient(to top, rgba(0,0,0,0) 0%, rgba(0,0,0,0.8) 30%, rgba(0,0,0,0.9) 50%, rgba(0,0,0,0.1) 85%, rgba(0,0,0,0) 100%);
}
#app-mount .searchResult-2N9RV4:not(.expanded-ovgtuV) .before-2BfuiJ:not(.sibling-1HG8JI),
#app-mount .searchResult-2N9RV4:not(.expanded-ovgtuV) .after-1oc6Rt:not(.sibling-1HG8JI) {
	display: none;
}

.jumpButton-1ol35X {										/* message				jumpbutton							*/ 
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}
.jumpButton-1ol35X:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.jumpButton-1ol35X + .jumpButton-1ol35X {
	margin-left: 2px;
}

#app-mount .pagination-1m6Ll- {
	color: rgb(var(--fontwhite3));
}

/* ----		6.7.	CALL							---- */

#app-mount .incomingCallInner-2VmFiR {						/* popout				inner								*/
	background: transparent;
	border: none;
}
.incomingCallInner-2VmFiR:after,
.incomingCallInner-2VmFiR:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.incomingCallInner-2VmFiR:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.incomingCallInner-2VmFiR:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .members-2BNiuX {								/* popout				members							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .subtitle-1H8FPn {								/* popout				subtitle						*/
	color: rgb(var(--fontwhite3));
}

#app-mount .wrapper-2qzCYF {								/* call					wrapper							*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 0.8));
}
#app-mount .root-217Brm {									/* call					root							*/
	color: rgb(var(--fontwhite1));
}
.videoWrapper-2v09vt	{									/* call					video wrapper					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.video-1FfuMD {												/* call					video							*/
	background-color: transparent;
}
.tile-2gi3tr {												/* call					user video						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.gradientContainer-10lXLB {
	background: linear-gradient(rgb(var(--vtransparencycolor)), transparent 15%, transparent 85%, rgb(var(--vtransparencycolor)));
}
.centerButton-3CaNcJ {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
.centerButton-3CaNcJ:hover {
	background-color: rgb(var(--vaccentcolor));
}
.controlButton-2MhVEL.leaveButton-2YnTyt {
	background-color: rgba(240, 71, 71, 0.5);
}
.controlButton-2MhVEL.leaveButton-2YnTyt:hover {
	background-color: rgb(240, 71, 71);
}
.regionSelectPopout-p9-0_W {
	width: 170px;
}

/* ----		6.8.	UNAVAILABLESCREEN				---- */

.category-2haXBH,											/* loadingplaceholders										*/
.channelIcon-1TvDoP,
.channelName-2wrHHc {
	background-color: rgb(var(--vaccentcolor));
}
.splashImage-13vBzp {										/* screen				image								*/
	opacity: 0.7;
}
.splashHeader-ehL7gZ {										/* screen				headertext							*/
	color: rgb(var(--fontwhite1));
}


/* ~~~~		7.		PEOPLES							~~~~ */

.wrapper-1cBijl {											/* friendsadd			inputcontainer						*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
.wrapper-1cBijl:hover {
	border-color: rgb(var(--vtransparencycolor));
}
.wrapper-1cBijl .addFriendInput-4bcerK {
	color: rgb(var(--fontwhite1));
}
.wrapper-1cBijl .addFriendInput-4bcerK::placeholder,
.addFriendHint-3Y70FX {
	color: rgb(var(--fontwhite4));
}

.tableHeaderText-2io-_N,									/* tableheader			text								*/
.onlineStatusGroupTitle-6ObdV6 {							/* groupheader												*/
	color: rgb(var(--fontwhite2));
}

.tableHeader-2Ctu7Y {										/* tablerheader			border								*/
	border-top-color: rgba(var(--fontwhite4), 0.5);
}
.peopleListItem-2nzedh {									/* peoples				row									*/
	border-top-color: rgba(var(--fontwhite1), 0.1);
}
.peopleListItem-2nzedh .username-31C1TQ {					/* peoples				username							*/
	color: rgb(var(--fontwhite2));
}
.peopleListItem-2nzedh .discriminator-22Okc1 {				/* peoples				discriminator						*/
	color: rgb(var(--fontwhite4));
}
.peopleListItem-2nzedh .subtext-24R4-w {					/* peoples				subtext								*/
	color: rgb(var(--fontwhite3));
}
.peopleListItem-2nzedh .actionButton-uPB8Fs {				/* peoples				actionbutton						*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite3));
}
.peopleListItem-2nzedh:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.peopleListItem-2nzedh:hover .username-31C1TQ {
	color: rgb(var(--fontwhite1));
}
.peopleListItem-2nzedh:hover .discriminator-22Okc1 {
	color: rgb(var(--fontwhite3));
}
.peopleListItem-2nzedh:hover .subtext-24R4-w {
	color: rgb(var(--fontwhite2));
}
.peopleListItem-2nzedh:hover .actionButton-uPB8Fs {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
.peopleListItem-2nzedh .actionButton-uPB8Fs:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.header-13Cw0- {											/* playing				header								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .outer-1AjyKL {									/* playing				card								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .outer-1AjyKL.active-1xchHY,
#app-mount .outer-1AjyKL.interactive-3B9GmY:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .inset-3sAvek {									/* playing				card inner							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.emptyCard-1RJw8n {											/* playing				empty card							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .popout-38lTFE {									/* playing				popout								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 8px 16px 0 rgba(var(--vtransparencycolor), 0.3);
	overflow: hidden;
}
.popout-38lTFE:after,
.popout-38lTFE:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-38lTFE:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
}
.popout-38lTFE:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .memberListItem-31QoHj:not(.popoutDisabled-2RK7MF):hover,
#app-mount .enabled-1t_Gxm:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}


/* ~~~~		7.		STORE/NITRO						~~~~ */

.gridItemBadge-1Se-Pu {
	text-shadow: 1px 1px var(--vtextshadow);
}
.gridItemHeading-3D4Rb2 {
	color: rgb(var(--fontwhite1));
}
.gridItemSubheading-FIneEP {
	color: rgb(var(--fontwhite1));
}

.marketingHeader-2Iq7qk {									/* marketingheader											*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.detailsBlock-FoDTGA {										/* billing 				details								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.sectionHeader-127c3L {										/* header													*/
	color: rgb(var(--fontwhite1));
}
.tier2PlanName-2TttcQ {										/* header				svgtitle							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .title-2a5mvx {									/* header				title								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .subtitle-UfhpvR,								/* header				subtitle							*/
#app-mount .subtitleRepositioned-11uB9- {
	color: rgb(var(--fontwhite2));
}
.yearlyButtonDiscount-2K7GZZ {
	border-color: rgba(var(--fontwhite1), 0.3);
}

.subsectionHeader-1SVMaW {									/* subsection			header								*/
	color: rgb(var(--fontwhite1));
}
.blurb-1H7VPv {												/* subsection			description							*/
	color: rgb(var(--fontwhite2));
}
.title-3IUNJ6 {												/* subsection			featuretitle						*/
	color: rgb(var(--fontwhite1));
}
.description-yMw5z0 {										/* subsection			featuredescription					*/
	color: rgb(var(--fontwhite2));
}
.guildMoreFeatures-svfRvH {									/* subsection			footer								*/
	color: rgb(var(--fontwhite1));
}

#app-mount .categoryHeader-1D7Tqy,							/* categoryheader											*/
#app-mount .premiumApplicationsHeader-Zmkm5e {
	color: rgb(var(--fontwhite1));
	border-color: rgba(var(--fontwhite4), 0.3);
}

.gradientOverlay-298TBM {									/* cardscroller			gradient							*/
	display: none;
}
.scrollerButton-1Vm5_P {									/* cardscroller			button								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

#app-mount .tile-QA_yMc {									/* gamecard				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
#app-mount .description-2oYgWO {							/* gamecard				description							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .tagline-EIH5-W,									/* gamecard				tagline								*/
#app-mount .title-2XwaXv {									/* gamecard				title								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .perkTag-2O4dx4 {								/* gamecard				perktag								*/
	border-radius: 4px;
	color: rgb(var(--fontwhite1));
}

#app-mount .tier1Banner-1BTgv0 {							/* tier1banner			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.headerIcon-3bqya6 {										/* tier1banner			svgtitle							*/
	color: rgb(var(--fontwhite1));
}

.carouselButtonsContainer-Rba2-D {							/* gamepreview			container							*/
	color: rgb(var(--fontwhite1));
}
.smallCarousel-2e0IQc {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 5px;
}
#app-mount .item-3V15ea {									/* gamepreview			previewitem							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.arrow-3jRqK8 {												/* gamepreview			prev/nextarrow (big)				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.arrow-vOpU7R {												/* gamepreview			prev/nextarrow (small)				*/
	color: rgb(var(--fontwhite1));
}
.dot-2Q_mMZ {												/* gamepreview			itemdot (small)						*/
	background-color: rgb(var(--fontwhite1));
}

#app-mount .root-1bFE0x {									/* gameinfo				sectioncontainer					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .header-3HFF3R {									/* gameinfo				sectionheader						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .section-7tu4tu {								/* gameinfo				subsection							*/
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .playerOverflow-2Hf77M {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
#app-mount .description-2Ifi6N {							/* gameinfo				subsectiondescription				*/
	color: rgb(var(--fontwhite3));
}
#app-mount .description-2Ifi6N strong,
#app-mount .username-2gp_Xw {								/* gameinfo				subsectionusername					*/
	color: rgb(var(--fontwhite1));
}
#app-mount .smallHeader-2h-9-U {							/* gameinfo				subsectionheader					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .text-1Z3P6i {									/* gameinfo				subsectiontext						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .iconCircle-1dlYo0 {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .circle-1nK_79 {
	color: rgb(var(--fontwhite1));
}

#app-mount .divider-21LyPb {								/* section				divider								*/
	border-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .blurb-1iBKJy {									/* section				description							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .description-1AwRKJ,								/* section				subdescription						*/
#app-mount .markdown-11q6EU {
	color: rgb(var(--fontwhite3));
}

#app-mount .tile-PuWjfs {									/* perkcard				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c {					/* perkcard				imagecontainer						*/
	position: relative;
	z-index: 5;
}
.tile-PuWjfs .description-2h6giI {							/* perkcard				imagecontainer						*/
	color: rgb(var(--fontwhite1));
	z-index: 6;
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c:after,
.tile-PuWjfs div.splashPlaceholder-1ev-9c:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c:before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
	background-attachment: fixed;
}
.tile-PuWjfs img.splashPlaceholder-1ev-9c {					/* perkcard				image								*/
	-webkit-mask: linear-gradient(rgba(0,0,0,1) 60%, rgba(0,0,0,0) 100%);
}
#app-mount .mediaFade-2NVPtV {								/* perkcard				fade								*/
	background: transparent;
}
#app-mount .item-2yFVoY {									/* newscard				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
#app-mount .collapsedTimestamp-2gjDIM,						/* newscard				timestamp							*/
#app-mount .openTimestamp-sTgPmn {
	color: rgb(var(--fontwhite3));
}
#app-mount .title-i-qCkH {									/* newscard				title								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .openDescription-2XUOH3 {						/* newscard				description							*/
	color: rgb(var(--fontwhite3));
}

#app-mount .requirements-dEriwm {							/* requirements												*/
	color: rgb(var(--fontwhite2));
}
#app-mount .requirementKey-14DT2D {							/* requirements			key									*/
	color: rgb(var(--fontwhite4));
}
#app-mount .content-1zhNsr {								/* requirements			rating								*/
	color: rgb(var(--fontwhite4));
}
#app-mount .content-3FEARf {								/* requirements			copyright							*/
	color: rgb(var(--fontwhite4));
}

#app-mount .bodySection-jqkkIP {							/* sidebar				section								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .actionText-3EKWER {								/* sidebar				header								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .purchaseUnitOperatingSystem-cnbJPz {			/* sidebar				OSicon								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .price-4PDWNj,									/* sidebar				price								*/
#app-mount .listingPrice-2GiDSc {
	color: rgb(var(--fontwhite1));
}
#app-mount .title-2xCQKy {									/* sidebar				subtitle							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .skuNormal-3h1es- {								/* sidebar				pricerow							*/
	border-bottom-color: rgba(var(--fontwhite4), 0.4);
}
#app-mount .name-u2zgy7 {									/* sidebar				pricename							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .price-NUANu6 {									/* sidebar				priceamount							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .label-13UUcd {									/* sidebar				label								*/
	color: rgb(var(--fontwhite4));
}
#app-mount .info-1Emy1X {									/* sidebar				labelinfo							*/
	color: rgb(var(--fontwhite1));
}

#app-mount .content-35aVm0 {								/* invitecard			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .name-3TBxUq {									/* invitecard			guildname							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .memberInfo-1TAaKC {								/* invitecard			memberinfo							*/
	color: rgb(var(--fontwhite4));
}

#app-mount .row-1bU71H {									/* features				row									*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .featureIcon-1f78KU {							/* features				featureicon							*/
	color: rgb(var(--fontwhite3));
}


/* ~~~~		9.		LIBRARY							~~~~ */

.header-39GIC8 {											/* library				table header						*/
	background: transparent;
	border-bottom-color: rgba(var(--fontwhite4), 0.5);
	color: rgb(var(--fontwhite3));
	position: relative;
}
.header-39GIC8:after,
.header-39GIC8:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.header-39GIC8:after {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.header-39GIC8:before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
	background-attachment: fixed;
}
.headerCell-3L6rFG {										/* library				table headercell					*/
	border-left-color: rgba(var(--fontwhite4), 0.3);
}
.clickable-VxMZ3b {
	color: rgb(var(--fontwhite2));
}
.clickable-VxMZ3b:hover {
	color: rgb(var(--fontwhite1));
}
.lastPlayedCell-2arbtc,
.platformCell-XyBBs6 {
	color: rgb(var(--fontwhite3));
}
.headerCellSorted-3a5AzJ,
.headerCellSorted-3a5AzJ:hover {
	color: rgb(var(--fontwhite1));
}
.row-ZLfFhY {												/* library				table row							*/
	color: rgb(var(--fontwhite3));
}
.rowWrapperActive-2L7i9f {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.rowWrapper-2fB6P0 + .rowWrapper-2fB6P0 .row-ZLfFhY {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
.nameCellText-1mpqtF {										/* library				table namecell						*/
	color: rgb(var(--fontwhite2));
}
.row-ZLfFhY:hover .nameCellText-1mpqtF {
	color: rgb(var(--fontwhite1));
}
.textCell-1aBIUP {											/* library				table textcell						*/
	color: rgb(var(--fontwhite4));
}
.row-ZLfFhY:hover .textCell-1aBIUP {
	color: rgb(var(--fontwhite3));
}
.icon-1IKq3C {												/* library				table icon							*/
	color: rgb(var(--fontwhite4));
}
.row-ZLfFhY:hover .icon-1IKq3C {
	color: rgb(var(--fontwhite3));
}
.emptyWumpus-12J3jI {										/* library				no games							*/
	opacity: 0.6;
}


/* ~~~~		10.		DISCOVERY						~~~~ */

.categoryItem-3zFJns {										/* categoryitem			container						*/
	color: rgb(var(--fontwhite3));
}
.clickable-1JJAn8.categoryItem-3zFJns:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-1JJAn8.categoryItem-3zFJns:active,
.selected-aXhQR6.categoryItem-3zFJns {
	color: rgb(var(--fontwhite1));
}
.categoryItem-3zFJns:hover .layout-2DM8Md {					/* categoryitem			inner							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.selected-aXhQR6.categoryItem-3zFJns .layout-2DM8Md {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.selected-aXhQR6.categoryItem-3zFJns .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.categoryItem-3zFJns .name-uJV0GL {
	color: rgb(var(--fontwhite2));
}
.categoryItem-3zFJns:hover .name-uJV0GL,
.categoryItem-3zFJns.selected-aXhQR6 .name-uJV0GL {
	color: rgb(var(--fontwhite1));
}

#app-mount .pageWrapper-1PgVDX {							/* guilddiscovery		container							*/
	color: rgb(var(--fontwhite1));
}
.select-2TCrqx.languageSelector-1R8fPE [class*="css-"][class*="-control"] {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.container-RHl2Ju {											/* guilddiscovery		news container						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .sectionSeparator-2OWiNT {						/* guilddiscovery		separator							*/
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
															/* guilddiscovery		pagebutton							*/
#app-mount .pageButton-MknE-_:not(.activeButton-1BJAiN):hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .activeButton-1BJAiN,
#app-mount .activeButton-1BJAiN:hover {						/* guilddiscovery		pagebuttonactive					*/
	color: rgb(var(--fontwhite1));
}

#app-mount .card-3DjzTQ {									/* guildcard			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .iconMask-3b8GzQ {								/* guildcard			iconmask							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .card-3DjzTQ:hover,
#app-mount .iconMask-3b8GzQ:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .cardPlaceholder-1zrbbe {						/* guildcard			placeholder							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .loading-17PYl_ {								/* guildcard			loading								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .guildName-1yURO5 {								/* guildcard			guildname							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .description-2QALGo {							/* guildcard			description							*/
	color: rgb(var(--fontwhite3));
}

.search-1iTphC .searchBox-2_mAlO .searchBoxInput-K6mkng {	/* search				searchinput							*/
	color: rgb(var(--fontwhite1));
}
.search-1iTphC .searchBox-2_mAlO .cta-BiH9zX {				/* search				searchtip							*/
	color: rgb(var(--fontwhite3));
}
.categoryPill-34fszg .categoryLabel-2G3r2V {				/* search				categorypill						*/
	color: rgb(var(--fontwhite3));
}
.emojiContainer-1u-_sQ {									/* search				emojicontainer						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.emptyContainer-1_gwCl {									/* search				no results							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}


/* ~~~~		11.		USERSETTINGS					~~~~ */

.themed-OHr7kt.item-PXvHYJ {								/* sidebar				item								*/
	color: rgb(var(--fontwhite3));
}
.item-PXvHYJ[style^="color: rgb(255, 255, 255)"],
.item-PXvHYJ[style*=" color: rgb(255, 255, 255)"] {
	color: rgb(var(--fontwhite1)) !important;
}
.item-PXvHYJ[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--vtextshadow);
}
.themed-OHr7kt.item-PXvHYJ:hover {
	color: rgb(var(--fontwhite2));
}
.side-8zPYf6 .themed-OHr7kt.item-PXvHYJ:hover,				/* sidebar				sideitem							*/
.topPill-30KHOu .themed-OHr7kt.item-PXvHYJ:hover {			/* sidebar				tabitems							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.side-8zPYf6 .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ,
.topPill-30KHOu .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}

.header-2RyJ0Y {											/* sidebar				sideitemheader						*/
	color: rgb(var(--fontwhite3));
}
.separator-gCa7yv {											/* sidebar				sideitemseparator					*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .foreground-26ym5y {								/* sidebar				sideitemlink						*/
	fill: rgb(var(--fontwhite3));
}
#app-mount .link-1IoFq-:hover .foreground-26ym5y {
	fill: rgb(var(--fontwhite1));
}

#app-mount .closeButton-1tv5uR {							/* closebutton			item								*/
	border-color: rgb(var(--fontwhite4));
}
#app-mount .closeButton-1tv5uR path.fill {
	fill: rgb(var(--fontwhite4));
}
#app-mount .closeButton-1tv5uR:hover {
	background-color: rgba(var(--vaccentcolor), 0.2);
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .closeButton-1tv5uR:hover path.fill {
	fill: rgb(var(--vaccentcolor));
}
#app-mount .keybind-KpFkfr {								/* closebutton			keybind								*/
	color: rgb(var(--fontwhite4));
}

.cardPrimary-1Hv-to, .cardPrimaryEditable-3KtE4g {			/* settingsitems		card								*/
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
.cardPrimary-1Hv-to {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.cardPrimaryEditable-3KtE4g {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.cardPrimaryOutline-29Ujqw {
	border-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .card-2qG0dv {
	color: rgb(var(--fontwhite1));
}

.title-31JmR4 {												/* settingsitems		settingstitle						*/
	color: rgb(var(--fontwhite1));
}
.divider-3573oO {											/* settingsitems		settingstitle						*/
	background-color: rgba(var(--fontwhite1), 0.3);
}

#app-mount .userSettingsAccount-2eMFVR .viewBody-2Qz-jg {	/* myaccount			info								*/
	color: rgb(var(--fontwhite3));
}
.questionMark-CWEQZn .icon-3a_Jgd {							/* myaccount			questionmark						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .avatarUploader-3XDtmn .removeButton-1hcZyG	{	/* myaccount			removeavatar						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .userSettingsSecurity-3IYeMF .codeCheckbox-1T0TTy {
	color: rgb(var(--fontwhite2));
}

															/* connections			platforms							*/
.connection-1fbD7X[style*="background-color: rgb(89, 54, 149)"] {
	background-color: rgba(89, 54, 149, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(203, 33, 32)"] {
	background-color: rgba(203, 33, 32, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(0, 157, 215)"] {
	background-color: rgba(0, 157, 215, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(24, 35, 50)"] {
	background-color: rgba(24, 35, 50, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(2, 31, 37)"] {
	background-color: rgba(2, 31, 37, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(0, 154, 229)"] {
	background-color: rgba(0, 154, 229, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(255, 69, 0)"] {
	background-color: rgba(255, 69, 0, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(29, 161, 242)"] {
	background-color: rgba(29, 161, 242, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(29, 185, 84)"] {
	background-color: rgba(29, 185, 84, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(53, 80, 137)"] {
	background-color: rgba(53, 80, 137, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(16, 124, 16)"] {
	background-color: rgba(16, 124, 16, 0.8) !important;
}
.connection-1fbD7X[style*="background-color: rgb(20, 41, 160)"] {
	background-color: rgba(20, 41, 160, 0.8) !important;
}
.accountBtn-2Nozo3 .accountBtnInner-sj5jLs {				/* connections			connectioninner						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.accountBtn-2Nozo3 .accountBtnInner-sj5jLs:hover {
	background-color: rgb(var(--vaccentcolor));
}
.connectionHeader-2MDqhu {									/* connections			header								*/
	border-bottom-color: rgba(var(--vtransparencycolor), 0.15);
}
.connectionHeader-2MDqhu .connectionAccountValue-3VdBGs {
	color: rgb(var(--fontwhite1));
}
.connectionHeader-2MDqhu .description-3_Ncsb {
	color: rgb(var(--fontwhite2)) !important;
	opacity: 1;
}
.subEnabledTitle-2ElRo_ {
	color: rgb(var(--fontwhite1));
}
.connectionDelete-2Odoln {									/* connections			delete								*/
	border-color: rgba(var(--fontwhite1), 0.3);
}
.connectionDelete-2Odoln:hover {
	border-color: rgb(var(--fontwhite1));
}
.connectionDelete-2Odoln:after,
.connectionDelete-2Odoln:before {
	background-color: rgba(var(--fontwhite1), 0.6);
}
.connectionDelete-2Odoln:hover:after,
.connectionDelete-2Odoln:hover:before {
	background-color: rgb(var(--fontwhite1));
}

#app-mount .codeRedemptionRedirect-1wVR4b {					/* payment				coderedem							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite1));
}

.emptyStateImage-2MrSNs {									/* giftinventory		no gifts							*/
	opacity: 0.6;
}

.guildHeader-3nh5RK {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
.guildSubscriptionSlots-JPXXvN {							/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.cardWrapper-2Min21 {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.cardWrapper-2Min21:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.cardWrapper-2Min21 .card-3AyPWq,							/* boostsettings		suggestioncard inner				*/
.cardWrapper-2Min21 .card-3AyPWq:hover {
	background-color: transparent;
}
#app-mount .gemIndicatorContainer-2jdECl {					/* boostsettings		suggestioncard circle				*/
	background-color: transparent;
}
#app-mount .paymentPane-3bwJ6A {							/* boostsettings		past transations					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .summaryInfo-2QFKUg {							/* boostsettings		past transations summary			*/
	color: rgb(var(--fontwhite1));
}
#app-mount .paymentHeader-3QlZQi {							/* boostsettings		past transations header				*/
	border-color: rgba(var(--fontwhite3), 0.5);
	color: rgb(var(--fontwhite3));
}
#app-mount .payment-xT17Mq {								/* boostsettings		past transations payment			*/
	background-color: transparent;
	color: rgb(var(--fontwhite2));
}
#app-mount .hoverablePayment-Yc6mK7:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .paymentText-2vaF7U {							/* boostsettings		past transations paymenttext		*/
	color: rgb(var(--fontwhite3));
}
#app-mount .expandedInfo-3kfShd {							/* boostsettings		past transations expandedinfo		*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .giftIcon-3DRGI6 {								/* boostsettings		past transations gifticon			*/
	color: rgb(var(--fontwhite1));
}
#app-mount .paginator-166-09 {								/* boostsettings		past transations paginator			*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .bottomDivider-1K9Gao {							/* boostsettings		past transations divider			*/
	border-bottom-color: rgba(var(--fontwhite3), 0.5);
}
#app-mount .tab-1kx2RU {									/* boostsettings		past transations tab				*/
	color: rgb(var(--fontwhite3));
}
#app-mount .appleRowHeader-241O5v {							/* boostsettings		past transations applerowheader		*/
	color: rgb(var(--fontwhite2));
}
#app-mount .appleRowBody-2B5tp2 {							/* boostsettings		past transations applerowbody		*/
	color: rgb(var(--fontwhite3));
}

.introHeader-4MPach {										/* hypesquad			header								*/
	color: rgb(var(--fontwhite1));
}
.introBlurb-3gFgTQ {										/* hypesquad			description							*/
	color: rgb(var(--fontwhite2));
}
.title-PMZpEi {												/* hypesquad			perktitle							*/
	color: rgb(var(--fontwhite1));
}
.description-1W0DiL {										/* hypesquad			description							*/
	color: rgb(var(--fontwhite2));
}
.attendeeCTA-3ZZQWt {										/* hypesquad			attendeeCTA							*/
	color: rgb(var(--fontwhite2));
}
.membershipDialogHouse1-3KhKE- {							/* hypesquad			membershipdialogs					*/
	background-color: rgba(156, 132, 239, 0.8);
}
.membershipDialogHouse2-35h9SY {
	background-color: rgba(244, 123, 103, 0.8);
}
.membershipDialogHouse3-15OBIQ {
	background-color: rgba(69, 221, 192, 0.8);
}

.container-3PXSwK {											/* voicesettings		voicebarcontainer					*/
	-webkit-mask: url('data:image/svg+xml;base64,PHN2ZyB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iOCIgaGVpZ2h0PSIyMCIgZmlsbD0iIzM2MzkzZiI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBkPSJNNCAyYTIgMiAwIDAgMC0yIDJ2MTJhMiAyIDAgMSAwIDQgMFY0YTIgMiAwIDAgMC0yLTJ6Ii8+PC9zdmc+');
}
#app-mount .progress-1IcQ3A {								/* voicesettings		voicebar							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.userSettingsVoice-iwdUCU .media-engine-video {				/* voicesettings		video								*/
	background: transparent;
}
#app-mount .userSettingsVoice-iwdUCU .previewOverlay-2O7_KC {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}

.option-n0icdO {											/* overlay				option								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.option-n0icdO:hover,
.option-n0icdO.selected-mKYnfr {
	box-shadow: 0 2px 0 rgba(var(--vtransparencycolor), 0.3);
}
.disabled-3I9jyo {
	color: rgba(var(--vtransparencycolor), 0.4);
}

.notificationsSound-27jFSh {								/* notifications		row									*/
	color: rgb(var(--fontwhite2));
	box-shadow: inset 0 -1px 0 0 rgba(var(--fontwhite4), 0.2);
}

#app-mount .row-2okwlC {									/* hotkeys				row									*/
	color: rgb(var(--fontwhite2));
	box-shadow: inset 0 -1px 0 rgba(var(--fontwhite4), 0.3);
}

#app-mount .card-FDVird:before {							/* settingscard			backdrop							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .button-2CgfFz {									/* settingscard			removebutton						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.6), 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .button-2CgfFz:hover {
	background-color: rgba(var(--vtransparencycolor), 0.7);
}

#app-mount .game-1ipmAa {									/* games				card								*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .notDetected-33MY4s {							/* games				nogame								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .nowPlayingAdd-1Kdmh_ {							/* games				descriptionhint						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .gameName-1RiWHm {								/* games				gamename							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .lastPlayed-3bQ7Bo,								/* games				lastplayed							*/
#app-mount .overlayStatusText-L2IACa {						/* games				overlaystatustext					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .overlayToggleIconOn-3UNmty .fill-1ugeBG {		/* games				overlaystatusicon					*/
	fill: rgb(var(--fontwhite3));
}
#app-mount .nowPlaying-284llR .lastPlayed-3bQ7Bo,
#app-mount .nowPlaying-284llR .overlayStatusText-L2IACa {
	color: rgb(var(--fontwhite2));
}
#app-mount .nowPlaying-284llR .overlayToggleIconOff-1kT42w .fill-1ugeBG,
#app-mount .nowPlaying-284llR .overlayToggleIconOn-3UNmty .fill-1ugeBG {
	fill: rgb(var(--fontwhite2));
}
#app-mount .gameNameInput-385LoS:focus,
#app-mount .gameNameInput-385LoS:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .text-GwUZgS,
#app-mount .title-2BxgL2 {
	color: rgb(var(--fontwhite4));
}

#app-mount .installationPath-24giJj {						/* gamelibrary			path								*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .usageInfo-2WQAwr {								/* gamelibrary			usageinfo							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .background-yZEZik {								/* gamelibrary			usagebar							*/
	stroke: rgb(var(--vtransparencycolor), 0.5);
}
#app-mount .rowTitle-3xCiqy {								/* gamelibrary			rowtitle							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .defaultIndicator-2X8Auf {						/* gamelibrary			rowtag								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .rowBody-10yI-R {								/* gamelibrary			rowdescription						*/
	color: rgb(var(--fontwhite3));
}

.preview-2nSL_2 {											/* appearance			preview								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .item-3eFBNF {									/* languagesettings		row									*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
.item-3eFBNF:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.item-3eFBNF.selected-2DeaDa {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

#app-mount .experimentDate-2ymg99 {							/* experiments			date								*/
	color: rgb(var(--fontwhite3));
}


/* ~~~~		12.		GUILDSETTINGS					~~~~ */

#app-mount .emojiAliasInput-1y-NBz .emojiInput-1aLNse {		/* emojisettings		nameinput							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
}

#app-mount .selectableItem-1MP3MQ {							/* auditlogs			popoutitem							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .selectableItem-1MP3MQ:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .selectableItem-1MP3MQ[style*=" color: rgb(255, 255, 255)"] {
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .selectableItem-1MP3MQ polyline[stroke="#ffffff"] {
	stroke: rgb(var(--fontwhite1));
}

#app-mount .auditLog-3jNbM6 {								/* auditlogs			logitem								*/
	border-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite4));
}
#app-mount .headerClickable-2IVFo9,							/* auditlogs			loginner							*/
#app-mount .headerDefault-1wrJcN {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .headerExpanded-CUEwZ5 {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
#app-mount .divider-1pnAR2 {								/* auditlogs			loginnerdivider						*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .changeDetails-bk98pu {							/* auditlogs			logdetails							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .userHook-3AdCBF {								/* auditlogs			userhook							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .auditLog-3jNbM6 strong {						/* auditlogs			targets								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .timestamp-1mruiI {								/* auditlogs			timestamp							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .expandForeground-1nZ4VR {						/* auditlogs			expandarrow							*/
	stroke: rgb(var(--fontwhite2));
}
.themeOverrideLight-3bx_5B.icon-RTGJu3,						/* auditlogs			logicon								*/
.themeOverrideDark-1u5Vo0.icon-RTGJu3,
#app-mount .icon-RTGJu3 {
	background: none !important;
}
.icon-RTGJu3:before {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: rgb(var(--fontwhite1));
}
.icon-RTGJu3.targetAll-13V3n6:before {
	-webkit-mask: url(https://discordapp.com/assets/fc3f5f9be1a4db14b02336b7cb02e6ce.svg);
}
.icon-RTGJu3.targetBan-3mbIPL:before {
	-webkit-mask: url(https://discordapp.com/assets/edb23a53ea40ac60f212ebae66e5c5c7.svg);
}
.icon-RTGJu3.targetChannel-TrRFlx:before {
	-webkit-mask: url(https://discordapp.com/assets/343c9ff4c775c66a7d4af1f8691c34e0.svg);
}
.icon-RTGJu3.targetGuild-mDWfAV:before {
	-webkit-mask: url(https://discordapp.com/assets/30af96a386520760ad107c5b77ba002a.svg);
}
.icon-RTGJu3.targetEmoji-3vhPhM:before {
	-webkit-mask: url(https://discordapp.com/assets/7a9bf92329dad473ef0383ae75367215.svg);
}
.icon-RTGJu3.targetInvite-1RQBlr:before {
	-webkit-mask: url(https://discordapp.com/assets/4b33371531a1a89f99296a73fc9ef588.svg);
}
.icon-RTGJu3.targetMemberRole-jowY3I:before {
	-webkit-mask: url(https://discordapp.com/assets/a9098042cb36b955c5021259f1d48f91.svg);
}
.icon-RTGJu3.targetMember-2iuwxX:before {
	-webkit-mask: url(https://discordapp.com/assets/af043346e036ef7b1aac1cf42cd1e699.svg);
}
.icon-RTGJu3.targetPermission-ZRUN5n:before {
	-webkit-mask: url(https://discordapp.com/assets/2a37995eb832bae805190a93ba043857.svg);
}
.icon-RTGJu3.targetRole-2MoUny:before {
	-webkit-mask: url(https://discordapp.com/assets/0176a91b4c44ed05c05af68784e78da8.svg);
}
.icon-RTGJu3.targetVanityUrl-3OpsYX:before {
	-webkit-mask: url(https://discordapp.com/assets/84215a5fec3d9de9960a225143238d74.svg);
}
.icon-RTGJu3.targetWebhook-1xS7Z7:before {
	-webkit-mask: url(https://discordapp.com/assets/a6975850d800aa86162b4aa5f18c41ac.svg);
}
.icon-RTGJu3.targetWidget-3hFVSM:before {
	-webkit-mask: url(https://discordapp.com/assets/4ac0e382cc7b8aa0cb1d6d074b0e8ba5.svg);
}
.icon-RTGJu3.targetMessage-2kBYMT:before {
	-webkit-mask: url(https://discordapp.com/assets/8c85e30795486caa8caacd829703459d.svg);
}
.icon-RTGJu3.targetIntegration-3rnyMN:before {
	-webkit-mask: url(https://discordapp.com/assets/da8463a04b4a289801d2516f50eb4c19.svg);
}

.addRoleIcon-3YjErH {										/* rolesettings			addrolebutton						*/
	-webkit-mask: url(https://discordapp.com/assets/cef02719c12d8aaf38894c16dca7fbe6.svg);
	background: rgb(var(--fontwhite3));
	object-position: -9999999px -9999999px;
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm {		/* rolesettings			colorswatchnocolor					*/
	border-color: rgba(var(--fontwhite1), 0.3);
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm .colorPickerDropperFg-3jYKWI {
	fill: rgb(var(--fontwhite1));
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm polyline {
	stroke: rgb(var(--fontwhite1));
}

.descriptionBox-1EKQKL {									/* templatesettings		descriptionbox					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .tierHeaderLocked-1a2opw {						/* boostsettings		tierheaderlocked					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierLock-1oFMOZ {								/* boostsettings		tierlock							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .tierHeaderUnlocked-2RhWqn {						/* boostsettings		tierheaderunlocked					*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .tierUnlocked-27DwHo {							/* boostsettings		tierunlocked						*/
	background-color: rgb(var(--fontwhite1));
}
#app-mount .tierBody-x9kBBp {								/* boostsettings		tierbody							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierInProgress-3mBoXq {							/* boostsettings		tiermilestone						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .background-3xPPFc {								/* boostsettings		tierbar	(settings)					*/
	color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .member-1q7VfX {									/* membersettings		membercard							*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .member-1q7VfX .name-8yzEIY {					/* membersettings		membercardname						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .member-1q7VfX .tag-1YGWN9 {						/* membersettings		membercardtag						*/
	color: rgb(var(--fontwhite4));
}
#app-mount .actionButton-VzECiy {							/* membersettings		addrolebutton						*/
	border-color: rgb(var(--fontwhite4));
	color: rgb(var(--fontwhite3));
}
#app-mount .member-1q7VfX .overflowIconFg-QMRRFI {			/* membersettings		3-doticon							*/
	fill: rgb(var(--fontwhite1));
}

#app-mount .overflowRolesPopout-140n9i,						/* membersettings		roleoverflow popout					*/
#app-mount .overflowRolesPopoutArrow-2O66oH {
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.2), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.2);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.overflowRolesPopout-140n9i:after,
.overflowRolesPopout-140n9i:before,
.overflowRolesPopoutArrow-2O66oH:after,
.overflowRolesPopoutArrow-2O66oH:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.overflowRolesPopout-140n9i:after,
.overflowRolesPopoutArrow-2O66oH:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
}
.overflowRolesPopout-140n9i:before,
.overflowRolesPopoutArrow-2O66oH:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.overflowRolesPopoutHeaderIcon-6PNEZA path {
	fill: rgb(var(--fontwhite2));
}
.overflowRolesPopoutHeaderText-1SW-y3 {
	color: rgb(var(--fontwhite2));
}

#app-mount .inviteSettingsInviteRow-3p2O-N {				/* invitesettings		invitecard							*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite2));
}
.user-3x-NP9 {												/* invitesettings		user								*/
	color: rgb(var(--fontwhite1));
}
.channelName-13-Sm9 {										/* invitesettings		channelname							*/
	color: rgb(var(--fontwhite3));
}

#app-mount .bannedUser-1IalTM {								/* bansettings			bancard								*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .bannedUser-1IalTM .username-1b3MVI {			/* invitesettings		username							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .bannedUserModal-3RJCOV .reasonHeader-2etdjy {	/* invitesettings		banmodalreasonheader				*/
	color: rgb(var(--fontwhite2));
}
#app-mount .bannedUser-1IalTM .username-1b3MVI .discrim-oGb-FO,
#app-mount .bannedUserModal-3RJCOV .reason-YbfGC6,			/* invitesettings		banmodalreason						*/
#app-mount .bannedUserModal-3RJCOV .userDiscrim-1D2NlF {	/* invitesettings		discriminator						*/
	color: rgb(var(--fontwhite3));
}


/* ~~~~		13.		MODALS							~~~~ */

#app-mount .root-1gCeng,									/* modal				container (foldersettings)			*/
#app-mount .modal-yWgWj- {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	border-radius: 5px;
}
.root-1gCeng:after,
.root-1gCeng:before,
.modal-yWgWj-:after,
.modal-yWgWj-:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.root-1gCeng:after,
.modal-yWgWj-:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.root-1gCeng:before,
.modal-yWgWj-:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.root-1gCeng .modal-yWgWj-:after,
.root-1gCeng .modal-yWgWj-:before {
	display: none;
}
#app-mount .footer-2gL1pp {									/* modal				footer							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}
#app-mount .closeButton-1tv5uR,								/* modal				closebutton						*/
#app-mount .close-hZ94c6 {
	color: rgb(var(--fontwhite1));
}
#app-mount .closeButton-1tv5uR:hover,
#app-mount .close-hZ94c6:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .guildName-3WI6ml,								/* modal				guildname						*/
#app-mount .date-2WJGyu,
#app-mount .override-2YgiXd,
#app-mount .overrideHighlight-YPcBxt {
	color: rgb(var(--fontwhite3));
}
#app-mount .channelName-28iMRJ {							/* modal				channelname						*/
	color: rgb(var(--fontwhite1));
}

.tabBarContainer-1s1u-z {									/* modal				tabbarcontainer					*/
	border-top-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .modal-6GHvdM .tabBarContainer-1s1u-z {
	background: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.1);
}
.top-28JiJ- .themed-OHr7kt.item-PXvHYJ,						/* modal				tabbaritem						*/
.top-28JiJ- .item-PXvHYJ[style*="rgba(79, 84, 92, 0.4)"],
.top-28JiJ- .item-PXvHYJ[style*="rgba(255, 255, 255, 0.4)"],
.themed-OHr7kt.tabBarItem-1b8RUP,
.tabBarItem-1b8RUP[style*="rgba(79, 84, 92, 0.4)"],
.tabBarItem-1b8RUP[style*="rgba(255, 255, 255, 0.4)"] {
	color: rgba(var(--fontwhite1), 0.4) !important;
}
.top-28JiJ- .themed-OHr7kt.item-PXvHYJ:hover,				/* modal				tabbaritem hover				*/
.top-28JiJ- .item-PXvHYJ[style*="rgba(79, 84, 92, 0.6)"],
.top-28JiJ- .item-PXvHYJ[style*="rgba(255, 255, 255, 0.6)"],
.themed-OHr7kt.tabBarItem-1b8RUP:hover,
.tabBarItem-1b8RUP[style*="rgba(79, 84, 92, 0.6)"],
.tabBarItem-1b8RUP[style*="rgba(255, 255, 255, 0.6)"] {
	border-color: rgba(var(--fontwhite1), 0.6) !important;
	color: rgba(var(--fontwhite1), 0.6) !important;
}
.top-28JiJ- .themed-OHr7kt.item-PXvHYJ.selected-3s45Ha,		/* modal				tabbaritem selected				*/
.top-28JiJ- .item-PXvHYJ[style*="rgb(79, 84, 92)"],
.top-28JiJ- .item-PXvHYJ[style*="rgb(255, 255, 255)"],
.themed-OHr7kt.tabBarItem-1b8RUP.selected-3s45Ha,
.tabBarItem-1b8RUP[style*="rgb(79, 84, 92)"],
.tabBarItem-1b8RUP[style*="rgb(255, 255, 255)"] {
	border-color: rgb(var(--fontwhite1)) !important;
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .content-8biNdB p,								/* modal				listentry						*/
#app-mount .content-8biNdB ul li {
	color: rgb(var(--fontwhite2));
}
#app-mount .content-8biNdB ul li:before {					/* modal				listentrydot					*/
	background-color: rgb(var(--fontwhite2));
}

/* ----		13.1.	USERMODAL						----- */

#app-mount .root-SR8cQa {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.root-SR8cQa:after,
.root-SR8cQa:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.root-SR8cQa:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.root-SR8cQa:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .topSectionNormal-2-vo2m {						/* modal				headernormal						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.topSectionPlaying-1J5E4n {									/* modal				headerplaying						*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.headerFill-adLl4x {										/* modal				activity							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.body-3ND3kc {												/* modal				body								*/
	background-color: transparent;
}
.discriminator-xUhQkU {										/* header				discriminator						*/
	color: rgb(var(--fontwhite1));
}
.topSectionNormal-2-vo2m .discriminator-xUhQkU {
	color: rgb(var(--fontwhite2));
}
.additionalActionsIcon-1FoUlE,								/* header				additionalactionsicon				*/
.topSectionNormal-2-vo2m .additionalActionsIcon-1FoUlE,
.topSectionNormal-2-vo2m .additionalActionsIcon-1FoUlE:hover {
	color: rgb(var(--fontwhite1));
}
.topSectionNormal-2-vo2m .tabBarContainer-1s1u-z {			/* header				tabbarcontainer						*/
	border-top-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .header-QKLPzZ .textRow-19NEd_ {
	color: rgb(var(--fontwhite2));
}
#app-mount .topSectionNormal-2-vo2m .header-QKLPzZ .textRow-19NEd_ {
	color: rgb(var(--fontwhite3));
}
#app-mount .activityProfile-2bJRaP .headerText-1HLrL7 {		/* header				activitytext						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .activityProfile-2bJRaP .content-3JfFJh,			/* header				activitycontent						*/
#app-mount .activityProfile-2bJRaP .details-38sfDr,			/* header				activitydetails						*/
#app-mount .activityProfile-2bJRaP .name-29ETJS {			/* header				activityname						*/
	color: rgb(var(--fontwhite2));
}
.activityName-1IaRLn,
.nameNormal-2lqVQK,
.nameWrap-3Z4G_9 {
	color: rgb(var(--fontwhite1));
}
.userInfoSectionHeader-CBvMDh {								/* body					sectionheader						*/
	color: rgb(var(--fontwhite3));
}
.userInfoSection-2acyCx + .userInfoSection-2acyCx {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
.connectedAccount-36nQx7 {									/* body					connectedaccount					*/
	border-color: rgba(var(--fontwhite4), 0.3);
}
.connectedAccountName-f8AEe2 {								/* body					connectedaccountname				*/
	color: rgb(var(--fontwhite2));
}
.connectedAccountOpenIcon-2cNbq5 {
	color: rgb(var(--fontwhite2));
}
.connectedAccountOpenIcon-2cNbq5:hover {
	color: rgb(var(--fontwhite1));
}
.listRow-hutiT_ {											/* body					listrow								*/
	color: rgb(var(--fontwhite2));
}
.guildNick-3uAm3i {											/* body					guildnick							*/
	color: rgb(var(--fontwhite3));
}
.listRow-hutiT_:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite1));
}
.listRow-hutiT_:hover .guildNick-3uAm3i {
	color: rgb(var(--fontwhite2));
}
.emptyIcon-pGTAhd {											/* body					emptypic							*/
	opacity: 0.6;
}
.emptyText-6tYmO5 {											/* body					emptytext							*/
	color: rgb(var(--fontwhite2));
}

/* ----		13.2.	GUILDADD/CREATION				----- */

#app-mount .wrapper-2ZbzR9 {								/* modal				wrapper								*/
	background: transparent;
}
.wrapper-2ZbzR9 > * > * {
	top: unset !important;
	transform: unset !important;
}
#app-mount .slide-2pHaq5 {									/* modal				slide								*/
	background: transparent;
}
#app-mount .action-1lSjCi {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 4px rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .actionBody-1qj65C {								/* modal				actiontext							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .actionButton-2PeQbJ {							/* modal				actionbutton						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .or-3THJsp {										/* modal				oricon								*/
	-webkit-mask: url(https://discordapp.com/assets/b9cf5548cc5a23a6943f194a0ace88f8.svg) center/52px 52px no-repeat;
	background: none;
	color: rgb(var(--fontwhite1));
	line-height: 306px;
    order: unset;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    border-radius: unset;
    border: unset;
}
.or-3THJsp:after,
.or-3THJsp:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.or-3THJsp:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.or-3THJsp:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .cancelButton-RGXhAE {							/* modal				cancelbutton						*/
	color: rgb(var(--fontwhite2));
}
#app-mount .cancelButton-RGXhAE:hover {
	color: rgb(var(--fontwhite1));
	border-bottom-color: rgb(var(--fontwhite1));
}
#app-mount .cancelButton-RGXhAE:before {
	-webkit-mask: url(https://discordapp.com/assets/eb57a76361c43375bf23207ad2acc631.svg) 0/18px 12px no-repeat;
	background: rgb(var(--fontwhite2));
}
#app-mount .cancelButton-RGXhAE:hover:before {
	background: rgb(var(--fontwhite1));
}

#app-mount .description-QF3836 {							/* create				description							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .helpText-h3r3wC {								/* create				helptext							*/
	color: rgb(var(--fontwhite2));
}
.avatar-21196O {											/* create				avataruploader						*/
	border-color: rgb(var(--fontwhite1));
}
.avatarUploaderAcronym-3SioMc,								/* create				avataruploaderacronym				*/
.avatarUploaderHint-3SN212 {								/* create				avataruploaderhint					*/
	color: rgb(var(--fontwhite1));
}
.avatarUploader-3XDtmn .sizeInfo-SKMPPw {					/* create				avatarsizeinfo						*/
	color: rgb(var(--fontwhite2));
}
#app-mount .regionSelect-3lf4eE .regionSelectInner-24f4Ce,	/* create				regionselect						*/
#app-mount .regionSelect-3lf4eE button {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .regionSelect-3lf4eE:hover button {
	color: rgb(var(--fontwhite1));
}
#app-mount .regionSelectName-2-2FWh {						/* create				regionselectname					*/
	color: rgb(var(--fontwhite2));
}

#app-mount .description-Bw8krY {							/* join					description							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .inputLabel-vJ2Z0B {								/* join					inputlabel							*/
	color: rgb(var(--fontwhite2));
}

/* ----		13.3.	REGIONSELECTMODAL				---- */

#app-mount .regionSelectModal-12e-57 {						/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.regionSelectModal-12e-57:after,
.regionSelectModal-12e-57:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.regionSelectModal-12e-57:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.regionSelectModal-12e-57:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3 {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalFooter-20C5iA {
	color: rgb(var(--fontwhite3));
}

/* ----		13.4.	UPLOADMODAL						---- */

#app-mount .uploadModal-2ifh8j {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	border-radius: 10px;
}
.uploadModal-2ifh8j:after,
.uploadModal-2ifh8j:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 10px;
	z-index: -1;
}
.uploadModal-2ifh8j:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.uploadModal-2ifh8j:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc {
	width: unset;
}
.uploadModal-2ifh8j .inner-3nWsbo,							/* modal				inner								*/
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo {
	border-color: rgba(var(--fontwhite1), 0.5);
	color: rgb(var(--fontwhite1));
}
.uploadModal-2ifh8j .inner-3nWsbo .file-34mY5K .description-2ug5H_ .filename-ovv3c5 {
	color: rgb(var(--fontwhite1));
}
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo .title-2Vtl4y {
	text-shadow: 1px 1px var(--vtextshadow);
}
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo .instructions-2Du9gG {
	color: rgb(var(--fontwhite3));
	text-shadow: 1px 1px var(--vtextshadow);
}
.content-P4SiGI {											/* modal				errorcontent						*/
	color: rgb(var(--fontwhite3));
}
.navArrow-3Q9QPC {											/* modal				navarrow							*/
	-webkit-mask: url(https://discordapp.com/assets/c83861b2303b7ee40c419e9590d57f11.svg) center/contain no-repeat;
	background-color: rgb(var(--fontwhite3));
	object-position: -9999999px -9999999px;
}
.uploadModal-2ifh8j .inner-zqa7da {							/* modal				channeltextarea						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.uploadModal-2ifh8j .footer-3mqk7D {						/* modal				footer								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.uploadModal-2ifh8j .checkbox-1ix_J3 {						/* modal				checkbox							*/
	border-color: rgb(var(--fontwhite1)) !important;
}
.uploadModal-2ifh8j .inner-3nWsbo .file-34mY5K .icon-kyxXVr.image-2yrs5j {
	box-shadow: 0 2px 8px rgba(var(--vtransparencycolor), 0.4);
}

/* ----		13.5.	KEYBOARDSHORTCUTSMODAL			---- */

#app-mount .keyboardShortcutsModal-3piNz7 {					/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.keyboardShortcutsModal-3piNz7:after,
.keyboardShortcutsModal-3piNz7:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.keyboardShortcutsModal-3piNz7:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.keyboardShortcutsModal-3piNz7:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .modalTitle-37O4n6 {								/* modal				title								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .modalSubtitle-1Pj5nv {							/* modal				subtitle							*/
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .keyboardShortcutList-13cQ-8 .keybindGroup--6Qp-w .keybindDescription-2RDbC2 {
	color: rgb(var(--fontwhite2));
}
#app-mount .keybindShortcut-1BD6Z1 {
	color: rgb(var(--fontwhite1));
}
#app-mount .keybindShortcut-1BD6Z1 span {
	color: rgb(var(--fontwhite1));
	box-shadow: inset 0 -4px 0 rgb(0, 0, 0, 0.4);
	border: 1px solid rgb(0, 0, 0, 0.4);
	background-color: rgb(var(--fontwhite4));
}
#app-mount .keybindShortcut-1BD6Z1 span [fill^="#"] {
	fill: rgb(var(--fontwhite1));
}

/* ----		13.6.	QUICKSWITCHER					---- */

#app-mount .quickswitcher-3JagVE {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.quickswitcher-3JagVE:after,
.quickswitcher-3JagVE:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.quickswitcher-3JagVE:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.quickswitcher-3JagVE:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .input-2VB9rf {									/* modal				input								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .input-2VB9rf::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .header-13MUnb {									/* modal				header								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .resultFocused-3aIoYe {							/* modal				resultfocused						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .contentUnread-3gTHvA {							/* modal				contentunread						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .contentDefault-16dKSY,							/* modal				contentdefault						*/
#app-mount .icon-30q1Or,									/* modal				icon								*/
#app-mount .misc-1CT3G7 {									/* modal				misc								*/
	color: rgb(var(--fontwhite3));
}
#app-mount .note-S--UP5 {									/* modal				note								*/
	color: rgb(var(--fontwhite4));
}
#app-mount .resultFocused-3aIoYe .contentDefault-16dKSY,
#app-mount .resultFocused-3aIoYe .icon-30q1Or,
#app-mount .contentUnread-3gTHvA .icon-30q1Or,
#app-mount .resultFocused-3aIoYe .misc-1CT3G7 {
	color: rgb(var(--fontwhite1));
}
#app-mount .resultFocused-3aIoYe .note-S--UP5 {
	color: rgb(var(--fontwhite3));
}
#app-mount .tipsWithoutResults-lGY-De,
#app-mount .tipsWithResults-HhTE9b {
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .keybindShortcutTipsSelect-HDyfe8:last-of-type:before {
	background-color: rgba(var(--fontwhite4), 0.3);
}

/* ----		13.7.	INVITEMODAL						---- */

#app-mount .contentWrapper-3WC1ID {								/* modal				guildinvitemodal				*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.contentWrapper-3WC1ID:after,
.contentWrapper-3WC1ID:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-3WC1ID:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.contentWrapper-3WC1ID:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

#app-mount .friendSelected-1sa4bG,								/* modal				groupdmrow						*/
#app-mount .inviteRow-2L02ae:hover {							/* modal				guildrow						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .friend-3KALPe,										/* modal				groupdmrow						*/
#app-mount .inviteRowName-1tVaxu {								/* modal				username						*/
	color: rgb(var(--fontwhite2));
}
#app-mount .friendSelected-1sa4bG,
#app-mount .inviteRow-2L02ae:hover .inviteRowName-1tVaxu {
	color: rgb(var(--fontwhite1));
}
#app-mount .checkBoxLabel-4PWfpk,
#app-mount .footerText-2a7NxZ,
#app-mount .subTitle-3TUjmF,
#app-mount .subtitle-2P4u9v,
#app-mount .subText-bCySlS {
	color: rgb(var(--fontwhite3));
}
.tag-2gHSR7 {													/* modal				added user						*/
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
.pill-1dHPfk {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}

/* ----		13.8.	LOGINSCREEN						---- */

#app-mount .wrapper-3Q5DdO {								/* login				wrapper								*/
	background: transparent;
}
.wrapper-3Q5DdO:before,										/* login				winbuttonshadow						*/
.wrapper-3Q5DdO .rightSplit-2US0xy,							/* login				background							*/
.wrapper-3Q5DdO .canvas-3XuBXe {							/* login				movingshadow						*/
	display: none;
}
#app-mount .authBox-hW6HRx {								/* login				modal								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
	position: relative;
	overflow: hidden;
}
#app-mount .quote-3aooyW {									/* login				loadingquote						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .contentBase-11jeVK {							/* login				loadingcontent						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .problems-3mgf6w {								/* login				loadingproblems						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .problemsText-1Yx-Kl {							/* login				loadingproblemtext					*/
	color: rgb(var(--fontwhite3));
}

/* ----		13.9.	TERMACCEPTMODAL					---- */

#app-mount .modal-DRZfgq {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.modal-DRZfgq:after,
.modal-DRZfgq:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.modal-DRZfgq:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.modal-DRZfgq:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

[style*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"],	/* modal				image								*/
[src*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"] {
	filter: brightness(85%) invert(100%);
	opacity: 0.7;
}

#app-mount .modal-DRZfgq .checked-3_4uQ9 {					/* modal				ackcheckbox							*/
	background-color: rgb(var(--vaccentcolor));
}
#app-mount .modal-DRZfgq .checkbox-1ix_J3 [stroke="#7289da"] {
	stroke: rgb(var(--fontwhite1)) !important;
}
#app-mount .ack-2yIUvY {									/* modal				acklabel							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .buttonContainer-3S_miP {						/* modal				footer							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}

/* ----		13.10.	DOWNLOADAPPMODAL				---- */

#app-mount .downloadApps-wbBFdZ {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.downloadApps-wbBFdZ:after,
.downloadApps-wbBFdZ:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.downloadApps-wbBFdZ:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.downloadApps-wbBFdZ:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.downloadApps-wbBFdZ .header-nJMe-Q {
	color: rgb(var(--fontwhite2));
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 {
	border-color: rgb(var(--fontwhite3));
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 p {
	color: rgb(var(--fontwhite3));
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 .downloadButton-1bWXpg {
	background-color: rgb(var(--fontwhite3));
}
.downloadApps-wbBFdZ .footer-1nkeBm {
	color: rgb(var(--fontwhite3));
}

/* ----		13.11.	GUILDBOOSTMODAL					---- */

.carouselContainer-2-vIZS {									/* modal				scrollercontainer					*/
	-webkit-mask: linear-gradient(to right, rgba(0,0,0,0) 0px, rgba(0,0,0,1) 60px, rgba(0,0,0,1) calc(100vw - 60px), rgba(0,0,0,0) 100vw);
}
.carouselGradientEdge-2W94ou {								/* modal				scrollergradient					*/
	display: none;
}
#app-mount .subscriberCount-27QHc5 {						/* modal				subcount							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .subscriberCount-27QHc5 strong {
	color: rgb(var(--fontwhite2));
}
#app-mount .moreSubscribers-1cuWDE {						/* modal				suboverflow							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

#app-mount .subscribersPopout-2CP6Ln {						/* subpopout			container							*/
	background-color: transparent;
	box-shadow: 0 2px 10px rgba(var(--vtransparencycolor), 0.2);
	overflow: hidden;
}
.subscribersPopout-2CP6Ln:after,
.subscribersPopout-2CP6Ln:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.subscribersPopout-2CP6Ln:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.35));
}
.subscribersPopout-2CP6Ln:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .subscribersPopoutUser-3rC75S {					/* subpopout			users								*/
	color: rgb(var(--fontwhite3));
}

#app-mount .ctaBar-2UsjF2 {									/* current boost stats	container							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	background-image: url(https://discordapp.com/assets/94ff6fdc535b6ecb7b1bc54f2dd56a10.svg);
}
.guildIcon-3raYf3 {											/* current boost stats	guild icon							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .perk-2WeBWW {									/* modal				perkcard							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

#app-mount .tierHeaderLocked-1s2JJz {						/* modal				tierheaderlocked 					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierLock-3CSxSX {								/* modal				tierlock 							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .tierHeaderUnlocked-1n-OTI {						/* modal				tierheaderunlocked 					*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .tierUnlocked-25K6Kv {							/* modal				tierunlocked 						*/
	background-color: rgb(var(--fontwhite1));
}
#app-mount .boostCount-UFqabz {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierBody-16Chc9 {								/* modal				tierbody 							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierNoneContainer-3hhK3h {						/* modal				tiernonecontainer					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.tierNoneCard-peD7hV {										/* modal				tiernonecard						*/
	opacity: 0.6;
}
#app-mount .tierNoneText-2OvCv7 {
	color: rgb(var(--fontwhite3));
}
#app-mount .tierCloseHint-380zIA,							/* modal				tierclose							*/
#app-mount .tierCloseClose-2z5dSa {
	color: rgb(var(--fontwhite1));
}
#app-mount .tierMarkerBackground-3q29am {					/* modal				tiermilestone 						*/
	background: transparent;
}
#app-mount .tierMarkerInProgress-24LMzJ {
	background: rgba(var(--vtransparencycolor), 0.3) !important;
}
#app-mount .selectedTier-1JkO7i .tierMarker-5HkGJ_ {
	box-shadow: 0 4px 8px rgba(var(--vtransparencycolor), 0.24);
}
#app-mount .tierMarkerLabel-2PluTw {						/* modal				tiermilestonelabel					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .selectedTier-1JkO7i .tierMarkerLabel-2PluTw {
	color: rgb(var(--fontwhite1));
}
#app-mount .barBackground-2EEiLw {							/* modal				tierbar 								*/
	background: linear-gradient(to right, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 3%, rgba(var(--vtransparencycolor), 0.3) 3%, rgba(var(--vtransparencycolor), 0.3) 30.2%, rgba(0,0,0,0) 30.2%, rgba(0,0,0,0) 36.2%, rgba(var(--vtransparencycolor), 0.3) 36.2%, rgba(var(--vtransparencycolor), 0.3) 63.5%, rgba(0,0,0,0) 63.5%, rgba(0,0,0,0) 69.5%, rgba(var(--vtransparencycolor), 0.3) 69.5%, rgba(var(--vtransparencycolor), 0.3) 96.7%, rgba(0,0,0,0) 96.7%, rgba(0,0,0,0) 100%);
}
.barSecondary-3B1aP2 {
	background-color: rgb(var(--vaccentcolor));
}
.wrapper-3nSjSv .heading-4znNKq {							/* modal				boostaddwrapper header						*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.tier-1EY-yj {												/* modal				boostaddwrapper tier						*/
	background-color: rgb(var(--vtransparencycolor), 0.3);
}
#app-mount .giftIcon-2Pjbiy {								/* modal				gifticon							*/
	color: rgb(var(--fontwhite3));
	margin: 0 18px;
}
#app-mount .button-38aScr:hover .giftIcon-2Pjbiy {
	color: rgb(var(--fontwhite2));
}
#app-mount .button-38aScr:active .giftIcon-2Pjbiy {
	color: rgb(var(--fontwhite1));
}

.header-1F6gxU {											/* prebuy popout		header								*/
	background: rgba(var(--vtransparencycolor), 0.3);
	padding-bottom: 10px;
	margin-bottom: 10px;
}
#app-mount .iconWrapper-3LVgIo {							/* prebuy popout		amount icon wrapper					*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
.icon-TYbVk4:hover {										/* prebuy popout		amount icon							*/
	background: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.upsellFooter-6EgwMe {										/* prebuy popout		footer details						*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
.perksList-1vtwXn {											/* prebuy popout		perkslist							*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
.perkRow-2dYUqs {											/* prebuy popout		perkrow								*/
	border-bottom-color: rgba(var(--fontwhite3), 0.3);
}

#app-mount .selectGuild-1Ygl76:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .tierPill-3gJ0eN {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

/* ----		13.12.	NEWUSERMODAL					---- */

#app-mount .modalNewUser-3IRw8L {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border-radius: 5px;
	overflow: hidden;
	min-height: unset;
}
.modalNewUser-3IRw8L:after,
.modalNewUser-3IRw8L:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.modalNewUser-3IRw8L:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.modalNewUser-3IRw8L:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

.modalNewUser-3IRw8L > .steps-370EKx {
	background: transparent;
	height: unset;
}
.modalNewUser-3IRw8L > .steps-370EKx > li {
	position: unset;
}
.modalNewUser-3IRw8L > .steps-370EKx .step1-28s17G {
	background: none;
}
.form-236Xmo .formActions-1-Snm- {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border: none;
}
.form-236Xmo .btnDefault-3gHhPM {
	background: transparent;
	border-color: transparent;
}

/* ----		13.13.	REACTIONSMODAL					---- */

#app-mount .sidebar-1-SQro {								/* modal				sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .reactors-Blmlhw {								/* modal				list								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .reactionDefault-GBA58K:hover {					/* modal				reaction							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .reactionSelected-1pqISm {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .count-1vzEyg {									/* modal				reaction count						*/
	color: rgb(var(--fontwhite2));
}
#app-mount .reactionDefault-GBA58K:hover .count-1vzEyg,
#app-mount .reactionSelected-1pqISm .count-1vzEyg {
	color: rgb(var(--fontwhite1));
}
#app-mount .nickname-miBZxb {								/* modal				nickname							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .username-Af3M5Y {								/* modal				username							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .discriminator-byOsvi {							/* modal				discriminator						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .tagFaded-WP86yt {
	opacity: 0.5;
}
#app-mount .remove-3V-yj8 {									/* modal				remove								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .remove-3V-yj8:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}

/* ----		13.14.	GUILDTEMPLATEMODAL				---- */

.ctaSection-izWwhs {										/* modal				ctasection							*/
	background-color: transparent;
}
.formSection-1NFAGI {										/* modal				formsection							*/
	background-color: transparent;
}

.divider-2gQcba {											/* modal				divider								*/
	border-color: rgba(var(--fontwhite3), 0.5);
}

.usagePill-2WGS4A {											/* modal				usagepill 1							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.usagePill-_nSrnP {											/* modal				usagePill 2							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.channelsWrapper-2HhUER {									/* modal				channelswrapper						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.channel-OaJouZ {											/* modal				channel								*/
	color: rgb(var(--fontwhite3));
}

.rolesWrapper-2yOx9S {										/* modal				roleswrapper							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .role-3paDXR {									/* modal				role								*/
	border-color: rgba(var(--fontwhite3), 0.6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-3paDXR[style*="border-color: rgba(185, 187, 190, 0.6)"] {
	border-color: rgba(var(--fontwhite3), 0.6) !important;
}
#app-mount .role-3paDXR .roleName-1JcOmP {					/* modal				rolename							*/
	color: rgb(var(--fontwhite1));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-3paDXR .roleCircle-3DE8xJ {				/* modal				rolecircle							*/
	position: absolute;
	background-color: rgb(var(--fontwhite3));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	left: 0;
	top: 0;
}
#app-mount .role-3paDXR .roleCircle-3DE8xJ[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--fontwhite3)) !important;
}

/* ----		13.15.	GUILDWELCOMEMODAL				---- */

.optionContainer-15srkc {									/* modal				option								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.optionContainer-15srkc:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}


/* ~~~~		14.		POPOUTS							~~~~ */

#app-mount .popout-2iWAc-:not(.noShadow-3pu20z) {
	box-shadow: 0 0 1px rgba(var(--vtransparencycolor), 0.2), 0 1px 4px rgba(var(--vtransparencycolor), 0.1);
}
.popout-2iWAc-[style*="translateY(-100%)"] {
	transform: unset !important;
}
.popout-2iWAc-[style*="translateX(-50."],
.popout-2iWAc-[style*="translateX(-50%)"] {
	transform: translateX(-50%) !important;
}
.popout-2iWAc-[style*="translateX(-84."],
.popout-2iWAc-[style*="translateX(-84%)"] {
	transform: translateX(-84%) !important;
}
.popout-2iWAc-[style*="translateX(-100%)"] {
	transform: translateX(-100%) !important;
}
.popout-2iWAc-[style*="translateY(-100%)"] > *:only-child {
	margin-top: -100%;
}
.popout-2iWAc-[style*="translateX(-50."] > *,
.popout-2iWAc-[style*="translateX(-50%)"] > * {
	margin-left: -50%;
	transform: translateX(50%);
}
.popout-2iWAc-[style*="translateX(-84."] > *,
.popout-2iWAc-[style*="translateX(-84%)"] > * {
	margin-left: -84%;
	transform: translateX(84%);
}
.popout-2iWAc-[style*="translateX(-100%)"] > * {
	margin-left: -100%;
	transform: translateX(100%);
}
.popout-2iWAc-[style*="translateX(-50."] > *.scrollerWrap-2lJEkd,
.popout-2iWAc-[style*="translateX(-50%)"] > *.scrollerWrap-2lJEkd {
	margin-right: 50%;
}
.popout-2iWAc-[style*="translateX(-100%)"] > *.scrollerWrap-2lJEkd {
	margin-right: 100%;
}

#app-mount .container-2x5lvQ,								/* RTCpopout			(for example voicequality)			*/
#app-mount .quickSelectPopout-X1hvgV,						/* quickselect			(for example regionselect)			*/
#app-mount .themedPopout-1TrfdI,							/* themed popout		(for example mentionpopout)			*/
#app-mount .popoutList-T9CKZQ {								/* listpopout			(for example auditlogs)				*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
	position: relative;
}
.container-2x5lvQ:after,
.container-2x5lvQ:before,
.quickSelectPopout-X1hvgV:after,
.quickSelectPopout-X1hvgV:before,
.themedPopout-1TrfdI:after,
.themedPopout-1TrfdI:before,
.popoutList-T9CKZQ:after,
.popoutList-T9CKZQ:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
.container-2x5lvQ:after,
.quickSelectPopout-X1hvgV:after,
.themedPopout-1TrfdI:after,
.popoutList-T9CKZQ:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.container-2x5lvQ:before,
.quickSelectPopout-X1hvgV:before,
.themedPopout-1TrfdI:before,
.popoutList-T9CKZQ:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.popout-googletranslate .themedPopout-1TrfdI {
	margin-top: -427px !important;
}
#app-mount .quickSelectPopoutOption-opKBx9:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .quickSelectPopoutOption-opKBx9.selected {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}
#app-mount .container-2x5lvQ .header-2C89wJ {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .container-2x5lvQ section {
	background-color: transparent;
}
#app-mount .container-2x5lvQ section p {
	color: rgb(var(--fontwhite3));
}
#app-mount .container-2x5lvQ section strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .debugButton-1Zec0y {
	color: rgb(var(--fontwhite3));
}

#app-mount .header-3po9qd {									/* popout				innerheader (for example GoLive)	*/
	color: rgb(var(--fontwhite1));
}
#app-mount .breadcrumbWrapper-WmDjgG {						/* popout				breadcrumbs (for example NitroGift)	*/
	color: rgb(var(--fontwhite3));
}
#app-mount .activeBreadcrumb-p6aw-F {
	color: rgb(var(--fontwhite1));
}

#app-mount .divider-1que2t {								/* popout				divider								*/
	border-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .giftBlurb-4VKZWm,
#app-mount .trialNote-wEO1RW,
#app-mount .trialText-2gR3-S {
	color: rgb(var(--fontwhite2));
}
#app-mount .price-3dKlQv,
#app-mount .annualDiscount-1VxngV {
	color: rgb(var(--fontwhite1));
}
#app-mount .interval-bfFUiQ {
	color: rgb(var(--fontwhite3));
}
#app-mount .option-1l2vXE {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .addGamePopout-2RY8Ju {							/* addgamepopout											*/
	background-color: transparent;
}
.addGamePopout-2RY8Ju:after,
.addGamePopout-2RY8Ju:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.addGamePopout-2RY8Ju:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.15));
}
.addGamePopout-2RY8Ju:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

/* ----		14.1.	CONTEXTMENU						---- */

.styleFlexible-wGDiIL,											/* contextmenu			flexible							*/
.styleFixed-sX-yHV,												/* contextmenu			fixed								*/
.submenu-2-ysNh {												/* contextmenu			submenu								*/
	background: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	z-index: 1;
}
.styleFlexible-wGDiIL:after,
.styleFlexible-wGDiIL:before,
.styleFixed-sX-yHV:after,
.styleFixed-sX-yHV:before,
.submenu-2-ysNh:after,
.submenu-2-ysNh:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.styleFlexible-wGDiIL:after,
.styleFixed-sX-yHV:after,
.submenu-2-ysNh:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
}
.styleFlexible-wGDiIL:before,
.styleFixed-sX-yHV:before,
.submenu-2-ysNh:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.submenu-2-ysNh {
	position: relative;
}
.item-1tOPte.colorDefault-2K3EoJ {								/* contextmenu			item								*/
	color: rgb(var(--fontwhite2));
}
.item-1tOPte.colorBrand-ROmMP1,
.item-1tOPte.colorPremium-p4p7qO {
	color: rgb(var(--vaccentcolor));
}
.item-1tOPte.colorDanger-2qLCe1 {
	color: #F04747;
}
.item-1tOPte.colorDefault-2K3EoJ.focused-3afm-j,
.item-1tOPte.colorDefault-2K3EoJ:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite1));
}
.item-1tOPte.colorDanger-2qLCe1.focused-3afm-j,
.item-1tOPte.colorDanger-2qLCe1:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(240, 71, 71, 0.2);
	color: rgb(var(--fontwhite1)) !important;
}
.item-1tOPte.colorBrand-ROmMP1.focused-3afm-j,
.item-1tOPte.colorBrand-ROmMP1:hover:not(.hideInteraction-1iHO1O),
.item-1tOPte.colorPremium-p4p7qO.focused-3afm-j,
.item-1tOPte.colorPremium-p4p7qO:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(var(--vaccentcolor), 0.2);
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .item-1tOPte .checkbox-3s5GYZ {						/* contextmenu			checkbox 							*/
	color: rgb(var(--vaccentcolor));
}
#app-mount .item-1tOPte.colorDanger-2qLCe1 .checkbox-3s5GYZ {
	color: #F04747;
}
#app-mount .item-1tOPte .check-1JyqgN {							/* contextmenu			checkmark 							*/
	color: rgb(var(--fontwhite1));
	stroke: var(--vtextshadow);
}
.separator-2I32lJ {												/* contextmenu			separator							*/
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
}
.button-1I8KM5 {												/* contextmenu			quick reaction button				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.button-1I8KM5:hover {
	background-color: rgb(var(--vaccentcolor));
}

/* ----		14.2.	USERPOPOUT						---- */

.userPopout-3XzG_A {										/* popout				container							*/
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}
.userPopout-3XzG_A:after,
.userPopout-3XzG_A:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.userPopout-3XzG_A:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.userPopout-3XzG_A:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.header-2BwW8b {											/* popout				header								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .headerNormal-T_seeN {							/* popout				headernormal						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.headerPlaying-j0WQBV {										/* popout				headerplaying						*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.headerStreaming-2FjmGz {									/* popout				headerstreaming						*/
	background: #593695;
}
.activity-11LB_k {											/* popout				activity							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .body-3iLsc4,									/* popout				body								*/
#app-mount .bodyInner-245q0L,								/* popout				bodyinner							*/
#app-mount .footer-1fjuF6 {									/* popout				footer								*/
	background-color: transparent;
	color: rgb(var(--fontwhite2));
}
#app-mount .footer-1fjuF6 {
	border-color: rgba(var(--fontwhite4), 0.3);
}

.headerTag-2pZJzA {											/* header				headertag							*/
	color: rgb(var(--fontwhite2));
}
.headerName-fajvi9,											/* header				username							*/
.headerTagUsernameNoNickname-2_H881,
#app-mount .headerNormal-T_seeN .headerName-fajvi9,
#app-mount .headerNormal-T_seeN .headerTagUsernameNoNickname-2_H881 {
	color: rgb(var(--fontwhite1));
}
#app-mount .headerTop-3C2Zn0 .textRow-19NEd_ {
	color: rgb(var(--fontwhite2));
}
#app-mount .headerNormal-T_seeN .headerTop-3C2Zn0 .textRow-19NEd_ {
	color: rgb(var(--fontwhite3));
}
#app-mount .activityUserPopout-2yItg2 .headerText-1HLrL7 {	/* header				activitytext						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .activityUserPopout-2yItg2 .content-3JfFJh,		/* header				activitycontent						*/
#app-mount .activityUserPopout-2yItg2 .details-38sfDr,		/* header				activitydetails						*/
#app-mount .activityUserPopout-2yItg2 .name-29ETJS {		/* header				activityname						*/
	color: rgb(var(--fontwhite2));
}
.activityName-1IaRLn {										/* header				activityname						*/
	color: rgb(var(--fontwhite1));
}
.bar-3urHkF {												/* header				activitybar							*/
	background-color: rgba(var(--fontwhite1), 0.2);
}
.barInner-3NDaY_ {											/* header				activitybarfill						*/
	background-color: rgb(var(--fontwhite1));
}
.text-AOoUen {												/* header				activitybartext						*/
	color: rgb(var(--fontwhite2));
}
.listenAlongIcon-2vb1HG {									/* header				listenalong							*/
	color: rgb(var(--fontwhite1));
}

.bodyTitle-Y0qMQz {											/* body					title								*/
	color: rgb(var(--fontwhite3));
}
.root-3-B5F3 {												/* body					roles								*/
	max-height: 100px;
	overflow-x: hidden;
	overflow-y: scroll;
}
#app-mount .root-3-B5F3::-webkit-scrollbar {
	width: 4px;
}
#app-mount .role-2irmRk {									/* body					role								*/
	border-color: rgba(var(--fontwhite3), 0.6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-2irmRk[style*="border-color: rgba(185, 187, 190, 0.6)"] {
	border-color: rgba(var(--fontwhite3), 0.6) !important;
}
#app-mount .role-2irmRk .roleName-32vpEy {					/* body					rolename							*/
	color: rgb(var(--fontwhite1));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j {				/* body					rolecircle							*/
	position: absolute;
	background-color: rgb(var(--fontwhite3));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	left: 0;
	top: 0;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--fontwhite3)) !important;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j:not(:empty):hover {
	opacity: 1;
	z-index: 2000;
	cursor: pointer;
}

.note-3kmerW textarea {										/* body					note								*/
	color: rgba(var(--fontwhite2));
}
.note-3kmerW textarea:focus {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.note-3kmerW textarea::placeholder {
	color: rgba(var(--fontwhite4));
}

.wumpusWrapper-yrvoR3 {										/* footer				wumpus new user 					*/
	margin-top: 27px;
}

#app-mount .quickMessage-1yeL4E {							/* footer				quickmessage						*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .quickMessage-1yeL4E:hover {
	border-color: rgb(var(--vtransparencycolor));
}
#app-mount .quickMessage-1yeL4E:focus {
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .quickMessage-1yeL4E::placeholder {
	color: rgb(var(--fontwhite3));
}

/* ----		14.3.	EMOJIPICKER						---- */

#app-mount .emojiPicker-3m1S-j,								/* picker				container							*/
#app-mount .diversitySelector-tmmMv0 .popout-2nUePc,		/* picker				diversitypopout						*/
#app-mount #bda-qem,										/* picker				BDtoolbar							*/
#app-mount #bda-qem-twitch-container,						/* picker				BDtwitchcontainer					*/
#app-mount #bda-qem-favourite-container {					/* picker				BDfavcontainer						*/
	background-color: transparent;
	border: none !important;
	position: relative;
	overflow: hidden;
}
.popout-2iWAc-[style*="translateX(-100%)"] .emojiPicker-3m1S-j,
.popout-2iWAc-[style*="translateX(-100%)"] #bda-qem,
.popout-2iWAc-[style*="translateX(-100%)"] #bda-qem-twitch-container,
.popout-2iWAc-[style*="translateX(-100%)"] #bda-qem-favourite-container {
	margin-left: -100%;
	transform: translateX(100%);
}
.emojiPicker-3m1S-j:after,
.emojiPicker-3m1S-j:before,
.diversitySelector-tmmMv0 .popout-2nUePc:after,
.diversitySelector-tmmMv0 .popout-2nUePc:before,
#bda-qem:after,
#bda-qem:before,
#bda-qem-twitch-container:after,
#bda-qem-twitch-container:before,
#bda-qem-favourite-container:after,
#bda-qem-favourite-container:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#bda-qem:after,
#bda-qem-twitch-container:after,
#bda-qem-favourite-container:after,
.emojiPicker-3m1S-j:after,
.diversitySelector-tmmMv0 .popout-2nUePc:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
#bda-qem:before,
#bda-qem-twitch-container:before,
#bda-qem-favourite-container:before,
.emojiPicker-3m1S-j:before,
.diversitySelector-tmmMv0 .popout-2nUePc:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

#app-mount .emojiPicker-3m1S-j,
#app-mount .emojiPicker-3m1S-j .dimmer-3iH-5D,				/* picker				diversitydimmer						*/
#app-mount #bda-qem-twitch-container,
#app-mount #bda-qem-favourite-container {
	border-radius:  0 0 5px 5px;
}
#app-mount .emojiPicker-3m1S-j:only-child,
#app-mount .emojiPicker-3m1S-j .dimmer-3iH-5D:only-child,
#app-mount #bda-qem-twitch-container:only-child,
#app-mount #bda-qem-favourite-container:only-child {
	border-radius: 5px;
}
#app-mount .noShadow-3pu20z .emojiPicker-3m1S-j,
#app-mount .noShadow-3pu20z .emojiPicker-3m1S-j .diversitySelector-tmmMv0 .popout-2nUePc,
#app-mount .noShadow-3pu20z #bda-qem,
#app-mount .noShadow-3pu20z #bda-qem-twitch-container,
#app-mount .noShadow-3pu20z #bda-qem-favourite-container {
	box-shadow: 0 0 1px rgba(var(--vtransparencycolor), 0.82), 0 1px 4px rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .emojiPicker-3m1S-j,
#app-mount #bda-qem-twitch-container,
#app-mount #bda-qem-favourite-container {
	height: 424px;
}
#app-mount .emojiPicker-3m1S-j .scrollerWrap-2lJEkd {
	height: unset;
}
#app-mount #bda-qem {
	height: 30px;
}
.popout-2iWAc-[style*="translateY(-100%)"] #bda-qem {
	margin-top: -358px;
}
#app-mount .emojiPicker-3m1S-j,
#app-mount #bda-qem,
#app-mount #bda-qem-twitch-container,
#app-mount #bda-qem-favourite-container {
	width: 384px;
	box-sizing: border-box;
}
#app-mount #bda-qem {
	background-color: rgb(var(--vtransparencycolor), 0.3);
	overflow: hidden;
	padding: 0 !important;
}
#app-mount #bda-qem button {
	background-color: transparent;
	border: none;
	border-radius: 0;
	box-shadow: none;
	color: rgb(var(--fontwhite2));
}
#app-mount #bda-qem button:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount #bda-qem button.active {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}
.emojiPicker-3m1S-j .header-1nkwgG {
	background-color: rgb(var(--vtransparencycolor), 0.3);
}
#app-mount .emojiPicker-3m1S-j .category-2U57w6,			/* picker				category							*/
#app-mount .emojiPicker-3m1S-j .stickyHeader-1SS0JU {		/* picker				stickycategory						*/
	background: transparent;
	color: rgb(var(--fontwhite2));
}
.emojiPicker-3m1S-j .stickyHeader-1SS0JU:after,
.emojiPicker-3m1S-j .stickyHeader-1SS0JU:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.emojiPicker-3m1S-j .stickyHeader-1SS0JU:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.emojiPicker-3m1S-j .stickyHeader-1SS0JU:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#bda-qem-favourite-container .emote-container:hover,
#bda-qem-twitch-container .emote-container:hover,
#app-mount .emojiPicker-3m1S-j .emojiItem-109bjA:hover,
#app-mount .emojiPicker-3m1S-j .emojiItem-109bjA.selected-39BZ4S {
	background-color: rgb(var(--vaccentcolor));
	border-radius: 5px;
}
.infoBar-U6oBFk {
	background-color: rgb(var(--vtransparencycolor), 0.3);
}
.emojiPicker-3m1S-j .categories-1feg4n {
	background-color: rgb(var(--vtransparencycolor), 0.3);
	justify-content: space-evenly;
}
.emojiPicker-3m1S-j .categories-1feg4n .item-16cXuq {
	transition: none;
}
.sadImage-2ph8SI {
	opacity: 0.6;
}
#app-mount .wrapper-1GJGVj {
	color: rgb(var(--fontwhite3));
}
#app-mount .emojiPicker-3m1S-j .dimmer-3iH-5D {
	z-index: 2;
}
#app-mount .emojiPicker-3m1S-j .dimmer-3iH-5D.visible-3k45bQ {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .diversitySelector-tmmMv0 .popout-2nUePc .item-16cXuq:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

/* NEW */

.contentWrapper-2txmjs,										/* picker				wrapper								*/
.diversitySelectorPopout-3FiGaM {							/* picker				diversityselector					*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	overflow: hidden;
}
.contentWrapper-2txmjs:after,
.contentWrapper-2txmjs:before,
.diversitySelectorPopout-3FiGaM:after,
.diversitySelectorPopout-3FiGaM:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-2txmjs:after,
.diversitySelectorPopout-3FiGaM:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.contentWrapper-2txmjs:before,
.diversitySelectorPopout-3FiGaM:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.diversitySelectorPopout-3FiGaM:after,
.diversitySelectorPopout-3FiGaM:before {
	border-radius: 5px;
}

.diversityEmojiItem-L6_IXw:hover {							/* picker				diversityemoji						*/
	background-color: rgb(var(--vaccentcolor));
}

.navButton-3Mnpqt {											/* picker				navbutton							*/
	color: rgb(var(--fontwhite3));
}
.navButtonActive-3RPAJy {									/* picker				navbuttonactive						*/
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}

.wrapper-2N7X54 {											/* picker				sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.guildIcon-3h-1IH {											/* picker				guildicon							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.categoryItemDefaultCategory-aBZ6nJ:hover {					/* picker				categoryitem						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.categoryItemDefaultCategorySelected-_HCKoz,
.categoryItemDefaultCategorySelected-_HCKoz:hover {			/* picker				categoryitem selected				*/
	background-color: rgb(var(--vaccentcolor));
}
.categoryItemDefaultCategorySelected-_HCKoz svg,
.categoryItemDefaultCategorySelected-_HCKoz:hover svg {		/* picker				categoryitem selected				*/
	filter: drop-shadow(1px 1px var(--vtextshadow));
}

.unicodeShortcut-15J8Ck {									/* picker				unicodeemojis shortcut				*/
	background-color: transparent;
	color: rgb(var(--fontwhite3));
	border: none;
	overflow: hidden;
	z-index: 100;
}
.unicodeShortcut-15J8Ck:hover {
	color: rgb(var(--fontwhite1));
}
.unicodeShortcut-15J8Ck:after,
.unicodeShortcut-15J8Ck:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.unicodeShortcut-15J8Ck:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.35));
}
.unicodeShortcut-15J8Ck:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}

.inspector-sdLnLS {											/* picker				emojiinfowrapper					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.categoryWrapper-UZ5YNj {									/* picker				categoryheader						*/
	background: transparent;
	position: static;
}

.emojiItem-14v6tW.emojiItemSelected-1aLkfV {				/* picker				emoji selected						*/
	background-color: rgb(var(--vaccentcolor));
}
.emojiItemDisabled-1FvFuF {									/* picker				emoji disabled						*/
	filter: none;
	cursor: no-drop;
}
.emojiItemDisabled-1FvFuF > * {
	filter: grayscale(1);
}

.premiumPromo-fVlLu- {										/* picker				premium warning						*/
	background-color: transparent;
	opacity: 1;
}
.premiumPromo-fVlLu-:after,
.premiumPromo-fVlLu-:before {
	content: "";
	opacity: 0.9;
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.premiumPromo-fVlLu-:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.29));
}
.premiumPromo-fVlLu-:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}


/* ----		14.4.	PINS/MENTIONS					---- */

.messagesPopoutWrap-1MQ1bW,								/* popout				wrapper								*/
.container-PbeQka {										/* popout				wrapper	(inbox)						*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	overflow: hidden;
}
.messagesPopoutWrap-1MQ1bW > *,
.container-PbeQka > * {
	z-index: 1000;
}
.messagesPopoutWrap-1MQ1bW:after,
.messagesPopoutWrap-1MQ1bW:before,
.container-PbeQka:after,
.container-PbeQka:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.messagesPopoutWrap-1MQ1bW:after,
.container-PbeQka:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.messagesPopoutWrap-1MQ1bW:before,
.container-PbeQka:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .messagesPopout-24nkyi {							/* popout				innerwrap							*/
	background-color: transparent;
}

.themedPopout-1TrfdI .header-2Kf7Yu {
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.1);
}
.header-ykumBX {											/* popout				header								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.2);
}
.header-ykumBX .title-3pkaKd {								/* popout				headertitle							*/
	color: rgb(var(--fontwhite1));
}

.themedPopout-1TrfdI .footer-1K57q_ {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.footer-1kmXd4 {											/* popout				footer								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.tutorial-i_drPV {											/* popout				tutorial							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.tutorialIcon-G9i5Ne {										/* popout				tutorial icon						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}


.messageGroupWrapper-o-Zw7G {
	background-color: transparent;
	border: none;
	overflow: visible;
	padding: 11px 10px 10px 10px;
}
.messageGroupWrapper-o-Zw7G + .messageGroupWrapper-o-Zw7G:before {
	content: "";
	border-top: 1px solid rgba(var(--fontwhite4), 0.3);
	position: absolute;
	top: -3px;
	left: 0;
	width: 100%;
}
.messageGroupWrapper-o-Zw7G .contentCozy-3XX413 {
	overflow: hidden;
}
.actionButtons-1sUUug {										/* popout				actionbuttonscontainer				*/
	top: 4px;
	right: 14px;
}
.jumpButton-3DTcS_ {										/* popout				jumpbutton (pins)					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}
.jumpButton-3DTcS_:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.jumpButton-3DTcS_ + .jumpButton-3DTcS_ {
	margin-left: 2px;
}
.messageGroupWrapper-o-Zw7G:hover .actionButtons-1sUUug .closeButton-17RIVZ {
	opacity: 1;
}
.channelName-3kBz6H {										/* popout				dividerchannelname					*/
	color: rgb(var(--fontwhite1));
}
.guildName-1Bc3Ta {											/* popout				dividerguildname					*/
	color: rgb(var(--fontwhite2));
}
.hasMoreButton-1MELpI {										/* popout				hasmorebutton						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border: none;
}

.emptyPlaceholder-1zh-Eu .body-bvcIjN {						/* popout				emptytext							*/
	color: rgb(var(--fontwhite3));
}
.image-2JDb81 {												/* popout				emptyimage							*/
	opacity: 0.6;
}

															/* popout				active tab							*/
#app-mount .header-2-Imhb .tabBar-1kuXvJ .tab-ck0077.active-1MbGPa {
	background-color: rgb(var(--vaccentcolor));
}
.secondary-dIudih,											/* popout				header button						*/
.tertiary-aMXF0g,											/* popout				message button						*/
.collapseButton-3V3Cqh {									/* popout				collapse button						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
.secondary-dIudih:hover,
.tertiary-aMXF0g:hover,
.collapseButton-3V3Cqh:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}
.collapseButton-3V3Cqh {
	position: static;
	margin-left: 12px;
	border-radius: 32px;
	box-sizing: border-box;
	cursor: pointer;
	flex-shrink: 0;
	height: 32px;
	min-height: 32px;
	width: 32px;
	min-width: 32px;
	padding: 8px;
	transform: unset !important;
}
.collapseButton-3V3Cqh.collapsed-b6uSCG svg {
	transform: rotate(-90deg);
}

.channelHeader-3Gd2xq {										/* popout				channelheader						*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	padding-right: 16px;
	border-radius: 5px 5px 0 0;
	position: static;
}
.channelHeader-3Gd2xq:only-child {
	border-radius: 0;
}
.messageContainer-gbhlwo,									/* popout				messagecontainer					*/
.messages-3G3erD {											/* popout				messagecontainer (inbox)			*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 0;
}
.messageContainer-gbhlwo:last-child,
.messages-3G3erD:last-child {
	border-radius: 0 0 5px 5px;
}

.emptyStateIcon-3VCpT2 {									/* popout				no messages (inbox)					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}

/* ----		14.5.	SEARCHPOPOUT					---- */

#app-mount .container-3ayLPN {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	overflow: hidden;
	position: relative;
}
.container-3ayLPN:after,
.container-3ayLPN:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-3ayLPN:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
}
.container-3ayLPN:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .queryContainer-RKFJW- {
	color: rgb(var(--fontwhite3));
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .queryContainer-RKFJW- strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .focused-2bY0OD {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .resultsGroup-r_nuzN:before {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .resultsGroup-r_nuzN .header-2N-gMV,
#app-mount .resultsGroup-r_nuzN .plusIcon-v0BTrL,
#app-mount .resultsGroup-r_nuzN .searchClearHistory-2cSSMO,
#app-mount .resultsGroup-r_nuzN .searchLearnMore-3SQUAj a {
	color: rgb(var(--fontwhite2));
}
#app-mount .option-96V44q:after {
	display: none;
}
#app-mount .option-96V44q.selected-rZcOL- {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .option-96V44q.selected-rZcOL-:before {
	background-color: rgb(var(--vaccentcolor));
	border-radius: 3px;
	width: 34px;
}
#app-mount .option-96V44q .answer-1n6g43,
#app-mount .option-96V44q .nonText-3CRkO0,
#app-mount .option-96V44q strong {
	color: rgb(var(--fontwhite2));
}
#app-mount .option-96V44q .filter-3Y_im- {
	color: rgb(var(--fontwhite4));
}
#app-mount .option-96V44q.user-O3Czj0 .displayedNick-3xxvzU {
	color: rgb(var(--fontwhite2));
}
#app-mount .option-96V44q.user-O3Czj0 .displayUsername-Qekxml {
	color: rgb(var(--fontwhite3));
}
#app-mount .searchOption-zQ-1l6 .filter-3Y_im- {
	color: rgb(var(--fontwhite2));
}
#app-mount .searchOption-zQ-1l6 .answer-1n6g43 {
	color: rgb(var(--fontwhite4));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hint-165cR4 {
	color: rgb(var(--fontwhite2));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z {
	color: rgb(var(--fontwhite1));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z:hover {
	background-color: #677bc4;
}
#app-mount .searchResultChannelCategory-1l0lSn,
#app-mount .searchResultChannelIcon-1DnTme {
	color: rgb(var(--fontwhite4));
}

#app-mount .calendarPicker-2yf6Ci .react-datepicker {
	background: transparent;
}
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--outside-month) {
	border-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--outside-month {
	border-color: transparent;
	background: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .datePicker--XZbmJ .react-datepicker__header,
#app-mount .datePicker--XZbmJ .react-datepicker__month-container,
#app-mount .datePicker--XZbmJ .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	background: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .datePicker--XZbmJ .react-datepicker__header {
	padding-bottom: 5px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation {
	background: transparent;
	border-color: rgba(var(--fontwhite1), 0.5);
	top: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation:before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	-webkit-mask: url(https://discordapp.com/assets/7619529e87dad31fd2ae83d9b9583e49.svg) center/6px 12px no-repeat;
	background-color: rgb(var(--fontwhite1));
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation--previous {
	left: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation--next {
	right: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__current-month {
	border-color: transparent;
	padding: 10px 0;
}
#app-mount .datePicker--XZbmJ .react-datepicker__current-month,
#app-mount .datePicker--XZbmJ .react-datepicker__day-name,
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--disabled):hover,
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--disabled):not(.react-datepicker__day--outside-month),
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hint-165cR4,
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z {
	color: rgb(var(--fontwhite1));
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	color: rgb(var(--fontwhite3));
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--outside-month {
	color: rgb(var(--fontwhite4));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw {
	margin: 0;
	padding: 20px;
	display: flex;
	justify-content: center;
}

/* ----		14.6.	COLORPICKER						---- */

#app-mount .colorPickerCustom-2CWBn2 {						/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.colorPickerCustom-2CWBn2:after,
.colorPickerCustom-2CWBn2:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.colorPickerCustom-2CWBn2:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.35));
}
.colorPickerCustom-2CWBn2:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .saturation-1FDvtn > div > div > div > div {							/* popout				saturationcursor					*/
	box-shadow: rgb(var(--fontwhite1)) 0px 0px 0px 1.5px, rgba(var(--vtransparencycolor), 0.6) 0px 0px 1px 1px inset, rgba(var(--vtransparencycolor), 0.6) 0px 0px 1px 2px !important;
}
#app-mount .hue-13HAGb > div > div > div > div,									/* popout				huecursor							*/
#app-mount .BDFDB-colorpicker .alpha-bar > div > div > div > div {				/* popout				alphacursor							*/
	background: rgb(var(--fontwhite1)) !important;
	box-shadow: rgba(var(--vtransparencycolor), 1) 0px 0px 2px !important;
}
#app-mount .BDFDB-colorpicker .gradient-button {								/* popout				gradientbutton						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor > div {			/* popout				gradientcursor						*/
	border-color: rgb(var(--fontwhite4));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor > div:before {		/* popout				gradientcursorpointer				*/
	border-top-color: rgb(var(--fontwhite4));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor.selected > div {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor.selected > div:before {
	border-top-color: rgb(var(--fontwhite1));
}

/* ----		14.7.	ADDROLE							---- */

#app-mount .container-VSDcQc {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.container-VSDcQc:after,
.container-VSDcQc:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-VSDcQc:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
}
.container-VSDcQc:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#app-mount .header-2bNvm4,
#app-mount .autocompleteHeaderBackground-30T70q {			/* popout				header								*/
	background: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 5px 5px 0 0;
}
#app-mount .container-VSDcQc .headerText-3i6A8K {			/* popout				headertext							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .container-VSDcQc .input-1ppKdn {				/* popout				headerinput							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .container-VSDcQc .input-1ppKdn::placeholder {
	color: rgb(var(--fontwhite4));
}
#app-mount .autocompleteArrow-Zxoy9H {						/* popout				arrow								*/
	display: none;
}
#app-mount .autocompleteShadow-iiGWFU {						/* popout				shadow								*/
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .container-VSDcQc .sectionTag-pXyto9 {			/* popout				body								*/
	background: transparent;
	border-radius: 0 0 5px 5px;
	color: rgb(var(--fontwhite3));
}
#app-mount .row-rrHHJU,										/* popout				row									*/
#app-mount .row-rrHHJU span {								/* popout				rowspan								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .row-rrHHJU.selected-1pIgLL {
	background: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 0 5px 5px 0;
}


/* ----		14.8.	EVERYONEMENTION					---- */

#app-mount .everyonePopout-nEbJY3 {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.everyonePopout-nEbJY3:after,
.everyonePopout-nEbJY3:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.everyonePopout-nEbJY3:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
}
.everyonePopout-nEbJY3:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.everyonePopout-nEbJY3 .animation-3GofIz {
	opacity: 0.7;
}
#app-mount .header-3_S6dz {
	color: rgb(var(--fontwhite1));
}
#app-mount .buttonHint-2OxJB8 {
	color: rgb(var(--fontwhite3));
}
#app-mount .buttonHint-2OxJB8 strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .footer-2aTx0s {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .footer-2aTx0s .icon-2qOzDL path {
	fill: rgb(var(--fontwhite3));
}


/* ----		14.9.	CHANNELFOLLOW					---- */

#app-mount .header-1pGpFt {
	background: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .separator-3gy7tq {
	box-shadow: 0 1px 0 0 rgba(var(--vtransparencycolor), 0.3), 0 1px 2px 0 rgba(var(--vtransparencycolor), 0.3);
}
.channelContainer-1x3D6I {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.channel-2PJTLY {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.channelContainer-1x3D6I .channel-2PJTLY {
	background-color: transparent;
}
.channelIcon-3ci4bV {
	color: rgb(var(--fontwhite3));
}

/* ----		14.10.	CHANNELFOLLOWINFO				---- */

#app-mount .guildPopout-3CgKqR {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.guildPopout-3CgKqR:after,
.guildPopout-3CgKqR:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.guildPopout-3CgKqR:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
}
.guildPopout-3CgKqR:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}


/* ~~~~		15.		GENERAL							~~~~ */

::-webkit-input-placeholder, body, button, input, select, textarea {
	font-family: var(--vfont);
}

::selection {												/* selection												*/
	background: rgb(var(--vaccentcolor));
}

#app-mount .elevationLow-2lY09M, .lightElevationLow-3_Ybxi, .darkElevationLow-DABD7i {
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .elevationHigh-3A9Xbf, .lightElevationHigh-3usmGv, .darkElevationHigh-6iWpWi {
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .elevationBorderLow-2qgTRQ, .lightElevationBorderLow-3APXjz, .darkElevationBorderLow-39dDV7 {
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .elevationBorderHigh-2WYJ09, .lightElevationBorderHigh-2T98IF, .darkElevationBorderHigh-2U1nXW {
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}

.pointerEvents-2zdfdO[fill="#ffffff"] {						/* status				whitedot							*/
	fill: rgb(var(--fontwhite1));
}

.dots-3Bkt3k,												/* loading				3-dots								*/
.dots-3Bkt3k.themed-IQiCm3 {
	color: rgb(var(--fontwhite1));
}

/* ----		15.1.	TEXT							---- */

.username-3gJmXY {
	color: rgb(var(--fontwhite1));
}
.discriminator-uTZ08z {
	color: rgb(var(--fontwhite3));
}
.h5-18_1nd {
	color: rgb(var(--fontwhite3));
}
.white-1VR_aZ,
.white-3xi-nx {
	color: rgb(var(--fontwhite1));
}
#app-mount h1.title-3KTIjF,
#app-mount h2.title-3KTIjF {
	color: rgb(var(--fontwhite1));
}
#app-mount h3.title-3KTIjF {
	color: rgb(var(--fontwhite2));
}
#app-mount h4.title-3KTIjF,
#app-mount h5.title-3KTIjF,
#app-mount h6.title-3KTIjF {
	color: rgb(var(--fontwhite3));
}
#app-mount .coloredText-1kAd0O {
	color: rgb(var(--fontwhite1));
}
#app-mount .defaultColor-1_ajX0 {
	color: rgb(var(--fontwhite1));
}

/* ----		15.2.	BUTTONS							---- */

.searchSuggestion-2K8OBX:hover,
.form-236Xmo .btnPrimary-346kfV,
.button-22FETM,
.questionMark-CWEQZn,
.btn-1PnLxm.btnPrimary-1jluZW,
.btn-15Au6M.btnPrimary-ggBniE,
.bd-modal-wrapper .footer button,
.bd-pfbtn,
.bda-settings-button,
.btn-primary,
.platform-iik236.active-iLSdWQ .downloadButton-1bWXpg,
.action-1lSjCi.create-3jownz .actionButton-2PeQbJ,
.ui-button.brand.filled,
.lookFilled-1Gx00P.hoverBrand-1_Fxlk.hasHover-3X1-zV:hover,
.lookFilled-1Gx00P.colorBrand-3pXr91:not([style*="background-color"]) {
	text-shadow: 1px 1px var(--vtextshadow);
}
.lookFilled-1Gx00P.hoverBrand-1_Fxlk.hasHover-3X1-zV:hover svg,
.lookFilled-1Gx00P.colorBrand-3pXr91:not([style*="background-color"]) svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}

.lookFilled-1Gx00P:not(.colorWhite-rEQuAQ) .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite1)) !important;
}
.lookFilled-1Gx00P:not(.colorWhite-rEQuAQ) {
	color: rgb(var(--fontwhite1)) !important;
}
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ):hover {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1)) !important;
}
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ):active {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2)) !important;
}
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ),
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ):disabled {
	background: rgb(var(--fontwhite1)) !important;
}
.theme-light .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover,
.theme-light .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active {
	color: rgb(var(--fontwhite1)) !important;
}
.theme-light .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover {
	background-color: rgb(var(--fontwhite2)) !important;
}
.theme-light .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active {
	background-color: rgb(var(--fontwhite3)) !important;
}


.lookFilled-1Gx00P.colorWhite-rEQuAQ .spinnerItem-3GlVyU {
	background-color: rgb(var(--vtransparencycolor));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ .spinnerItem-3GlVyU,
.lookOutlined-3sRXeN.colorWhite-rEQuAQ .spinnerItem-3GlVyU,
.lookGhost-2Fn_0-.colorWhite-rEQuAQ .spinnerItem-3GlVyU,
.lookLink-9FtZy-.colorWhite-rEQuAQ .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite1));
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ {
	color: rgb(var(--vtransparencycolor));
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ:hover,
.theme-light .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1)) !important;
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ:active,
.theme-light .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:active {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2)) !important;
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ,
.lookFilled-1Gx00P.colorWhite-rEQuAQ:disabled {
	background: rgb(var(--fontwhite1));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ:hover,
.theme-light .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.1),rgba(255,255,255,.1));
	color: rgb(var(--fontwhite2));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ:active,
.theme-light .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:active {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.2),rgba(255,255,255,.2));
	color: rgb(var(--fontwhite3));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ,
.lookInverted-2D7oAl.colorWhite-rEQuAQ:disabled {
	background-color: rgb(var(--vtransparencycolor));
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ {
	border-color: rgba(var(--fontwhite1), 0.3);
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:hover,
.theme-light .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite1), 0.6);
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:active,
.theme-light .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	background-color: rgba(var(--fontwhite1), 0.1);
	border-color: rgb(var(--fontwhite1));
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:disabled {
	border-color: rgba(var(--fontwhite1), 0.3);
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ {
	background-color: rgba(var(--fontwhite1), 0.1);
	color: rgb(var(--fontwhite1));
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ:hover {
	color: rgb(var(--fontwhite1));
	background-color: rgba(var(--fontwhite1), 0.15);
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ:active,
.theme-light .lookGhost-2Fn_0-.hoverWhite-2uUmXw.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverWhite-2uUmXw.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite1), 0.2);
	color: rgb(var(--fontwhite1));
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ:disabled {
	background-color: rgba(var(--fontwhite1), 0.1);
}
#app-mount .backButtonColor-1zIPlh,
#app-mount .backButtonColor-N09dXJ,
.lookLink-9FtZy-.colorWhite-rEQuAQ {
	color: rgb(var(--fontwhite1));
}
#app-mount .backButtonColor-1zIPlh:hover .contents-18-Yxp,
#app-mount .backButtonColor-N09dXJ:hover .contents-18-Yxp,
.lookLink-9FtZy-.colorWhite-rEQuAQ:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverWhite-2uUmXw.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverWhite-2uUmXw.hasHover-3X1-zV:hover .contents-18-Yxp {
	color: rgb(var(--fontwhite1));
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite1)) 0, rgb(var(--fontwhite1)) 2px, transparent 0);
}

.lookInverted-2D7oAl.colorBlack-1jwPVL .spinnerItem-3GlVyU,
.lookOutlined-3sRXeN.colorBlack-1jwPVL .spinnerItem-3GlVyU,
.lookGhost-2Fn_0-.colorBlack-1jwPVL .spinnerItem-3GlVyU,
.lookLink-9FtZy-.colorBlack-1jwPVL .spinnerItem-3GlVyU {
	background-color: rgb(var(--vtransparencycolor));
}
.lookFilled-1Gx00P.colorBlack-1jwPVL:hover,
.theme-light .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:hover {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.1),rgba(255,255,255,.1));
}
.lookFilled-1Gx00P.colorBlack-1jwPVL:active,
.theme-light .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.2),rgba(255,255,255,.2));
}
.lookFilled-1Gx00P.colorBlack-1jwPVL,
.lookFilled-1Gx00P.colorBlack-1jwPVL:disabled {
	background: rgb(var(--vtransparencycolor));
}
.theme-light .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-light .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	color: rgb(var(--vtransparencycolor));
}
.lookInverted-2D7oAl.colorBlack-1jwPVL,
.lookInverted-2D7oAl.colorBlack-1jwPVL:disabled {
	color: rgb(var(--vtransparencycolor));
}
.lookOutlined-3sRXeN.colorBlack-1jwPVL:hover,
.theme-light .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:hover {
	border-color: rgba(var(--vtransparencycolor), 0.6);
	color: rgb(var(--vtransparencycolor));
}
.lookOutlined-3sRXeN.colorBlack-1jwPVL:active,
.theme-light .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgb(var(--vtransparencycolor));
	color: rgb(var(--vtransparencycolor));
}
.lookOutlined-3sRXeN.colorBlack-1jwPVL,
.lookOutlined-3sRXeN.colorBlack-1jwPVL:disabled {
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
.lookGhost-2Fn_0-.colorBlack-1jwPVL:active,
.theme-light .lookGhost-2Fn_0-.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--vtransparencycolor));
}
.lookGhost-2Fn_0-.colorBlack-1jwPVL,
.lookGhost-2Fn_0-.colorBlack-1jwPVL:disabled {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.lookLink-9FtZy-.colorBlack-1jwPVL {
	color: rgb(var(--vtransparencycolor));
}
.lookLink-9FtZy-.colorBlack-1jwPVL:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverBlack-3jULb8.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverBlack-3jULb8.hasHover-3X1-zV:hover .contents-18-Yxp {
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--vtransparencycolor)) 0, rgb(var(--vtransparencycolor)) 2px, transparent 0);
	color: rgb(var(--vtransparencycolor));
}

.theme-light .lookInverted-2D7oAl.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookInverted-2D7oAl.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookLink-9FtZy-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookLink-9FtZy-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookInverted-2D7oAl.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookInverted-2D7oAl.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-light .lookLink-9FtZy-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookLink-9FtZy-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite4));
}
.buttonColor-1agP3J:hover,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV:hover,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV:hover,
.theme-light .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6:hover,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6:hover,
.theme-light .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	background: rgb(var(--fontwhite4)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1));
}
.buttonColor-1agP3J:active,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV:active,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV:active,
.theme-light .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6:active,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6:active,
.theme-light .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background: rgb(var(--fontwhite4)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2));
}
.buttonColor-1agP3J,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV:disabled,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV:disabled,
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6,
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6:disabled,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6:disabled {
	background: rgb(var(--fontwhite4));
}
.theme-light .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-light .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-light .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-light .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	color: rgb(var(--fontwhite4));
}
.theme-light .lookInverted-2D7oAl.colorGrey-2DXtkV,
.theme-dark .lookInverted-2D7oAl.colorGrey-2DXtkV,
.theme-light .lookInverted-2D7oAl.colorGrey-2DXtkV:disabled,
.theme-dark .lookInverted-2D7oAl.colorGrey-2DXtkV:disabled,
.theme-light .lookInverted-2D7oAl.colorPrimary-3b3xI6,
.theme-dark .lookInverted-2D7oAl.colorPrimary-3b3xI6,
.theme-light .lookInverted-2D7oAl.colorPrimary-3b3xI6:disabled,
.theme-dark .lookInverted-2D7oAl.colorPrimary-3b3xI6:disabled {
	color: rgb(var(--fontwhite4));
}
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV:hover,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV:hover,
.theme-light .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6:hover,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6:hover,
.theme-light .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite4), 0.6);
	color: rgb(var(--fontwhite4));
}
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV:active,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV:active,
.theme-light .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6:active,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6:active,
.theme-light .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite4), 0.1);
	border-color: rgb(var(--fontwhite4));
	color: rgb(var(--fontwhite4));
}
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV,
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV:disabled,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV:disabled,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6:disabled,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6:disabled {
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite4));
}
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV:active,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV:active,
.theme-light .lookGhost-2Fn_0-.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6:active,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6:active,
.theme-light .lookGhost-2Fn_0-.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite4), 0.2);
}
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV,
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV:disabled,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV:disabled,
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6,
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6:disabled,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6:disabled {
	background-color: rgba(var(--fontwhite4), 0.1);
	color: rgb(var(--fontwhite4));
}
.theme-light .lookLink-9FtZy-.colorGrey-2DXtkV,
.theme-dark .lookLink-9FtZy-.colorGrey-2DXtkV,
.theme-light .lookLink-9FtZy-.colorPrimary-3b3xI6,
.theme-dark .lookLink-9FtZy-.colorPrimary-3b3xI6 {
	color: rgb(var(--fontwhite4));
}
.theme-light .lookLink-9FtZy-.colorGrey-2DXtkV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.colorGrey-2DXtkV:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverGrey-2CBXu0.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverGrey-2CBXu0.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.colorPrimary-3b3xI6:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.colorPrimary-3b3xI6:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover .contents-18-Yxp {
	color: rgb(var(--fontwhite4));
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite4)) 0, rgb(var(--fontwhite4)) 2px, transparent 0);
}

.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9 .spinnerItem-3GlVyU {
	background-color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-light .lookLink-9FtZy-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookLink-9FtZy-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite2));
}
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9:hover,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9:hover,
.theme-light .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--fontwhite1), 0.05);
	color: rgb(var(--fontwhite1));
}
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9:active,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9:active,
.theme-light .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite1), 0.01);
	color: rgb(var(--fontwhite1));
}
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9,
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9:disabled,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9:disabled {
	background-color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9:hover,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9:hover,
.theme-light .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--fontwhite1), 0.05);
	color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9:active,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9:active,
.theme-light .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite1), 0.1);
	color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9,
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9:disabled,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9:disabled {
	background-color: rgb(var(--fontwhite1));
	color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9:hover,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9:hover,
.theme-light .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite2), 0.6);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9:active,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9:active,
.theme-light .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite2), 0.1);
	border-color: rgb(var(--fontwhite2));
	color: rgb(var(--fontwhite2));
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9,
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9:disabled,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9:disabled {
	border-color: rgba(var(--fontwhite2), 0.3);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9:active,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9:active,
.theme-light .lookGhost-2Fn_0-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite2), 0.2);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9,
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9:disabled,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9:disabled {
	background-color: rgba(var(--fontwhite2), 0.1);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookLink-9FtZy-.colorTransparent-1ewNp9,
.theme-dark .lookLink-9FtZy-.colorTransparent-1ewNp9 {
	color: rgb(var(--fontwhite2));
}
.theme-light .lookLink-9FtZy-.colorTransparent-1ewNp9:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.colorTransparent-1ewNp9:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover .contents-18-Yxp {
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite2)) 0, rgb(var(--fontwhite2)) 2px, transparent 0);
	color: rgb(var(--fontwhite2));
}

/* ----		15.3.	INPUTS							---- */

.input-cIJ7To {												/* valueinput			bordered							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.input-cIJ7To:hover:not(:focus) {
	border-color: rgb(var(--vtransparencycolor));
}
.input-cIJ7To::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .input-1mgnkM,									/* valueinput			underlined							*/
#app-mount .input-UJ9Tr3 {
	border-color: rgba(var(--fontwhite1), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .input-1mgnkM:hover,
#app-mount .input-UJ9Tr3:hover {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .input-1mgnkM:focus,
#app-mount .input-UJ9Tr3:focus {
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .input-1mgnkM::placeholder,
#app-mount .input-UJ9Tr3::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .copyInput-2rOSt7 {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .copyInputDefault-21sXtF {
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .hiddenMessage-1iiFV5,
#app-mount .inputDefault-A2ud2y {
	color: rgb(var(--fontwhite1));
}
#app-mount .inputDefault-A2ud2y::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .multiInputLast-1aQ3YA:before {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .inputPrefix-2VAOGg {
	color: rgb(var(--fontwhite1));
	opacity: 0.3;
}
.maxLength-39QFBo {
	color: rgb(var(--fontwhite3));
}
#app-mount .inputNumberWrapper .numberinput-button-up {
	border-bottom-color: rgb(var(--fontwhite3));
}
#app-mount .inputNumberWrapper .numberinput-button-up:hover {
	border-bottom-color: rgb(var(--fontwhite1));
}
#app-mount .inputNumberWrapper .numberinput-button-down {
	border-top-color: rgb(var(--fontwhite3));
}
#app-mount .inputNumberWrapper .numberinput-button-down:hover {
	border-top-color: rgb(var(--fontwhite1));
}

.themeDefault-24hCdX {										/* checkboxswitch											*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.switch-3wwwcV[style*="background-color: rgba(255, 255, 255, 0.3)"] {
	background-color: rgba(var(--fontwhite1), 0.3) !important;
}
.themeDefault-24hCdX.sizeDefault-2YlOZr {
	box-shadow: inset 0 1px 1px rgba(var(--vtransparencycolor), 0.15);
}
.themeClear-1EjkE4.valueUnchecked-2lU_20.sizeDefault-2YlOZr {
	box-shadow: inset 0 0 0 2px rgba(var(--fontwhite1), 0.2);
}
.themeDefault-24hCdX.sizeDefault-2YlOZr:after {
	box-shadow: 0 2px 4px rgba(var(--vtransparencycolor), 0.6);
}
.size-3rFEHg:after,
.size-3rFEHg:active:after {
	background-color: rgb(var(--fontwhite1));
}

.radioGroup-1GBvlr {										/* radiogroup			container							*/
	color: rgb(var(--fontwhite1));
}
.item-26Dhrx[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--vtextshadow);
}
.item-26Dhrx[style*="background-color: rgb(114, 137, 218)"] .checked-3_4uQ9[style*="border-color: rgb(114, 137, 218)"] {
	border-color: var(--vtextshadow) !important;
}
.checkboxMute-14hTGS:before,
.desc-2Dttbk {												/* radiogroup			description							*/
	color: rgb(var(--fontwhite3));
}
.descChecked-XkfPsU, 
.titleChecked-2wg0pd {
	color: rgb(var(--fontwhite1)) !important;
}

#app-mount .checkboxContainer-2vV9zd:before {				/* checkbox				container							*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .checkbox-1ix_J3 {								/* checkbox				inner								*/
	border-color: rgb(var(--fontwhite3));
}
#app-mount .checked-3_4uQ9 {								/* checkbox				checked								*/
	background-color: rgb(var(--fontwhite1));
	border-color: rgb(var(--fontwhite1));
}
#app-mount .checked-3_4uQ9.round-2jCFai,					/* checkbox				roundchecked						*/
#app-mount .checked-3_4uQ9[style*="border-color: rgb(79, 84, 92)"] {
	background-color: rgb(var(--vaccentcolor)) !important;
	border-color: rgb(var(--vaccentcolor)) !important;
}
#app-mount .checked-3_4uQ9.round-2jCFai svg,
#app-mount .checked-3_4uQ9[style*="border-color: rgb(79, 84, 92)"] svg,
#app-mount .checked-3_4uQ9[style*="background-color: rgb(114, 137, 218)"] svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
#app-mount .checked-3_4uQ9 polyline[stroke="#43b581"],		/* checkbox				checkmark							*/
#app-mount .checked-3_4uQ9 polyline[stroke="#4f545c"],
#app-mount .checked-3_4uQ9 polyline[stroke="#ffffff"] {
	stroke: rgb(var(--fontwhite1));
}
.checkboxMute-14hTGS:before {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .bar-2Qqk5Z {									/* slider				backgroundbar						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.grabber-3mFHz2 {											/* slider				grabber								*/
	background-color: rgb(var(--fontwhite1));
	border-color: rgb(var(--fontwhite1));
	box-shadow: 0 3px 1px 0 rgba(var(--vtransparencycolor), 0.05), 0 2px 2px 0 rgba(var(--vtransparencycolor), 0.1), 0 3px 3px 0 rgba(var(--vtransparencycolor), 0.05);
}
#app-mount .markValue-2DwdXI {								/* slider				markvalue							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .defaultValue-3gC7yw .markValue-2DwdXI {
	color: #43b581;
}
#app-mount .markDash-3hAolZ {
	background: transparent;
	color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .defaultValue-3gC7yw .markDash-3hAolZ {
	color: #43b581;
}
#app-mount .markDash-3hAolZ:before,
#app-mount .markDash-3hAolZ:after {
	content: "";
	position: absolute;
	background: currentColor;
	height: 8px;
	width: 2px;
}
#app-mount .markDash-3hAolZ:before {
	top: 14px;
}
#app-mount .markDash-3hAolZ:after {
	top: 30px;
}
#app-mount .fontScaleLarge-3xtq7i,
#app-mount .fontScaleSmall-368quy {
	color: rgb(var(--fontwhite1));
}
#app-mount .bubble-3we2di {									/* slider				bubble								*/
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
#app-mount .bubble-3we2di:before {
	border-top-color: rgb(var(--vaccentcolor));
}

#app-mount .container-1nZlH6 {								/* hotkeyinput			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
.input-1UhAnY {												/* hotkeyinput			input								*/
	color: rgb(var(--fontwhite1));
}
.input-1UhAnY::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .editIcon-13gaox {								/* hotkeyinput			editicon							*/
	-webkit-mask: url(https://discordapp.com/assets/860396b3ff3fa1c4ae355bebfabadecb.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite1));
}
#app-mount .container-CpszHS.recording-1H2dS7 .button-34kXw5 {
	color: #f04747;
	background-color: rgba(240,71,71,.1);
}

#app-mount .quickSelect-3BxO0K {							/* quickselect			container							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .quickSelectLabel-2r3iJ_ {						/* quickselect			label								*/
	color: rgb(var(--fontwhite3));
}
#app-mount .quickSelectArrow-1QublR {						/* quickselect			arrow								*/
	-webkit-mask: url(https://discordapp.com/assets/f58cf3b8fc79e9d671ab649ab37651a9.svg) 50% no-repeat;
	background: rgb(var(--fontwhite1));
}

.select-2TCrqx [class*="css-"][class*="-container"] {		/* select				container							*/
	background-color: transparent;
}
#app-mount .lookFilled-1h1y05.select-1Pkeg4,
.select-2TCrqx [class*="css-"][class*="-control"] {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .lookFilled-1h1y05.select-1Pkeg4:hover.selectOpen-hQuR6b,
#app-mount .lookFilled-1h1y05.selectOpen-hQuR6b {
	border-color: rgb(var(--vtransparencycolor)) rgb(var(--vtransparencycolor)) rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .select-1Pkeg4,
#app-mount .lookFilled-1h1y05 .arrow-2KJjTM,
.select-2TCrqx [class*="css-"][class*="-singleValue"],
.select-2TCrqx [class*="css-"][class*="-placeholder"],
.select-2TCrqx [class*="css-"][class*="-indicatorContainer"] {
	color: rgb(var(--fontwhite1));
}
#app-mount .optionNormal-12VR9V,
.css-1aymab5-option,
.css-ddw2o3-option {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite2));
}
#app-mount .optionNormal-12VR9V:hover,
.css-1gnr91b-option,
.css-qgio2y-option {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
#app-mount .optionActive-KkAdqq,
.css-12o7ek3-option,
.css-1kft5vg-option {
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .popout-2sKjHu,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"] {
	background: transparent;
	border: 1px solid rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0px 1px 5px 0px rgba(var(--vtransparencycolor), 0.3);
	overflow: hidden;
}
#app-mount .popout-2sKjHu:after,
#app-mount .popout-2sKjHu:before,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]:after,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .popout-2sKjHu:after,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
#app-mount .popout-2sKjHu:before,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}


/* ----		15.4.	SEARCHBARS						---- */

.container-2XeR5Z,											/* searchbar			inner								*/
.container-cMG81i {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.input-1Rv96N,												/* searchbar			input								*/
.input-3Xdcic {
	color: rgb(var(--fontwhite1));
}
.input-1Rv96N::placeholder,
.input-3Xdcic::placeholder,
#app-mount .searchBox-3Y2Vi7 .searchBoxInput-uJtBcv::placeholder {
	color: rgb(var(--fontwhite3));
}
.icon-3cZ1F_,												/* searchbar			icon								*/
.icon-1S6UIr,
#app-mount .clearIcon-2N9YIn,
#app-mount .searchIcon-1a1-yA,
#app-mount .searchIcon-32i2pb {
	color: rgb(var(--fontwhite3));
}
.clear-1pMieT .icon-3cZ1F_,
.icon-1S6UIr.clear--Eywng,
#app-mount .clearIcon-xXwSFS,
#app-mount .clear-U3WkKp .clearIcon-2N9YIn,
#app-mount .clear-U3WkKp .searchIcon-1a1-yA,
#app-mount .clear-U3WkKp .searchIcon-32i2pb {
	color: rgb(var(--fontwhite2));
}
.clear-1pMieT.iconLayout-1WxHy4:hover .icon-3cZ1F_,
.iconLayout-3OgqU3:hover .icon-1S6UIr.clear--Eywng,
#app-mount .clearIcon-xXwSFS:hover,
#app-mount .clear-U3WkKp:hover .clearIcon-2N9YIn,
#app-mount .clear-U3WkKp:hover .searchIcon-1a1-yA,
#app-mount .clear-U3WkKp:hover .searchIcon-32i2pb {
	color: rgb(var(--fontwhite1));
}

#app-mount .searchBox-3Y2Vi7 {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 2px 5px 0 rgba(var(--vtransparencycolor), 0.2);
}

/* ----		15.5.	TAGS							---- */

.botTagRegular-2HEhHi {										/* bottag				regular								*/
	color: rgb(var(--fontwhite1));
}
.botTagRegular-2HEhHi:not([style]) {						/* bottag				regular								*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.botTagRegular-2HEhHi:not([style]) svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.botTagInvert-18-95s {										/* bottag				inverted							*/
	background-color: rgb(var(--fontwhite1));
}

.iconBadge-2wi9r4 {											/* iconbadge												*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.base-PmTxvP {												/* mentionbadge												*/
	color: rgb(var(--fontwhite1));
}

.disableColor-MwOAZf,										/* nitrobadge			flower							*/
.iconBackgroundTierNone-3MPhMJ,
.iconBackgroundTierOne-2LhaMB,
.iconBackgroundTierThree-3qw3JX,
.iconBackgroundTierTwo-3bCmdc {
	color: rgb(var(--fontwhite4));
}
.bannerVisible-14J9lQ .iconBackgroundTierOne-2LhaMB,		/* nitrobadge			icon							*/
.bannerVisible-14J9lQ .iconBackgroundTierThree-3qw3JX,
.bannerVisible-14J9lQ .iconBackgroundTierTwo-3bCmdc,
.iconTierOne-BHC2T8, .iconTierTwo-_1edeM {
	color: rgb(var(--fontwhite1));
}
.flowerStarContainer-3zDVtj path[fill="#4f545c"] {			/* flowerbadge			flower							*/
	fill: rgb(var(--fontwhite4));
}
.flowerStarContainer-3zDVtj path[fill="#ffffff"] {			/* flowerbadge			icon							*/
	fill: rgb(var(--fontwhite1));
}
.icon-1ihkOt {												/* flowerbadge			icon							*/
	color: rgb(var(--fontwhite1));
}

/* ----		15.6.	ICONS							---- */

.emptySearchImage-1qOMLW,									/* empty search												*/
.image-1GzsFd {												/* no peoples/webhooks/etc.									*/
	opacity: 0.6;
}

.gameIcon-gg34Dz {											/* gameicon				unknowngame							*/
	color: rgb(var(--fontwhite1));
}

#app-mount .invalidPoop-pnUbq7 {							/* erroricon			invalidpoop							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	opacity: 0.7;
}
#app-mount .guildIconExpired-2Qcq05 {						/* erroricon			expiredguild						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	opacity: 0.7;
}

img[src="/assets/4c1bab3f945269a5c1be0b3a2c177141.png"],	/* connectionicon		twitch								*/
img[src="/assets/402008166e5ef53b0045b10930b263b0.png"] {
	-webkit-mask: url(https://discordapp.com/assets/4c1bab3f945269a5c1be0b3a2c177141.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/0ef81742942677bcef0bebdfb7061d29.png"],	/* connectionicon		youtube								*/
img[src="/assets/3f8d3e1dd3c9426ac7e680dada39650e.png"] {
	-webkit-mask: url(https://discordapp.com/assets/0ef81742942677bcef0bebdfb7061d29.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/3a257c4cab129e956b05bd50047eb0f9.png"],	/* connectionicon		battlenet							*/
img[src="/assets/cf74f0c780cba6ae11728b8ca740b30c.png"] {
	-webkit-mask: url(https://discordapp.com/assets/3a257c4cab129e956b05bd50047eb0f9.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/de5fb9e860729912c65048c1c657e1a3.png"],	/* connectionicon		skype								*/
img[src="/assets/1c419ecaf6e5406addbae729c7fa2e75.png"] {
	-webkit-mask: url(https://discordapp.com/assets/de5fb9e860729912c65048c1c657e1a3.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/fbbd224a0d94747c102515090682bbe1.png"],	/* connectionicon		LoL									*/
img[src="/assets/f87228c98e49168b6cf7ad38651b4e87.png"] {
	-webkit-mask: url(https://discordapp.com/assets/fbbd224a0d94747c102515090682bbe1.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/baf4bdd36b7ef74e8f34b402e66f81f4.png"],	/* connectionicon		steam								*/
img[src="/assets/6ca4a49418715a16e226be1280494f46.png"] {
	-webkit-mask: url(https://discordapp.com/assets/baf4bdd36b7ef74e8f34b402e66f81f4.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/bcc7bc0c0b27f9cbadaa1a47ea79db22.png"],	/* connectionicon		reddit								*/
img[src="/assets/51edbb92b1904c19197eb16be97bc6fb.png"] {
	-webkit-mask: url(https://discordapp.com/assets/bcc7bc0c0b27f9cbadaa1a47ea79db22.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/c926e69c482dac25b8e940db74496813.png"],	/* connectionicon		facebook							*/
img[src="/assets/27fb89c30127405c6a5370b477590da6.png"] {
	-webkit-mask: url(https://discordapp.com/assets/c926e69c482dac25b8e940db74496813.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/2ac50d286a1c883f28b5149239a8ad36.png"],	/* connectionicon		twitter								*/
img[src="/assets/c38327e52d3a859d550af398edb8d8e0.png"] {
	-webkit-mask: url(https://discordapp.com/assets/2ac50d286a1c883f28b5149239a8ad36.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/fe3770614c2658a07dea3ecb286ce745.png"],	/* connectionicon		spotify								*/
img[src="/assets/739cb09703de9dcfe68d0200a163d9fc.png"] {
	-webkit-mask: url(https://discordapp.com/assets/fe3770614c2658a07dea3ecb286ce745.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/850ed4fcf5839b7a32651f5959e8511e.png"],	/* connectionicon		xbox								*/
img[src="/assets/4c59c8e37dda86294d3cf237b2695dde.png"] {
	-webkit-mask: url(https://discordapp.com/assets/850ed4fcf5839b7a32651f5959e8511e.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}

img[src="/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png"] {	/* videosettings		opus								*/
	-webkit-mask: url(https://discordapp.com/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png) center/contain no-repeat;
	background: rgb(var(--fontwhite2));
	object-position: -9999999px -9999999px;
}

[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadge-2BqF-Z {					/* userbadges			xbox								*/
	background: rgb(var(--fontwhite1));
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeStaff-13GO7z {
	-webkit-mask: url(https://discordapp.com/assets/7cfd90c8062139e4804a1fa59f564731.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgePartner-SjK6L2 {
	-webkit-mask: url(https://discordapp.com/assets/a0e288a458c48dfcf548dadc277e42e6.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypesquad-1YIe7Z {
	-webkit-mask: url(https://discordapp.com/assets/3a050fcc884255231b99b7033c776070.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypeSquadOnlineHouse1-xN6tES {
	-webkit-mask: url(https://discordapp.com/assets/1115767aed344e96a27a12e97718c171.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypeSquadOnlineHouse2-3jBpXR {
	-webkit-mask: url(https://discordapp.com/assets/d3478c6bd5cee0fc600e55935ddc81aa.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypeSquadOnlineHouse3-1YbjMX {
	-webkit-mask: url(https://discordapp.com/assets/2a085ed9c86f3613935a6a8667ba8b89.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypeSquadOnlineHouse1Winner-3OGyO6 {
	-webkit-mask: url(https://discordapp.com/assets/75f75c3142b8d44ea7052c2bcb9a9043.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypeSquadOnlineHouse2Winner-3GW5Sm {
	-webkit-mask: url(https://discordapp.com/assets/d4a8fe68fc5f40c8a778f858881a7b84.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeHypeSquadOnlineHouse3Winner-2iVu11 {
	-webkit-mask: url(https://discordapp.com/assets/5dc48a7859a00e7d95ad8382156aab84.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeEarlySupporter-PQB_0a {
	-webkit-mask: url(https://discordapp.com/assets/ce15562552e3d70c56d5408cfeed2ffd.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgePremium-3kZ9Qj {
	-webkit-mask: url(https://discordapp.com/assets/379d2b3171722ef8be494231234da5d1.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileBadgeBugHunter-IV0vLE {
	-webkit-mask: url(https://discordapp.com/assets/df26f079738a4dcd07cbce6eb3c957f1.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileGuildSubscriberlvl1-pKd1EZ {
	-webkit-mask: url(https://discordapp.com/assets/24e49184598820f274e62293349a2e43.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileGuildSubscriberlvl2-1aIFve {
	-webkit-mask: url(https://discordapp.com/assets/cc73fba5c2e9b70752bbd1db35a1b9c3.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileGuildSubscriberlvl3-33AROf {
	-webkit-mask: url(https://discordapp.com/assets/a4c3939a9b03274246df9b144fcd86cf.svg) center/contain no-repeat;
}
[class*="topSection"]:not(.topSectionNormal-2-vo2m) .profileGuildSubscriberlvl4-2yY8EG {
	-webkit-mask: url(https://discordapp.com/assets/d01bee8a9b41bd9dda26a43221b2e7e8.svg) center/contain no-repeat;
}

/* ----		15.7.	SCROLLBARS						---- */

::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar {
	width: 8px;
	height: 8px;
}
#app-mount .scroller-3vODG7::-webkit-scrollbar,
#app-mount #bda-qem-twitch-container .scroller-2FKFPG::-webkit-scrollbar,
#app-mount #bda-qem-favourite-container .scroller-2FKFPG::-webkit-scrollbar {
	width: 6px;
	height: 6px;
}
#app-mount .scroller--qpKGq::-webkit-scrollbar,
#app-mount .scrollbar-3dvm_9::-webkit-scrollbar,
#app-mount .scroller-2PSBSf::-webkit-scrollbar {
	width: 4px;
	height: 4px;
}
 ::-webkit-scrollbar,
 ::-webkit-scrollbar-track,
 ::-webkit-scrollbar-track-piece,
#app-mount ::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar-track,
#app-mount ::-webkit-scrollbar-track-piece {
	border-color: transparent;
	background: transparent;
}
::-webkit-scrollbar-thumb,
#app-mount ::-webkit-scrollbar-thumb {
	border-radius: 10px;
	border: none;
	background-color: rgb(var(--vaccentcolor));
}
::-webkit-scrollbar-corner,
#app-mount ::-webkit-scrollbar-corner {
	visibility: hidden;
}
.scrollerThemed-2oenus.themeHidden-2yP93k .scroller-2FKFPG::-webkit-scrollbar-corner,
.scrollerThemed-2oenus.themeHidden-2yP93k .scroller-2FKFPG::-webkit-scrollbar-thumb,
.scrollerThemed-2oenus.themeHidden-2yP93k .scroller-2FKFPG::-webkit-scrollbar-track,
.scrollerThemed-2oenus.themeHidden-2yP93k .scroller-2FKFPG::-webkit-scrollbar {
	display: none;
}

/* ----		15.8.	NOTIFICATIONBAR					---- */

#app-mount .notice-2FJMB4 {
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .notice-2X5hT5 {
	background-color: rgba(var(--vtransparencycolor), 0.6);
}
#app-mount .button-1MICoQ:not(:hover) {
	border-color: rgba(var(--fontwhite1), 0.25);
	color: rgb(var(--fontwhite1));
}
#app-mount .button-1MICoQ:hover {
	border-color: rgb(var(--fontwhite1));
	background-color: rgb(var(--fontwhite1));
}
#app-mount .dismiss-SCAH9H {
	-webkit-mask: url(https://discordapp.com/assets/7731c77d99babca1a8faec204d98c380.svg) 50% 55%/10px 10px no-repeat;
	background: rgb(var(--fontwhite1));
}
#app-mount .icon-KgjVwm:empty,
#app-mount .platformIcon-2NdO9F:empty {
	background: rgb(var(--fontwhite1));
}
#app-mount .iconWindows-1KG_XN {
	-webkit-mask: url(https://discordapp.com/assets/24b843ed68d70abffbf4fdab9b400cc9.svg) center/contain no-repeat;
}
#app-mount .iconApple-1hp9Sq {
	-webkit-mask: url(https://discordapp.com/assets/ca511da5c9b326e5cb3f6befab1a3143.svg) center/contain no-repeat;
}
#app-mount .iconAndroid-3HTSwF {
	-webkit-mask: url(https://discordapp.com/assets/296aebeec33f5ce47db9ebbee9ccf1fc.svg) center/contain no-repeat;
}
#app-mount .premiumLogo-30dge3 {
	-webkit-mask: url(https://discordapp.com/assets/9328a2df4b542ac8725b57010a52f73b.svg) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
}
.noticeBrand-3nQBC_ {
	text-shadow: 1px 1px var(--vtextshadow);
}
.noticeBrand-3nQBC_ .button-1MICoQ {
	box-shadow: 1px 1px var(--vtextshadow);
	text-shadow: 1px 1px var(--vtextshadow);
}
#app-mount .noticeBrand-3nQBC_ .icon-KgjVwm:empty:after,
#app-mount .noticeBrand-3nQBC_ .platformIcon-2NdO9F:empty:after,
#app-mount .noticeBrand-3nQBC_ .premiumLogo-30dge3:after,
#app-mount .noticeBrand-3nQBC_ .dismiss-SCAH9H:after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background: var(--vtextshadow);
}

/* ----		15.9.	TOOLTIPS						---- */

.headerText-1e7ZU0,
.bodyText-3yi6Dj {
	color: rgb(var(--fontwhite1));
}
#app-mount .tooltip-2QfLtc {
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .tooltipBlack-PPG47z {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
#app-mount .tooltipBlack-PPG47z .tooltipPointer-3ZfirK {
	border-top-color: rgb(var(--vaccentcolor));
}
.emptyUser-7txhlW {
	background: rgba(var(--vtransparencycolor), 0.5);
}
.moreUsers-7v8yWY {
	background: rgba(var(--vtransparencycolor), 0.5);
}

/* ----		15.10.	TOASTS							---- */

#app-mount .toast,
#app-mount .bd-toast {
	background-color: rgb(var(--vaccentcolor));
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
#app-mount .toast.icon,
#app-mount .bd-toast.icon {
	background-image: none !important;
}
#app-mount .toast.icon:before,
#app-mount .bd-toast.icon:before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: rgb(var(--fontwhite1)) !important;
}
#app-mount .toast.toast-brand.icon:after,
#app-mount .bd-toast.toast-brand.icon:after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background: var(--vtextshadow);
}
#app-mount .toast.toast-brand.icon:before,
#app-mount .bd-toast.toast-brand.icon:before,
#app-mount .toast.toast-brand.icon:after,
#app-mount .bd-toast.toast-brand.icon:after {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHhtbDpzcGFjZT0icHJlc2VydmUiIHg9IjBweCIgeT0iMHB4IiB3aWR0aD0iNTEycHgiIGhlaWdodD0iNTEycHgiIHZpZXdCb3g9IjI3IDI3IDExNSAxMTUiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDkwIDkwOyI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMTEuMywxMjQuMWMwLDAtMy40LTQuMS02LjMtNy43YzEyLjYtMy41LDE3LjQtMTEuMywxNy40LTExLjMgYy00LDIuNi03LjcsNC40LTExLjEsNS42Yy00LjgsMi05LjUsMy4zLTE0LDQuMWMtOS4yLDEuNy0xNy42LDEuMy0yNC45LTAuMWMtNS41LTEtMTAuMi0yLjUtMTQuMS00LjFjLTIuMi0wLjgtNC42LTEuOS03LjEtMy4zIGMtMC4zLTAuMi0wLjYtMC4zLTAuOS0wLjVjLTAuMS0wLjEtMC4zLTAuMi0wLjQtMC4yYy0xLjctMS0yLjYtMS42LTIuNi0xLjZzNC42LDcuNiwxNi44LDExLjJjLTIuOSwzLjYtNi40LDcuOS02LjQsNy45IGMtMjEuMi0wLjYtMjkuMy0xNC41LTI5LjMtMTQuNWMwLTMwLjYsMTMuOC01NS40LDEzLjgtNTUuNGMxMy44LTEwLjMsMjYuOS0xMCwyNi45LTEwbDEsMS4xQzUyLjgsNTAuMyw0NSw1Ny45LDQ1LDU3LjkgczIuMS0xLjIsNS43LTIuN2MxMC4zLTQuNSwxOC40LTUuNywyMS44LTZjMC41LTAuMSwxLjEtMC4yLDEuNi0wLjJjNS45LTAuNywxMi41LTAuOSwxOS40LTAuMmM5LjEsMSwxOC45LDMuNywyOC45LDkuMSBjMCwwLTcuNS03LjItMjMuOS0xMi4xbDEuMy0xLjVjMCwwLDEzLjEtMC4zLDI2LjksMTBjMCwwLDEzLjgsMjQuOCwxMy44LDU1LjRDMTQwLjYsMTA5LjYsMTMyLjUsMTIzLjUsMTExLjMsMTI0LjF6IE0xMDEuNyw3OS43Yy01LjQsMC05LjgsNC43LTkuOCwxMC41YzAsNS44LDQuNCwxMC41LDkuOCwxMC41YzUuNCwwLDkuOC00LjcsOS44LTEwLjUgQzExMS41LDg0LjQsMTA3LjEsNzkuNywxMDEuNyw3OS43eiBNNjYuNyw3OS43Yy01LjQsMC05LjgsNC43LTkuOCwxMC41YzAsNS44LDQuNCwxMC41LDkuOCwxMC41YzUuNCwwLDkuOC00LjcsOS44LTEwLjUgQzc2LjUsODQuNCw3Mi4xLDc5LjcsNjYuNyw3OS43eiIvPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-danger.icon:before,
#app-mount .toast.toast-error.icon:before,
#app-mount .bd-toast.toast-danger.icon:before,
#app-mount .bd-toast.toast-error.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTUgMTMuNTlMMTUuNTkgMTcgMTIgMTMuNDEgOC40MSAxNyA3IDE1LjU5IDEwLjU5IDEyIDcgOC40MSA4LjQxIDcgMTIgMTAuNTkgMTUuNTkgNyAxNyA4LjQxIDEzLjQxIDEyIDE3IDE1LjU5eiIvPiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PC9zdmc+) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-facebook.icon:before,
#app-mount .bd-toast.toast-facebook.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHg9IjBweCIgeT0iMHB4IiB3aWR0aD0iNTEycHgiIGhlaWdodD0iNTEycHgiIHZpZXdCb3g9Ii01IC01IDEwMCAxMDAiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDkwIDkwOyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+PGc+PHBhdGggaWQ9IkZhY2Vib29rX194MjhfYWx0X3gyOV8iIGQ9Ik05MCwxNS4wMDFDOTAsNy4xMTksODIuODg0LDAsNzUsMEgxNUM3LjExNiwwLDAsNy4xMTksMCwxNS4wMDF2NTkuOTk4ICAgQzAsODIuODgxLDcuMTE2LDkwLDE1LjAwMSw5MEg0NVY1NkgzNFY0MWgxMXYtNS44NDRDNDUsMjUuMDc3LDUyLjU2OCwxNiw2MS44NzUsMTZINzR2MTVINjEuODc1QzYwLjU0OCwzMSw1OSwzMi42MTEsNTksMzUuMDI0VjQxICAgaDE1djE1SDU5djM0aDE2YzcuODg0LDAsMTUtNy4xMTksMTUtMTUuMDAxVjE1LjAwMXoiIGZpbGw9IndoaXRlIi8+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-info.icon:before,
#app-mount .bd-toast.toast-info.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPiAgICA8cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnptMSAxNWgtMnYtNmgydjZ6bTAtOGgtMlY3aDJ2MnoiLz48L3N2Zz4=) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-premium.icon:before,
#app-mount .bd-toast.toast-premium.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDMiIGhlaWdodD0iMjYiPiAgPHBhdGggZmlsbD0iI0ZGRiIgZmlsbC1ydWxlPSJldmVub2RkIiBkPSJNOTYuMjgyNiA4LjYwMjc4ODI0bC0xLjIxNTUgOC4zOTAzNTI5NmMtLjI3NzUgMS45ODI2Mjc0LTIuNDY1NSAyLjkwMzMzMzMtNC40NzkgMi45MDMzMzMzLTEuODc1IDAtMy43MTU1LS45MjA3MDU5LTMuNDcyNS0yLjcyNTkyMTZsMS4yMTU1LTguNTY3NzY0NjZjLjI3NzUtMS44NzY1ODgyNCAyLjQ2NTUtMi44MzI0NzA2IDQuNDc5LTIuODMyNDcwNiAyLjAxNCAwIDMuNzUuOTU1ODgyMzYgMy40NzI1IDIuODMyNDcwNk05My43NzIxLjAwMzkyNTVsLjAwMDUtLjAwNDA3ODQ0aC0xMy4wODRjLS4zMzQgMC0uNjE4LjI1MDMxMzcyLS42NjYuNTg3Mjk0MTJsLS42MzY1IDQuNDMyMjM1M2MtLjA1OTUuNDE0NDcwNTguMjU2Ljc4NjExNzY0LjY2NjUuNzg2MTE3NjRoMi4zODk1Yy4yNCAwIC40MDQ1LjI0OTgwMzkyLjMxLjQ3NTY0NzA2LS4yOTguNzEyMTk2MDctLjUxNTUgMS40ODYwNzg0My0uNjM2IDIuMzIxNjQ3MDZsLTEuMjE1NSA4LjU2Nzc2NDY2Yy0uNzk5IDUuNzM1Mjk0MiAzLjg4OSA4LjYwMjQzMTQgOC45OTMgOC42MDI0MzE0IDUuMzQ3NSAwIDEwLjU5MDUtMi44NjcxMzcyIDExLjM4OS04LjYwMjQzMTRsMS4yMTUtOC41Njc3NjQ2NmMuNzgzLTUuNjIyMTE3NjUtMy43Mzk1LTguNDg4MjM1My04LjcyNTUtOC41OTg4NjI3NW0tNzguNTk1MjUgMTEuNzI4NjUxbC4wNjcgNC4xNTg5ODA0Yy4wMDE1LjA4NTEzNzItLjA1NS4xNjA1ODgyLS4xMzYuMTgxNDkwMmgtLjAwMDVsLTEuMzg1NS01LjAxNjQ3MDZjLS4wMDItLjAwNzY0NzEtLjAwNS0uMDE0Nzg0My0uMDA4LS4wMjI0MzE0TDkuNDE0MzUuNzcwNzcyNTNjLS4xMDYtLjI1Mjg2Mjc1LS4zNDk1LS40MTY1MDk4LS42MTk1LS40MTY1MDk4aC00Ljg3MjVjLS4zMzYgMC0uNjIwNS4yNTIzNTI5NC0uNjY3LjU5MTM3MjU0TC4wMDY4NSAyNC42MzcyNDMxYy0uMDU3LjQxMzQ1MS4yNTc1Ljc4MjAzOTMuNjY2NS43ODIwMzkzaDQuODU0Yy4zMzY1IDAgLjYyMTUtLjI1MzM3MjYuNjY3NS0uNTkyOTAybDEuMjcyLTkuNDEyNTA5OGMuMDAxNS0uMDA5MTc2NS4wMDItLjAxODM1My4wMDItLjAyNzUyOTRsLS4wNjk1LTQuODM2NTA5OC4xMzg1LS4wMzUxNzY1IDEuNDU1NSA1LjAxNjQ3MDZjLjAwMjUuMDA3MTM3Mi4wMDUuMDEzNzY0Ny4wMDc1LjAyMDkwMmw0LjAyMTUgOS40NTM4MDM5Yy4xMDY1LjI1MDgyMzUuMzQ5NS40MTM0NTEuNjE3NS40MTM0NTFoNS4yNTY1Yy4zMzYgMCAuNjIwNS0uMjUyMzUzLjY2Ny0uNTkxODgyNGwzLjI0OTUtMjMuNjkxNjA3ODRjLjA1NjUtLjQxMjk0MTE4LS4yNTgtLjc4MTUyOTQyLS42NjctLjc4MTUyOTQyaC00LjgyMDVjLS4zMzYgMC0uNjIwNS4yNTE4NDMxNC0uNjY3LjU5MDg2Mjc1bC0xLjQ4IDEwLjc1ODkwMmMtLjAwMS4wMDkxNzY0LS4wMDE1LjAxODg2MjctLjAwMTUuMDI4NTQ5bTkuMzk0IDEzLjY4NjYwMzloNC44NTVjLjMzNiAwIC42MjA1LS4yNTIzNTI5LjY2Ny0uNTkxMzcyNmwzLjI0OS0yMy42OTIxMTc2Yy4wNTY1LS40MTI5NDEyLS4yNTgtLjc4MTUyOTQ0LS42NjctLjc4MTUyOTQ0aC00Ljg1NWMtLjMzNiAwLS42MjA1LjI1MjM1Mjk0LS42NjcuNTkxMzcyNTVsLTMuMjQ5IDIzLjY5MjExNzY4Yy0uMDU2NS40MTI5NDEyLjI1OC43ODE1Mjk0LjY2Ny43ODE1Mjk0TTM2LjYyMTE1LjkwNjA3NDVsLS42MzYgNC40MzIyMzUzYy0uMDU5NS40MTQ0NzA2LjI1NTUuNzg2MTE3NjUuNjY2Ljc4NjExNzY1aDUuMDgwNWMuNDA4NSAwIC43MjMuMzY3NTY4NjMuNjY3NS43ODA1MDk4bC0yLjM5MzUgMTcuNzM0MDM5MjVjLS4wNTU1LjQxMjQzMTMuMjU4NS43OC42NjcuNzhoNC45MjU1Yy4zMzY1IDAgLjYyMS0uMjUyODYyOC42NjctLjU5MjkwMmwyLjQ0NC0xOC4xMDg3NDUxYy4wNDYtLjMzOTUyOTQuMzMwNS0uNTkyOTAxOTUuNjY3LS41OTI5MDE5NWg1LjQ2MjVjLjMzNCAwIC42MTgtLjI0OTgwMzkyLjY2Ni0uNTg3Mjk0MTJsLjYzNy00LjQzMjIzNTNjLjA1OTUtLjQxNDQ3MDU4LS4yNTU1LS43ODYxMTc2NC0uNjY2NS0uNzg2MTE3NjRoLTE4LjE4NzVjLS4zMzQ1IDAtLjYxOC4yNTAzMTM3LS42NjY1LjU4NzI5NDFNNzEuMDM4NyA5LjA5ODM2ODZjLS4xNzQgMS40NTE0MTE3Ny0xLjI4NDUgMi45MDI4MjM1Ny0zLjE5NSAyLjkwMjgyMzU3aC0yLjg2OTVjLS40MSAwLS43MjQ1LS4zNjk2MDc5LS42NjctLjc4MzA1ODlsLjYwNzUtNC4zNjE4ODIzM2MuMDQ3LS4zMzg1MDk4LjMzMTUtLjU5MDM1Mjk0LjY2Ny0uNTkwMzUyOTRoMy4wNjFjMS44NDA1IDAgMi41Njk1IDEuMzEwMTk2MDggMi4zOTYgMi44MzI0NzA2TTY5LjMzNzIuMzU0MjExNzZoLTkuMjQwNWMtLjMzNiAwLS42MjA1LjI1MjM1Mjk0LS42NjcuNTkxMzcyNTRsLTMuMjQ5IDIzLjY5MjExNzdjLS4wNTY1LjQxMjk0MTEuMjU4Ljc4MTUyOTQuNjY3Ljc4MTUyOTRoNC45MjM1Yy4zMzY1IDAgLjYyMTUtLjI1MzM3MjYuNjY3NS0uNTkyOTAybC45NTYtNy4wNzY1ODgyYy4wMjMtLjE2OTc2NDcuMTY1LS4yOTYxOTYxLjMzMzUtLjI5NjE5NjFoLjYzM2MuMTE0NSAwIC4yMjE1LjA1OTY0NzEuMjgzNS4xNTgwMzkybDQuNzAyIDcuNDkxMDU4OGMuMTI0LjE5NzI5NDIuMzM3NS4zMTY1ODgzLjU2NzUuMzE2NTg4M2g2LjA4MWMuNTQ1IDAgLjg2NDUtLjYyNTAxOTYuNTUyLTEuMDgwMjc0NWwtNC45MzQ1LTcuMTkxODA0Yy0uMTE4LS4xNzI4MjM1LS4wNTc1LS40MTI0MzEzLjEyOC0uNTA0NzA1OCAzLjE1MDUtMS41Njk2ODYzIDQuOTc5NS0zLjE3ODExNzcgNS41ODMtNy42NTAxMTc3LjY5MzUtNS44NzcwMTk2LTIuOTE3LTguNjM4MTE3NjMtNy45ODY1LTguNjM4MTE3NjMiLz48L3N2Zz4=) 6px 50%/63px 16px no-repeat;
}
#app-mount .toast.toast-spotify.icon:before,
#app-mount .bd-toast.toast-spotify.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pgo8IS0tIEdlbmVyYXRvcjogQWRvYmUgSWxsdXN0cmF0b3IgMTkuMC4wLCBTVkcgRXhwb3J0IFBsdWctSW4gLiBTVkcgVmVyc2lvbjogNi4wMCBCdWlsZCAwKSAgLS0+CjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIiBpZD0iQ2FwYV8xIiB4PSIwcHgiIHk9IjBweCIgdmlld0JveD0iMCAwIDUwOC41MiA1MDguNTIiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDUwOC41MiA1MDguNTI7IiB4bWw6c3BhY2U9InByZXNlcnZlIiB3aWR0aD0iMjRweCIgaGVpZ2h0PSIyNHB4Ij4KPGc+Cgk8Zz4KCQk8Zz4KCQkJPHBhdGggZD0iTTI1NC4yNiwwQzExMy44NDUsMCwwLDExMy44NDUsMCwyNTQuMjZzMTEzLjg0NSwyNTQuMjYsMjU0LjI2LDI1NC4yNiAgICAgczI1NC4yNi0xMTMuODQ1LDI1NC4yNi0yNTQuMjZTMzk0LjY3NSwwLDI1NC4yNiwweiBNMzcxLjY5Niw0MDMuMjg4Yy0zLjE3OCw1LjgxNi05LjEyMiw5LjA1OC0xNS4yODcsOS4wNTggICAgIGMtMi44NiwwLTUuNzIxLTAuNjY3LTguNDIyLTIuMTI5Yy00MC43MTMtMjIuNDM4LTg2Ljk1Ny0zNC4yOTMtMTMzLjY3Ny0zNC4yOTNjLTI4LDAtNTUuNjUxLDQuMTYzLTgyLjEyNiwxMi4zNjMgICAgIGMtOS4yMTcsMi44Ni0xOS4wMDYtMi4yODgtMjEuODM1LTExLjUzN2MtMi44Ni05LjE4NSwyLjI4OC0yOC43LDExLjUzNy0zMS41OTJjMjkuODQ0LTkuMjQ5LDYwLjk1OS0xMy45MjEsOTIuNDU1LTEzLjkyMSAgICAgYzUyLjU2OCwwLDEwNC42NiwxMy4zNDksMTUwLjUyMiwzOC42MTZDMzczLjMxNywzNzQuNDYxLDM3Ni40LDM5NC44NjYsMzcxLjY5Niw0MDMuMjg4eiBNNDA0LjAxOSwzMDcuNTI3ICAgICBjLTMuNjIzLDcuMDI0LTEwLjc0MiwxOC4zMzgtMTguMDg0LDE4LjMzOGMtMy4yMSwwLTYuMzg4LTAuNjk5LTkuMzc2LTIuMzJjLTUwLjQ3MS0yNi4xODktMTA1LjA0MS0zOS40NzQtMTYyLjIxOC0zOS40NzQgICAgIGMtMzEuNDk2LDAtNjIuNzcsNC4xMzItOTIuOTY0LDEyLjQ1OWMtMTAuOTAxLDIuOTU2LTIyLjA4OS0zLjQwMS0yNS4wNDUtMTQuMzAyYy0yLjkyNC0xMC45MDEsMy40NjQtMjkuNDMxLDE0LjMzNC0zMi4zODYgICAgIGMzMy42ODktOS4xODUsNjguNTg3LTEzLjg1NywxMDMuNjc0LTEzLjg1N2M2Mi44OTgsMCwxMjUuNDQ1LDE1LjI1NiwxODAuOTM4LDQ0LjExNCAgICAgQzQwNS4yOSwyODUuMjQ4LDQwOS4xOTksMjk3LjUxNiw0MDQuMDE5LDMwNy41Mjd6IE00MTcuNTI2LDIzMC44MzZjLTMuNDY0LDAtNy4wMjQtMC43OTUtMTAuMzYxLTIuNDQ3ICAgICBjLTYwLjIyOC0zMC4wMzQtMTI1LjA5Ni00NS4yMjYtMTkyLjc2MS00NS4yMjZjLTM1LjI3OSwwLTcwLjQzLDQuMjkxLTEwNC41MzMsMTIuNzEzYy0xMi41MjIsMy4wODMtMjUuMTQtNC41MTMtMjguMjIzLTE3LjAwNCAgICAgYy0zLjExNS0xMi40NTksNC41MTMtMjcuNTU1LDE3LjAwNC0zMC42MzhjMzcuNzI2LTkuMzc2LDc2LjY1OS0xNC4xMTEsMTE1LjcyLTE0LjExMWM3NC45NzUsMCwxNDYuODY3LDE2Ljg3NywyMTMuNTc4LDUwLjEyMSAgICAgYzExLjUzNyw1Ljc1MywxNi4yNDEsMTkuNzM3LDEwLjQ4OCwzMS4yNDJDNDM0LjMwOCwyMjMuNjUzLDQyNi4xMDgsMjMwLjgzNiw0MTcuNTI2LDIzMC44MzZ6IiBmaWxsPSIjRkZGRkZGIi8+CgkJPC9nPgoJPC9nPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+Cjwvc3ZnPgo=) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-streamermode.icon:before,
#app-mount .bd-toast.toast-streamermode.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHg9IjBweCIgeT0iMHB4IiB2aWV3Qm94PSItMjUgLTI1IDU0MiA1NDIiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDQ5MiA0OTI7IiB4bWw6c3BhY2U9InByZXNlcnZlIiB3aWR0aD0iNTEycHgiIGhlaWdodD0iNTEycHgiPjxwYXRoIGQ9Ik00ODguMywxNDIuNXYyMDMuMWMwLDE1LjctMTcsMjUuNS0zMC42LDE3LjdsLTg0LjYtNDguOHYxMy45YzAsNDEuOC0zMy45LDc1LjctNzUuNyw3NS43SDc1LjdDMzMuOSw0MDQuMSwwLDM3MC4yLDAsMzI4LjQgICBWMTU5LjljMC00MS44LDMzLjktNzUuNyw3NS43LTc1LjdoMjIxLjhjNDEuOCwwLDc1LjcsMzMuOSw3NS43LDc1Ljd2MTMuOWw4NC42LTQ4LjhDNDcxLjMsMTE3LDQ4OC4zLDEyNi45LDQ4OC4zLDE0Mi41eiIgZmlsbD0iI0ZGRkZGRiIvPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-success.icon:before,
#app-mount .bd-toast.toast-success.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPiAgICA8cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnptLTIgMTVsLTUtNSAxLjQxLTEuNDFMMTAgMTQuMTdsNy41OS03LjU5TDE5IDhsLTkgOXoiLz48L3N2Zz4=) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.toast-warning.icon:before,
#app-mount .toast.toast-warn.icon:before,
#app-mount .bd-toast.toast-warning.icon:before,
#app-mount .bd-toast.toast-warn.icon:before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPiAgICA8cGF0aCBkPSJNMSAyMWgyMkwxMiAyIDEgMjF6bTEyLTNoLTJ2LTJoMnYyem0wLTRoLTJ2LTRoMnY0eiIvPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
#app-mount .toast.icon:not(.toast-brand):not(.toast-danger):not(.toast-error):not(.toast-facebook):not(.toast-info):not(.toast-premium):not(.toast-spotify):not(.toast-streamermode):not(.toast-success):not(.toast-warning):not(.toast-warn):before, .bd-toast.icon:not(.toast-brand):not(.toast-danger):not(.toast-error):not(.toast-facebook):not(.toast-info):not(.toast-premium):not(.toast-spotify):not(.toast-streamermode):not(.toast-success):not(.toast-warning):not(.toast-warn):before {
	display: none;
}


/* ~~~~		16.		BDSUPPORT						~~~~ */

.arrow-uglXxc {
	-webkit-mask: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4NCjwhLS0gR2VuZXJhdG9yOiBBZG9iZSBJbGx1c3RyYXRvciAxOS4wLjAsIFNWRyBFeHBvcnQgUGx1Zy1JbiAuIFNWRyBWZXJzaW9uOiA2LjAwIEJ1aWxkIDApICAtLT4NCjxzdmcgdmVyc2lvbj0iMS4xIiBpZD0iQ2FscXVlXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4Ig0KCSB2aWV3Qm94PSItOTUwIDUzMiAxOCAxOCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAtOTUwIDUzMiAxOCAxODsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPHN0eWxlIHR5cGU9InRleHQvY3NzIj4NCgkuc3Qwe2ZpbGw6bm9uZTt9DQoJLnN0MXtmaWxsOm5vbmU7c3Ryb2tlOiNGRkZGRkY7c3Ryb2tlLXdpZHRoOjEuNTtzdHJva2UtbWl0ZXJsaW1pdDoxMDt9DQo8L3N0eWxlPg0KPHBhdGggY2xhc3M9InN0MCIgZD0iTS05MzIsNTMydjE4aC0xOHYtMThILTkzMnoiLz4NCjxwb2x5bGluZSBjbGFzcz0ic3QxIiBwb2ludHM9Ii05MzYuNiw1MzguOCAtOTQxLDU0My4yIC05NDUuNCw1MzguOCAiLz4NCjwvc3ZnPg0K);
	background: rgb(var(--fontwhite1));
}

#app-mount .bd-modal-inner {								/* modal				container							*/
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.bd-modal-inner:after,
.bd-modal-inner:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.bd-modal-inner:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
.bd-modal-inner:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.bd-modal-wrapper .header {									/* modal				header								*/
	background-color: transparent;
	box-shadow: none;
	color: rgb(var(--fontwhite1));
}
.bd-modal-wrapper .bd-modal-body {							/* modal				body								*/
	background-color: transparent;
	color: rgb(var(--fontwhite1));
}
.bd-modal-wrapper .footer {									/* modal				footer								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}
.bd-modal-wrapper .footer button {
	color: rgb(var(--fontwhite1));
}
.bd-modal-wrapper .tab-bar-container {						/* modal				tabbarcontainer						*/
	background: rgba(var(--vtransparencycolor), 0.2);
	border-top-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.1);
}		
.bd-modal-wrapper .tab-bar-container .tab-bar-item {		/* modal				tabbaritem							*/
	color: rgb(var(--fontwhite1)) !important;
}
.bd-modal-wrapper .tab-bar-container .tab-bar-item.selected,/* modal				tabbaritem selected					*/
.bd-modal-wrapper .tab-bar-container .tab-bar-item:hover {	/* modal				tabbaritem hover					*/
	border-color: rgb(var(--fontwhite1)) !important;
}
.bd-modal-wrapper .table-header,							/* modal				tableheader							*/
.bd-modal-wrapper .error {									/* modal				tablerow							*/
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite1));
}
	
#pubslayer .ui-tab-bar-item,
#app-mount #bd-settings-sidebar .ui-tab-bar-item {			/* sidebar				item								*/
	color: rgb(var(--fontwhite3));
}
#pubslayer .ui-tab-bar-item:hover,
#app-mount #bd-settings-sidebar .ui-tab-bar-item:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite2));
}
#pubslayer .ui-tab-bar-item.selected,
#app-mount #bd-settings-sidebar .ui-tab-bar-item.selected {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
#pubslayer .ui-tab-bar-header,
#app-mount #bd-settings-sidebar .ui-tab-bar-header {		/* sidebar				sideitemheader						*/
	color: rgb(var(--fontwhite3));
}
#pubslayer .ui-tab-bar-separator,
#app-mount #bd-settings-sidebar .ui-tab-bar-separator {		/* sidebar				sideitemseparator					*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#bd-settings-sidebar [style*=" color: rgb(114, 118, 125)"] {/* sidebar				credits								*/
	color: rgb(var(--fontwhite4)) !important;
}

.bd-server-description-container {							/* pubslayer			guilddescription					*/
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite3));
}
.bd-server-card .bd-server-tags {							/* pubslayer			guildtags							*/
	color: rgb(var(--fontwhite3));
}
#pubslayer h2.ui-form-title {								/* pubslayer			header								*/
	color: rgb(var(--fontwhite1));
}
#pubslayer button {											/* pubslayer			button								*/
	color: rgb(var(--fontwhite1));
}
#pubslayer input {											/* pubslayer			input								*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#pubslayer input:hover {
	border-color: rgb(var(--vtransparencycolor));
}
#pubslayer input::placeholder {
	color: rgb(var(--fontwhite3));
}

#app-mount #bd-settingspane-container h2.ui-form-title {	/* settingsitems		header								*/
	color: rgb(var(--fontwhite1));
	min-width: 100px;
}
#app-mount #bd-settingspane-container .ui-switch-item h3 {
	color: rgb(var(--fontwhite1));
}
#app-mount #bd-settingspane-container .ui-switch-item .style-description {
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite3));
}

.bd-switch: {												/* bd switch												*/
	box-shadow: inset 0 1px 1px rgba(var(--vtransparencycolor), 0.15);
}
.bd-switch:not(.bd-switch-checked) {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.bd-switch:before {
	background-color: rgb(var(--fontwhite1));
	box-shadow: 0 2px 4px rgba(var(--vtransparencycolor), 0.6);
}

.bd-select-wrapper {										/* bd select			wrapper								*/
	color: rgb(var(--fontwhite1));
}
.bd-select {												/* bd select			inner								*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color:  rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.bd-select-arrow {											/* bd select			arrow								*/
	fill: rgb(var(--fontwhite1));
}
.bd-select .bd-select-options {								/* bd select			popout								*/
	background: transparent;
	border: none;
	border-radius: 4px;
	box-shadow: rgba(var(--vtransparencycolor), 0.3) 0px 2px 5px 0px;
    box-sizing: border-box;
    padding: 6px 8px;
	margin-left: -9px;
}
.bd-select .bd-select-options:after,
.bd-select .bd-select-options:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.bd-select .bd-select-options:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
}
.bd-select .bd-select-options:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
.bd-select .bd-select-option {								/* bd select			popout option						*/
    display: flex;
    align-items: center;
    min-height: 32px;
    border-radius: 2px;
    box-sizing: border-box;
	color: var(--interactive-normal);
    font-size: 14px;
    font-weight: 500;
    line-height: 18px;
    margin-top: 2px;
    margin-bottom: 2px;
    padding: 0 8px;
}
.bd-select .bd-select-option:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: var(--interactive-hover);
}
.bd-select .bd-select-option.selected {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: var(--interactive-active);
}

.bd-pfbtn {													/* addonlist			folderbutton						*/
	color: rgb(var(--fontwhite1));
}

.bd-search-wrapper {										/* addonlist			searchbar container					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.bd-search {												/* addonlist			searchbar input						*/
	color: rgb(var(--fontwhite1))
}
.bd-search::placeholder {
	color: rgb(var(--fontwhite3));
}
.bd-search-wrapper svg[fill] {								/* addonlist			searchbar icon						*/
	fill: rgb(var(--fontwhite1));
}

#app-mount .bd-addon-list .bd-addon-card {					/* addonlist			addoncard							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-color: transparent;
	color: rgb(var(--fontwhite1));
}
#app-mount .bd-addon-list .bda-header {						/* addonlist			header								*/
	color: rgb(var(--fontwhite1));
	border-bottom-color: rgba(var(--fontwhite2), 0.3);
}
#app-mount .bd-addon-list .bd-addon-button svg[fill] {			/* addonlist			header button icon					*/
	fill: currentColor;
}
#app-mount .bd-addon-list .bd-addon-button svg {				/* addonlist			header button icon					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .bd-addon-list .bd-addon-button svg:hover {
	color: rgb(var(--fontwhite1));
}
#app-mount .bd-addon-list .bda-description {				/* addonlist			description							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .bd-addon-list .bda-description::-webkit-scrollbar {
	width: 4px;
	height: 4px;
}
#app-mount .bd-addon-list .bda-footer {						/* addonlist			footer								*/
	border-top-color: rgba(var(--fontwhite2), 0.3);
}
.bd-addon-list .bda-footer button {							/* addonlist			footer button						*/
	color: rgb(var(--fontwhite1));
}

#bd-customcss-detach-container {							/* customcsseditor		detached							*/
	background: transparent;
}
#app-mount .ace-monokai {									/* customcsseditor		container							*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .ace_selection {
	background-color: rgb(var(--vaccentcolor));
}
#app-mount .ace_selected-word {
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .ace_gutter {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite4));
}
#app-mount .ace_active-line {
	background-color: rgba(var(--vaccentcolor), 0.5);
}
#app-mount .ace_gutter-active-line {
	background-color: rgba(var(--vaccentcolor), 0.7);
}
#bd-customcss-attach-controls {
	background-color: rgba(var(--vtransparencycolor), 0.8);
	box-shadow: none;
}
.contentRegion-3nDuYy #bd-customcss-attach-controls,
#bd-customcss-detach-container #bd-customcss-attach-controls {
	background-color: rgba(var(--vtransparencycolor), 0.5);
	box-shadow: inset 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite1));
}
.standardSidebarView-3F1I7i #bd-customcss-attach-controls button,
.bd-detached-css-editor #bd-customcss-attach-controls button {
	color: rgb(var(--fontwhite1));
	background: rgba(var(--vtransparencycolor), 0.5);
	border: none !important;
	border-radius: 3px !important;
	margin: 5px 5px 0 0;
	transition: background-color 0.1s ease;
}
.standardSidebarView-3F1I7i #bd-customcss-attach-controls button:hover,
.bd-detached-css-editor #bd-customcss-attach-controls button:hover {
	background: rgb(var(--vaccentcolor));
}
.standardSidebarView-3F1I7i #editor-detached h3 {
	color: rgb(var(--fontwhite3));
}
#bd-customcss-attach-controls .help-text .inline {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

body #ace_settingsmenu_container > div {					/* customcsseditor		settings							*/
	position: absolute;
	background: transparent;
	top: 10vh !important;
	right: calc(50vw - 300px) !important;
	bottom: 10vh !important;
	left: calc(50vw - 300px) !important;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	box-sizing: border-box;
	padding-top: 50px;
	transform: none;
}
body #ace_settingsmenu_container > div:after,
body #ace_settingsmenu_container > div:before {
	border-radius: 5px;
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	z-index: -1;
	pointer-events: none;
}
body #ace_settingsmenu_container > div:after {
	background: rgba(var(--vtransparencycolor),calc(var(--vtransparencyalpha) * 3));
}
body #ace_settingsmenu_container > div:before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
body .ace_closeButton {
	position: absolute;
	top: -35px;
	right: 12px;
	border-radius: 5px;
	cursor: pointer;
	height: 23px;
	width: 23px;
}
body .ace_closeButton:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
body .ace_closeButton:after {
	content: "Custom CSS Settings";
	color: rgb(var(--fontwhite1));
	font-weight: 600;
	font-size: 18px;
	position: absolute;
	top: 2px;
	left: -550px;
	pointer-events: none;
}
body .ace_closeButton:before {
	color: rgb(var(--fontwhite1));
	line-height: 24px;
	margin-left: 5px;
	opacity: 0.7;
}
body .ace_closeButton:hover:before {
	opacity: 1;
}
body #ace_settingsmenu {
	background-color: transparent;
	box-shadow: none;
	color: rgb(var(--fontwhite1));
	height: calc(80vh - 50px);
	overflow: scroll;
	padding: 0 0.5em 0 1em;
	position: static;
	left: 0;
}
body #ace_settingsmenu .ace_optionsMenuEntry {
	height: 40px;
	display: flex;
	align-items: center;
	justify-content: flex-start;
	margin-bottom: 10px;
}
body #ace_settingsmenu .ace_optionsMenuEntry:hover {
	background: transparent;
}
body #ace_settingsmenu > *:last-child {
	color: rgb(var(--fontwhite1));
	float: right;
}
body #ace_settingsmenu .ace_optionsMenuEntry label {
	color: rgb(var(--fontwhite1));
	font-size: 16px;
	line-height: 24px;
	cursor: pointer;
	flex: 1 0 auto;
	font-weight: 500;
	margin-right: 10px;
}
body #ace_settingsmenu .ace_optionsMenuEntry input[type="text"],
body #ace_settingsmenu .ace_optionsMenuEntry select {
	box-sizing: border-box;
	flex: 0 1 auto;
	width: 200px;
	float: none;
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
	height: 40px;
	padding: 10px;
	border-radius: 3px;
	border-style: solid;
	border-width: 1px;
	transition: background-color .15s ease,border .15s ease;
	font-size: 16px;
}
body #ace_settingsmenu .ace_optionsMenuEntry input[type="text"]:hover,
body #ace_settingsmenu .ace_optionsMenuEntry select:hover {
	border-color: #040405;
}
body #ace_settingsmenu .ace_optionsMenuEntry input[type="text"]:focus,
body #ace_settingsmenu .ace_optionsMenuEntry select:focus {
	border-color: rgb(var(--vaccentcolor));
}
body #ace_settingsmenu .ace_optionsMenuEntry select option {
	background-color: #303339;
	color: rgb(var(--fontwhite1));
}
body #ace_settingsmenu input[type="checkbox"] {
	position: relative;
	width: 44px;
	height: 24px;
	-webkit-appearance: none;
}
body #ace_settingsmenu input[type="checkbox"]:before {
	content: "";
	display: block;
	position: relative;
	width: 44px;
	height: 24px;
	background: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 14px;
	transition: background .15s ease-in-out,box-shadow .15s ease-in-out,border .15s ease-in-out;
}
body #ace_settingsmenu input[type="checkbox"]:checked:before {
	background: rgb(var(--vaccentcolor));
}
body #ace_settingsmenu input[type="checkbox"]:after {
	content: "";
	display: block;
	width: 18px;
	height: 18px;
	position: absolute;
	top: 3px;
	left: 3px;
	bottom: 3px;
	background-color: rgb(var(--fontwhite1));
	border-radius: 10px;
	transition: all .15s ease;
	box-shadow: 0 2px 4px rgba(var(--vtransparencycolor), 0.6);
}
body #ace_settingsmenu input[type="checkbox"]:checked:after {
	transform: translateX(20px);
}


/* ~~~~		17.		PLUGINSUPPORT					~~~~ */

/* ----		17.1.	DATEVIEWER						---- */

#app-mount #dv-mount {
	background: transparent;
}
#app-mount #dv-main {
	border-top-color: rgba(var(--fontwhite1), 0.1);
	color: rgb(var(--fontwhite1));
}
#app-mount #dv-main .dv-date {
	color: rgb(var(--fontwhite3));
	opacity: 1;
}

/* ----		17.2.	SERVERFOLDERS					---- */

body.folderContentIsOpen-zz6FgW .titleBar-AC4pGV.typeMacOS-3EmCyP,
body.folderContentIsOpen-zz6FgW .titleBar-AC4pGV.typeMacOS-3EmCyP .macButtons-2MuSAC {
	width: 144px;
}
body.folderContentIsOpen-zz6FgW .titleBar-AC4pGV.typeMacOS-3EmCyP .macButtons-2MuSAC {
	padding-right: 82px;
}
.base-PmTxvP[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--vtextshadow);
}

/* ----		17.3.	MEMBERCOUNT						---- */

#app-mount #MemberCount {
	background-color: transparent;
	color: rgb(var(--fontwhite2));
	width: calc(100% - 8px);
	margin: 0;
	line-height: 0;
	height: 30px;
}
#MemberCount:after,
#MemberCount:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
#MemberCount:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + var(--vmemberlisttransparency) * 0.85));
}
#MemberCount:before {
	background: var(--vbackground) center/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
	background-attachment: fixed;
}

/* ----		17.4.	SENDBUTTON						---- */

.send-button img {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTIuMDEgMjFMMjMgMTIgMi4wMSAzIDIgMTBsMTUgMi0xNSAyeiIvPiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PC9zdmc+) center/contain no-repeat;
	background: rgb(var(--fontwhite3));
	cursor: pointer;
	object-position: -9999999px -9999999px;
	opacity: 1;
}
.send-button img:hover {
	background: rgb(var(--fontwhite2));
	transform: none;
}
.send-button img:active {
	background: rgb(var(--fontwhite1));
}
.innerDisabled-2mc-iF .send-button {
	display: none;
}

/* ----		17.5.	CHARCOUNTER						---- */

#app-mount #charcounter {
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
.innerDisabled-2mc-iF #charcounter {
	display: none;
}

/* ----		17.6.	REPLYER							---- */

.replyer-icon {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
	border-radius: 3px !important;
	position: relative;
	padding: 0 3px 1px 3px;
	margin-top: 1px;
}
.replyer[style*="cursor:pointer;color:rgba(255,255,255,.4) !important;position:relative;top:-1px;"] {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/70% no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
	border-radius: 3px !important;
	filter: none !important;
	font-size: 0 !important;
	margin: 0 0 0 6px !important;
	opacity: 0.7 !important;
	padding: 7px 10px !important;
	top: -5px !important;
	transition: unset !important;
}
.replyer-icon:hover,
.replyer[style*="cursor:pointer;color:rgba(255,255,255,.4) !important;position:relative;top:-1px;"]:hover {
	-webkit-mask: none !important;
	background: rgba(var(--vtransparencycolor), 0.4) url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/70% no-repeat !important;
	opacity: 1 !important;
}
.replyer-icon:active,
.replyer[style*="cursor:pointer;color:rgba(255,255,255,.4) !important;position:relative;top:-1px;"]:active {
	-webkit-mask: none !important;
	background: rgb(var(--vaccentcolor)) url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/70% no-repeat !important;
}

/* ----		17.7.	CITADOR							---- */

.quote-msg {
	background-color: rgba(var(--vtransparencycolor) , 0.2);
	border-radius: 5px 5px 0 0;
}
.quote-msg .replyer,
.quote-msg .replyer-icon,
.quote-msg .buttonContainer-KtQ8wc {
	display: none;
}
.quote-msg ~ .inner-zqa7da {
	border-radius: 0 0 8px 8px;
}
.quote-close {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxuczpza2V0Y2g9Imh0dHA6Ly93d3cuYm9oZW1pYW5jb2RpbmcuY29tL3NrZXRjaC9ucyIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIiBpZD0iTGF5ZXJfMSIgeD0iMHB4IiB5PSIwcHgiIHdpZHRoPSIyMHB4IiBoZWlnaHQ9IjIwcHgiIHZpZXdCb3g9IjQwIDQwIDIwIDIwIiBlbmFibGUtYmFja2dyb3VuZD0ibmV3IDQwIDQwIDIwIDIwIiB4bWw6c3BhY2U9InByZXNlcnZlIj4NCjxnIGlkPSJQYWdlXzEiPg0KCTxwYXRoIGlkPSJDbG9zZSIgZmlsbD0iIzk5YWFiNSIgZD0iTTQwLjQ0NSw0Mi44NTNsMi40MDgtMi40MDhjMC41OTMtMC41OTMsMS41NTUtMC41OTMsMi4xNDcsMGw1LDVsNS01ICAgYzAuNTkzLTAuNTkzLDEuNTU0LTAuNTkzLDIuMTQ3LDBsMi40MDgsMi40MDhjMC41OTMsMC41OTMsMC41OTMsMS41NTQsMCwyLjE0N2wtNSw1bDUsNWMwLjU5MywwLjU5MywwLjU5MiwxLjU1NCwwLDIuMTQ3ICAgbC0yLjQwOCwyLjQwOGMtMC41OTMsMC41OTMtMS41NTUsMC41OTMtMi4xNDcsMGwtNS01bC01LDVjLTAuNTkzLDAuNTkzLTEuNTU0LDAuNTkzLTIuMTQ3LDBsLTIuNDA4LTIuNDA4ICAgYy0wLjU5My0wLjU5My0wLjU5My0xLjU1NCwwLTIuMTQ3bDUtNWwtNS01QzM5Ljg1Miw0NC40MDcsMzkuODUyLDQzLjQ0NSw0MC40NDUsNDIuODUzeiIvPg0KPC9nPg0KPC9zdmc+) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
}
.delete-msg-btn {
	-webkit-mask: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDE3LjEuMCwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDEuMS8vRU4iICJodHRwOi8vd3d3LnczLm9yZy9HcmFwaGljcy9TVkcvMS4xL0RURC9zdmcxMS5kdGQiPgo8c3ZnIHZlcnNpb249IjEuMSIgaWQ9IkxheWVyXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4IgoJIHZpZXdCb3g9IjAgMCAxNiAxNiIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgMTYgMTYiIHhtbDpzcGFjZT0icHJlc2VydmUiPgo8ZyBpZD0iZWRpdG9yaWFsXy1fdHJhc2hfY2FuIj4KCTxnPgoJCTxwYXRoIGZpbGw9IiNmZmZmZmYiIGQ9Ik01LDYuNUg0djZoMVY2LjV6IE0xNC41LDJIMTBWMC41QzEwLDAuMiw5LjgsMCw5LjUsMGgtNEM1LjIsMCw1LDAuMiw1LDAuNVYySDAuNUMwLjIsMiwwLDIuMiwwLDIuNQoJCQlTMC4yLDMsMC41LDNIMXYxMmMwLDAuNiwwLjQsMSwxLDFoMTFjMC42LDAsMS0wLjQsMS0xVjNoMC41QzE0LjgsMywxNSwyLjgsMTUsMi41UzE0LjgsMiwxNC41LDJ6IE02LDFoM3YxSDZWMXogTTEzLDE0LjUKCQkJYzAsMC4zLTAuMiwwLjUtMC41LDAuNWgtMTBDMi4yLDE1LDIsMTQuOCwyLDE0LjVWM2gxMVYxNC41eiBNOCw1LjVIN3Y3aDFWNS41eiBNMTEsNi41aC0xdjZoMVY2LjV6Ii8+Cgk8L2c+CjwvZz4KPC9zdmc+Cg==) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
}

.citar-btn {
	-webkit-mask: url(https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_format_quote_white_48px.svg) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
	border-radius: 3px;
	filter: none !important;
	font-size: 0;
	margin: 0 0 0 6px !important;
	opacity: 0.7;
	padding: 7px 10px;
	position: relative;
	top: -5px;
	transition: unset !important;
}
.citar-btn:hover {
	-webkit-mask: none !important;
	background: rgba(var(--vtransparencycolor), 0.4) url(https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_format_quote_white_48px.svg) center/contain no-repeat !important;
	opacity: 1;
}
.citar-btn:active {
	-webkit-mask: none !important;
	background: rgb(var(--vaccentcolor)) url(https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_format_quote_white_48px.svg) center/contain no-repeat !important;
}
/* ----		17.8.	LINENUMBERS						---- */

.hljs ol li {
	border-left-color: rgba(var(--fontwhite1), 0.2);
}
.hljs ol li::before {
	color: rgb(var(--fontwhite4));
}

/* ----		17.9.	PERMISSIONVIEWER				---- */

#permissions-modal-wrapper #permissions-modal {				/* modal				container							*/
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
#permissions-modal-wrapper #permissions-modal:after,
#permissions-modal-wrapper #permissions-modal:before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#permissions-modal-wrapper #permissions-modal:after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
}
#permissions-modal-wrapper #permissions-modal:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
}
#permissions-modal-wrapper .header {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite1));
}
#permissions-modal-wrapper .modal-body {
	background-color: transparent;
}
#permissions-modal-wrapper .scroller-title {
	border-bottom: 1px solid rgba(var(--vtransparencycolor), 0.3);
}
#permissions-modal-wrapper .role-side {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#permissions-modal-wrapper .role-item {
	color: rgb(var(--fontwhite2));
}
#permissions-modal-wrapper .role-item:hover {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#permissions-modal-wrapper .role-item.selected {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#permissions-modal-wrapper .perm-side {
	background-color: transparent;
}
#permissions-modal-wrapper .perm-item {
	box-shadow: inset 0 -1px 0 rgba(var(--fontwhite4), 0.3);
}
#permissions-modal-wrapper .perm-name {
	color: rgb(var(--fontwhite3));
}

/* ----		17.10.	BETTERSEARCHPAGE				---- */

#app-mount .BSP-pagination-button {
	background: transparent;
	border-color: rgba(var(--fontwhite1), 0.5);
	left: 0;
	position: relative;
	top: 0;
}
#app-mount .BSP-pagination-button:before {
	content: "»";
	color: rgb(var(--fontwhite1));
	font-size: 20px;
	font-weight: 500;
	line-height: 15px;
	margin-left: -1px;
	position: absolute;
	text-align: center;
	width: 20px;
}

/* ----		17.11.	REPOCONTROLS					---- */

#app-mount #bd-settingspane-container .editIcon,
#app-mount #bd-settingspane-container .trashIcon {
	color: rgb(var(--fontwhite2));
}
#app-mount #bd-settingspane-container .editIcon:hover,
#app-mount #bd-settingspane-container .trashIcon:hover {
	color: rgb(var(--fontwhite1));
}

/* ----		17.12.	DIRECTDOWNLOAD					---- */

#files_directDownload .file {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-color: rgba(var(--vaccentcolor), 0.2);
	border-radius: 6px 6px 0 0;
}
#files_directDownload .file svg {
	fill: rgb(var(--fontwhite1));
	opacity: 0.5;
}
#files_directDownload .file svg:hover {
	opacity: 1;
}
#files_directDownload .file span {
	color: rgb(var(--fontwhite1));
}
#files_directDownload .file .progress-bar {
	background-color: rgb(var(--vaccentcolor));
}

/* ----		17.13.	BETTERFORMATINGREDUX			---- */

.innerDisabled-2mc-iF ~ .bf-toolbar {
	display: none;
}
.bf-arrow {
	-webkit-mask: url('data:image/svg+xml;utf8,<svg fill="white" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z"/><path d="M0 0h24v24H0z" fill="none"/></svg>') center/contain no-repeat;
	background: rgb(var(--fontwhite1)) !important;
}
.bf-toolbar {
	background: transparent;
	overflow: hidden;
	transform: none;
	top: -50px;
}
.bf-toolbar:after {	
	content: "";
	display: block;
	position: absolute;
	width: 100%;
	height: calc(100% - 15px);
	pointer-events: none;
	left: 0px;
	top: 5px;
	background-color: rgba(var(--vtransparencycolor), 0.5);
	border-radius: 3px;
	transform: translate(0, 55px);
	transition: all 200ms ease;
	z-index: 200;
}
.bf-toolbar.bf-visible:after,
.bf-toolbar.bf-hover:hover:after {
	transform: translate(0, 0);
	transition: all 200ms cubic-bezier(0,0,0,1);
}
.bf-toolbar:before {
	background: var(--vpopout) center/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
	z-index: 100;
}
.theme-brand .bf-toolbar:after {
	background: rgb(var(--vaccentcolor)) linear-gradient(rgba(var(--vtransparencycolor), 0.2), rgba(var(--vtransparencycolor), 0.2))!important;
}
.theme-brand .bf-toolbar:before {
	display: none;
}
.bf-toolbar > * {
	z-index: 300;
}
.bf-toolbar .format {
	color: rgb(var(--fontwhite2));
}
.bf-toolbar .format:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}

/* ----		17.14	PLUGIN/THEMEREPO				---- */

#app-mount .pluginEntry svg[fill="currentColor"],
#app-mount .pluginEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN),
#app-mount .themeEntry svg[fill="currentColor"],
#app-mount .themeEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN) {
	color: rgb(var(--fontwhite2)) !important;
}

#app-mount .pluginEntry svg[fill="currentColor"]:hover,
#app-mount .pluginEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN):hover,
#app-mount .themeEntry svg[fill="currentColor"]:hover,
#app-mount .themeEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN):hover {
	color: rgb(var(--fontwhite1)) !important;
}

/* ----		17.15	CHANNELHISTORY					---- */

.channelHistoryButtons {
	top: 4px;
	left: 310px;
}

/* ----		17.16	DISPLAYLARGEMESSAGES			---- */

#app-mount .injectButton-8eKqGu {							/* attachment			injectbutton						*/
	color: rgb(var(--fontwhite4));
}
#app-mount .injectButton-8eKqGu:hover {
	color: rgb(var(--fontwhite3));
}
#app-mount .injectButton-8eKqGu:active {
	color: rgb(var(--fontwhite2));
}


/* ~~~~		18.		THEMESUPPORT					~~~~ */

/* ----		18.1.	THEMEDEVBADGE					---- */

#app-mount .root-SR8cQa .wrapper-3t9DeA.dev-A7f2Rx:not(.statusHovered-gF2976):hover + .headerInfo-30uryT:before,
#app-mount .userPopout-3XzG_A .avatarWrapper-3H_478.dev-A7f2Rx:not(.statusHovered-gF2976):hover .wrapper-3t9DeA:before,
#app-mount .root-SR8cQa .wrapper-3t9DeA.supporter-Z3FfwL:not(.statusHovered-gF2976):hover + .headerInfo-30uryT:before,
#app-mount .userPopout-3XzG_A .avatarWrapper-3H_478.supporter-Z3FfwL:not(.statusHovered-gF2976):hover .wrapper-3t9DeA:before {
	background-color: rgb(var(--vaccentcolor)) !important;
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3) !important;
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .root-SR8cQa .wrapper-3t9DeA.dev-A7f2Rx:not(.statusHovered-gF2976):hover + .headerInfo-30uryT:after,
#app-mount .root-SR8cQa .wrapper-3t9DeA.supporter-Z3FfwL:not(.statusHovered-gF2976):hover + .headerInfo-30uryT:after {
	border-right-color: rgb(var(--vaccentcolor)) !important;
}
#app-mount .userPopout-3XzG_A .avatarWrapper-3H_478.dev-A7f2Rx:not(.statusHovered-gF2976):hover .wrapper-3t9DeA:after,
#app-mount .userPopout-3XzG_A .avatarWrapper-3H_478.supporter-Z3FfwL:not(.statusHovered-gF2976):hover .wrapper-3t9DeA:after {
	border-top-color: rgb(var(--vaccentcolor)) !important;
}

/* ----		18.2.	BETTERDOCSBLOCK					---- */

html.theme-dark body #app-mount .wrapper-35wsBm .icon-3o6xvg[style*="/icons/153708594091655168" i]::before,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="www.discordsource." i]::before,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="://discordsource." i]::before,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="www.betterdocs." i]::before,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="://betterdocs." i]::before {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.4)) !important;
	border-top-color: transparent !important;
	border-right-color: transparent !important;
	border-bottom-color: transparent !important;
	color: rgb(var(--fontwhite2)) !important;
	z-index: 4 !important;
}
html.theme-dark body #app-mount .wrapper-35wsBm .icon-3o6xvg[style*="/icons/153708594091655168" i]::after,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="www.discordsource." i]::after,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="://discordsource." i]::after,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="www.betterdocs." i]::after,
html.theme-dark body #app-mount .embed-IeVjo6 .embedLink-1G1K1D[href*="://betterdocs." i]::after {
	content: "" !important;
	background: var(--vbackground) center/var(--vbackgroundsize) !important;
	background-attachment: fixed !important;
	border-radius: 5px !important;
	position: absolute !important;
	top: 0 !important;
	right: 0 !important;
	bottom: 0 !important;
	left: -4px !important;
}


/* ~~~~		19.		UPDATENOTICE					~~~~ */

html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp:before {
	content: "Your version of   BasicBackground   by DevilBro is outdated. Please download the newest version from:	https://github.com/mwittrien/BetterDiscordAddons/blob/master/Themes/BasicBackground" !important;
	display: var(--version1_0_5, block) !important;
	background-color: #4a90e2 !important;
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3) !important;
	color: rgb(var(--fontwhite1)) !important;
	flex-grow: 0 !important;
	flex-shrink: 0 !important;
	font-size: 14px !important;
	font-weight: 500 !important;
	height: 36px !important;
	line-height: 36px !important;
	opacity: 1 !important;
	padding-left: 4px !important;
	padding-right: 28px !important;
	position: relative !important;
	text-align: center !important;
	visibility: unset !important;
	white-space: pre !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	max-width: unset !important;
	min-width: unset !important;
	max-height: unset !important;
	min-height: unset !important;
	transform: unset !important;
	animation: unset !important;
	z-index: 101 !important;
	pointer-events: none !important;
}

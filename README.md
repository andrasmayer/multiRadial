Multi Orientation Radial Menu


Needed libraries:     Bootstrap font-awesome jquery jquery-ui (included in the zip)

Multiple radial menus can be placed on the same page. The menus and sub-menus must be contained in a radials named object.

Each radial object can contain maximum 8(full) or 5(each other) sub-menus (more will trash up the page)


Submenu object must be look like this

{icon:"fa-dashboard",
	title:"SubMenu 1",								//Label
	btn:"dark",									//color based on bootsrap color
	src:"1/1/1"									//source url if it has. It will negate if has submenu object
	submenu:[									//Its optonal. Don't use it if u don't have any sub-menus
		{icon:"fa-dashboard",title:"SubMenu 1",btn:"dark",src:"1/1/1"},
		{icon:"fa-dashboard",title:"SubMenu 1",btn:"dark",src:"1/1/1"}		//sub-menus can't contain any lower level menus
	]
		
},
Sample object:
radials={};
radials.first=[

	{icon:"fa-search",title:"Menu 1",btn:"primary",
		submenu:[
			{icon:"fa-dashboard",title:"SubMenu 1",btn:"dark",src:"1/1/1"},
			{icon:"fa-flag",title:"SubMenu 2",btn:"primary",src:"1/1/2"},
			{icon:"fa-camera-retro",title:"SubMenu 3",btn:"success",src:"1/1/3"},
		]
	},
	{icon:"fa-rocket",title:"Menu 2",btn:"primary",
		submenu:[
			{icon:"",title:"FULL fixed Positon",btn:"dark"},
			{icon:"fa-dashboard",title:"SubMenu 4",btn:"info",src:"1/2/1"},
			{icon:"fa-flag",title:"SubMenu 5",btn:"primary",src:"1/2/2"},
			{icon:"fa-camera-retro",title:"SubMenu 6",btn:"dark",src:"1/2/3"},
		]
	},
	{icon:"fa-eye",title:"Menu 3",btn:"success",src:"1/3/0"},
	{icon:"fa-home",title:"Menu 4",btn:"info",src:"1/4/0"},
	{icon:"fa-desktop",title:"Menu 5",btn:"info",src:"1/5/0"},
	{icon:"fa-bell-o",title:"Menu 6",btn:"danger",src:"1/6/0"},
	{icon:"fa-bullhorn",title:"Menu 7",btn:"warning",src:"1/7/0"},
	{icon:"fa-coffee",title:"Menu 8",btn:"dark",src:"1/8/0"},
];

radials.first.target	=	"#menu";					//target of the emenent you want to insert the menu
radials.first.type	=	"full";						//type is position of the menu 
										//POSSIBLE: full, top, bottom, left, right
radials.first.color	=	"danger";					//Color of the main menu
												


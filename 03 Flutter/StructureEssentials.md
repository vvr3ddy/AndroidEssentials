## Flutter Essentials Cheatsheet

### 1. Scaffold
A top-level container that provides a structure for the visual interface.

```dart
Scaffold(
  appBar: AppBar(
    title: Text('App Title'),
  ),
  body: Center(
    child: Text('Hello, World!'),
  ),
  bottomNavigationBar: BottomNavigationBar(
    items: const <BottomNavigationBarItem>[
      BottomNavigationBarItem(
        icon: Icon(Icons.home),
        label: 'Home',
      ),
      BottomNavigationBarItem(
        icon: Icon(Icons.business),
        label: 'Business',
      ),
      BottomNavigationBarItem(
        icon: Icon(Icons.school),
        label: 'School',
      ),
    ],
  ),
  drawer: Drawer(
    child: ListView(
      padding: EdgeInsets.zero,
      children: <Widget>[
        DrawerHeader(
          decoration: BoxDecoration(
            color: Colors.blue,
          ),
          child: Text(
            'Drawer Header',
            style: TextStyle(
              color: Colors.white,
              fontSize: 24,
            ),
          ),
        ),
        ListTile(
          leading: Icon(Icons.home),
          title: Text('Home'),
          onTap: () {
            // Handle the tap
          },
        ),
        ListTile(
          leading: Icon(Icons.settings),
          title: Text('Settings'),
          onTap: () {
            // Handle the tap
          },
        ),
      ],
    ),
  ),
)
```

### 2. AppBar
A material design app bar that can be used as a top app bar.

```dart
AppBar(
  title: Text('App Title'),
  actions: <Widget>[
    IconButton(
      icon: Icon(Icons.search),
      onPressed: () {
        // Handle the press
      },
    ),
    IconButton(
      icon: Icon(Icons.more_vert),
      onPressed: () {
        // Handle the press
      },
    ),
  ],
)
```

### 3. BottomNavigationBar
A material design bottom navigation bar.

```dart
BottomNavigationBar(
  items: const <BottomNavigationBarItem>[
    BottomNavigationBarItem(
      icon: Icon(Icons.home),
      label: 'Home',
    ),
    BottomNavigationBarItem(
      icon: Icon(Icons.business),
      label: 'Business',
    ),
    BottomNavigationBarItem(
      icon: Icon(Icons.school),
      label: 'School',
    ),
  ],
  currentIndex: 0, // Set the current index
  selectedItemColor: Colors.amber[800],
  onTap: (int index) {
    // Handle the tap
  },
)
```

### 4. NavigationRail
A material design navigation rail for side navigation.

```dart
NavigationRail(
  selectedIndex: 0,
  onDestinationSelected: (int index) {
    // Handle the tap
  },
  labelType: NavigationRailLabelType.selected,
  destinations: const <NavigationRailDestination>[
    NavigationRailDestination(
      icon: Icon(Icons.favorite_border),
      selectedIcon: Icon(Icons.favorite),
      label: Text('First'),
    ),
    NavigationRailDestination(
      icon: Icon(Icons.bookmark_border),
      selectedIcon: Icon(Icons.book),
      label: Text('Second'),
    ),
    NavigationRailDestination(
      icon: Icon(Icons.star_border),
      selectedIcon: Icon(Icons.star),
      label: Text('Third'),
    ),
  ],
)
```

### 5. Drawer
A material design drawer that slides in from the left.

```dart
Drawer(
  child: ListView(
    padding: EdgeInsets.zero,
    children: <Widget>[
      DrawerHeader(
        decoration: BoxDecoration(
          color: Colors.blue,
        ),
        child: Text(
          'Drawer Header',
          style: TextStyle(
            color: Colors.white,
            fontSize: 24,
          ),
        ),
      ),
      ListTile(
        leading: Icon(Icons.home),
        title: Text('Home'),
        onTap: () {
          // Handle the tap
        },
      ),
      ListTile(
        leading: Icon(Icons.settings),
        title: Text('Settings'),
        onTap: () {
          // Handle the tap
        },
      ),
    ],
  ),
)
```

### 6. TabBar and TabBarView
A material design tab bar and tab bar view for tab navigation.

```dart
DefaultTabController(
  length: 3,
  child: Scaffold(
    appBar: AppBar(
      bottom: TabBar(
        tabs: [
          Tab(icon: Icon(Icons.directions_car)),
          Tab(icon: Icon(Icons.directions_transit)),
          Tab(icon: Icon(Icons.directions_bike)),
        ],
      ),
      title: Text('Tabs Demo'),
    ),
    body: TabBarView(
      children: [
        Icon(Icons.directions_car),
        Icon(Icons.directions_transit),
        Icon(Icons.directions_bike),
      ],
    ),
  ),
)
```

### 7. BottomSheet
A material design bottom sheet.

```dart
Scaffold(
  appBar: AppBar(
    title: Text('Bottom Sheet Demo'),
  ),
  body: Center(
    child: ElevatedButton(
      onPressed: () {
        showModalBottomSheet(
          context: context,
          builder: (BuildContext context) {
            return Container(
              height: 200,
              color: Colors.white,
              child: Center(
                child: Text('Bottom Sheet'),
              ),
            );
          },
        );
      },
      child: Text('Show Bottom Sheet'),
    ),
  ),
)
```

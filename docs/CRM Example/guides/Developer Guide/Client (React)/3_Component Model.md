# Component Model

## index.html

Defines the ```root``` div element and loads ```main.jsx``` into it.

## main.jsx

Loads the ```AppRoutes``` component into the ```root``` div element.

## Routes.jsx
The ```AppRoutes``` component is defined in this file.
Navigation links are mapped to their respective components and added to the ```App.jsx``` component.
```json
{
    path: '/',
    element: <App />, // layout shell with <Outlet />
    children: [
      {
        index: true, // the default child route
        element: <Navigate to="/clients" replace />
      },
      {
        path: 'clients',
        element: <ClientsPage />
      },
      {
        path: 'contacts',
        element: <ContactsPage />
      },
      {
        path: 'viewlog', 
        element: <ViewLog />
      }
    ]
  }
```

## App.jsx


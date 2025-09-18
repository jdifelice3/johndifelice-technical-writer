# Third Party Components

## AG-Grid-React
[ag-grid-react (npmjs.com)](https://www.npmjs.com/package/ag-grid-react)

AG Grid is a fully-featured and highly customizable React Data Grid. It delivers outstanding performance and has no third-party dependencies.

### Versions

AG Grid is available in two versions: Community & Enterprise.

`ag-grid-community`
:   is free, available under the MIT license, and comes with all of the core features expected from a React Data Grid, including Sorting, Filtering, Pagination, Editing, Custom Components, Theming and more.

`ag-grid-enterprise` 
:   is available under a commercial license and comes with advanced features, like Integrated Charting, Row Grouping, Aggregation, Pivoting, Master/Detail, Server-side Row Model, and Exporting in addition to dedicated support from our Engineering team.

For ZohoDataExplorer, both Community and Enterprise are required. The Server-Side Row Model and Master/Detail row features are only
available in the Enterprise Edition:

```json
{...
"ag-grid-community": "^28.2.1",
"ag-grid-enterprise": "^28.2.1",
"ag-grid-react": "^28.2.1",
...}
```
*e.g.* in the ```Client.jsx``` page.
```js
<AgGridReact
           ref={gridRef}
           columnDefs={columnDefs}
           defaultColDef={defaultColDef}
           rowModelType="serverSide"
           pagination={true}
           paginationPageSize={50}
           cacheBlockSize={100}
           rowSelection="single"
           getRowId={params => params.data.id}
           onGridReady={onGridReady}
           serverSideStoreType="partial"
           onCellValueChanged={handleCellValueChanged}
           domLayout='normal'
           masterDetail={true}
           detailCellRendererParams={{
             getDetailRowData,
             detailGridOptions: {
               columnDefs: contactColumnDefs,
               defaultColDef: {
                 flex: 1,
                 minWidth: 150,
                 sortable: true,
                 filter: true,
                 resizable: true
               }
             }
           }}
           isRowMaster={() => true}
           detailRowHeight={300}
         />
```
## QueryBuilder
[react-querybuilder (npmjs.com)](https://www.npmjs.com/package/react-querybuilder)

**React Query Builder** is a fully customizable query builder component for React, along with a collection of utility functions for importing from, and exporting to, various query languages like SQL, MongoDB, and more.

*e.g.* in the ```Client.jsx``` page.
```js
<div>
    <QueryBuilder
        fields={clientsQueryFields}
        query={query}
        onQueryChange={(q) => setQuery(q)}
        controlElements={{ addGroupAction: () => '' }}
        translations={customTranslations}
    />
</div>
<div className="advancedFilterContainer">
    <button className="advancedFilter" onClick={() => gridRef.current.api.purgeServerSideCache()}>Apply Filter</button>
</div>
```
## React Toastify

Toast notifications, or toast messages, are unobtrusive, in-app pop-up messages that provide users with feedback about an operation. Toasts usually disappear after a given time; therefore, removing them doesn’t require any user action. However, you can also close a toast notification before the expiration of the timeout.
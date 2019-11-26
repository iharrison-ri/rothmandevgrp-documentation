Component:
DynamicTable

Functions:
setDOSOnPageLoad: set the DOS to state when returning to page if it's not already set
getDOSDates: returns the start and end filtered dates
hasSelectedADateRange: returns a boolean to determine if there is a filtered datange range
onDateRangePage: returns a boolean to determine if the currect page has to date range filter available
handleDateInputChange: handles a date range change
handleDateOnChange:
openEndDateDialogBox
setDatePickerDialogReference:
handleEndDateReject:
handleEndDateAccept:
disableDaysBeforeStartDate:
onOrderChange:
onFilterChange:
onPageChange: change the page offset when switching between pages
onRowsPerPageChange:
flattenWhereQuery:
onRowClick:
getDateRangeFilterLabel:
isHighRisk:
getColumnByKey:
Returns the key in the column data
ex: if column data = { key: "something", name: "isaiah", ... } this returns "something"
cacheColumnPaths:
split the column key on "." to insert into _path on the column.
ex: if column.key = "hey.you" -> column._path = ["hey", "you"]
resolveColumnPath:
take the _path array on teh column and return the value in the data object corresponding to the path.
ex: if data = { hey: { you: "hi" } } and _path=["hey", "you"] it returns "hi"

props:
classes
rowClasses

columns
key: The key in this.data the we wont to display
label: The label to deisplay on the table column
sortDown: false
sortable: true
style: obj of styles to be given to the cell
_path: path to the value in this.data. The property is set in cacheColumnPaths

idKey
showFilters
data
query
header
noDataMessage
preloadMessage
inDialog
rowExtraRenderer


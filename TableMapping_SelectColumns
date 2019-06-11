// Allows you to select columns based on a list of column names found within an Excel file.

// First, create a new blank query and paste in the following code, replacing paths, sheet names and the name of the column
// containing column names to select.
// Save this query using a name such as "ColumnSelection" or "Mapping_SelectColumns"

let
    Source = Excel.Workbook(File.Contents("____WORKBOOK_PATH____"), null, true),
    Navigation = Source{[Item="____WORKSHEET_NAME____",Kind="Sheet"]}[Data],
    #"Removed Top Rows" = Table.Skip(Navigation,2),
    #"Promoted Headers" = Table.PromoteHeaders(#"Removed Top Rows", [PromoteAllScalars=true]),
    #"SelectedColumns" = #"Promoted Headers"[#"_____NAME_OF_COLUMN_WITH_COLUMN_NAMES_____"]
in
    #"SelectedColumns"
    
    
    
 // Within the query which contains all columns (including those to be selected), add the following step at a point you
 // deem appropriate, replacing the name of the previous step and the name you used for the query above:
 
 #"Selected Columns" = Table.SelectColumns(#"___PREVIOUS_STEP____",____NAME_OF_THE_QUERY_ABOVE_____)

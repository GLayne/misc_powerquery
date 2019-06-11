// This allows you to rename columns within an M Query based on a mapping table contained within an Excel file.

// Create a new blank query and paste the following code, replacing the workbook path and worksheet name
// in order to point to a mapping table contained in an Excel File.
// You will also need to replace the list of columns to be removed in order to only keep the two columns to be used for the mapping.
// If not needed, you can remove this step.
// Finally, you also need to replace the name of the columns that contain the mapping input and output

// Give a relevant name to this query such as Mapping_RenameColumns

let
    Source = Excel.Workbook(File.Contents("____WORKBOOK_PATH____"), null, true),
    Navigation = Source{[Item="____WORKSHEET_NAME____",Kind="Sheet"]}[Data],
    #"Removed Top Rows" = Table.Skip(Navigation,2),
    #"Promoted Headers" = Table.PromoteHeaders(#"Removed Top Rows", [PromoteAllScalars=true]),
    #"Removed Columns" = Table.RemoveColumns(#"Promoted Headers",{___PROVIDE_A_LIST_OF_COLUMNS_TO_REMOVE_IN_ORDER_TO_ONLY_KEEP_YOUR_2_MAPPING_COLUMNS___}),
    #"Reordered Columns" = Table.ReorderColumns(#"Removed Columns",{"___NAME_OF_COLUMN_CONTAINING_MAPPING_INPUT__", "___NAME_OF_COLUMN_CONTAINING_MAPPING_OUTPUT__"}),
    #"Transposed Table" = Table.Transpose(#"Reordered Columns"),
    #"RenamedColumns" = Table.ToColumns(#"Transposed Table")
in
    #"RenamedColumns"
    
  
// Once the query above as been created, add this step at the point of the other query when you want to rename columns:

#"Renamed Columns" = Table.RenameColumns(#"Selected Columns",___NAME_GIVEN_TO_THE_QUERY_ABOVE_____)

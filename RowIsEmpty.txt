= Table.AddColumn(#"Renamed Columns", "Empty Row", each List.IsEmpty(List.RemoveMatchingItems(Record.FieldValues(_), {"", null})))

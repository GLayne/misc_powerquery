let
    InvertName  = (string as text, separator as text) as text =>
        // takes a string as input in the format : Lainesse, Gabriel, also providing as input the separator ","
        // and returns an inverted name like: Gabriel Lainesse
        let
            BeforeSeparator = Text.Trim(Text.BeforeDelimiter(string, separator)),
            AfterSeparator = Text.Trim(Text.AfterDelimiter(string, separator)),
            FinalText = Text.Combine({AfterSeparator, " ", BeforeSeparator})
        in
            FinalText
in
    InvertName

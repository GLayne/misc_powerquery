let
    RemoveTextWithinParenthesis  = (string as text) as text =>
        let
            BeforeParenthesis = Text.BeforeDelimiter(string, "("),
            AfterParenthesis = Text.AfterDelimiter(string, ")"),
            FinalText = Text.Combine({BeforeParenthesis, AfterParenthesis})
        in
            FinalText
in
    RemoveTextWithinParenthesis

= (MinuteCount as text) as duration => 
    // Expects a text value representing a duration and formatted as such: 135:25  
    // Will return a duration value as such : #duration(0, 2, 15, 25)
    let 
        // splitting parts around the Seconds Delimiter
        MinutePart = Number.FromText(Text.BeforeDelimiter(MinuteCount, ":")),
        SecondsPart = Number.FromText(Text.AfterDelimiter(MinuteCount, ":")),

        DurationMinutes = Number.Mod(MinutePart, 60),
        DurationHours = Number.Mod(Number.IntegerDivide(MinutePart, 60), 24),
        DurationDays = Number.IntegerDivide(MinutePart, 60 * 24),
        OutputDuration = #duration(DurationDays, DurationHours, DurationMinutes, SecondsPart)
    in
        OutputDuration

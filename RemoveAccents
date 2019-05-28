let
    RemoveAccents = (string as text) as text => 
        let 
            // uppercase
            #"RemovedÀ" = Text.Replace(string, "À", "A"),
            #"RemovedÂ" = Text.Replace(#"RemovedÀ", "Â", "A"),
            #"RemovedÄ" = Text.Replace(#"RemovedÂ", "Ä", "A"),
            #"RemovedÉ" = Text.Replace(#"RemovedÄ", "É", "E"),
            #"RemovedÈ" = Text.Replace(#"RemovedÉ", "È", "E"),
            #"RemovedÊ" = Text.Replace(#"RemovedÈ", "Ê", "E"),
            #"RemovedË" = Text.Replace(#"RemovedÊ", "Ë", "E"),
            #"RemovedÎ" = Text.Replace(#"RemovedË", "Î", "I"),
            #"RemovedÏ" = Text.Replace(#"RemovedÎ", "Ï", "I"),
            #"RemovedÔ" = Text.Replace(#"RemovedÏ", "Ô", "O"),
            #"RemovedÖ" = Text.Replace(#"RemovedÔ", "Ö", "O"),
            #"RemovedÇ" = Text.Replace(#"RemovedÖ", "Ç", "C"),
            #"RemovedÛ" = Text.Replace(#"RemovedÇ", "Û", "U"),
            #"RemovedÙ" = Text.Replace(#"RemovedÛ", "Ù", "U"),
            #"RemovedÜ" = Text.Replace(#"RemovedÛ", "Ü", "U"),
            // lowercase
            #"Removedà" = Text.Replace(#"RemovedÜ", "à", "a"),
            #"Removedâ" = Text.Replace(#"Removedà", "â", "a"),
            #"Removedä" = Text.Replace(#"Removedâ", "ä", "a"),
            #"Removedé" = Text.Replace(#"Removedä", "é", "e"),
            #"Removedè" = Text.Replace(#"Removedé", "è", "e"),
            #"Removedê" = Text.Replace(#"Removedè", "ê", "e"),
            #"Removedë" = Text.Replace(#"Removedê", "ë", "e"),
            #"Removedî" = Text.Replace(#"Removedë", "î", "i"),
            #"Removedï" = Text.Replace(#"Removedî", "ï", "i"),
            #"Removedô" = Text.Replace(#"Removedï", "ô", "o"),
            #"Removedö" = Text.Replace(#"Removedô", "ö", "o"),
            #"Removedç" = Text.Replace(#"Removedö", "ç", "c"),
            #"Removedû" = Text.Replace(#"Removedç", "û", "u"),
            #"Removedù" = Text.Replace(#"Removedû", "ù", "u"),
            #"Removedü" = Text.Replace(#"Removedù", "ü", "u")
        in
            #"Removedü"
in 
    RemoveAccents

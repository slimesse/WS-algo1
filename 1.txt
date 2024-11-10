ALGORITHM counter

VAR

    sen: STRING;
    char: CHAR;
    cptChar, cptW, cptV: INTEGER;
    
BEGIN

// init

    cptChar := 0; 
    cptW := 0;
    cptV := 0;

    Write("Put your sentence");
    Read(sen);

    char := sen[0];

// process    

    WHILE char <> '.' DO

        cptChar := cptChar + 1; //count characters

        IF char = ' ' THEN
            cptW := cptW + 1; //count words
        END_IF
        
        IF (char = 'a') OR (char = 'e') OR (char = 'i') OR (char = 'o') OR (char = 'u') OR (char = 'A') OR (char = 'E') OR (char = 'I') OR (char = 'O') OR (char = 'U')  THEN
            cptV := cptV + 1; //count vowels
        END_IF

        char := sen[cptChar];
        
    END_WHILE

// outputs

    Write("Number of characters: ", cptChar + 1);
    Write("Number of words: ", cptW + 1);
    Write("Number of vowels: ", cptV);
END
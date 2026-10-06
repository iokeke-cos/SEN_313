some commits were mad e after the deadline of sun 4th oct 11:59pm


Q1:
Note:
 fn number(&mut self) {
        // TODO(you): scan a number literal: digits, then a fractional part only when a digit
        //            follows the dot (1.4).
        while self.peek().is_ascii_digit(){
            self.advance();
        }

        if self.peek() == '.' && self.peek_next().is_ascii_digit(){
            self.advance(); 

            while self.peek().is_ascii_digit(){
                self.advance();
            }
        }
        
        self.add(TokenType::Number);
        
    }

   NOte the decimal check 
Q2:
Note:
fn run(&mut self) {
        // TODO(you): drive the scan: read one token at a time until the source runs out, then
        //            add the EOF token. Spec 6.1 says which line EOF carries.
            while !self.at_end() {
            self.start = self.current;
            self.scan_token();
        }

        self.start = self.current;

        if let Some(t) = self.tokens.last() {
            self.line = t.line;
        } else {
            self.line = 1;
        }

        self.add(TokenType::Eof);
     }

Note :the self.line = and self.line += 1

Q3:
Note the EFO fix line 
Both commits were made on 6 Oct, after the 4 Oct deadline, so they do not meet the timing condition.



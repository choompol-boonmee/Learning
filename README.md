```
use std::process::*;
use std::io::stdout;
use std::io::Write;
use std::{thread, time};

fn main() {
    let command = ["ls","-l","-s""];
    let waitsec = 1*60;
    let mut cnt = 0;
        
    loop {
        cnt = cnt+1;
        println!("running======= {}",cnt);
        let output = Command::new(command[0])
            .args(&command[1..])
            .output()
            .expect("output() failed");
        stdout().write_all(output.stdout.as_slice()).expect("write failed");
        thread::sleep(time::Duration::from_secs(waitsec));
    }   
}
```

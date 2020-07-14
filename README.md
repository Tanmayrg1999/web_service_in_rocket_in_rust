# web_service_in_rocket_in_rust
Rocket is a web framework for Rust. It is used to design Web applications in the RUST programming languages.
## Steps to run a simple hello world program
1. In your system install the nightly version of Rust using the command -> **rustup default nightly**
2. One can use per-directory overrides to use the nightly version only for your Rocket project by running the following command in the directory -> **rustup override set nightly**
3. After installing the nightly version we will create a new binary-based Cargo project using the command -> **cargo new tanmay --bin**
4. Then we need to move our action to the created directory using the -> **cd tanmay**
5. Now a cargo.toml file would be created by default we need to add:
[dependencies]
rocket = "0.4.5"
6.  Now we need to add to the main.rs:

#![feature(proc_macro_hygiene, decl_macro)]

#[macro_use] extern crate rocket;

#[get("/")]

fn index() -> &'static str {

    "Hello, world!"
    
}

fn main() {

    rocket::ignite().mount("/", routes![index]).launch();
    
}


7. Now go to the create cargo project and use the **cargo run**

8. If the cargo project runs succesfully , then just open the [Link](https://localhost:8000) in any browser and the output will be displayed on the webpage.
## OUTPUT
![Untitled](https://user-images.githubusercontent.com/53641559/87393811-59dedf00-c5cc-11ea-80ef-a9a37e912b21.png)

# Tutorial 6

## Commit 1 Reflection Notes
The `handle_connection` function takes a mutable reference to a `TcpStream`. Inside this function, a `BufReader` is created from the `TcpStream` to efficiently read lines of data from the stream.

The `lines()` method of BufReader returns an iterator over the lines of data. The `map()` method is used to unwrap each line. The `take_while()` method is used to collect lines until an empty line is encountered, indicating the end of the HTTP request. The collected lines are stored in a `Vec<String>` named `http_request`. Finally, the contents of `http_request` are printed to the console using `println!()`.
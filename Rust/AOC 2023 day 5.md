'''rust
struct Transformer {
    out_start: u32,
    in_start: u32,
    len: u32
}

fn covert(seed: u32, list: Vec<Transformer>) -> u32 {
    for tran in list.iter() {
        if (seed < tran.in_start || seed > tran.in_start + tran.len) {
            continue;
        }
        seed + tran.out_start - tran.in_start
    }
    seed
}
'''
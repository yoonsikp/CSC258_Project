# CSC258_Project

## Milestone 1

Roles:

### Joshua
* module for stage/player/crates bitmap -> sprite id / x / y (20 x 16 times)

### Yoonsik
#### `sprite_draw` module takes in above -> x / y / colour (64 times)
Takes 66 clock cycles to completely draw one sprite.
`begin_draw` must be high for at least one clock cycle, and then low, then drawing starts.
`w_x` is the top left corner x-coordinate (with respect to a 160x120 screen size).
`w_sprite_id` can be found in the table below.
```
    sprite_draw spriteD(
            .resetn(resetn),
            .clk(CLOCK_50),
            .x_in(w_x),
            .y_in(w_y),
            .begin_draw(w_begin_draw),
            .sprite_id_in(w_sprite_id),
            );
```

## Sprite Table
Numbered 0 - 7

* Wall
* Crate
* Player
* Floor
* Goal
* Crate on top of Goal
* Player on top of Goal
`

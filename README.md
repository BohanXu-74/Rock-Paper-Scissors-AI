# Rock Paper Scissors AI (74xx Logic, Simulated)

A Rock Paper Scissors opponent built entirely from digital logic:
gates, decoders, multiplexers, and flip-flops, using 74-series components. 
It does not use any microcontroller. Runs in the Digital logic simulator.

## How it works
The AI stores your recent moves in a small flip-flop memory. Each round,
it randomly selects one remembered entry and plays the move that beats it.
If you keep playing rock, its memory fills with "play paper" entries,
so it will most likely play paper.

It's simple and easy to exploit (mix up your moves to beat it), but it
really does adapts to your habits.

## Running it
1. Download and install [Digital](https://github.com/hneemann/Digital).
2. Open `rps-ai.dig` (the project file in this repo) in Digital.
3. Press the play/start button and use the input switches to choose your move.

## Circuit overview
- Memory: Made out of 16 flip flops
- Random selection: A decoder that scrolls through memory super fast and stops when you play somthing
- Win/lose logic: Logic gates
- Counters that can count how many times you and AI win or tie

## Possible improvements
- Larger memory, or weight recent moves more heavily
- Can learn patterns as well

## Credits
Built and simulated with [Digital](https://github.com/hneemann/Digital),
the digital logic designer and circuit simulator by Helmut Neemann (hneemann).

## License
MIT

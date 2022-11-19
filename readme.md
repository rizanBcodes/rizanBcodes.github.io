I am using this repo to store information about chords and chord-shapes. If you want to use this for your projects, you can fetch "/data/chord-store.json" into your own codebase and do something like:

```
//assuming the chord type exists in our chordStore
async function getChordShape(chordType, store){
  let chordShapes = [];
	for (i of store){
	if (i.type == chordType){
    await chordShapes.push(i);
    }
  }
  //return chordShapes;
  console.log(chordShapes);
}

```

```
getChordShape("maj", chordStore);
//usage, should return an array with major chords

Example:
[
    {
        "name": "C",
        "type": "maj",
        "third": "E",
        "fifth": "G",
        "seventh": "B",
        "relative": "A minor",
        "scale": "C D E F G A B",
        "shape": {
            "1": "0",
            "2": "1",
            "3": "0",
            "4": "2",
            "5": "3",
            "6": "x"
        }
    }
]
//you get the type of chord, degrees, relative of the chord from the parent scale, and a chord shape that tells you what frets to fret on the fingerboard.
```

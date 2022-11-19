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

//usage
////should return an array with major chords
getChordShape("maj", chordStore);
```
Supported chord types: maj, min
```
Example response for 
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
```

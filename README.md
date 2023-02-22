# Blobs-to-arrays-

var blob = new Blob(["\x01\x02\x03\x04"]),
 fileReader = new FileReader(),
 array;
fileReader.onload = function() {
 array = this.result;
 console.log("Array contains", array.byteLength, "bytes.");
};
fileReader.readAsArrayBuffer(blob);

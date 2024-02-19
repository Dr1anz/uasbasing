<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vocabulary About Informatics Engineering
        English to Indonesia 
        
        Oleh Adriana Syahban 1A
        (2330511027)</title>
<style>
    body {
        font-family: Arial, sans-serif;
    }
    #searchInput {
        padding: 5px;
        width: 250px;
        margin-bottom: 10px;
    }
    #result {
        margin-top: 10px;
    }
</style>
</head>
<body>

<h2>Vocabulary About Informatics Engineering
        English to Indonesia 
        
        Oleh Adriana Syahban 1A
        (2330511027)</h2>

<input type="text" id="searchInput" placeholder="Cari kata...">
<div id="result"></div>

<script>
    // Data kamus
    var dictionary = [
        { word_en: "apple", word_id: "apel" },
        { word_en: "banana", word_id: "pisang" },
        { word_en: "cat", word_id: "kucing", },
        { word_en: "dog", word_id: "anjing", }
        // tambahkan kata-kata lain di sini
    ];

    // Fungsi pencarian
    function searchDictionary() {
        var input = document.getElementById("searchInput").value.toLowerCase();
        var resultDiv = document.getElementById("result");
        resultDiv.innerHTML = ""; // Mengosongkan hasil sebelumnya

        if (input.trim() === "") {
            resultDiv.innerHTML = "Input here a word to search.";
            return;
        }

        var found = false;
        for (var i = 0; i < dictionary.length; i++) {
            if (dictionary[i].word_en.toLowerCase().includes(input) || dictionary[i].word_id.toLowerCase().includes(input)) {
                resultDiv.innerHTML += "<b>English:</b> " + dictionary[i].word_en + "<br>" +
                                       "<b>Indonesian:</b> " + dictionary[i].word_id + "<br>" +
                found = true;
            }
        }

        if (!found) {
            resultDiv.innerHTML = "Word cannot be found.";
        }
    }

    // Memanggil fungsi searchDictionary saat tombol ditekan
    document.getElementById("searchInput").addEventListener("keyup", function(event) {
        if (event.key === "Enter") {
            searchDictionary();
        }
    });
</script>

</body>
</html>
# uasbasing

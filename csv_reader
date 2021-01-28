import java.io.BufferedReader
import java.io.FileReader

fun readCsvFile(path: String, sep: String = ","): Pair<List<String>, MutableMap<String,MutableList<Any>>> {
    val csvReader = BufferedReader(FileReader(path));
    val header = csvReader.readLine().split(sep)
    val cols : MutableMap<String,MutableList<Any>> = mutableMapOf()
    val nbrElem : Int  = header.size
    for (h in header)
        cols[h] = mutableListOf()

    val lines = csvReader.readLines()
    for (line in lines){
        val oneLine = line.split(sep)
        for(i in 0 until nbrElem)
        cols[header[i]]?.add(oneLine[i])
    }

    return Pair(header,cols)
}

val (header, cols) = readCsvFile(path = "YOUR_PATH")

println("==== header =====")
println(header)

println("==== All elements of the column ${header[0]} ====")

println(cols[header[0]])

"# NexaThon" 
function findHospital(){

    let location = document.getElementById("location").value;

    fetch("http://127.0.0.1:5000/find_hospital?location="+location)
    .then(response => response.json())
    .then(data => {

        if(data.length == 0){
            document.getElementById("hospitalResult").innerHTML = "No hospital found";
            }
        else{
            document.getElementById("hospitalResult").innerHTML = data[0].name;
        }

    });

}

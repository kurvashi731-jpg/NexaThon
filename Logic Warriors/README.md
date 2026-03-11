"# NexaThon" 
<!DOCTYPE html>
    <html>
        <head>
            <title>MedLink - Healthcare Finder</title>

            <link rel="stylesheet" href="style.css">
            <img src="https://user-gen-media-assets.s3.amazonaws.com/gemini_images/cbe1a48c-5909-4182-b8e2-dbcc794ecfda.png" alt="logo" height="80">
            
        </head>

    <body>

        <header>
            <h1>MedLink</h1>
            <p>Smart Healthcare Resource Finder</p>
            <img src="https://t4.ftcdn.net/jpg/16/87/28/89/360_F_1687288942_u3eY2dwL8stTpEmXjRu5IdSF1S1RaVci.jpg" alt="Banner" height="300">
        </header>

        <div class="container">
            <h2>Find Nearby Hospitals in Ranchi</h2>
            <input type="text" id="location" placeholder="location">
            <button onclick="findHospital()">Search</button>
            <p id="hospitalResult"></p>
        </div>

        <div class="container">
            <button onclick="openDonorForm()">Register As a Donor</button>
            <script> function openDonorForm(){
                window.loation.href="donor.html";
            }</script>
        </div>

        <div>
            <h2>Find Blood Donor</h2>
            <select id="blood">
                <option>Select Blood Group</option>
                <option>A+</option>
                <option>A-</option>
                <option>B+</option>
                <option>B-</option>
                <option>O+</option>
                <option>O-</option>
                <option>AB+</option>
                <option>AB-</option>
            </select>

            <button onclick="findDonor()">Search</button>
            <p id="donorResult"></p>
        </div>

        <div class="container">
            <h2>Hospital Resource Dashboard</h2>
            <table>
                <tr>
                    <th>Hospital</th>
                    <th>Location</th>
                    <th>ICU Beds</th>
                    <th>Ventilators</th>
                    <th>Emergency Number</th>
                    <th>Book Ambulance Number</th>
                </tr>

                <tr>
                    <td>RIMS</td>
                    <td>Bariatu</td>
                    <td>130</td>
                    <td>150</td>
                    <td>1244662145</td>
                    <td>5462845283</td>
                </tr>

                <tr>
                    <td>Sadar Hospital</td>
                    <td>Namkum</td>
                    <td>40</td>
                    <td>50</td>
                    <td>3574657382</td>
                    <td>3574657352</td>
                </tr>

                <tr>
                    <td>Paras HEC Hospital</td>
                    <td>Dhurwa</td>
                    <td>73</td>
                    <td>80</td>
                    <td>3574658382</td>
                    <td>3574654382</td>
                </tr>

                <tr>
                    <td>Orchid Hospital</td>
                    <td>Lalpur</td>
                    <td>58</td>
                    <td>71</td>
                    <td>3564658382</td>
                    <td>3524654382</td>
                </tr>
                <tr>
                    <td>Aalam Hospital</td>
                    <td>Bariatu</td>
                    <td>78</td>
                    <td>85</td>
                    <td>3574628382</td>
                    <td>3574624382</td>
                </tr>

            </table>
        </div>

        <div class="container">

        </div>

            <h2>Emergency</h2>

            <button class="sos" onclick="sos()">SOS</button>

    </div>

        <script src="script.js"></script>

    </body>
</html>

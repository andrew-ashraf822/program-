# program-

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
</head>

<body>
    <div class="container text-center">
        <div class="row align-items-start">
            <div class="col-8" style="padding: 20px; border: 2px solid black;margin-right:auto;margin-left:auto;padding:20px">

                <form action="<?php echo site_url()?>/Welcome/insert_new_user" method="post">
                    <h1> DODOZ PROJECT</h1>
                    <h1>Sign Up</h1>

                    <div class="row">
                        <div class="col">

                            <div class="input-group mb-3">
                                <span class="input-group-text" id="basic-addon1">full name</span>
                                <input type="text" class="form-control" name="full_name" required placeholder="full name" aria-label="Username" aria-describedby="basic-addon1">
                            </div>
                            
                            <div class="input-group mb-3">
                                <input type="text" class="form-control" name="user_name" required placeholder="user name" aria-label="Recipient's username" aria-describedby="basic-addon2">
                                <span class="input-group-text" id="basic-addon2">User Name</span>
                            </div>

                            <div class="input-group mb-3">
                                <input type="email" class="form-control" name="email" required placeholder="user name" aria-label="Recipient's username" aria-describedby="basic-addon2">
                                <span class="input-group-text" id="basic-addon2">@example.com</span>
                            </div>

                            <div class="form-check" style="margin: auto left;">
                                <input class="form-check-input" type="radio" value="male" name="gender" id="flexRadioDefault1">
                                <label class="form-check-label" for="flexRadioDefault1">Male</label>
                            </div>
                            <div class="form-check">
                                <input class="form-check-input" type="radio" value="female" name="gender" id="flexRadioDefault2">
                                <label class="form-check-label" for="flexRadioDefault2">Female</label>
                            </div>

                            <div class="input-group input-group-sm mb-3">
                                <span class="input-group-text" id="inputGroup-sizing-sm">phone</span>
                                <input type="text" class="form-control" aria-label="Sizing example input" name="mobile" required aria-describedby="inputGroup-sizing-sm">
                            </div>

                            <input class="form-control" type="date" placeholder="Default input" name="birthdate" required aria-label="default input example">
                            <br>

                        </div>

                        <div class="col">

                            <select class="form-select" name="grade_id" aria-label="Default select example">

                                <option selected disabled value="0">Please select your grade</option>

                                <?php
                                foreach ($grades as $line) { ?>

                                    <option value="<?php echo $line->id; ?>"><?php echo $line->grade_name; ?></option>

                                <?php } ?>

                            </select>
                        <br>

                            <input class="form-control" type="text" name="a_national_number" required placeholder="a_national_number" aria-label="readonly input example">

                            <br>

                            <select class="form-select" name="government_id" aria-label="Default select example">

                                <option selected disabled value="0">Please select your Government</option>

                                <?php
                                foreach ($governments as $line) { ?>

                                    <option value="<?php echo $line->id; ?>"><?php echo $line->governments_name; ?></option>

                                <?php } ?>

                            </select>
                            <br>


                            <div class="form-floating mb-3">
                                <input type="text" class="form-control" id="floatingInput" name="address" required placeholder="Address">
                                <label for="floatingInput">Address</label>
                            </div>


                            <div class="form-floating">
                                <input type="password" class="form-control" id="floatingPassword" name="password" required placeholder="Password">
                                <label for="floatingPassword">Password</label>
                            </div>

                            <br>

                        </div>


                        <div class="row">
                            <div class="col">
                                <div class="input-group">
                                    <span class="input-group-text">Comment</span>
                                    <textarea class="form-control" name="comment" required aria-label="With textarea"></textarea>
                                </div>
                            </div>
                        </div>



                        <br><br><br>
                        <button style="width: 100%;" type="submit" class="btn btn-primary">Save</button>
                    </div>
                    </form>
            </div>
        </div>

    </div>
    <br>



    <div class="row">

        <div class="col">
            <a href="<?php echo site_url() ?>/Welcome/view_all_users/" style="width: 20%;" class="btn btn-secondary"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-recycle" viewBox="0 0 16 16">
                    <path d="M9.302 1.256a1.5 1.5 0 0 0-2.604 0l-1.704 2.98a.5.5 0 0 0 .869.497l1.703-2.981a.5.5 0 0 1 .868 0l2.54 4.444-1.256-.337a.5.5 0 1 0-.26.966l2.415.647a.5.5 0 0 0 .613-.353l.647-2.415a.5.5 0 1 0-.966-.259l-.333 1.242zM2.973 7.773l-1.255.337a.5.5 0 1 1-.26-.966l2.416-.647a.5.5 0 0 1 .612.353l.647 2.415a.5.5 0 0 1-.966.259l-.333-
            1.242-2.545 4.454a.5.5 0 0 0 .434.748H5a.5.5 0 0 1 0 1H1.723A1.5 1.5 0 0 1 .421 12.24zm10.89 1.463a.5.5 0 1 0-.868.496l1.716 3.004a.5.5 0 0 1-.434.748h-5.57l.647-.646a.5.5 0 1 0-.708-.707l-1.5 1.5a.5.5 0 0 0 0 .707l1.5 1.5a.5.5 0 1 0 .708-.707l-.647-.647h5.57a1.5 1.5 0 0 0 1.302-2.244z" />
                </svg>
            </a>
        </div>

    </div>




    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>

</html>





<!-- Ctrl / -->





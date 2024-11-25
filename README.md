$(".errorPno").css({
                    "visibility": "hidden"
                })
                $(".btn").css({
                    "visibility": "visible"
                });
                $(".error").css({
                    "visibility": "hidden"
                })
            } else {
                $(".errorPno").css({
                    "visibility": "visible"
                })
                $(".btn").css({
                    "visibility": "hidden"
                });
                $(".error").css({
                    "visibility": "visible"
                })
            }
        });
        $(".btn").click(function () {
            $.ajax({
                url: "addTour.php",
                type: "post",
                data: $("#frm").serialize(),
                success: function (data) {
                    alert(data)
                  
                    $("#status").html(data)
                    $("#frm")[0].reset();
                    $(".form").fadeOut();
                    $(".a").fadeIn();
                }
            })
           
           
            
        })
    })
</script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/js/bootstrap.min.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/js/bootstrap.min.js"></script>

</html>

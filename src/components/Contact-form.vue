<template>
      <div class='container'>
		<div class='wrapper animated bounceInLeft'>
			<div class='company-info'>
				
				<ul>
					<li><i class="fa fa-road"></i> Cape Town, South Africa</li>
					<li><i class="fa fa-phone"></i>(+27) 074 525 0800</li>
					<li><i class="fa fa-envelope"></i> hannahdalwai4@gmail.com</li>
					<img src="image/logo.png" alt="">
				</ul>
		</div>
		<div class='contact'>
			<h3>Get in touch</h3>
			<form  target="_blank" class="was-validated" method="post"  action="https://formspree.io/f/xqkwonnz">
				<p>
					<label for="validationTextarea"> Name</label>
					<input type="text" name='name' class="form-control is-invalid" id="validationTextarea" placeholder="Insert Name Here" required> 
				</p>

				<p>
					<label >Company</label>
					<input type="text" name='company'> 
				</p>

				<p>
					<label  for="validationTextarea">Email Address</label>
					<input type="email" name='email'  class="form-control is-invalid" id="validationTextarea" placeholder="Insert Email Address Here" required> 
				</p>

				<p>
					<label for="validationTextarea">Phone Number</label>
					<input type="text" name='phone' class="form-control is-invalid" id="validationTextarea" placeholder="Insert Phone Number  Here" required> 
				</p>

				<p class='full'>
					<label for="validationTextarea">Message</label>
					<textarea name="message" rows="5" class="form-control is-invalid" id="validationTextarea" placeholder="Insert Message Here" required></textarea> 
				</p>

				<p class='full'>
					<button id="button" type="submit">Submit</button>
				</p>
			</form>
		</div>
	</div>
   </div>


</template>

<script>
export default {
data() {
    return {
       
    }
},
}
</script>

<style>
*{
	box-sizing: border-box;
}

.container{
	max-width:1170px;
	margin-left: auto;
	margin-right: auto;
	padding: 1em;
    border-radius: 5px;
}

ul{
	list-style: none;
	padding: 0;
}

.brand{
	text-align: center;
}
.brand span{
	color: #fff;
}

.wrapper{
	box-shadow: 0 0 20px 0 #6762a6;
	margin-left: 50px;
} 

.wrapper >*{
	padding: 1em;
}

.company-info{
	background:  #6762a6;
	text-align: center;
	color: whitesmoke;
	text-align: center;
}

.company-info h3, .company-info ul{
	text-align: center;
	margin: 0 0 1rem 0;
}

.contact{
	background: #f9feff;
	text-align: center;
}

/* FORM CONTACTS
 MOBILE SIZE FIRST */

.contact form{
	display: grid;
	grid-template-columns: 1fr 1fr;
	grid-gap: 20px;
}

.contact form label{
	display: block;
}

.contact form p{
	margin:0; 
}

.contact form .full{
	grid-column: 1/3;
}

.contact form button, .contact form input, .contact form textarea{
	width: 100%;
	padding: 1em;
	/* border: 1px solid #; */

}

.contact form button{
	background:#6762a6 ;
	border: 0;
	text-transform: uppercase;
}

.contact form button:hover, .contact form button:focus{
	background: #c9c3e6;
	color: #fff;
	outline:0;
	transition: background-color 0.5 s ease-out;
}

/* LARGE SCREENS */
@media(min-width:700px){
	.wrapper{
		display: grid;
		grid-template-columns: 1fr 2fr;
	}

	.wrapper>*{
		padding:2em;
	}

	.company-info h3, .company-info ul, .brand{
		text-align: left;
	}
}
/* LARGE SCREENS */
@media(max-width:700px){
	img{
		display: none;
	}
}

</style>
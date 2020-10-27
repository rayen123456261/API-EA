# API-EA
How i can Fix ERR_TOO_MANY_REDIRECTS 


var xhr = new XMLHttpRequest();
var ch = "";
xhr.open('GET', 'https://ea.com/login', true);
xhr.onload = function () {
console.log(xhr.responseURL);
$("document").ready(function(){
$.post(xhr.responseURL,
    {
		email: "",
		password: "",
		pn_text: null,
		passwordForPhone: null,
		country: null,
		phoneNumber: null,
		_rememberMe: "on",
		rememberMe: "on",
		_eventId: "submit",
		gCaptchaResponse: null,
		thirdPartyCaptchaResponse: null ,
		isPhoneNumberLogin: false,
		isIncompletePhone: null,
		countryPrefixPhoneNumber: null,
	},
	function(data,status,a){	
	for (var i=0;i<8;i++){
	ch = ch + data[i];
						}
	console.log(data);
	}
);
});
}
xhr.send(null);

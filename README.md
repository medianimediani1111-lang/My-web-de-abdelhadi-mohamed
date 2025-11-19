
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="ar-aa" lang="ar-aa">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>موقع متوسطة المنصورية لمتابعة تعلمات تلاميذ الرابعة متوسط</title>
<link rel = "stylesheet" href = "miseenForme.css" />

  <link rel="stylesheet" href="//code.jquery.com/ui/1.13.0/themes/base/jquery-ui.css">
  <link rel="stylesheet" href="/resources/demos/style.css">

  <script src="https://code.jquery.com/jquery-3.6.0.js"></script>
  <script src="https://code.jquery.com/ui/1.13.0/jquery-ui.js"></script>

  <script language="javascript">

  $( function() {
  	$.datepicker.regional['fr'] = {
                changeMonth: true,
                changeYear: true,
                dateFormat: 'yy-mm-dd',
                closeText: 'Fermer',
                prevText: '&#x3c;Préc',
                nextText: 'Suiv&#x3e;',
                currentText: 'Aujourd\'hui',
                monthNames: ['Janvier','Fevrier','Mars','Avril','Mai','Juin',
                'Juillet','Aout','Septembre','Octobre','Novembre','Decembre'],
                monthNamesShort: ['Jan','Fev','Mar','Avr','Mai','Jun',
                'Jul','Aou','Sep','Oct','Nov','Dec'],
                dayNames: ['Dimanche','Lundi','Mardi','Mercredi','Jeudi','Vendredi','Samedi'],
                dayNamesShort: ['Dim','Lun','Mar','Mer','Jeu','Ven','Sam'],
                dayNamesMin: ['Di','Lu','Ma','Me','Je','Ve','Sa'],
                weekHeader: 'Sm',
                firstDay: 1,
                isRTL: false,
                showMonthAfterYear: false,
                yearSuffix: '',
                minDate: '-20Y',
                maxDate: '+12M +0D',
                numberOfMonths: 1,
                showButtonPanel: true
                };
$.datepicker.setDefaults($.datepicker.regional['fr']);
    //$( "#textboxDate1" ).datepicker();
    $( ".dateSaisieDeb" ).each(function(){
    	$(this).datepicker();
	 });
	 $( ".dateSaisieFin" ).each(function(){
    	$(this).datepicker();
	 });
  } );


    // fonction qui poste les donnees de la solution du devoir quant l.eleve la fait apparaitre
		function sendData()
		{
  			var numDevoir = $("input[name=numDevoir]").val();
  			var idEleve = $("input[name=idEleve]").val();
  			$.ajax({
    			type: 'post',
    			url: 'insertVuSol.php',
    			data: {
      			numDevoir:numDevoir,
      			idEleve:idEleve
    			},
    			success: function (response) {
      			//$('#divPrincipal').html("numDevoir2 " + numDevoir2 + ", idEleve2: " + idEleve2);
    			}
  			});
  		return false;
	}

</script>

</head>

<body id = "haut" >


<style>
.boutonmenuprincipal {
color: #FFFF00;
border: none;
cursor: pointer;
font-size: 15px;

float: right;
background: none;
margin-left: 1%;
margin-right: 1%
}
.boutonmenuprincipal:hover {

float: right;
background: none;
margin-left: 1%;
margin-right: 1%
}
.dropdown {
position: relative;
display: inline-block;
color:#FFFF00;

float: right;
}
.dropdown-child {
display: none;
min-width: 50px;
color:#FFFF00;

float: right;
margin-left: 1%;
margin-right: 1%;
}
.dropdown-child a {
padding: 10px;
text-decoration: none;
display: block;
background-color: #563333;
color:#FFFF00;

text-align: right;
}
.dropdown:hover .dropdown-child {
display: block;
color:#FFFF00;

float: right;
margin-left: 1%;
margin-right: 1%
}

.dropdown-child a:hover {
display: block;
background-color: #883333;
color:#FFFF00;
}
</style>

<div class = 'img_header' ><p><a class = 'titreheader'>متابعة تعلمات تلاميذ السنة الرابعة متوسط في مادة الرياضيات</a></p></div><div style = 'color:#FFFF00;background:#663333'><a style = 'color:#FFFF00;background:#663333; margin-left: 1%; margin-right: 1%'>مرحبا ب </a><a id = 'deconnexion' href = 'index.php?deconnecter=oui' style = 'float: right;  color:#FFFF00;background:#663333; margin-left: 1%; margin-right: 1%'>تسجيل الخروج</a></div>
<p>
	<div class = 'menu' >
		<ul class = 'sousMenu'><p><li  class = 'lien1' style = 'color:#00FF66'><a href = 'demandesTestsEleve.php' class = 'lien1'>تسيير طلبات الاختبارات</a></li></p></ul><ul class = 'sousMenu'><p><li class = 'lien1'><a href = 'acquisitionEleves.php' class = 'lien1' >قائمة إدراك الكفاءات</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'ExercicesCompetencesEleves.php' class = 'lien1' >نماذج تمارين الكفاءات</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'ExercicesIntegrationEleves.php' class = 'lien1' >تمارين إدماج الكفاءات</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'acquisitionGroupeEleves.php' class = 'lien1' >إدراك تلاميذ مجموعتك</a></li></p></ul><hr /><ul class = 'sousMenu'><p><li  class = 'lien1' style = 'color: yellow;'><a style = 'color: yellow;' href = 'ComposPDF.php' class = 'lien1'>نماذج من اختبارات وفروض</a></li></p></ul><hr /><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'coursMinisteriels.php' class = 'lien1' >دروس وزارة التربية الوطنية</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'coursZakaria.php' class = 'lien1' >دروس المعلم زكرياء</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'coursTaybiAmmar.php' class = 'lien1' >دروس الأستاذ طايبي عمار</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'solExosZakariaMoumni.php' class = 'lien1' >حلول تمارين الكتاب المدرسي</a></li></p></ul><hr /><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'statistiquesEleves.php' class = 'lien1' >معلومات عامة</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'presenceRenforcementEleves.php' class = 'lien1' >حضور حصص الدعم</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'notesPresenceRenforcement.php' class = 'lien1' >نقاط حضور حصص الدعم</a></li></p></ul><hr /><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'tachesParGroupe.php' class = 'lien1' >مهام تعلم مجموعتك</a></li></p></ul><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'statsTachesParGroupe.php' class = 'lien1' >إحصائيات مهام تعلم المجموعات</a></li></p></ul><ul class = 'sousMenu'><p><li class = 'lien1'><a href = 'notesTaches.php' class = 'lien1' >نقاط مهام التعلم بين التلاميذ</a></li></p></ul>		<hr />
		<div class = "session">
		<br />
		<center><h2>المستخدم الحالي:   </h2></center><center><a href = 'index.php?deconnecter=oui' class = 'lien1'>تسجيل الخروج</a></center><br /><br /><center><a href = 'https://cem-4m2.ahlamontada.com/' class = 'lien1' target='_blank'>دخول منتدى قسم الرابعة متوسط</a></center><br /><br /><hr /><ul class = 'sousMenu'><p><li  class = 'lien1'><a href = 'aideSite.php' class = 'lien1' >كيف تسجل وتدخل المنتدى</a></li></p></ul>		</div>
	</div>
</p>

	<table style = 'width: 77%; float: right;'>
		<tr>
			<td  style = 'width: 70%;'>
<div class = 'formRecherche' style = 'width: 100%'><h1 style = 'text-align: center;'>فروض واختبارات من مواقع</h1><form name = 'form4' method = 'post'  action = 'ComposPDF.php'><p class = 'detail' style = 'direction: rtl; font-size: 24px'>اختر الفصل:		<select name='trimestre' class = 'textbox' style = 'direction: rtl; font-size: 24px'><option value='0' selected>كل الفصول</option><option value='1'>1</option><option value='2'>2</option></select>	اختر نوع الامتحان:		<select name='typeExamen' class = 'textbox' style = 'direction: rtl; font-size: 24px'><option value='0' selected>فروض</option><option value='1'>اختبارات</option><option value='2'>شهادات التعليم المتوسط</option></select>	<input type = 'submit' name = 'afficher' class = 'boutonRech' value ='عرض الامتحانات' style = 'float: left;margin-bottom: 20px;margin-top: 20px;font-size: 24px'/>	</p></p></form></div><div class = 'formRecherche' style = 'width: 100%'><h2 style = 'margin-right: 5%'>1- </h2><p style = 'font-size: 20px; margin-right: 10%;'><embed src='ComposPDF/devoir_dzexam_2025_trim2_2.pdf' width='100%' height='800' type='application/pdf'/></p><h3 style = 'margin-right: 5%'>الحل:</h2><p style = 'font-size: 20px; margin-right: 10%;'><embed src='ComposPDF/sol_devoir_dzexam_2025_trim2_2.pdf' width='100%' height='800' type='application/pdf'/></p><h2 style = 'margin-right: 5%'>2- فرض الفصل الأول</h2><p style = 'font-size: 20px; margin-right: 10%;'><embed src='ComposPDF/devoir_dzexam_trim1_1.pdf' width='100%' height='800' type='application/pdf'/></p><h3 style = 'margin-right: 5%'>الحل:</h2><p style = 'font-size: 20px; margin-right: 10%;'><embed src='ComposPDF/sol_devoir_dzexam_trim1_1.pdf' width='100%' height='800' type='application/pdf'/></p><h2 style = 'margin-right: 5%'>3- نموذج فرض الفصل الثاني موسم 2021-2022</h2><p style = 'font-size: 20px; margin-right: 10%;'><embed src='ComposPDF/devoir_dzexam_2022_trim2_1.pdf' width='100%' height='800' type='application/pdf'/></p><h3 style = 'margin-right: 5%'>الحل:</h2><p style = 'font-size: 20px; margin-right: 10%;'><embed src='ComposPDF/sol_devoir_dzexam_2022_trim2_1.pdf' width='100%' height='800' type='application/pdf'/></p></div>
			</td>
			<td style = 'width: 2%;'>
			</td>
		</tr>
	</table>

</body>
</html>

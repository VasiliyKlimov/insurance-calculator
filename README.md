<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Калькулятор страхования от клеща</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>Калькулятор страхования от клеща</h2>

    <div>
        <label>Программа страхования:</label>
        <input type="radio" id="basic" name="program" value="basic" checked>
        <label for="basic">Базовая</label>
        <input type="radio" id="complex" name="program" value="complex">
        <label for="complex">Комплексная</label>
        <input type="radio" id="complex_ambulance" name="program" value="complex_ambulance">
        <label for="complex_ambulance">Комплексная + скорая</label>
    </div>

    <div>
        <label for="insuranceDays">Срок страхования (дни):</label>
        <input type="number" id="insuranceDays" value="30" min="1">
    </div>

    <div>
        <label for="coverageAmount">Сумма страхового покрытия (₽):</label>
        <input type="number" id="coverageAmount" value="50000" min="1">
    </div>

    <fieldset>
        <legend>Данные страхователя:</legend>
        <label for="startDate">Дата начала договора:</label>
        <input type="date" id="startDate">
        <label for="contractTerm">Срок договора (дни):</label>
        <input type="number" id="contractTerm" value="365" min="1">
        <label for="fioInsurer">ФИО страхователя:</label>
        <input type="text" id="fioInsurer">
        <label for="fioInsured">ФИО застрахованного лица (если отличается):</label>
        <input type="text" id="fioInsured">
        <label for="passportData">Паспортные данные:</label>
        <input type="text" id="passportData">
        <label for="snils">СНИЛС:</label>
        <input type="text" id="snils">
        <label for="inn">ИНН:</label>
        <input type="text" id="inn">
        <label for="phone">Телефон для связи:</label>
        <input type="tel" id="phone">
        <label for="email">Электронный почтовый ящик:</label>
        <input type="email" id="email">
        <label for="birthDate">Дата рождения:</label>
        <input type="date" id="birthDate">
        <label for="registrationAddress">Адрес регистрации:</label>
        <input type="text" id="registrationAddress">
        <label for="actualAddress">Адрес фактического проживания (если отличается):</label>
        <input type="text" id="actualAddress">
    </fieldset>

    <button onclick="calculatePremium()">Рассчитать</button>

    <div id="premiumResult">Введите данные и нажмите "Рассчитать".</div>

    <h3>Информация о страховщике</h3>
    <p>Наименование организации: <strong>Страхование жизни и здоровье</strong></p>
    <p>ИНН: <strong>222000555333</strong></p>
    <p>ОГРН: <strong>2222222222</strong></p>
    <p>Юридический адрес: <strong>Алтайский край, г. Барнаул, пр-т Ленина, дом 1, помещение 1</strong></p>
    <p>Email: <a href="mailto:strahov@inbox.ru">strahov@inbox.ru</a></p>
    <p>Телефон: <a href="tel:+73852221122">+7 (385) 222-11-22</a></p>

    <hr>

    <h3>ТИПОВОЙ ДОГОВОР № ______<br>
    добровольного медицинского страхования<br>
    «___» __________ 20__ г.</h3>

    <p>Публичное акционерное общество Страховая компания «Росгосстрах», именуемое в дальнейшем «СТРАХОВЩИК», в лице ____________________________________________________________________________, действующего на основании ________________________________ № ______ от «___» __________, с одной стороны, и _____________________________________________________________________________________________________________________________, именуемый (-ая) в дальнейшем «СТРАХОВАТЕЛЬ», действующий на основании ____________________________________________________________________________ от __________________________, с другой стороны, именуемые в дальнейшем «стороны», заключили настоящий договор о следующем:</p>

    <ol>
        <li><b>ТИПОВОЙ ДОГОВОР  №	
добровольного медицинского страхования
 


«	»	
 

Публичное акционерное общество Страховая компания «Росгострах», именуемое в дальнейшем	«СТРАХОВЩИК»,	в
 
лице
его на основании	№	от «  »	с одной стороны	и
 
,действующ
 
	 , именуемый (-ая) в дальнейшем «СТРАХОВАТЕЛЬ»
действующий на основании 	 от 	 , с другой стороны, именуемые в дальнейшем «стороны», заключили настоящий договор о следующем:

1.	ПРЕДМЕТ ДОГОВОРА
1.1.	СТРАХОВЩИК принимает на себя организацию, оплату и контроль качества медицинских и иных услуг, оказываемых гражданам, включенным в представленные СТРАХОВАТЕЛЕМ списки (далее застрахованным), являющиеся неотъемлемой частью настоящего договора страхования.
Страховым случаем является факт документально подтвержденного обращения застрахованного в медицинское учреждение из числа предусмотренных Договором страхования за получением медицинских и иных услуг в экстренном и/или плановом порядке, в случаях острых заболеваний, отравлений, ожогов или травм, а также обострений хронических заболеваний, возникших в период действия Договора страхования, требующих оказания медицинской помощи.
Услуги предоставляются Застрахованному в соответствии с программой страхования или по согласованию со Страховщиком путем оказания консультативной, лечебной, диагностической, профилактической, реабилитационно-восстановительной, санаторно- курортной, медикаментозной, скорой и неотложной медицинской и иной помощи.
1.2.	Перечень медицинских и иных услуг, оказываемых застрахованному, а также перечень медицинских учреждений определяются сторонами по каждой программе страхования, которые прилагаются к настоящему договору и являются его неотъемлемой частью.
1.3.	Общая  численность застрахованных на момент заключения договора составляет
	человек, из них:
по программе «	» - 	человек,
по программе «	» - 	человек, и т.д.
Списки	застрахованных,	составленные	по	программам	страхования	по	форме, утвержденной СТРАХОВЩИКОМ, передаются СТРАХОВАТЕЛЕМ СТРАХОВЩИКУ.
1.4.	СТРАХОВЩИК выдает застрахованному (ым) через СТРАХОВАТЕЛЯ или представителя в течение 10 рабочих дней после вступления договора страхования в силу полис (ы) добровольного медицинского страхования установленной формы с приложением выписки из правил добровольного медицинского страхования и программы страхования.
1.5.	СТРАХОВАТЕЛЬ, заключивший настоящий договор добровольного медицинского страхования в пользу другого лица, прав застрахованного не приобретает.
 
2.	СТРАХОВАЯ	СУММА.	РАЗМЕР,	СРОКИ	И	ПОРЯДОК	ВНЕСЕНИЯ СТРАХОВОЙ ПРЕМИИ (ВЗНОСОВ)
2.1.	Размер страховой премии за каждого застрахованного составляет:
по программе «	» - 	руб., страховой тариф 	,
по программе «	» - 	 руб., страховой тариф 	 и т.д.
Страховая премия по настоящему договору составляет (всего)	(словами) руб.
2.2.	Страховая сумма на одного застрахованного по настоящему договору составляет: по программе «	» -	руб.,
по программе «	» -	руб., и т.д..
Общая страховая сумма по настоящему договору составляет 	руб.
2.3.	По согласованию со СТРАХОВАТЕЛЕМ размер страховой премии в течение срока действия договора может изменяться в зависимости от изменения страховой программы, увеличения страхового риска.
2.4.	Оплата страховой премии (страховых взносов) производится СТРАХОВАТЕЛЕМ в рублях путем безналичных расчетов на расчетный счет СТРАХОВЩИКА единовременно или в следующем порядке:
Первый взнос в размере 	  руб. – « » 	 20_ г. Второй взнос в размере 	  руб. – « » 	 20_ г. Третий взнос в размере 	 руб. – «   » 	20_ г.
Четвертый взнос в размере 	 руб. – «	» 	20_ г. и т.д.
СТРАХОВАТЕЛЬ вправе в одностороннем порядке изменить сроки оплаты страховых взносов в сторону уменьшения (сокращения) таковых.
Страховщик информирует страхователя:
-	о факте просрочки уплаты страхового взноса
-	о факте неполной уплаты страхового взноса.

3.	СРОК	ДЕЙСТВИЯ	ДОГОВОРА.	ВСТУПЛЕНИЕ	ДОГОВОРА СТРАХОВАНИЯ В СИЛУ
3.1.	Срок действия настоящего договора один год с даты вступления договора в силу.
3.2.	Настоящий договор вступает в силу с « »   20_г. вне зависимости от уплаты страховой премии (первого страхового взноса), если иное не предусмотрено договором и действует по « » 20_г.
3.3.	Страхование, обусловленное настоящим договором, распространяется на страховые случаи, происшедшие после вступления договора в силу и до окончания срока действия договора.
4.	ОТВЕТСТВЕННОСТЬ СТОРОН
4.1.	Права и обязанности сторон определяются действующим законодательством и правилами   добровольного  медицинского  страхования  (КС)  №58кс  ПАО  СК
«РОСГОССТРАХ» от «	»		20_г.
4.2.	СТРАХОВАТЕЛЬ несет ответственность за полноту и достоверность сведений, предоставляемых страховщику при заключении договора страхования и своевременность уплаты страховой премии (взноса), определенной настоящим договором.
4.3.	СТРАХОВЩИК несет ответственность за полноту, своевременность и качество оказываемых медицинских и иных услуг застрахованным.
4.4.	СТРАХОВЩИК за свой счет оплачивает медицинские услуги, необходимые для исправления ущерба здоровья застрахованного, если такой ущерб был нанесен при оказании медицинской помощи в медицинских учреждениях, указанных в программах страхования.
4.5.	При досрочном прекращении договора страхования в отношении одного или нескольких застрахованных СТРАХОВАТЕЛЬ обязан уведомить их в соответствии со статьей 955 Гражданского Кодекса Р.Ф. о прекращении действия договора страхования и вернуть СТРАХОВЩИКУ страховую документацию (страховые полиса или страховые
 
карточки) по данным застрахованным.

5.	ВНЕСЕНИЕ ИЗМЕНЕНИЙ И/ИЛИ ДОПОЛНЕНИЙ В ДОГОВОР
5.1.	Все изменения и дополнения к настоящему договору совершаются по соглашению сторон и считаются действительными, если они совершены в письменной форме, скреплены печатями обеих сторон и подписаны уполномоченными на это представителями сторон.
5.2.	Изменение и/или дополнение условий настоящего договора производится на основании письменного заявления одной из сторон в течение семи дней с момента получения заявления другой стороной и оформляется дополнительным соглашением сторон.
5.3.	Если какая-либо из сторон не согласна на внесение изменений и/или дополнений в настоящий договор, в семидневный срок решается вопрос о действии договора на прежних условиях или о прекращении его действия.
6.	ПОРЯДОК РАЗРЕШЕНИЯ СПОРОВ
6.1.	Все неурегулированные споры между сторонами по настоящему договору рассматриваются в порядке, установленном действующим законодательством РФ.

Актуальная  информация  об  адресах  центров  урегулирования  убытков  ПАО  СК
«РОСГОССТРАХ», принимающих документы о наступлении страхового случая, имеется на официальном сайте РОСГОССТРАХ - www.RGS.ru., а так же указанную информацию можно получить позвонив  по круглосуточному номеру телефона ПАО СК
«РОСГОССТРАХ» 8-800-700-42-00	.
7.	АДРЕСА И РЕКВИЗИТЫ СТОРОН СТРАХОВЩИК: ПАО СК «РОСГОССТРАХ»
Местонахождение:

Почтовый адрес:

_
ИНН:


Банковские реквизиты: Р/с 		в 		, к/с 	, БИК 		
CТРАХОВАТЕЛЬ:
К настоящему договору прилагаются:
1.	Списки застрахованных
2.	Программа добровольного медицинского страхования 	
3.	Выписка из Правил добровольного медицинского страхования (КС) №58кс ПАО СК «РОСГОССТРАХ» от « » 20_г. и т.д., которые Страхователь получил.

ПОДПИСИ СТОРОН

СТРАХОВЩИК	CТРАХОВАТЕЛЬ
(Должность)

 
	(ФИО)
М.П.
 
	(ФИО)
 

<br>
            по программе «_________» - __________ руб., и т.д.<br>
            Общая страховая сумма по настоящему договору составляет __________ руб.<br>
            2.3. По согласованию со СТРАХОВАТЕЛЕМ размер страховой премии в течение срока действия договора может изменяться в зависимости от изменения страховой программы, увеличения страхового риска.<br>
            2.4. Оплата страховой премии (страховых взносов) производится СТРАХОВАТЕЛЕМ в рублях путем безналичных расчетов на расчетный

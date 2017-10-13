<h1>SQL Viewer (Query Builder)</h1>
<div>
Инструмент по работе с картами и формирования url для получения изображений спутниковых снимков
и отображению их на картах в web интервейсе
</div>

<h2>Описание кода</h2>

## Members

<dl>
<dt><a href="#prfx">prfx</a></dt>
<dd><p>Created by bykovdenis on 05.09.17.</p>
</dd>
<dt><a href="#setUriSearch">setUriSearch</a></dt>
<dd><p>Определяем параметры location.search с которыми быдем работать</p>
</dd>
<dt><a href="#setApprovedFields">setApprovedFields</a></dt>
<dd><p>setter для инициализации доступных параметров в URL</p>
</dd>
<dt><a href="#setApprovedFields">setApprovedFields</a></dt>
<dd><p>setter для инициализации доступных параметров в URL</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#Types">Types</a></dt>
<dd><p>Created by bykovdenis on 27.08.17.</p>
</dd>
<dt><a href="#getColors">getColors</a></dt>
<dd><p>маппинг цветовых параметров</p>
</dd>
<dt><a href="#parseColorPallete">parseColorPallete</a> ⇒ <code>string</code></dt>
<dd><p>парсинг параметра цвета при загрузке из URL
Костылезированная функция для маппинга параметров формы и URL</p>
</dd>
<dt><a href="#prepareColorPalette">prepareColorPalette</a> ⇒ <code>*</code></dt>
<dd><p>Форматирование параметра цветовой палитры для URL</p>
</dd>
<dt><a href="#getInitialStateFromURL">getInitialStateFromURL</a></dt>
<dd><p>Action инициализации значений формы и карты</p>
</dd>
<dt><a href="#setLocation">setLocation</a> ⇒ <code>Object</code></dt>
<dd><p>Action для установки актуального знанения позиции на карте</p>
</dd>
<dt><a href="#getLocation">getLocation</a></dt>
<dd><p>Action для получения текущей локации</p>
</dd>
<dt><a href="#buildSqlQuery">buildSqlQuery</a></dt>
<dd><p>Функция построения URL</p>
</dd>
<dt><a href="#togglePopup">togglePopup</a></dt>
<dd><p>Action для отображения/сокрытия popup</p>
</dd>
<dt><a href="#changeColorParam">changeColorParam</a></dt>
<dd><p>Action для переключения цветовых параметров</p>
</dd>
<dt><a href="#changeTab">changeTab</a></dt>
<dd><p>Action переключения табов на sql-tools</p>
</dd>
<dt><a href="#changeFullScreenMode">changeFullScreenMode</a> ⇒ <code>Object</code></dt>
<dd><p>Action переведения работы приложения в полноэкранный режим</p>
</dd>
<dt><a href="#setHoverLocation">setHoverLocation</a></dt>
<dd><p>Action установка параметров широты долготы</p>
</dd>
<dt><a href="#exitFullScreen">exitFullScreen</a></dt>
<dd><p>Action Выход из полноэкранного режима</p>
</dd>
<dt><a href="#RENDER_TILE_LAYERS">RENDER_TILE_LAYERS</a></dt>
<dd><p>Created by Denis on 13.03.2017.</p>
</dd>
<dt><a href="#initialState">initialState</a></dt>
<dd><p>Created by Denis on 18.08.2017.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#numberDaysOfYearXXX">numberDaysOfYearXXX(number)</a> ⇒ <code>string</code></dt>
<dd><p>метод преобразования номера дня в году в трехразрядное число ввиде строки</p>
</dd>
<dt><a href="#convertDateToNumberDay">convertDateToNumberDay(date)</a> ⇒ <code>integer</code></dt>
<dd><p>Метод определения порядкового номера в году</p>
</dd>
<dt><a href="#convertNumberDayToDate">convertNumberDayToDate(date)</a> ⇒ <code>date</code></dt>
<dd><p>Метод преообразует дату формата yyyy-<number day in year> в yyyy-mm-dd</p>
</dd>
<dt><a href="#formatDate">formatDate(date)</a> ⇒ <code>string</code></dt>
<dd><p>Метод преобразования даты вида yyyy-<number day in year></p>
</dd>
<dt><a href="#getCurrentDate">getCurrentDate()</a> ⇒ <code>string</code></dt>
<dd><p>Метод возвращает текущую отформатированную дату yyyy-mm-dd</p>
</dd>
<dt><a href="#getDateLastThreeMonth">getDateLastThreeMonth()</a> ⇒ <code>string</code></dt>
<dd><p>Возвращает последние три месяца</p>
</dd>
<dt><a href="#getCurrentSummerDate">getCurrentSummerDate()</a> ⇒ <code>*</code></dt>
<dd><p>Возвращает интервал дат текущего лета</p>
</dd>
<dt><a href="#getCurrentSpringDate">getCurrentSpringDate()</a> ⇒ <code>array</code></dt>
<dd><p>Возвращает интервал дат текущего лета</p>
</dd>
<dt><a href="#getLastSummerDate">getLastSummerDate()</a> ⇒ <code>array</code></dt>
<dd><p>Возвращает интервал дат предыдущего лета</p>
</dd>
<dt><a href="#getDateBeforeDay">getDateBeforeDay()</a></dt>
<dd><p>Возвращает полученныую дату равную текущей минус X дней</p>
</dd>
<dt><a href="#randomInteger">randomInteger()</a></dt>
<dd><p>Created by bykovdenis on 16.08.17.</p>
</dd>
<dt><a href="#getArrayURI">getArrayURI(uri)</a> ⇒ <code>*</code></dt>
<dd><p>Обрабатываем URI, URL строки</p>
</dd>
<dt><a href="#getData">getData(uri)</a> ⇒ <code>*</code></dt>
<dd><p>Получаем массив строк ключ=значение</p>
</dd>
<dt><a href="#compareData">compareData(key, value)</a></dt>
<dd><p>Сравнение запрошенных данных с данными URL</p>
</dd>
<dt><a href="#setURIParams">setURIParams(key, value)</a></dt>
<dd><p>Обновляем/добавляем URI параметр в URL</p>
</dd>
<dt><a href="#setURIParamsNotReloadPage">setURIParamsNotReloadPage(data)</a></dt>
<dd><p>Обновление параметров URL без перезагрузки страницы черз pushState</p>
</dd>
<dt><a href="#ignoreParams">ignoreParams(name)</a></dt>
<dd><p>Метод для добавления параметров для игнорирования при формаировании URL</p>
</dd>
<dt><a href="#getURL">getURL(data)</a></dt>
<dd><p>Метод для формирования url к тайловому серверу</p>
</dd>
<dt><a href="#getURLWithoutAPPID">getURLWithoutAPPID(data)</a></dt>
<dd><p>Метод для формирования url к тайловому серверу без ключа</p>
</dd>
<dt><a href="#getParams">getParams()</a> ⇒ <code>Object</code></dt>
<dd><p>Метод для получения данных для заполнения полей формы</p>
</dd>
<dt><a href="#getParamsURI">getParamsURI()</a></dt>
<dd><p>Вернуть объект ключей со значениями URI параметров
lat, lon, zoom</p>
</dd>
<dt><a href="#getParsedURL">getParsedURL(stateParam, value)</a> ⇒ <code>Object</code></dt>
<dd><p>Парсинг URL строки</p>
</dd>
<dt><a href="#getDefaultParams">getDefaultParams(values)</a></dt>
<dd><p>метод для инициализации начального state на основе файла конфигурации</p>
</dd>
</dl>

<a name="prfx"></a>

## prfx
Created by bykovdenis on 05.09.17.

**Kind**: global variable  
<a name="setUriSearch"></a>

## setUriSearch
Определяем параметры location.search с которыми быдем работать

**Kind**: global variable  

| Param |
| --- |
| params | 

<a name="setApprovedFields"></a>

## setApprovedFields
setter для инициализации доступных параметров в URL

**Kind**: global variable  

| Param |
| --- |
| values | 

<a name="setApprovedFields"></a>

## setApprovedFields
setter для инициализации доступных параметров в URL

**Kind**: global variable  

| Param |
| --- |
| values | 

<a name="Types"></a>

## Types
Created by bykovdenis on 27.08.17.

**Kind**: global constant  
<a name="getColors"></a>

## getColors
маппинг цветовых параметров

**Kind**: global constant  

| Param |
| --- |
| colors | 

<a name="parseColorPallete"></a>

## parseColorPallete ⇒ <code>string</code>
парсинг параметра цвета при загрузке из URL
Костылезированная функция для маппинга параметров формы и URL

**Kind**: global constant  

| Param |
| --- |
| value | 

<a name="prepareColorPalette"></a>

## prepareColorPalette ⇒ <code>\*</code>
Форматирование параметра цветовой палитры для URL

**Kind**: global constant  

| Param |
| --- |
| values | 

<a name="getInitialStateFromURL"></a>

## getInitialStateFromURL
Action инициализации значений формы и карты

**Kind**: global constant  
<a name="setLocation"></a>

## setLocation ⇒ <code>Object</code>
Action для установки актуального знанения позиции на карте

**Kind**: global constant  

| Param |
| --- |
| params | 

<a name="getLocation"></a>

## getLocation
Action для получения текущей локации

**Kind**: global constant  
<a name="buildSqlQuery"></a>

## buildSqlQuery
Функция построения URL

**Kind**: global constant  
<a name="togglePopup"></a>

## togglePopup
Action для отображения/сокрытия popup

**Kind**: global constant  

| Param |
| --- |
| popupName | 

<a name="changeColorParam"></a>

## changeColorParam
Action для переключения цветовых параметров

**Kind**: global constant  

| Param |
| --- |
| color | 
| values | 

<a name="changeTab"></a>

## changeTab
Action переключения табов на sql-tools

**Kind**: global constant  

| Param |
| --- |
| value | 

<a name="changeFullScreenMode"></a>

## changeFullScreenMode ⇒ <code>Object</code>
Action переведения работы приложения в полноэкранный режим

**Kind**: global constant  

| Param |
| --- |
| value | 

<a name="setHoverLocation"></a>

## setHoverLocation
Action установка параметров широты долготы

**Kind**: global constant  

| Param |
| --- |
| location | 

<a name="exitFullScreen"></a>

## exitFullScreen
Action Выход из полноэкранного режима

**Kind**: global constant  

| Param |
| --- |
| e | 

<a name="RENDER_TILE_LAYERS"></a>

## RENDER_TILE_LAYERS
Created by Denis on 13.03.2017.

**Kind**: global constant  
<a name="initialState"></a>

## initialState
Created by Denis on 18.08.2017.

**Kind**: global constant  
<a name="numberDaysOfYearXXX"></a>

## numberDaysOfYearXXX(number) ⇒ <code>string</code>
метод преобразования номера дня в году в трехразрядное число ввиде строки

**Kind**: global function  
**Returns**: <code>string</code> - трехзначное число ввиде строки порядкового номера дня в году  

| Param | Type | Description |
| --- | --- | --- |
| number | <code>integer</code> | число менее 999 |

<a name="convertDateToNumberDay"></a>

## convertDateToNumberDay(date) ⇒ <code>integer</code>
Метод определения порядкового номера в году

**Kind**: global function  
**Returns**: <code>integer</code> - Порядковый номер в году  

| Param | Type | Description |
| --- | --- | --- |
| date | <code>date</code> | Дата формата yyyy-mm-dd |

<a name="convertNumberDayToDate"></a>

## convertNumberDayToDate(date) ⇒ <code>date</code>
Метод преообразует дату формата yyyy-<number day in year> в yyyy-mm-dd

**Kind**: global function  
**Returns**: <code>date</code> - дата формата yyyy-mm-dd  

| Param | Type | Description |
| --- | --- | --- |
| date | <code>string</code> | дата формата yyyy-<number day in year> |

<a name="formatDate"></a>

## formatDate(date) ⇒ <code>string</code>
Метод преобразования даты вида yyyy-<number day in year>

**Kind**: global function  
**Returns**: <code>string</code> - дата ввиде строки формата yyyy-<number day in year>  

| Param | Type | Description |
| --- | --- | --- |
| date | <code>date1</code> | дата в формате yyyy-mm-dd |

<a name="getCurrentDate"></a>

## getCurrentDate() ⇒ <code>string</code>
Метод возвращает текущую отформатированную дату yyyy-mm-dd

**Kind**: global function  
**Returns**: <code>string</code> - текущая дата  
<a name="getDateLastThreeMonth"></a>

## getDateLastThreeMonth() ⇒ <code>string</code>
Возвращает последние три месяца

**Kind**: global function  
<a name="getCurrentSummerDate"></a>

## getCurrentSummerDate() ⇒ <code>\*</code>
Возвращает интервал дат текущего лета

**Kind**: global function  
<a name="getCurrentSpringDate"></a>

## getCurrentSpringDate() ⇒ <code>array</code>
Возвращает интервал дат текущего лета

**Kind**: global function  
<a name="getLastSummerDate"></a>

## getLastSummerDate() ⇒ <code>array</code>
Возвращает интервал дат предыдущего лета

**Kind**: global function  
<a name="getDateBeforeDay"></a>

## getDateBeforeDay()
Возвращает полученныую дату равную текущей минус X дней

**Kind**: global function  
<a name="randomInteger"></a>

## randomInteger()
Created by bykovdenis on 16.08.17.

**Kind**: global function  
<a name="getArrayURI"></a>

## getArrayURI(uri) ⇒ <code>\*</code>
Обрабатываем URI, URL строки

**Kind**: global function  

| Param |
| --- |
| uri | 

<a name="getData"></a>

## getData(uri) ⇒ <code>\*</code>
Получаем массив строк ключ=значение

**Kind**: global function  

| Param |
| --- |
| uri | 

<a name="compareData"></a>

## compareData(key, value)
Сравнение запрошенных данных с данными URL

**Kind**: global function  

| Param |
| --- |
| key | 
| value | 

<a name="setURIParams"></a>

## setURIParams(key, value)
Обновляем/добавляем URI параметр в URL

**Kind**: global function  

| Param |
| --- |
| key | 
| value | 

<a name="setURIParamsNotReloadPage"></a>

## setURIParamsNotReloadPage(data)
Обновление параметров URL без перезагрузки страницы черз pushState

**Kind**: global function  

| Param |
| --- |
| data | 

<a name="ignoreParams"></a>

## ignoreParams(name)
Метод для добавления параметров для игнорирования при формаировании URL

**Kind**: global function  

| Param |
| --- |
| name | 

<a name="getURL"></a>

## getURL(data)
Метод для формирования url к тайловому серверу

**Kind**: global function  

| Param |
| --- |
| data | 

<a name="getURLWithoutAPPID"></a>

## getURLWithoutAPPID(data)
Метод для формирования url к тайловому серверу без ключа

**Kind**: global function  

| Param |
| --- |
| data | 

<a name="getParams"></a>

## getParams() ⇒ <code>Object</code>
Метод для получения данных для заполнения полей формы

**Kind**: global function  
<a name="getParamsURI"></a>

## getParamsURI()
Вернуть объект ключей со значениями URI параметров
lat, lon, zoom

**Kind**: global function  
<a name="getParsedURL"></a>

## getParsedURL(stateParam, value) ⇒ <code>Object</code>
Парсинг URL строки

**Kind**: global function  

| Param |
| --- |
| stateParam | 
| value | 

<a name="getDefaultParams"></a>

## getDefaultParams(values)
метод для инициализации начального state на основе файла конфигурации

**Kind**: global function  

| Param |
| --- |
| values | 


<p>© 2017 VANE All rights reserved.</p>
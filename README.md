<!DOCTYPE html>
<html lang="en">
<head>
<script>
      var debug = false;
      if (!debug && window.location.protocol != "https:" && window.location.protocol != "file:")
          window.location.href = "https:" + window.location.href.substring(window.location.protocol.length);
    </script>
<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
<link rel="apple-touch-icon" sizes="57x57" href="/favicon/apple-icon-57x57.png">
<link rel="apple-touch-icon" sizes="60x60" href="/favicon/apple-icon-60x60.png">
<link rel="apple-touch-icon" sizes="72x72" href="/favicon/apple-icon-72x72.png">
<link rel="apple-touch-icon" sizes="76x76" href="/favicon/apple-icon-76x76.png">
<link rel="apple-touch-icon" sizes="114x114" href="/favicon/apple-icon-114x114.png">
<link rel="apple-touch-icon" sizes="120x120" href="/favicon/apple-icon-120x120.png">
<link rel="apple-touch-icon" sizes="144x144" href="/favicon/apple-icon-144x144.png">
<link rel="apple-touch-icon" sizes="152x152" href="/favicon/favicon/apple-icon-152x152.png">
<link rel="apple-touch-icon" sizes="180x180" href="/favicon/apple-icon-180x180.png">
<link rel="icon" type="image/png" sizes="192x192" href="/favicon/android-icon-192x192.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="/favicon/favicon-96x96.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon/favicon-16x16.png">
<link rel="manifest" href="/favicon/manifest.json">
<meta name="msapplication-TileColor" content="#ffffff">
<meta name="msapplication-TileImage" content="/favicon/ms-icon-144x144.png">
<meta name="theme-color" content="#ffffff">
<meta charset="utf-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="viewport" content="width=device-width, initial-scale=1" />

<meta name="description" content="" />
<meta name="author" content="" />
<title>GuildEX - The Tradeing Guild for Crypto</title>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" integrity="sha384-PsH8R72JQ3SOdhVi3uxftmaW6Vc51MKb0q5P2rRUpPvrszuE4W1povHYgTpBfshb" crossorigin="anonymous">

<link href="/css/styles.css" rel="stylesheet">
<script src="/js/sorttable.js"></script>
<script>
      'use strict';
    
      const SHARE = JSON.parse('{"tradeEnabled":true,"withdrawEnabled":true,"recaptchaEnabled":true,"emailVerificationEnabled":"enabled","pinVerificationEnabled":"enabled","TRADE_COMISSION":0.002,"DUST_VOLUME":0.001,"my_portSSL":443,"TRADE_MAIN_COIN":"Dogecoin","TRADE_MAIN_COIN_TICKER":"DOGE","TRADE_DEFAULT_PAIR":"GamersOnlineCoin"}');
      
      var grecaptcha;
      if (!SHARE.recaptchaEnabled) grecaptcha = null;
      
      const PORT_SSL = SHARE.my_portSSL;
      const MAIN_COIN = SHARE.TRADE_MAIN_COIN;
      const DEFAULT_PAIR = SHARE.TRADE_DEFAULT_PAIR;
      const TRADE_COMISSION = SHARE.TRADE_COMISSION;
    </script>
<script src='/js/utils.js'></script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script>
    $(document).ready(function(){
      $("#table-market-input").on("keyup", function() {
      var value = $(this).val().toLowerCase();
        $("#table-market tr").filter(function() {
          $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1)
         });
        });
      });
    </script>
<script>
    $(document).ready(function(){
      $("#id_wallet_body_input").on("keyup", function() {
      var value = $(this).val().toLowerCase();
        $("#id_wallet_body tr").filter(function() {
          $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1)
         });
        });
      });
    </script>
</head>
<body>
<div id="dark-image">
<nav class="navbar navbar-expand-lg navbar-light static-top bg-light">
<div class="container" style="max-width: 90%;">
<a class="navbar-brand" href="/">
<img height="30" border="0" align="center" src="/GuildEXLogo.png" />
</a>
<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
<span class="navbar-toggler-icon"></span>
</button>
<div class="collapse navbar-collapse" id="navbarSupportedContent">
<ul class="navbar-nav mr-auto">
<li class="nav-item active">
<a class="nav-link" href="/">Обменник</a>
</li>
<li class="nav-item active">
<a class="nav-link" target="_blank" href="https://discord.gg/dMFn5DK">Discord</a>
</li>
<li class="nav-item active">
<a class="nav-link" href="/API">API</a>
</li>
<li class="nav-item active">
<a class="nav-link" href="/add_coin">Add coin</a>
</li>
</ul>
</div>
<ul class="navbar-nav ml-auto">
<li class='nav-item staff_area'><a class='nav-link' href='/staff'>Staff Area</a></li>
<li class='nav-item chat_admin_area'><a class='nav-link' href='/staff'>Chat Admin</a></li>
<li class="nav-item dropdown">
<a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
<span>isky</span>
</a>
<div class="dropdown-menu" aria-labelledby="navbarDropdown">
<a class="dropdown-item" href="/profile">Profile</a>
<a class="dropdown-item" href="/wallet">Кошелек</a>
<a class="dropdown-item" href="/api_keys">API keys</a>
<a class="dropdown-item" href="/referals">Affiliate</a>
<div class="dropdown-divider"></div>
<a class="dropdown-item" href="/logout">Logout</a>
</div>
</li>
<li class="nav-item dropdown">
<a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
<span>Помощь</span>
</a>
<div class="dropdown-menu" aria-labelledby="navbarDropdown">
<a class="dropdown-item" href="https://support.guildex.io/index.php">Поддержка</a>
<a class="dropdown-item" href="/fees">Комиссии</a>
</div>
<div class="collapse navbar-collapse" id="navbarSupportedContent">
</li>
</ul>
<label title="Night Mode" for="mode" class="switch">
<input id="mode" type="checkbox">
<span class="slider round"></span>
</label>
</div>
</nav>
<div id="loader" style="display:none;"></div>
<input id='id_lang' type='hidden' value='ru'>

<div class="container pt-2">
<div id='id-alerts' class='row'>
<div id='alert-fail' class="alert alert-danger alert-dismissible col-md-12" role="alert" style="display:none;">
<div id='fail-message'></div>
<button id='close_fail' type="button" class="close" aria-label="Close">
<span aria-hidden="true">&times;</span>
</button>
</div>
<div id='alert-success' class="alert alert-success alert-dismissible col-md-12" role="alert" style="display:none;">
<div id='success-message'></div>
<button id='close_success' type="button" class="close" aria-label="Close">
<span aria-hidden="true">&times;</span>
</button>
</div>
</div>
<input id='id_token' type='hidden' value='pk/O/TdOTVvCLoU7c1zH+3WgWsXyNAVFubLOPBXeiLI%3D'>
<div class='row'>
<div class="col-md-3 p-0">
<div class="card">
<div class="card-header">
Dogecoin Market
</div>
<div class="card-body p-0">
<div id='market-flex' class="d-flex d-flex-market align-items-start bd-highlight mb-0">
<div id='market-container' class='container p-0'>
<table class="table table-sm  table-hover table-orders sortable">
<thead>
<tr>
<th scope="col"></th>
<th scope="col">Coin</th>
<th scope="col">Price</th>
<th scope="col">Vol DOGE</th>
<th scope="col">Ch (%)</th>
</tr>
</thead>
<tbody id='table-market'>
</tbody>
</table>
</div>
</div>
</div>
</div>
</div>
<div class='col-md-6 pl-1.4'>
<div class='container p-0'>
<div class='row p-0'>

<div class="card"></div>
<div class='card-header' style='width:100%;'><div id='coinsymbolid'></div></div>
<script src='https://code.jquery.com/jquery-3.1.1.min.js'></script>
<script src='https://code.highcharts.com/stock/highstock.js'></script>
<script src='https://code.highcharts.com/stock/modules/drag-panes.js'></script>
<script src='https://code.highcharts.com/stock/modules/exporting.js'></script>
<div id='graphs' style='width:100%; height:100%'></div>
<script>
              var link = document.location.href;
              var coinsymbol = link.split("-").pop();
              var baseurl = window.location.origin + '/';
          
          if (link == baseurl){
            document.getElementById("coinsymbolid").innerHTML = 'Welcome to GuildEX, a DOGE paired exchange.';
            document.getElementById("graphs").innerHTML = '<div class="news">Please keep in mind this exchange is in ALPHA testing.<br>MotaCoin and Dravite have been added.<br>Pin Verification has been added.<br>New Layout and other backend upgrades have been made.<br>Night mode toggle has been added to the top right along with chat.<br></div>';
          } else {
          
          document.getElementById("coinsymbolid").innerHTML = 'Graph - ' + coinsymbol + '/DOGE';

          $.getJSON('/api/v1/public/getcharts?market=DOGE-'+coinsymbol, function (data) {
          var json_obj = data;
          Highcharts.stockChart('graphs', {
                title: {
                    text: null
                },
                 xAxis: {
                    gapGridLineWidth: 0
                },
                 rangeSelector: {
             selected: 1,
                    buttons: [{
                        type: 'day',
                        count: 1,
                        text: '1D'
                    }, {
                        type: 'day',
                        count: 3,
                        text: '3D'
                    }, {
                        type: 'day',
                        count: 7,
                        text: '7D'
                    }, {
                      type: 'day',
                        count: 14,
                        text: '14'
                    }, {
                        type: 'month',
                        count: 1,
                        text: '1M'
                    }, {
                        type: 'all',
                        count: 1,
                        text: 'All'
                    }],
                    inputEnabled: false
                },
            
            legend: {
                            enabled: true
                },
            
            exporting: {
                            enabled: false
                },
            plotOptions: {
         candlestick: {
              lineColor: '#2f7ed8',	    		
                upLineColor: 'silver',
                upColor: 'green',
                downColor: 'red'
                }
            },
                 series: [{
                    type: 'candlestick',
                    name: coinsymbol,
                    data: json_obj
                }]
            });
        });
        }
          </script>
</div>
</div>
</div>
<div class="col-md-3 p-0">
<div class="card">
<div id='id_chat_header' class="card-header">
Chat
</div>
<div style="position:absolute; right:10px; top:8px;">
<button id='id_btn_chat_ru' type="button" class="btn btn-outline-primary btn-sm">RM1</button>
<button id='id_btn_chat_en' type="button" class="btn btn-outline-primary btn-sm">RM2</button>
</div>
<div class="card-body p-0">
<div id='chat-flex' class="d-flex d-flex-chat align-items-start bd-highlight mb-0" style="height: 382px">
<div id='chat-container_loading' class='container'>
<div class='row'><div class='col-md-12'>Loading...</div></div>
</div>
<div id='chat-container_ru' class='container font_14'>
</div>
<div id='chat-container_en' class='container font_14'>
</div>
</div>
<div class="input-group">
<input id='chat_message' type="text" class="form-control" maxlength="150">
<span class="input-group-btn">
<button id='button_chat' class="btn btn-secondary" type="button">Submit</button>
</span>
</div>
</div>
</div>
</div>
</div>
<div class='row'>
<div class="col-md-3 p-1">
<div class="card">
<div id='header_buy' class="card-header">
</div>
<div class="card-body p-1">
<div class="alert alert-secondary p-1" role="alert">
<div class='container'>
<div class='row'>
<div class='col-md-6'>
<table>
<thead>
<tr><th>Your balance:</th></tr>
</thead>
<tbody>
<tr>
<td>
<span id='id_buy_balance'></span>
<div id="id_balance_spiner1">
<div id="circularG_1" class="circularG"></div>
<div id="circularG_2" class="circularG"></div>
<div id="circularG_3" class="circularG"></div>
<div id="circularG_4" class="circularG"></div>
<div id="circularG_5" class="circularG"></div>
<div id="circularG_6" class="circularG"></div>
<div id="circularG_7" class="circularG"></div>
<div id="circularG_8" class="circularG"></div>
</div>
</td>
</tr>
<tr><td id='id_buy_coin'></td></tr>
</tbody>
</table>
</div>
<div class='col-md-6'>
<table>
<thead>
<tr><th>Highest Ask:</th></tr>
</thead>
<tbody>
<tr><td id='id_max_ask'></td></tr>
<tr><td id='id_max_ask_coin'></td></tr>
</tbody>
</table>
</div>
</div>
</div>
</div>
<form id="form_buy" class="p-3">
<div class="form-group row">
<label for="inputBuyAmount" class="col-md-4 col-form-label form-control-sm">Amount:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputBuyAmount" placeholder="0.0" aria-describedby="id_amount_buy" onkeypress="return (event.charCode >= 48 && event.charCode <= 57) || event.charCode == 46 || event.charCode == 0 ">
<span class="currency" id="id_amount_buy"></span>
</div>
</div>
<div class="form-group row">
<label for="inputBuyPrice" class="col-md-4 col-form-label form-control-sm">Price:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputBuyPrice" placeholder="0.0" onkeypress="return (event.charCode >= 48 && event.charCode <= 57) || event.charCode == 46 || event.charCode == 0 ">
<span class="currency" id="id_price_buy"></span>
</div>
</div>
<div class="form-group row">
<label for="inputBuyComission" class="col-md-4 col-form-label form-control-sm">Comission:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputBuyComission" readonly placeholder="0.0">
<span class="currency" id="id_comission_buy"></span>
</div>
</div>
<div class="form-group row">
<label for="inputBuyTotal" class="col-md-4 col-form-label form-control-sm">Total:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputBuyTotal" placeholder="0.0" onkeypress="return (event.charCode >= 48 && event.charCode <= 57) || event.charCode == 46 || event.charCode == 0 ">
<span class="currency" id="id_total_buy"></span>
</div>
</div>
<button type="submit" class="btn btn-primary">Купить</button>
</form>
</div>
</div>
</div>
<div class="col-md-3 p-1">
<div class="card">
<div id='header_sell' class="card-header">
</div>
<div class="card-body p-1">
<div class="alert alert-secondary p-1" role="alert">
<div class='container'>
<div class='row'>
<div class='col-md-6'>
<table>
<thead>
<tr><th>Your balance:</th></tr>
</thead>
<tbody>
<tr>
<td>
<span id='id_sell_balance'></span>
<div id="id_balance_spiner2">
<div id="circularG_1" class="circularG"></div>
<div id="circularG_2" class="circularG"></div>
<div id="circularG_3" class="circularG"></div>
<div id="circularG_4" class="circularG"></div>
<div id="circularG_5" class="circularG"></div>
<div id="circularG_6" class="circularG"></div>
<div id="circularG_7" class="circularG"></div>
<div id="circularG_8" class="circularG"></div>
</div>
</td>
</tr>
<tr><td id='id_sell_coin'></td></tr>
</tbody>
</table>
</div>
<div class='col-md-6'>
<table>
<thead>
<tr><th>Highest Bid:</th></tr>
</thead>
<tbody>
<tr><td id='id_max_bid'></td></tr>
<tr><td id='id_max_bid_coin'></td></tr>
</tbody>
</table>
</div>
</div>
</div>
</div>
<form id="form_sell" class="p-3">
<div class="form-group row">
<label for="inputSellAmount" class="col-md-4 col-form-label form-control-sm">Amount:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputSellAmount" placeholder="0.0" onkeypress="return (event.charCode >= 48 && event.charCode <= 57) || event.charCode == 46 || event.charCode == 0 ">
<span class="currency" id="id_amount_sell"></span>
</div>
</div>
<div class="form-group row">
<label for="inputSellPrice" class="col-md-4 col-form-label form-control-sm">Price:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputSellPrice" placeholder="0.0" onkeypress="return (event.charCode >= 48 && event.charCode <= 57) || event.charCode == 46 || event.charCode == 0 ">
<span class="currency" id="id_price_sell"></span>
</div>
</div>
<div class="form-group row">
<label for="inputSEllComission" class="col-md-4 col-form-label form-control-sm">Comission:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputSellComission" readonly placeholder="0.0">
<span class="currency" id="id_comission_sell"></span>
</div>
</div>
<div class="form-group row">
<label for="inputSellTotal" class="col-md-4 col-form-label form-control-sm">Total:</label>
<div class="col-md-8">
<input type="text" class="form-control" id="inputSellTotal" placeholder="0.0" onkeypress="return (event.charCode >= 48 && event.charCode <= 57) || event.charCode == 46 || event.charCode == 0 ">
<span class="currency" id="id_total_sell"></span>
</div>
</div>
<button type="submit" class="btn btn-primary">Продать</button>
</form>
</div>
</div>
</div>
<div class="col-md-3 p-1">
<div class="card">
<div class="card-header p-0">
<table class='table table-orders m-0'>
<tr>
<td><strong>Sell orders</strong></td>
<td class='form_title_volume' align="right">Volume:<span id='id_sell_volume'></span></td>
</tr>
</table>
</div>
<div class="card-body div-orders p-0">
<table class="table table-striped table-sm table-orders table-hover">
<thead>
<tr id='id_sell_orders_header'>
</tr>
</thead>
<tbody id='id_sell_orders_body'>
</tbody>
</table>
</div>
</div>
</div>
<div class="col-md-3 p-1">
<div class="card">
<div class="card-header p-0">
<table class='table table-orders m-0'>
<tr>
<td><strong>Buy orders</strong></td>
<td class='form_title_volume' align="right">Volume:<span id='id_buy_volume'></span></td>
</tr>
</table>
</div>
<div class="card-body div-orders p-0">
<table class="table table-striped table-sm table-orders table-hover">
<thead>
<tr id='id_buy_orders_header'>
</tr>
</thead>
<tbody id='id_buy_orders_body'>
</tbody>
</table>
</div>
</div>
</div>
<div class="col-md-6 p-1">
<div class="card">
<div class="card-header p-0">

<ul class="nav nav-tabs">
<li class="nav-item">
<a class="nav-link active" id="active-orders-tab" data-toggle="tab" href="#active_orders" role="tab" aria-controls="active_orders" aria-selected="true">Ваши активные заявки</a>
</li>
<li class="nav-item">
<a class="nav-link" id="history-orders-tab" data-toggle="tab" href="#history-orders" role="tab" aria-controls="history-orders" aria-selected="false">Ваши исполненные заявки</a>
</li>
</ul>
<div class="card-body div-orders p-2">
<div class="tab-content" id="user-orders-tab-content">
<div class="tab-pane fade show active" id="active_orders" role="tabpanel" aria-labelledby="active-orders-tab">
<table class="table table-striped table-sm">
<thead>
<tr>
<th>Time</th>
<th>Type</th>
<th>Amount</th>
<th>Price</th>
<th></th>
</tr>
</thead>
<tbody id='id_user_orders'>
</tbody>
</table>
</div>
<div class="tab-pane fade" id="history-orders" role="tabpanel" aria-labelledby="history-orders-tab">
<table class="table table-striped table-sm">
<thead>
<tr>
<th>Time</th>
<th>Type</th>
<th>Amount</th>
<th>Price</th>
<th></th>
</tr>
</thead>
<tbody id='id_user_orders_history'>
</tbody>
</table>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="col-md-6 p-1">
<div class="card">

<div class="card-header p-0">
<table class='table table-orders m-0'>
<tr>
<td><strong>История торгов:</strong></td>
</tr>
</table>
</div>
<div class="card-body div-orders p-0">
<table class="table table-striped table-sm table-orders">
<thead>
<tr>
<th>Time</th>
<th>Type</th>
<th>Volume</th>
<th>Price</th>
<th></th>
</tr>
</thead>
<tbody id='id_trade_history'>
</tbody>
</table>
</div>
</div>
</div>
</div>
</div> 

<div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
<div class="modal-dialog" role="document">
<div class="modal-content">
<div class="modal-header">
<h4 class="modal-title" id="myModalLabel"></h4>
<button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
</div>
<div class="modal-body">
</div>
<div class="modal-footer">
<button id='id_modal_cancel' type="button" class="btn btn-default" data-dismiss="modal">Cancel</button>
<button id='id_modal_ok' type="button" class="btn btn-primary">Confirm</button>
</div>
</div>
</div>
</div>

<script src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.3/umd/popper.min.js" integrity="sha384-vFJXuSJphROIrBnz7yo7oB41mKfc8JzQZiCq4NCceLEaO4IHwicKwpJf9c9IpFgh" crossorigin="anonymous"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/js/bootstrap.min.js" integrity="sha384-alpBpkh1PFOepccYVYDB4do5UnbKysX5WZXm3XxPqe5iKTfUKjNkCk9SaVuEZflJ" crossorigin="anonymous"></script>
<script src='https://www.google.com/recaptcha/api.js' async defer></script>
</div>
<script src='/js/common.js'></script>
<script src='/js/index.js'></script>
</body>
</html>

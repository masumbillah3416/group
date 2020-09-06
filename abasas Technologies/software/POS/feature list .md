

- monthly sale stats
- category stats
- product and category comparishm
- sale man comparishn
- add switch button  
   - fixed price 
   - sale type 
   - due buy 
   - due sell 
   - discount type - [percentage or anount]
   - voucher 
- order status 
   - pending 
   - due 
   - delivered etc
- voucher 
   - percentage or fixed
   - refferal 
- sms sending 
- online login system . first  he should write his store name then asked user name and pass 


       secutity 
       ----------
       Add ip verification
















Route::get('delete', function(){
   $orders = Order::select(
      DB::raw('sum(total) as sums'), 
      DB::raw("DATE_FORMAT(created_at,'%d %M %y') as months")
)
->groupBy('months')
->get();

return view('delete',compact('orders'));

});
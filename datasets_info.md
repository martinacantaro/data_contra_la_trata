#Datasets Trata


Se publicaron 2 tipos de datasets
- Denuncias
- Orientaciones (para casos que no son trata)


##Denuncias

Los datasets están divididos por año y/o mes

2017 - Dataset anual
2018 - Datasets mensuales, 201801 a 201812
2019 - Datasets mensuales, 201901 a 201910 (no está completo todavía el año)

Las columnas se fueron modificando a lo largo del tiempo, en general fue aumentando el número de columnas para sumar más información, algunas desaparecieron y otras cambiaron de nombre.

2017

- 10 columnas
 'denuncia_fecha',
 'denuncia_tipo_explotacion',
 'denuncia_via_ingreso',
 'denunciante_tipo_acercamiento',
 'hecho_localidad',
 'hecho_provincia',
 'hecho_pais',
 'hecho_denuncia_previa',
 'derivacion_judicializacion_organismo',
 'derivacion_judicializacion_fecha'

201801

'denuncia_fecha' - Se mantiene
'denuncia_tipo_explotacion' - Se mantiene
'denuncia_via_ingreso' - Se mantiene
'denunciante_tipo_acercamiento' - Se transforma en 'acercamiento_tipo'
'hecho_localidad' - Desaparece
'hecho_provincia' - Se mantiene
'hecho_pais' - Desaparece
'hecho_denuncia_previa' se transforma en 'denuncia_previa'
'derivacion_judicializacion_organismo' se transforma en 'derivacion_organismo'
'derivacion_judicializacion_fecha' se transforma en 'derivacion_fecha'

Aparecen columnas nuevas:
'connivencia_fuerzas_seguridad'
'connivencia_poder_politico'
'denunciado_genero'
'denunciado_provincia'
'denunciado_provincia_indec_id'
'derivacion_seguimiento'
'hecho_provincia_indec_id'
'llamante_anonimo'
'llamante_es_victima'
'llamante_genero'
'llamante_provincia'
'llamante_provincia_indec_id'
'llamante_rango_etario'
'victima_cantidad'
'victima_discapacidad'
'victima_embarazada'
'victima_genero'
'victima_nacionalidad'
'victima_provincia_origen'
'victima_provincia_origen_indec_id'
'victima_rango_etario'

localizacion: se empieza a considerar no solamente en que provincia sucedio el hecho, sino de que provincia son los actores involucrados (victima y denunciado)
se recaban mas datos del denunciado y de la victima
se taguea la localizacion con una id del indec
se empieza a registrar la connivencia con el poder politico y las fuerzas de seguridad\
se registra como se acerco el denunciado a la victima

201806
se suma 'denunciado_rango_etario'


201807
Se diferencia entre víctimas 'identificadas' y 'estimadas'
Se suman:
'victima_identificada_discapacidad',
'victima_identificada_embarazada',
'victima_identificada_genero',
'victima_identificada_nacionalidad',
'victima_identificada_provincia_origen',
'victima_identificada_provincia_origen_indec_id',
'victima_identificada_rango_etario',
'victimas_estimadas_cantidad',
'victimas_estimadas_genero',
'victimas_estimadas_provincia_hecho',
'victimas_estimadas_provincia_hecho_indec_id',
'victimas_estimadas_rango_etario'

2019
Se mantiene igual con respecto a 2018 los primeros meses. En 201905 cambian los nombres de las columnas para sacarles la palabra 'indec'. El contenido presumiblemente es el mismo (chequear).
'denunciado_provincia_id'y eliminan 'denunciado_provincia_indec_id'
(probablemente sea un cambio de nombre)
lo mismo con 'llamante_provincia_indec_id' y 'llamante_provincia_id' 



- Chequear si los datos son iguales en las columnas que cambiaron de nombre antes de mergear


# Limpieza

denuncia_fecha                                       2
denuncia_tipo_explotacion                           43
denuncia_via_ingreso                                19
acercamiento_tipo                                    0
hecho_localidad                                   3845
hecho_provincia                                   2723
hecho_pais                                        3786
denuncia_previa                                   2449
derivacion_organismo                                69
derivacion_fecha                                   112
derivacion_seguimiento                            2836
llamante_anonimo                                  2835
llamante_genero                                   2835
llamante_rango_etario                             2835
llamante_provincia                                2835
llamante_es_victima                               2835
victima_identificada_genero                       2835
victima_identificada_rango_etario                 2835
victima_identificada_discapacidad                 2836
victima_identificada_embarazada                   2837
victima_identificada_provincia_origen             2835
victima_cantidad                                  5464
victima_identificada_nacionalidad                 2835
denunciado_genero                                 2966
denunciado_provincia                              2835
connivencia_fuerzas_seguridad                     2835
connivencia_poder_politico                        2835
hecho_provincia_indec_id                          5804
denunciado_rango_etario                           3766
victimas_estimadas_cantidad                       3897
victimas_estimadas_genero                         3897
victimas_estimadas_rango_etario                   3898
victimas_estimadas_provincia_hecho                3897
victima_identificada_provincia_origen_indec_id    5383


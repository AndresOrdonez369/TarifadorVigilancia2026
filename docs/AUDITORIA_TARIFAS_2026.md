# Auditoría del tarifador frente a la Circular Externa 20251300000115CS

**Norma:** Supervigilancia, Circular Externa 20251300000115CS del 30 de diciembre de 2025, "Tarifas mínimas para el cobro y prestación del servicio de vigilancia y seguridad privada del 25 al 31 de diciembre de 2025, y vigencia 2026". Se apoya en el Decreto 1070 de 2015 (arts. 2.6.1.1.6.1 y siguientes), la Ley 1920 de 2018 y el Decreto 1588 de 2021 (seguro de vida), y las Leyes 2101 de 2021 y 2466 de 2025.

**Conclusión:** la fórmula de horas del tarifador ya era la de la circular. Había cuatro desfases, uno de ellos grande (residencial estratos 4, 5 y 6). Con esta corrección, los 15 servicios frecuentes dan **exactamente al peso** el valor de la fórmula oficial en 120 combinaciones probadas (15 servicios × 4 modalidades/clientes × 2 períodos).

## 1. Lo que dice la circular

**Tarifa de 24 horas y 30 días (numerales 1.1 a 1.3):**

| Período 2026 | Fórmula | Tarifa base |
|---|---|---:|
| 1 ene – 30 jun | $1.750.905 × 9,77 | $17.106.341,85 + prima seguro de vida |
| 1 – 14 jul | $1.750.905 × 9,85 | $17.246.414,25 + prima seguro de vida |
| 15 jul – 31 dic | $1.750.905 × 10,21 | $17.876.740,05 + prima seguro de vida |

**Administración y supervisión (AyS)**, aplicada sobre (tarifa base + prima): 8 % medio humano sin arma, 10 % con arma, 11 % con canino.

- **Residencial estratos 4, 5 y 6:** 10 % siempre.
- **Residencial estratos 1, 2 y 3:** no hay tarifa mínima; el precio debe cubrir las obligaciones laborales y los costos operativos (art. 2.6.1.1.6.5).

**Prima del seguro de vida (numeral 1, literales a y b):** es costo directo, va antes de la AyS, y se suma "el valor individual de la prima del seguro de vida que corresponda al número de hombres que prestarán el servicio".

**Descuentos:** solo las cooperativas pueden cobrar hasta un 10 % menos (art. 2.6.1.1.6.6). Para una empresa de vigilancia la tarifa mínima no admite descuento.

**Servicios de menos de 24 horas o 30 días (numeral 1.4):**

```
((((SMMLV × factor + prima del seguro de vida) × variable) / 30) × días) / jornada) × horas requeridas
```

- Variable de proporcionalidad: **47,59 %** para el turno de 6:00 a. m. a 7:00 p. m. (13 horas diurnas); **52,41 %** para el turno de 7:00 p. m. a 6:00 a. m. (11 horas nocturnas).
- Días por mes para 2026:
  - Lunes a viernes sin festivos: **20**
  - Lunes a viernes con festivos: **22**
  - Lunes a sábado sin festivos: **24**
  - Lunes a sábado con festivo: **26**
  - Festivos: **2**
  - Sábados y domingos: **8**
  - Sábados, domingos y festivos: **10**
  - Mes completo: **30**

## 2. Desfases encontrados y corrección

| # | Desfase en el tarifador | Qué exige la circular | Corrección |
|---|---|---|---|
| 1 | La prima se multiplicaba siempre por 3 guardas | Valor individual × número de hombres que prestan el servicio | Hombres automáticos según las horas y la jornada vigente (24/7 = 4 hombres con 42 h), editable en la cotización |
| 2 | Redondeo en cadena: costo directo, luego AyS sobre el valor ya redondeado, luego base de IVA, luego IVA | La circular calcula con decimales ($17.876.740,05) | Cálculo con todos los decimales; cada renglón se redondea al peso solo al final |
| 3 | Residencial estratos 4, 5 y 6 sin arma usaba AyS del 8 % | AyS del 10 % para esos estratos | Nuevo campo "Tipo de cliente": empresas y entidades / residencial 4-6 / residencial 1-3 |
| 4 | El descuento se repartía hacia atrás y mostraba un costo directo menor al regulado | El costo directo y la AyS son fijos; solo las cooperativas pueden bajar hasta 10 % | El costo directo regulado no cambia; el descuento sale como renglón aparte y se marca como ilegal salvo para cooperativas |

**Sin desfase:**

- Factores 9,77 / 9,85 / 10,21.
- Variables 47,59 % y 52,41 %.
- División por 30 y por la jornada (13 y 11).
- Días por mes (20, 24, 30, festivos 2).
- IVA: 19 % sobre base del 10 % (art. 462-1 E.T.).

## 3. Ejemplos paso a paso (período 15 jul – 31 dic 2026)

**8 horas diurnas de lunes a viernes, sin arma (1 hombre):**

1. Tarifa base: 1.750.905 × 10,21 = 17.876.740,05
2. Prima: 900 × 1 = 900 → base del servicio 17.877.640,05
3. Proporción: × 47,59 % = 8.507.968,90 → ÷ 30 = 283.598,96 → × 20 días = 5.671.979,27 → ÷ 13 = 436.306,10 → × 8 horas = **3.490.448,82**
4. Costo directo al peso: **$3.490.449**
5. Tarifa + AyS 8 %: 3.490.448,82 × 1,08 = 3.769.684,73 → **$3.769.685**
6. IVA: 3.769.685 × 10 % × 19 % = **$71.624** → Total **$3.841.309**

**24 horas todos los días, con arma (4 hombres):**

1. Base del servicio: 17.876.740,05 + 900 × 4 = 17.880.340,05
2. Tarifa + AyS 10 %: × 1,10 = 19.668.374,06 → **$19.668.374**
3. IVA: **$373.699** → Total **$20.042.073**

## 4. Valores corregidos de los 15 servicios frecuentes

Período 15 jul – 31 dic 2026, prima de $900 por hombre, empresa de vigilancia (no cooperativa). "Total antes" es lo que calculaba la versión anterior.

### Sin arma (AyS 8 %)

| Servicio | Hombres | Costo directo | Tarifa (base + AyS) | Total con IVA (corregido) | Total antes | Diferencia |
|---|---:|---:|---:|---:|---:|---:|
| 24 h todos los días (24/7) | 4 | $17.880.340 | $19.310.767 | **$19.677.672** | $19.676.681 | +$991 |
| 24 h lunes a viernes | 3 | $11.919.627 | $12.873.197 | **$13.117.788** | $13.117.788 | $0 |
| 24 h lunes a sábado | 4 | $14.304.272 | $15.448.614 | **$15.742.138** | $15.741.345 | +$793 |
| 12 h diurnas todos los días | 2 | $7.853.905 | $8.482.218 | **$8.643.380** | $8.643.814 | −$434 |
| 12 h nocturnas todos los días | 2 | $10.024.635 | $10.826.606 | **$11.032.312** | $11.032.867 | −$555 |
| 12 h diurnas L–V | 2 | $5.235.937 | $5.654.812 | **$5.762.253** | $5.762.543 | −$290 |
| 12 h nocturnas L–V | 2 | $6.683.090 | $7.217.737 | **$7.354.874** | $7.355.244 | −$370 |
| 12 h diurnas L–S | 2 | $6.283.124 | $6.785.774 | **$6.914.704** | $6.915.051 | −$347 |
| 12 h nocturnas L–S | 2 | $8.019.708 | $8.661.285 | **$8.825.849** | $8.826.294 | −$445 |
| 12 h diurnas L–V + 4 h sábado | 2 | $5.584.999 | $6.031.799 | **$6.146.403** | $6.146.712 | −$309 |
| 8 h diurnas L–V | 1 | $3.490.449 | $3.769.685 | **$3.841.309** | $3.841.695 | −$386 |
| 8 h nocturnas L–V | 1 | $4.542.871 | $4.906.301 | **$4.999.521** | $5.000.023 | −$502 |
| 8 h diurnas L–S | 2 | $4.188.749 | $4.523.849 | **$4.609.802** | $4.610.035 | −$233 |
| 8 h nocturnas L–S | 2 | $5.451.719 | $5.887.857 | **$5.999.726** | $6.000.029 | −$303 |
| 16 h diurnas/mixtas todos los días | 3 | $11.064.448 | $11.949.603 | **$12.176.645** | $12.176.646 | −$1 |

### Con arma (AyS 10 %)

| Servicio | Hombres | Costo directo | Tarifa (base + AyS) | Total con IVA (corregido) | Total antes | Diferencia |
|---|---:|---:|---:|---:|---:|---:|
| 24 h todos los días (24/7) | 4 | $17.880.340 | $19.668.374 | **$20.042.073** | $20.041.064 | +$1.009 |
| 24 h lunes a viernes | 3 | $11.919.627 | $13.111.589 | **$13.360.709** | $13.360.710 | −$1 |
| 24 h lunes a sábado | 4 | $14.304.272 | $15.734.699 | **$16.033.658** | $16.032.851 | +$807 |
| 12 h diurnas todos los días | 2 | $7.853.905 | $8.639.296 | **$8.803.443** | $8.803.885 | −$442 |
| 12 h nocturnas todos los días | 2 | $10.024.635 | $11.027.098 | **$11.236.613** | $11.237.179 | −$566 |
| 12 h diurnas L–V | 2 | $5.235.937 | $5.759.530 | **$5.868.961** | $5.869.257 | −$296 |
| 12 h nocturnas L–V | 2 | $6.683.090 | $7.351.399 | **$7.491.076** | $7.491.453 | −$377 |
| 12 h diurnas L–S | 2 | $6.283.124 | $6.911.437 | **$7.042.754** | $7.043.108 | −$354 |
| 12 h nocturnas L–S | 2 | $8.019.708 | $8.821.679 | **$8.989.291** | $8.989.743 | −$452 |
| 12 h diurnas L–V + 4 h sábado | 2 | $5.584.999 | $6.143.499 | **$6.260.225** | $6.260.540 | −$315 |
| 8 h diurnas L–V | 1 | $3.490.449 | $3.839.494 | **$3.912.444** | $3.912.838 | −$394 |
| 8 h nocturnas L–V | 1 | $4.542.871 | $4.997.158 | **$5.092.104** | $5.092.617 | −$513 |
| 8 h diurnas L–S | 2 | $4.188.749 | $4.607.624 | **$4.695.169** | $4.695.405 | −$236 |
| 8 h nocturnas L–S | 2 | $5.451.719 | $5.996.891 | **$6.110.832** | $6.111.140 | −$308 |
| 16 h diurnas/mixtas todos los días | 3 | $11.064.448 | $12.170.892 | **$12.402.139** | $12.402.140 | −$1 |

### Residencial estratos 4, 5 y 6 sin arma: el desfase grande

La versión anterior no distinguía el tipo de cliente y aplicaba el 8 % de la modalidad sin arma. La circular fija 10 %, así que **el tarifador cobraba por debajo del mínimo legal**:

| Servicio | Total correcto (AyS 10 %) | Lo que cobraba el tarifador (AyS 8 %) | Faltante por mes |
|---|---:|---:|---:|
| 24 h todos los días (24/7) | **$20.042.073** | $19.676.681 | +$365.392 |
| 24 h lunes a viernes | **$13.360.709** | $13.117.788 | +$242.921 |
| 24 h lunes a sábado | **$16.033.658** | $15.741.345 | +$292.313 |
| 12 h diurnas todos los días | **$8.803.443** | $8.643.814 | +$159.629 |
| 12 h nocturnas todos los días | **$11.236.613** | $11.032.867 | +$203.746 |
| 12 h diurnas L–V | **$5.868.961** | $5.762.543 | +$106.418 |
| 12 h nocturnas L–V | **$7.491.076** | $7.355.244 | +$135.832 |
| 12 h diurnas L–S | **$7.042.754** | $6.915.051 | +$127.703 |
| 12 h nocturnas L–S | **$8.989.291** | $8.826.294 | +$162.997 |
| 12 h diurnas L–V + 4 h sábado | **$6.260.225** | $6.146.712 | +$113.513 |
| 8 h diurnas L–V | **$3.912.444** | $3.841.695 | +$70.749 |
| 8 h nocturnas L–V | **$5.092.104** | $5.000.023 | +$92.081 |
| 8 h diurnas L–S | **$4.695.169** | $4.610.035 | +$85.134 |
| 8 h nocturnas L–S | **$6.110.832** | $6.000.029 | +$110.803 |
| 16 h diurnas/mixtas todos los días | **$12.402.139** | $12.176.646 | +$225.493 |

## 5. Cómo se verificó

Se escribió un cálculo independiente de la fórmula literal de la circular (sección 1) y se comparó contra la página en 120 casos:

- 15 servicios frecuentes.
- 4 combinaciones: sin arma, con arma, canino y residencial 4-6.
- 2 períodos: 1 ene – 30 jun y 15 jul – 31 dic.

**Diferencia máxima: $0** en costo directo, tarifa y total.

## 6. Lo que la empresa debe confirmar

- **Valor individual de la prima del seguro de vida** que cobra la aseguradora. En el tarifador está en $900 y se cambia en el cotizador.
- **Número de hombres** asignados a cada puesto, si difiere del automático.
- **Cooperativa:** si la empresa lo fuera, marcarlo en Parámetros para habilitar el descuento de hasta 10 %.

# **Propuestas de Proyecto para Hackatón Interledger**

Este documento detalla las tres alternativas de proyecto evaluadas para participar en la hackatón de Interledger (ILF). Cada propuesta incluye la problemática, la solución planteada, fortalezas, debilidades, el modelo de funcionamiento sobre la red Open Payments y las características clave para la demostración en vivo.

## **Opción 1: SoftPOS para Vendedores Informales (Cobro Digital Instantáneo)**

### **1\. Problemática**

En Latinoamérica y Colombia, más del 80% de los micronegocios y comerciantes informales dependen del efectivo. Cuando un cliente no lleva dinero físico, la venta se pierde. Los datáfonos tradicionales y las pasarelas bancarias locales cobran arriendos mensuales, retienen comisiones del 2.5% al 3.5% y liquidan el dinero en 24 a 48 horas, lo cual ahoga el flujo de caja diario del comerciante.

### **2\. Solución Propuesta**

Una aplicación móvil que transforma cualquier smartphone de gama baja en un datáfono virtual (SoftPOS) sin necesidad de hardware adicional. El vendedor digita el monto a cobrar y genera un cobro digital transmitido por código QR dinámico o mediante proximidad NFC (tecnología NDEF). El comprador acerca su teléfono o escanea el código desde cualquier billetera compatible con Interledger, liquidando el dinero en menos de 200 milisegundos directamente de cuenta a cuenta.

### **3\. Puntos Fuertes y Débiles**

* **Puntos Fuertes:**  
  * **Cero costo de entrada:** No requiere adquirir datáfonos ni pagar arriendos.  
  * **Demostración muy visual:** El flujo físico de acercar dos teléfonos por NFC o escanear el QR es sumamente tangible para los jueces.  
  * **Impacto social directo:** Resuelve la pérdida de ventas en la economía informal urbana.  
* **Puntos Débiles:**  
  * **Riesgo en la presentación en vivo:** Posibles fallas de conectividad a Internet o lectura de antena NFC durante los 3 minutos del pitch.  
  * **Valor diferenciador moderado:** Muchas fintechs locales ofrecen cobros con QR; el valor radica únicamente en la velocidad/costos de Interledger.

### **4\. Modelo del Producto**

1. **Creación de la solicitud:** La app del vendedor invoca la API de Open Payments para crear un Incoming Payment vinculado al *Payment Pointer* del vendedor.  
2. **Transmisión del cobro:** La URL única de la solicitud de pago se transmite por NFC o QR dinámico.  
3. **Autorización y Pago:** La billetera del comprador procesa la solicitud mediante el flujo de autorización GNAP (*Grant Negotiation and Authorization Protocol*).  
4. **Confirmación:** La app del vendedor recibe un webhook/evento en tiempo real e informa la transacción aprobada.

### **5\. Características Clave para Hacer Brillar la Demo**

* **Cobro Simulado en Vivo:** Realizar un cobro real en el escenario (ej. \$5,000 COP por un café) mostrando la recepción instantánea del dinero en la pantalla del vendedor.  
* **Lectura NFC Instantánea:** Pasar un segundo teléfono por la parte trasera del dispositivo del vendedor para disparar el flujo de pago en un solo toque.

## **Opción 2: Crowdfunding Humanitario Transparente y Sin Custodia**

### **1\. Problemática**

Durante emergencias o desastres naturales, la ayuda internacional sufre de alta fricción: las transferencias SWIFT tardan de 3 a 5 días hábiles en llegar a las ONG locales, y entre el 5% y el 10% del dinero se destruye en tarifas de procesamiento bancario y cambio de divisa. Además, existe opacidad sobre cómo y cuándo llegan los fondos a las entidades de socorro en el terreno.

### **2\. Solución Propuesta**

Una plataforma global de respuesta humanitaria que mapea crisis por país y conecta donantes de cualquier parte del mundo directamente con los *Payment Pointers* oficiales de entidades verificadas (Cruz Roja, Bomberos, Defensa Civil). Al funcionar 100% sobre Open Payments, la plataforma opera bajo un modelo **sin custodia (non-custodial)**: el dinero nunca pasa por la plataforma, sino que viaja en milisegundos directamente de la billetera del donante a la ONG local con costos menores al 0.5%.

### **3\. Puntos Fuertes y Débiles**

* **Puntos Fuertes:**  
  * **Alineación directa con ILF:** Abraza de lleno la misión de inclusión social, equidad financiera e impacto global de la Interledger Foundation.  
  * **Demostración de capacidades avanzadas de ILP:** Permite implementar *Split Payments* para distribuir donaciones a múltiples entidades de socorro en un solo clic y de manera transparente.  
  * **Bajo riesgo técnico en vivo:** Es un flujo 100% web/app sin dependencia de hardware físico.  
* **Puntos Débiles:**  
  * **Menor impacto visual en escenario:** Al ser un flujo digital en pantalla, puede sentirse más abstracto que la interacción física de un datáfono.

### **4\. Modelo del Producto**

1. **Directorio Verificado:** La plataforma despliega mapas y causas humanitarias activas agrupadas por país y validadas mediante entidades oficiales.  
2. **Donación Directa (No-custodial):** Al hacer clic en "Donar", la plataforma inicia una llamada a la API de Open Payments conectando la billetera del usuario con la cuenta destino de la entidad oficial sin que la plataforma toque el dinero.  
3. **Split Automático Multientidad:** Si el usuario dona a una causa general (ej. "Terremoto en Colombia"), la API distribuye automáticamente el monto (ej. 50% Cruz Roja, 30% Defensa Civil, 20% Bomberos) a las cuentas de distintas entidades en una sola transacción.  
4. **Trazabilidad Pública:** Registro público e inmutable del flujo de dinero ingresando a la causa en tiempo real.

### **5\. Características Clave para Hacer Brillar la Demo**

* **Donación Multientidad en Vivo (Split Payments):** Realizar una sola donación desde la plataforma y mostrar en pantalla cómo el monto se divide e ingresa instantáneamente a las billeteras de dos ONG distintas.  
* **Visualización de Transferencia Transfronteriza:** Demostrar cómo una donación hecha en USD o EUR llega a la cuenta de la ONG local en moneda nacional en menos de un segundo y sin retenciones bancarias.

## **Opción 3: SoftPOS \+ Scoring Crediticio Alternativo (Propuesta Recomendada)**

### **1\. Problemática**

Aceptar pagos digitales no soluciona el problema de fondo del comerciante informal: la **falta de capital de trabajo**. Al no tener historial bancario, extractos o registros formales, las entidades financieras tradicionales no les otorgan préstamos. Esto obliga a los comerciantes a acudir a prestamistas informales o usureros ("gota a gota"), donde pagan tasas de interés exorbitantes (20% a 30% mensual) que destruyen sus ingresos.

### **2\. Solución Propuesta**

Una plataforma integral que convierte el celular del vendedor en un SoftPOS y utiliza el registro de sus ventas diarias sobre Interledger para construir un **historial crediticio alternativo basado en flujo de caja real (Cash-Flow Based Scoring)**. Al acumular un historial de ventas auditable mediante la red, la plataforma le pre-aprueba microcréditos de capital de trabajo y descuenta el pago de las cuotas de forma automática e indolora: restando un pequeño porcentaje (ej. 5%) de cada venta futura mediante la función *Split Payments* de Open Payments.

### **3\. Puntos Fuertes y Débiles**

* **Puntos Fuertes:**  
  * **Propuesta de valor completa:** Ataca la aceptación de pagos Y la bancarización/crecimiento del negocio en una sola app.  
  * **Uso maestro de Open Payments:** Demuestra la velocidad de cobro \+ la capacidad de hacer *splits* automáticos para el cobro del microcrédito.  
  * **Modelo de negocio sostenible:** Define claramente cómo la plataforma genera ingresos e inclusión financiera al mismo tiempo.  
* **Puntos Débiles:**  
  * **Mayor alcance de desarrollo:** Requiere programar la interfaz de cobro (SoftPOS) y el módulo/panel de gestión del crédito.

### **4\. Modelo del Producto**

1. **Cobro y Captura de Datos:** El vendedor procesa sus ventas diarias en la app con QR/NFC a través de Interledger.  
2. **Motor de Scoring:** La plataforma analiza variables en tiempo real: volumen semanal, frecuencia de cobro, consistencia y ticket promedio.  
3. **Desembolso del Microcrédito:** Cuando el score alcanza el umbral, la plataforma libera un microcrédito directamente a la billetera ILP del comerciante.  
4. **Amortización Indolora (Automatic Split):** La API de Open Payments intercepta cada venta futura: si el cliente paga \$10,000 COP, el sistema envía \$9,500 COP al vendedor y \$500 COP a la amortización de su crédito de forma transparente.

### **5\. Características Clave para Hacer Brillar la Demo**

* **Evolución del Score en Tiempo Real:** Realizar 2 o 3 cobros simbólicos durante el pitch y mostrar cómo la gráfica del score crediticio del vendedor sube en pantalla con cada venta.  
* **Desembolso y Retorno Automático:** Pre-aprobar un crédito en vivo y mostrar cómo al realizar la siguiente venta, el dinero se divide automáticamente entre el comercio y la cuota del préstamo.

## **Cuadro Comparativo Detallado**

| Criterio de Evaluación | 📱 Opción 1: SoftPOS Básico | 🌍 Opción 2: Crowdfunding Humanitario | 📈 Opción 3: SoftPOS \+ Credit Scoring |
| :---- | :---- | :---- | :---- |
| **Problema Principal que Resuelve** | Pérdida de ventas por falta de efectivo o datáfono. | Lentitud, opacidad y comisiones en ayuda humanitaria internacional. | **Exclusión financiera, falta de capital y usura ("gota a gota").** |
| **Público Objetivo** | Vendedores informales y micronegocios locales. | Donantes globales y ONG/Entidades de socorro. | **Vendedores informales que necesitan hacer crecer su negocio.** |
| **Alineación con la Filosofía ILF** | Alta (Inclusión financiera urbana). | Máxima (Impacto social y equidad global). | **Máxima (Inclusión financiera integral y empoderamiento económico).** |
| **Uso de Capacidades de Open Payments** | Medio (Llamadas a Incoming Payment y velocidad de 200 ms). | Alto (*No-custodial*, liquidez transfronteriza y *Split Payments*). | **Máximo (Velocidad \+ Registro de transacciones \+ *Split Payments* automáticos).** |
| **Atractivo del Modelo de Negocio** | Bajo (Difícil cobrar comisiones a vendedores informales). | Medio (Basado en donaciones o comisiones mínimas opcionales). | **Alto (Monetización clara mediante el margen de los microcréditos).** |
| **Impacto e Innovación Percibida** | Incremental (Ya existen cobros por QR). | Alto (Resuelve la opacidad del crowdfunding tradicional). | **Muy Alto (Abre la puerta al crédito formal mediante datos de pago).** |
| **Efecto "WOW" en el Pitch / Demo** | Alto (Interacción física con el teléfono). | Medio-Alto (Donación directa multientidad e impacto global). | **Máximo (Visualización de cobro \+ aprobación de crédito en vivo).** |
| **Complejidad de Desarrollo (24h)** | Media (Hardware NFC/QR \+ API básica). | Media (APIs de Open Payments \+ Frontend web). | **Media-Alta (Requiere lógica de cobro \+ motor de score simulado).** |


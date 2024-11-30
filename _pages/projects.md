---
layout: page
title: Contexto
permalink: /projects/
nav: true
nav_order: 3
---

<div class="py-5">
  <h1 class="mb-5">Contexto</h1>

  <hr class="mb-5">

  <section class="mb-5">
    <h2 class="mb-4">Datos y Variables</h2>
    <p class="mb-4">A continuación, se detalla la estructura y relevancia de las fuentes de datos utilizadas:</p>


    <h3 class="mt-4 mb-3">👨‍👩‍👧‍👦 Población Beneficiaria Diciembre 2023 (Fonasa) <code>beneficiarios_df</code></h3>
    <p class="mb-2"><strong>Descripción:</strong> Este conjunto de datos contiene información demográfica detallada sobre los beneficiarios de Fonasa en 2023.</p>
    <p class="mb-2"><strong>Variables Clave:</strong></p>
    <ul class="mb-4">
      <li>👩‍⚕️ SEXO: Género de los beneficiarios.</li>
      <li>📅 EDAD_TRAMO: Rango etario.</li>
      <li>👤 TITULAR_CARGA: Relación con el titular del sistema.</li>
      <li>🌎 NACIONALIDAD: Nacionalidad de los beneficiarios.</li>
    </ul>
    <p class="mb-2">🌐 <strong>Cobertura:</strong> Incluye datos de todas las regiones de Chile, con más de 10 millones de registros, permitiendo un análisis nacional y granular.</p>
    <p class="mb-4">📊 <strong>Aplicaciones:</strong> Analizar la composición demográfica de los beneficiarios y su distribución geográfica.</p>

    <hr class="mb-2">

    <h3 class="mt-4 mb-3">📋 Modalidad Libre Elección Diciembre 2023 <code>mle_2023_df</code></h3>
    <p class="mb-2"><strong>Descripción:</strong> Este conjunto de datos detalla el uso de prestaciones bajo la modalidad de libre elección en el sistema Fonasa.</p>
    <p class="mb-2"><strong>Variables Clave:</strong></p>
    <ul class="mb-4">
      <li>📆 MES_EMISION: Mes de emisión de la prestación.</li>
      <li>🆔 CODIGO_PRESTACION: Código asignado a cada tipo de prestación.</li>
      <li>📑 DESC_SECCION: Descripción de la sección correspondiente.</li>
      <li>📋 DESC_ITEM: Detalle del ítem relacionado con la prestación.</li>
      <li>📍 REGION_EMISION / COMUNA_EMISION: Ubicación geográfica de la emisión.</li>
    </ul>
    <p class="mb-4">📊 <strong>Aplicaciones:</strong> Estudio del acceso y uso de prestaciones por región y comuna, evaluando patrones y posibles desigualdades.</p>
  </section>

  <hr class="mb-2">

  <section class="mb-5">
    <h2 class="mb-4">💾 Tamaño y Accesibilidad</h2>
    <p class="mb-4">
      🔗 Ambos conjuntos están disponibles en formato CSV desde el portal de Fonasa:  
      <a href="https://www.fonasa.cl/sites/fonasa/datos-abiertos/estadisticas-anuales" target="_blank">https://www.fonasa.cl/sites/fonasa/datos-abiertos/estadisticas-anuales</a>.
    </p>
    <p class="mb-4">Estos archivos, con un tamaño conjunto superior a 10 GB, aseguran un nivel de detalle elevado.</p>
    <p class="mb-4">Además, se dispone de un conjunto de datos complementario que detalla los códigos de prestación, clave para interpretar los registros de la segunda fuente. Disponible en el siguiente enlace:  
      <a href="https://www.fonasa.cl/sites/fonasa/prestadores/modalidad-libre-eleccion#normativa-y-arancel-modalidad-libre-eleccin--mle-" target="_blank">
        Normativa y Arancel Modalidad Libre Elección
      </a>.
    </p>
  </section>

  <hr class="mb-2">

  <section>
    <h2 class="mb-4">🧠 Conceptos Importantes a Recordar</h2>
    <ul class="mb-5">
      <li>🩺 <strong>Prestaciones:</strong> Servicios, compensaciones o indemnizaciones que FONASA ofrece a sus asegurados ante un evento cubierto por la póliza.</li>
      <li>🏥 <strong>Modalidad Libre Elección (MLE):</strong> Una de las dos modalidades de atención otorgadas por FONASA, donde el beneficiario elige libremente al profesional o entidad de salud, del sector público o privado.</li>
      <li>💵 <strong>Arancel MLE:</strong> Cada prestación cuenta con un valor referencial, que determina tanto la bonificación financiada por FONASA como los pagos que debe realizar el beneficiario (copago).</li>
      <li>
        📊 <strong>Tramos de FONASA:</strong>  
        <ul class="mt-2">
          <li>Tramo A: Sin ingresos; acceso gratuito a servicios públicos.</li>
          <li>Tramos B, C y D: Divididos según ingresos, afectando los aranceles. Información detallada en <code>\data\originales\2 Planilla MLE 2023.xlsx</code>.</li>
        </ul>
      </li>
    </ul>
  </section>
</div>

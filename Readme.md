# Repubblica.it Scraper

Este es un scraper creado para extraer datos de noticias exclusivas para suscriptores de la página [Repubblica](https://www.repubblica.it/), más específicamente de la sección [de búsqueda de noticias](https://ricerca.repubblica.it/ricerca/).

El proyecto fue originalmente desarrollado para un investigador de alto rango en el campo de la ciencia de datos, quien me otorgó el permiso para compartirlo en este repositorio. El objetivo principal es demostrar cómo es posible acceder a datos sin necesidad de recurrir a recursos de pago, como proxies o servicios API, usando únicamente patrones de análisis e ingeniería aplicados al contenido web.

## Características

- **Web Scraping**: Extracción de noticias que están detrás de una barrera de suscripción.
- **Data Cleaning**: Limpieza y estructuración de los datos obtenidos para un formato legible y útil.
- **Exportación a CSV**: Los resultados se guardan en un archivo CSV dentro de la carpeta `Output` (se genera automáticamente).
- **Uso de BeautifulSoup y lxml**: Estas herramientas se utilizan para el raspado y análisis de las páginas HTML.

## Objetivos

- **Sin herramientas de pago**: El proyecto ha sido desarrollado sin el uso de proxies o servicios de almacenamiento externos, lo que demuestra la eficiencia y potencial de técnicas avanzadas de scraping.
- **Investigación**: El propósito de este proyecto es puramente académico y de investigación.
  
## Mejoras potenciales

Este proyecto, aunque fue desarrollado sin el uso de recursos de pago, tiene un gran potencial para expandirse utilizando:

- Proxies pagados para eludir restricciones de IP.
- Inyección de queries a bases de datos locales o remotas para almacenar la información.
- Mayor escalabilidad para manejar grandes volúmenes de datos.

## Advertencia Ética

Este proyecto podría romper ciertas cláusulas éticas en cuanto a scraping de contenido restringido. El único fin de este repositorio es contribuir a la investigación en scraping y manejo de datos. Si cualquier persona con autoridad en la página solicita el cierre de este proyecto, el repositorio será eliminado de inmediato.

No recomiendo el uso de este código con fines comerciales o malintencionados. Este proyecto es solo para fines educativos y de investigación. Por favor, ten en cuenta que extraer contenido protegido por restricciones de acceso puede infringir los términos de uso de los sitios web.

## Instalación

1. Clona este repositorio en tu máquina local:
    ```bash
    git clone https://github.com/tu-usuario/nombre-del-repositorio.git
    ```

2. Navega al directorio del proyecto:
    ```bash
    cd nombre-del-repositorio
    ```

3. Crea y activa un entorno virtual:
    ```bash
    python -m venv venv
    source venv/bin/activate # En Windows: venv\Scripts\activate
    ```

4. Instala las dependencias:
    ```bash
    pip install -r requirements.txt
    ```

## Uso

El scraper está diseñado para obtener el contenido de las noticias de la página [La Repubblica](https://www.repubblica.it/), específicamente de los artículos disponibles para suscriptores.

Para usar el scraper, debes ejecutar la función `main` en el archivo `src/run_scraper.ipynb` con los siguientes parámetros:
Los datos raspados serán exportados en formato CSV a la carpeta `Output`.

1. **Primer parámetro:** Palabra clave o frase que deseas buscar. Si buscas una frase, puedes usar espacios.
2. **Segundo parámetro:** Fecha de inicio de la búsqueda (en formato `YYYY-MM-DD`).
3. **Tercer parámetro:** Fecha de fin de la búsqueda (en formato `YYYY-MM-DD`).
4. **Cuarto parámetro:** Modalidad de la búsqueda, que puede ser:
    - `all`: para buscar todas las palabras clave.
    - `phrase`: para buscar la frase exacta.
    - `any`: para buscar cualquier palabra de la frase.

   **Recomendación:** Usa la modalidad `any` para obtener más resultados.

Ejemplo de ejecución en Jupyter Notebook:

```python
# src/run_scraper.ipynb

main("cambio climático", "2023-01-01", "2023-06-30", "any")
```

## Disclaimer

Este proyecto está destinado únicamente a investigación y aprendizaje. Si crees que este repositorio viola alguna política, no dudes en comunicarlo. Será cerrado y eliminado si es necesario.

---

### Contacto

Si deseas comunicarte conmigo, puedes hacerlo a través de [raulsedanomolina@gmail.com](mailto:raulsedanomolina@gmail.com)

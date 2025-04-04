# Interfaces de Hardware y Software

## Trabajo 1: HMI for Signal Processing

## Descripción

El proyecto implementa el procesamiento de señales de audio mediante filtros digitales. En esta tarea, se desarrolló una interfaz para la manipulación de señales, permitiendo la aplicación de filtros pasa bajos, pasa altos y pasa banda. Además, se visualiza la señal tanto en el dominio del tiempo como en la frecuencia utilizando la Transformada de Fourier. También se permite guardar el audio filtrado.

## Requisitos

Para ejecutar el proyecto, necesitas tener Python 3.10 instalado. Luego, instala las siguientes dependencias ejecutando el siguiente comando:
```bash
pip install gradio librosa matplotlib numpy scipy soundfile
```

Estas son las bibliotecas necesarias para ejecutar el proyecto:

- **gradio**: Para la interfaz gráfica de usuario.
- **librosa**: Para el procesamiento y análisis de archivos de audio.
- **matplotlib**: Para la visualización de las señales.
- **numpy**: Para el manejo de arrays y cálculos matemáticos.
- **scipy**: Para la aplicación de filtros digitales.
- **soundfile**: Para guardar los archivos de audio filtrados.

## Estructura del código

El código principal está contenido en el archivo `hmi_signal_processing.py` y se organiza en las siguientes funciones:

- **`load_audio(file)`**: Carga un archivo de audio y lo convierte a un array numpy mono.

- **`apply_filter(y, sr, filter_type, cutoff, order)`**: Aplica un filtro digital a la señal de audio.

- **`compute_fourier(y, sr)`**: Calcula la Transformada de Fourier de la señal.

- **`plot_signal(y, sr, title)`**: Genera y guarda una gráfica de la señal en el dominio del tiempo.

- **`plot_fourier(y, sr, title)`**: Genera y guarda la Transformada de Fourier de la señal.

- **`process_audio(file, filter_type, cutoff, order, apply_fourier)`**: Procesa el audio aplicando el filtro y generando las gráficas.

- **`create_interface()`**: Crea la interfaz gráfica con Gradio.

## Uso

1. **Cargar o grabar un archivo de audio**: Selecciona un archivo de audio para cargar desde tu dispositivo o grabarlo en tiempo real dentro de la interfaz.
2. **Seleccionar el filtro**: Elige entre los filtros `Lowpass`, `Highpass` o `Bandpass`.
3. **Ajustar frecuencias de corte**: Configura las frecuencias de corte según el tipo de filtro seleccionado.
4. **Procesar**: Haz clic en "Procesar" para aplicar el filtro y generar las gráficas de la señal.
5. **Visualización**:
   - Se visualizarán las gráficas en el dominio del tiempo de la señal original y filtrada.
   - Tienes la opción de visualizar la Transformada de Fourier de la señal original y filtrada mediante un checkbox.
6. **Descargar**: El audio filtrado y las gráficas generadas se pueden descargar directamente desde la interfaz.

## Ejemplo de ejecución

Para ejecutar el proyecto, primero descarga el código del repositorio. Luego, abre el archivo en un IDE como **VS Code**.

Cuando ejecutes el código, Gradio generará una URL en la terminal, que podrás abrir en tu navegador para acceder a la interfaz de usuario. Desde allí, podrás cargar un archivo de audio, aplicar los filtros, visualizar las transformadas de Fourier y descargar el audio filtrado y las gráficas.

Este proceso no requiere escribir comandos en la terminal una vez que el proyecto está configurado. Simplemente abre el código en tu IDE y corre el script, y la interfaz web se abrirá automáticamente.

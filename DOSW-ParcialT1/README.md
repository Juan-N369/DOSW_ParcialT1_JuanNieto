# DOSW_ParcialT1_JuanNieto.

## Requerimientos

#### Funcionales

- Los solicitantes deben poder pedir tutorias indicando una preferencia de tutor.
- Los solicitantes deben poder solicitar el perfil de un tutor.
- Los profesores y estudiantes de posgrado deben poder registrarse como tutor, siguiendo sus respectivas reglas.

#### No funcionales

- El diseño de la interfaz debe incorparar la indentidad visual institucional, con la paleta de colores del programa de sistemas.
- Debe emplear una tipografia legible con los estandares minimos de contraste y accesibilidad web(WCAG 2.1 Nivel AA) para facilitar lectura de horarios de tutoria y perfiles de tutores.

### Historias de Usuario

|**Funcionalidad**|**Historia de Usuario**|**Criterios de aceptacion**|
|:---:|---|---|
|**Solicitar tutoria segun la preferencia**|COMO estudiante de pregrado, QUIERO solicitar una tutoria indicando mi preferencia de tutor (profesor o estudiante de posgrado), para que el sistema me asigne el mejor tutor disponible.|Debe retornar un tutor asignado basandose en 3 preferencias de busqueda:<br>1. **FASTEST_AVAILABLE**: El usuario quiere la tutoría lo antes posible. Se descartan tutores no disponibles y se selecciona el que tenga el horario libre más próximo, sin importar si es profesor o posgrado.<br>2. **EXPERT_FIRST**: Prioriza profesores. Se busca primero en la lista de profesores de esa materia; si hay disponibles, se asigna el más próximo. Si no hay profesores disponibles, se busca entre los estudiantes de posgrado.<br>3. **PEER_TUTORING**: El estudiante prefiere aprender de otro estudiante. Se descartan los profesores por completo y se selecciona el estudiante de posgrado disponible qupertenezca al mismo programa académico del solicitante.|
|**Visualizar el perfil de un tutor**|COMO estudiante de pregrado QUIERO Visualizar el perfil de un tutor indicado PARA PODER determinar sus capacidades y determinar si estoy conforme con mi asignacion.| Debe retornar un String que muestre: <br>O. Nombre del tutor.<br>O. Materias que pueden tratar.<br>O. Carreras de la que pueden hablar. |
|Registrarse como tutor|COMO estudiante de posgrado QUIERO registrarme como tutor segun PARA PODER dar tutorias a los estudiante que los neseciten segun mis materias y mis programas academicos|Debe quedar en guardado en el sistema, con su nombre, materias a tratar y programas academicos que puede tratar.|
|Registrarse como tutor|COMO Profesor QUIERO registrarme como tutor segun PARA PODER dar tutorias a los estudiante que los neseciten segun mis materias|Debe quedar en guardado en el sistema, con su nombre, materias asignadas.|

### Diagrama de casos de uso

![alt text](<docs/images/UseCase Diagram.png>)
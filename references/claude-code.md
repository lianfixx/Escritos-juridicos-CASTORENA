# Trabajo en Claude Code

Leer al trabajar esta skill en Claude Code. No cambia el método: las reglas de [SKILL.md](../SKILL.md) y de las demás referencias siguen mandando.

## Frenos activos (hooks)

Configurados en `.claude/` de este repositorio:

1. Preguntar antes de enviar, responder, reenviar o publicar por conectores.
2. Preguntar antes de sobrescribir un `.docx` o `.pdf` ya existente, porque puede ser un original revisado.
3. Antes de cada commit, buscar secretos y datos personales en el diff.
4. Preguntar antes de `git push`; bloquear `git push --force`.
5. Si un commit cambia SKILL.md, comprobar que siga siendo compatible con claude.ai.

Sólo actúan en Claude Code dentro de este repositorio; no en claude.ai ni en otras IA. No sustituyen las reglas de la skill: un freno que no se dispara no autoriza enviar, presentar ni editar originales.

Las mismas reglas valen fuera de Claude Code: están en `ia/REGLAS.md` (generadas de `ia/politica.json`). Con terminal, `sh ia/instalar.sh` las activa como hooks de git para cualquier IA o persona, y GitHub revisa cada push con `registro-ia.yml`. En chat sin frenos (claude.ai, ChatGPT, Gemini), la IA las cumple por sí misma y entrega el registro pendiente. Además, todo commit sin entrada de registro con `Agente:` queda bloqueado.

## Plan y entrevista

Para escritos largos o auditorías completas, empezar en modo plan (Shift+Tab): leer, ubicar fuentes y proponer el plan sin tocar archivos. Pedir la entrevista sólo si falta un dato que cambie la solución y no está en los archivos. En encargos limitados (puntuación, ortografía, un fragmento), ir directo al trabajo.

Prompt para copiar:

```text
Antes de armar el plan, entrevístame. Hazme una pregunta a la vez, sólo sobre lo que falte y cambie la solución (materia, órgano, etapa, acto, objetivo, firmante, calidad procesal o plazo) y no esté en los archivos. No amplíes el alcance del encargo. Después muéstrame el plan.
```

## Reparto en paralelo

Para auditar un escrito extenso, preparar primero una sola ficha de hechos (dato, documento, ubicación y certeza) y pasarla a todos. Luego un subagente por dimensión:

- forma: ortografía, gramática, numeración y remisiones;
- hechos y cifras contra la fuente;
- fundamentos, vigencia y versión aplicable por fecha del acto;
- procedencia, plazo y cómputo, y personalidad.

Cada uno devuelve hallazgos clasificados y localizados, sin editar el escrito. Quien consolida elimina duplicados, prioriza lo que afecta procedencia, plazo o resultado, aplica los cambios y declara el estado. Ningún subagente envía, publica ni declara la revisión terminada.

## /goal

```text
/goal Seguir hasta que exista el escrito editable (y el estudio aplicado si corresponde), se hayan revisado todas las páginas renderizadas, cada hallazgo esté clasificado y localizado, los cambios rojos se hayan comprobado al aceptarlos y el estado diga «revisión terminada» o «listo para presentar» con sus pendientes. No enviar ni presentar nada.
```

## Navegador

Claude in Chrome usa tu Chrome con tus sesiones. Sirve para consultar fuentes oficiales que piden sesión o bloquean descargas automáticas, y para verificar la cédula profesional cuando el dato sea decisivo. Registrar la fuente como indica [fuentes](fuentes.md). Nunca usarlo para presentar, firmar ni eludir accesos.

## En la sesión

- `/context`: ver cuánto espacio ocupan el expediente y las referencias cargadas.
- `/compact <foco>`: resumir conservando la ficha de hechos y los hallazgos abiertos.
- `/clear`: empezar limpio al pasar a otro asunto, para no mezclar datos.
- `/rewind` (o Esc Esc): volver a un punto anterior si una edición tomó mal la base.
- `/btw`: preguntar algo al paso sin desviar la revisión.
- `!comando`: correr un comando directo, por ejemplo para renderizar páginas.

## Mejora continua

En Claude Code local, `/insights` ayuda a detectar patrones de uso y correcciones repetidas. Sus sugerencias son candidatas: se registran y clasifican conforme a [aprendizajes](aprendizajes.md), anonimizadas y sin generalizar casos, y sólo se persisten con autorización. Nunca son reglas automáticas.

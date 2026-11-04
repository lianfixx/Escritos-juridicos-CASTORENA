# Claude Code en este repositorio

- La skill `escritos-juridicos-castorena` es `SKILL.md` en la raíz de este repositorio; léela antes de redactar o auditar.
- Reglas comunes entre IA: `ia/REGLAS.md` y `ia/PROTOCOLO.md`. Frenos activos en `.claude/settings.json` → `ia/guard.py` (política en `ia/politica.json`, pruebas en `ia/test_guard.py`). Si un freno bloquea algo legítimo, explícaselo a Emi; no lo desactives ni lo rodees. Todo cambio se registra en el mismo commit con `Agente: Claude Code`.
- Reglas por tipo de archivo en `.claude/rules/` (se cargan solas al tocar esos archivos).
- Plan y entrevista, subagentes, `/goal` y demás trabajo en Claude Code: `references/claude-code.md`.

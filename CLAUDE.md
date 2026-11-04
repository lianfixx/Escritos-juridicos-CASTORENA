# Claude Code en este repositorio

- La skill `escritos-juridicos-castorena` es `SKILL.md` en la raíz de este repositorio; léela antes de redactar o auditar.
- Frenos activos en `.claude/settings.json` (política en `.claude/hooks/policy.json`, pruebas en `.claude/hooks/test_guard.py`). Si un freno bloquea algo legítimo, explícaselo a Emi; no lo desactives ni lo rodees.
- Reglas por tipo de archivo en `.claude/rules/` (se cargan solas al tocar esos archivos).
- Plan y entrevista, subagentes, `/goal` y demás trabajo en Claude Code: `references/claude-code.md`.

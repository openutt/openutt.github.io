## Qué cambia y por qué
(Qué problema resuelve o qué mejora trae. Si es un bug: cómo reproducirlo)

## Cómo probarlo
(Pasos para que quien revise reproduzca: comandos, página que tocar, qué debería verse)

## Checklist técnico
- [ ] El título sigue la convención (feat:, fix:, refactor:…)
- [ ] `hugo --gc --minify` compila sin errores (Hugo Extended ≥ 0.158)
- [ ] Revisado con `hugo server`: página afectada, en claro y en oscuro
- [ ] Si toca layouts o menú: probado en angosto (<640px) y ancho (≥640px)
- [ ] No se editaron `public/`, `resources/` ni `.hugo_build.lock` (son generados)
- [ ] Sin secretos en el diff ni en el workflow

## Alcance
- [ ] No mezcla cambios de rpoyectos (si trae, van aparte con `proyecto.md` o `mantenimiento.md`)

## Capturas (si hay cambio visual)

## Notas

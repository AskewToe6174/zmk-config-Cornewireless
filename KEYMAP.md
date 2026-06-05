# Keymap — Corne wireless

Mapa visual de las teclas y capas configuradas en este repo. Para detalles del código fuente ver [config/corne.keymap](config/corne.keymap).

## Cómo se activan las capas

El Corne tiene 3 capas. La que está activa depende de qué tecla del **pulgar** mantengas pulsada:

| Capa | Cómo activarla | Para qué sirve |
|---|---|---|
| `default` (capa 0) | Sin nada pulsado | Escribir normal (letras, espacio, enter) |
| `lower` (capa 1) | Mantén pulsada la tecla pulgar **izquierda** central (`LWR`) | Números, flechas, Bluetooth, volumen, multimedia |
| `raise` (capa 2) | Mantén pulsada la tecla pulgar **derecha** central (`RSE`) | Símbolos `! @ # $ % & * ( ) [ ] { } < > | \` |

Las capas son momentáneas: en cuanto sueltas `LWR` o `RSE`, vuelves al default.

## Esquema de la fila inferior (pulgares)

Las 6 teclas del pulgar — 3 en cada mitad:

```
       [ GUI ] [ LWR ] [ SPC ]    [ ENT ] [ RSE ] [ ALT ]
        (cmd)  (capa 1) (espacio)  (intro) (capa 2) (alt)
       └─── mitad izquierda ───┘  └─── mitad derecha ───┘
```

- **GUI** = tecla Cmd de Mac.
- **LWR** y **RSE** = activadores de capa (mantener pulsado).
- **SPC** y **ENT** = espacio y enter normales.
- **ALT** = tecla Option de Mac.

## Capa default (capa 0)

```
┌──────┬────┬────┬────┬────┬────┐    ┌────┬────┬────┬────┬────┬──────┐
│ TAB  │ Q  │ W  │ E  │ R  │ T  │    │ Y  │ U  │ I  │ O  │ P  │ BSPC │
├──────┼────┼────┼────┼────┼────┤    ├────┼────┼────┼────┼────┼──────┤
│ CTRL │ A  │ S  │ D  │ F  │ G  │    │ H  │ J  │ K  │ L  │ ;  │  '   │
├──────┼────┼────┼────┼────┼────┤    ├────┼────┼────┼────┼────┼──────┤
│ SHFT │ Z  │ X  │ C  │ V  │ B  │    │ N  │ M  │ ,  │ .  │ /  │ ESC  │
└──────┴────┴────┴────┼────┼────┤    ├────┼────┼────┴────┴────┴──────┘
                      │GUI │LWR │    │ENT │RSE │
                      └────┼────┤    ├────┼────┘
                           │SPC │    │ALT │
                           └────┘    └────┘
```

QWERTY estándar. Sin sorpresas.

## Capa lower (capa 1) — mantén `LWR`

Números, flechas, Bluetooth, volumen y multimedia.

```
┌──────┬────┬────┬────┬────┬────┐    ┌──────┬──────┬──────┬──────┬──────┬──────┐
│ TAB  │ 1  │ 2  │ 3  │ 4  │ 5  │    │  6   │  7   │  8   │  9   │  0   │ BSPC │
├──────┼────┼────┼────┼────┼────┤    ├──────┼──────┼──────┼──────┼──────┼──────┤
│BTCLR │BT1 │BT2 │BT3 │BT4 │BT5 │    │ LEFT │ DOWN │  UP  │ RIGHT│ VOL- │ VOL+ │
├──────┼────┼────┼────┼────┼────┤    ├──────┼──────┼──────┼──────┼──────┼──────┤
│ SHFT │    │    │    │    │    │    │ PREV │ PLAY │ NEXT │ MUTE │      │      │
└──────┴────┴────┴────┼────┼────┤    ├──────┼──────┴──────┴──────┴──────┴──────┘
                      │GUI │    │    │ ENT  │
                      └────┼────┤    ├──────┼─────┐
                           │SPC │    │ ALT  │     │
                           └────┘    └──────┴─────┘
```

### Bluetooth (mitad izquierda fila central)

| Tecla | Acción |
|---|---|
| `LWR` + `Q` (BTCLR) | **Borra** el perfil BT actual (úsalo si el Mac no quiere emparejar) |
| `LWR` + `A` (BT1) | Cambia al perfil BT **0** |
| `LWR` + `S` (BT2) | Cambia al perfil BT **1** |
| `LWR` + `D` (BT3) | Cambia al perfil BT **2** |
| `LWR` + `F` (BT4) | Cambia al perfil BT **3** |
| `LWR` + `G` (BT5) | Cambia al perfil BT **4** |

Permite emparejar hasta 5 dispositivos distintos y cambiar entre ellos.

### Flechas (mitad derecha fila central)

| Tecla | Acción |
|---|---|
| `LWR` + `H` | ← |
| `LWR` + `J` | ↓ |
| `LWR` + `K` | ↑ |
| `LWR` + `L` | → |

### Volumen y multimedia (añadido, mitad derecha)

| Tecla | Acción |
|---|---|
| `LWR` + `;` | **Bajar volumen** |
| `LWR` + `'` | **Subir volumen** |
| `LWR` + `N` | Pista anterior |
| `LWR` + `M` | Play / Pause |
| `LWR` + `,` | Pista siguiente |
| `LWR` + `.` | Mute |

## Capa raise (capa 2) — mantén `RSE`

Símbolos. Los superiores son shift+número, los inferiores son los símbolos típicos de programación.

```
┌──────┬────┬────┬────┬────┬────┐    ┌────┬────┬────┬────┬────┬──────┐
│ TAB  │ !  │ @  │ #  │ $  │ %  │    │ ^  │ &  │ *  │ (  │ )  │ BSPC │
├──────┼────┼────┼────┼────┼────┤    ├────┼────┼────┼────┼────┼──────┤
│ CTRL │    │    │    │    │    │    │ -  │ =  │ [  │ ]  │ \  │  `   │
├──────┼────┼────┼────┼────┼────┤    ├────┼────┼────┼────┼────┼──────┤
│ SHFT │    │    │    │    │    │    │ _  │ +  │ {  │ }  │ |  │  ~   │
└──────┴────┴────┴────┼────┼────┤    ├────┼────┼────┴────┴────┴──────┘
                      │GUI │    │    │ENT │    │
                      └────┼────┤    ├────┼────┘
                           │SPC │    │ALT │
                           └────┘    └────┘
```

## Cosas que NO están en el keymap (limitaciones conocidas)

- **No hay tap-dance, ni home row mods, ni combos.** El keymap es directo, una tecla = una acción.
- **No hay capa para emojis** ni layout extra (US es lo único).
- **Caps Lock** no está mapeado — para mayúsculas continuas hay que mantener Shift, o añadirlo en alguna capa si lo necesitas.
- **F1-F12** tampoco están — si las necesitas, hay sitio libre en `raise_layer` para añadirlas.

## OLED — qué muestra cada pantalla

| Mitad | Qué muestra |
|---|---|
| Izquierda (peripheral) | Estado BT, batería, animación bongo cat |
| Derecha (central, con USB) | Estado BT, batería, modificadores activos (símbolos macOS ⌃⇧⌥⌘), gato Luna reactivo a tu velocidad de tecleo |

Más detalle del módulo OLED en [mctechnology17/zmk-nice-oled](https://github.com/mctechnology17/zmk-nice-oled).

## Cómo cambiar el keymap

1. Edita [config/corne.keymap](config/corne.keymap).
2. Commit + push.
3. GitHub Actions compila los `.uf2` en ~3 min (mira en la pestaña Actions).
4. Descarga el zip de artifacts y flashea ambas mitades.

Referencia de códigos ZMK válidos para `&kp`: https://zmk.dev/docs/keymaps/list-of-keycodes

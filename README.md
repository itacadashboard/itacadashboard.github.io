# Ítaca · Centro de ejecución

App del equipo de Homeland para seguir los bootcamps del Programa Ítaca. Se instala en el celular o el computador y todos ven y editan los mismos datos.

- La app vive en GitHub Pages (estos archivos).
- Los datos y el login viven en Supabase.

## Montarla por primera vez

1. **Supabase.** Crea un proyecto en supabase.com. En *SQL Editor* pega todo `supabase/configurar.sql`, agrega los correos del equipo donde dice y dale *Run*.
2. **Usuarios.** En *Authentication > Users > Add user > Create new user* crea a cada persona con su correo y una contraseña, con *Auto Confirm User* marcado. En *Authentication > Sign In / Providers* apaga *Allow new users to sign up*.
3. **Conectar.** En *Project Settings > API* copia la *Project URL* y la *anon public key* y pégalas en `config.js`.
4. **GitHub.** Sube estos archivos a un repositorio. En *Settings > Pages* elige *Deploy from a branch*, rama `main`, carpeta `/ (root)`. En un par de minutos queda en `https://<usuario>.github.io/<repositorio>/`.

## Instalarla

- **iPhone (Safari):** abrir el enlace, Compartir, *Agregar a inicio*.
- **Android (Chrome):** abrir el enlace, menú ⋮, *Instalar app*.
- **Computador (Chrome o Edge):** abrir el enlace y tocar el ícono de instalar en la barra de direcciones.

## Agregar a alguien

1. Supabase > *Table Editor* > `equipo` > *Insert row* con su correo.
2. Supabase > *Authentication* > *Add user* con el mismo correo y una contraseña.

Para quitar a alguien, borra su fila en `equipo` y su usuario en *Authentication*.

## Cambiar la lista de encargados

En `index.html`, busca `const ENC=['Rafael','Cipriano','Ambar'];` y edítala.

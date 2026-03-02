# mermaidchartsandsvgdocu
This is a docu for creating and converting mermaid charts to svg

## Mermaid en Jekyll

- Crear `package.json` (si es que no esta creado) mediante el comando: `touch package.json`

- Ingresar `npm init -y`

- Instalar mermaid-cli mediante: `npm install --save-dev @mermaid-js/mermaid-cli`

- En caso de npm desactualizado, pues actualizar mediante: `npm install npm@latest`

- Crear carpeta `mkdir assets/mermaid`

### Convertir graficos de Mermaid a SVGs

1. Si se instalo globalmente: `mmdc -i mi-diagrama.mmd -o assets/images/mi-diagrama.svg`

2. Si se instalo local con npx (Recomendada si se siguieron los pasos anteriores): `npx mmdc -i assets/mermaid/mi-diagrama.md -o /assets/mermaid/mi-diagrama.svg`

### Ejemplo

#### Ejemplo 1


```markdown
flowchart TD
    subgraph Personajes
        n["Napoleón Bonaparte"]
        j["José de San Martín"]
        b["Simón Bolívar"]
    end
    
    subgraph Sucesos
        rev["Revolución Francesa"]
        ind["Independencias Latinoamericanas"]
        cong["Congreso de Viena"]
    end
    
    n -->|Participa en| rev
    rev -->|Inspira| j
    rev -->|Inspira| b
    j -->|Lidera| ind
    b -->|Lidera| ind
    n -->|Influye en| cong
```
